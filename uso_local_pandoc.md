### Pasos para reutilizar Pandoc WASM desde la misma carpeta

1. **Archivos que debes tener juntos**

| Archivo         | Contenido                                                            | Cómo se obtiene                                                   |                              |
| --------------- | -------------------------------------------------------------------- | ----------------------------------------------------------------- | ---------------------------- |
| `index.js`      | Envoltorio que exporta `pandoc(args, input, base64Wasm)`             | Copia el que viene con el paquete `wasm-pandoc` o el del proyecto |                              |
| `pandoc.b64.gz` | Cadena **base64** del binario `pandoc.wasm`, comprimida con **gzip** | Generación local:<br>\`gzip -c pandoc.wasm                        | base64 -w0 > pandoc.b64.gz\` |
| Tu HTML/JS      | Código de la aplicación                                              | Donde llamarás a `pandoc()`                                       |                              |

> Con esos tres ficheros en la misma carpeta (o sub-carpeta servida igual), todo funciona sin conexión.

2. **Carga del motor una sola vez**

```js
let base64PandocWasm = null;       // cache en memoria
let pandocInitialized = false;
const MAX_RETRIES = 3;

async function cargarBase64Wasm() {
  if (pandocInitialized && base64PandocWasm) return base64PandocWasm;

  const resp = await fetch('pandoc.b64.gz');            // misma carpeta
  base64PandocWasm = (await resp.text()).trim();        // el navegador ya descomprime
  pandocInitialized = true;
  return base64PandocWasm;
}
```

El navegador descomprime automáticamente porque el servidor envía `Content-Encoding: gzip` o porque el propio fichero está almacenado con extensión `.gz`. No necesitas desinflarlo a mano.&#x20;

3. **Conversión: siempre el mismo patrón**

```js
const md = trimInlineMath(textarea.value);      // tu contenido markdown

await cargarBase64Wasm();                       // te asegura el motor en RAM

const bytes = await pandoc(
  '-f markdown -t docx',  // args CLI normales de pandoc
  md,
  base64PandocWasm
);

// bytes es Uint8Array: crea Blob y descárgalo
const blob = new Blob([bytes], {
  type: 'application/vnd.openxmlformats-officedocument.wordprocessingml.document'
});
downloadBlob(blob, 'documento.docx');
```

Los cuatro casos habituales quedan así:

| Destino                        | Argumentos que pasas a **pandoc**        |
| ------------------------------ | ---------------------------------------- |
| **DOCX**                       | `-f markdown -t docx`                    |
| **ODT**                        | `-f markdown -t odt`                     |
| **LaTeX (fragmento)**          | `-f markdown -t latex --no-highlight`    |
| **LaTeX (documento completo)** | `-s -f markdown -t latex --no-highlight` |
| **HTML + MathJax**             | `-f markdown -t html --mathjax`          |
| **HTML fragmento**             | idéntico al anterior, quitando `-s`      |

> Cambiando solo la cadena de argumentos puedes añadir cualquier formato que Pandoc conozca en el futuro.

4. **Descarga o copia**

* **Archivo**: genera un `Blob`, crea un enlace `<a download>` y haz `click()`.
* **Copiar al portapapeles**: convierte `bytes` a texto (`new TextDecoder().decode(bytes)`) y usa la API Clipboard si quieres pegar directamente (ejemplo en el código original).&#x20;

5. **Detalles prácticos**

* El motor **solo se inicializa la primera vez**; guarda la cadena base64 en memoria.
* En iOS se añade un retardo de 300 ms y una lectura por chunks para evitar cuelgues del navegador.&#x20;
* Si algo falla, repites la descarga hasta tres veces (`MAX_RETRIES`).
* Puedes servir todo desde un servidor estático (GitHub Pages, Netlify, carpeta local con `python -m http.server`, etc.).

Con esta estructura ya tienes una “caja negra” Pandoc lista; para añadir nuevas conversiones solo escribirás la línea:

```js
const bytes = await pandoc('-f markdown -t <nuevoFormato> [opciones]', texto, base64PandocWasm);
```

y decidirás luego si guardas el `bytes` como archivo o lo pegas al portapapeles.

