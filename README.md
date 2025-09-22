MDAITex: editor para textos generados por IA
 
MDAITex es una aplicación web ligera para escribir Markdown con fórmulas LaTeX y exportar a DOCX, ODT, HTML (con MathJax) y LaTeX, todo en el navegador y sin depender de servidores externos. Se apoya en Pandoc compilado a WebAssembly y cargado localmente.

- Página principal: `index.html`
- Motor WASM: `pandoc.b64` / `pandoc.b64.gz`
- Puente de ejecución: `index.js` (navegador) y `pandoc.js` (utilidades empaquetadas)
- Textos de ayuda por idioma: `mdlatex*.md`
- Traducciones de interfaz: `locales/<código>/translation.json`

Estado
- Última versión publicada: 1.1
- Nota de la versión: ver Releases en GitHub.

Integración con EdiCuaTeX (fórmulas LaTeX)
MDAITex puede abrir el editor EdiCuaTeX en una ventana y recibir la fórmula de vuelta automáticamente mediante postMessage.

- Botón ∑ en la barra de herramientas: abre EdiCuaTeX.
- Edita o crea la fórmula en EdiCuaTeX y pulsa “Send to host”.
- La fórmula se inserta en la selección actual del editor Markdown y se actualiza la vista previa.

Detalles técnicos
- El editor utilizado es la instancia pública de GitHub Pages:
  - `https://jjdeharo.github.io/edicuatex/index.html?pm=1&origin=https%3A%2F%2Fjjdeharo.github.io`
- Seguridad: MDAITex valida el `origin` del mensaje recibido y solo acepta respuestas desde el editor configurado.
- Si necesitas apuntar a otra URL del editor, cambia la constante `EDI_CUATEX_BASE` en `index.html`.

Ejecutar en local
No hay paso de build. Sirve la carpeta de forma estática y abre el HTML en el navegador.

1) Levanta un servidor estático (ejemplos):
- `python -m http.server 8000`

2) Abre en el navegador:
- `http://localhost:8000/`

3) Prueba rápida
- Escribe Markdown + LaTeX en el panel izquierdo y usa “Exportar”.

Más detalles: `uso_local_pandoc.md`.

Funcionalidades clave
- Editor Markdown con previsualización y soporte MathJax.
- Limpieza automática de espacios en matemáticas inline `$...$`.
- Exportación a: DOCX, ODT, HTML (documento o fragmento) y LaTeX (documento o fragmento).
- Copia directa al portapapeles de HTML/LaTeX si se desea.
- Tema claro/oscuro y selector de idioma.
- Carga offline del motor Pandoc WASM tras la primera inicialización.

Idiomas
Las cadenas de interfaz residen en `locales/<código>/translation.json` (i18next). Mantén las mismas claves entre idiomas. Los textos de ayuda inicial están en `mdlatex*.md` y se seleccionan según el idioma.

Estructura del proyecto
- `index.html`: interfaz, lógica de UI e i18n.
- `index.js`: puente a WASI para ejecutar Pandoc WASM en navegador.
- `pandoc.js`: helper empaquetado (CRC/gzip) para entornos offline/Node‑like.
- `pandoc.b64` y `pandoc.b64.gz`: binario WASM en base64 (plano y gzip).
- `mdlatex*.md`: ayudas por idioma.
- `locales/*/translation.json`: textos de interfaz.
- `uso_local_pandoc.md`: notas de uso y ejemplos.

Licencias
- Licencia del código: AGPL v3. Consulta `LICENSE.txt` para el texto completo.
- Licencia de los contenidos educativos (textos, ejercicios, vídeos, imágenes): CC BY‑SA 4.0 — https://creativecommons.org/licenses/by-sa/4.0/

Atribución recomendada
- Título: MDAITex: editor para textos generados por IA
- Autoría: Juan José de Haro
- Año: 2025
- Enlace: https://github.com/mdaitex/mdaitex.github.io

Contribuciones
Las aportaciones son bienvenidas (issues y pull requests). Ten en cuenta:
- Mantén sincronizadas las claves de `locales/*/translation.json`.
- Si se actualiza el blob WASM, valida CRC y prueba en Chrome y Firefox.
- Evita introducir dependencias de terceros en la página de demo para preservar el uso offline.
- No modifiques la lógica de exportación (DOCX, ODT, HTML, LaTeX) sin aprobación del responsable del proyecto.

Créditos
- Pandoc (https://pandoc.org) — conversión de formatos.
- MathJax — render de fórmulas LaTeX en HTML.

Contacto
- Autor: Juan José de Haro — https://bilateria.es
