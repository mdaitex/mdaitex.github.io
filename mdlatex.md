# Editor Markdown con soporte LaTeX



Este editor permite trabajar con **textos generados por IA** y exportarlos fácilmente en varios formatos compatibles con todos los procesadores de texto. Las fórmulas matemáticas no solo se mostrarán correctamente, sino que podrán ser editadas desde Word, LibreOffice o Google Docs.


👉 Debes copiar el texto de la IA con el botón "Copiar" del chat, no selecciones manualmente el texto.

⚠️ **IMPORTANTE: Si el navegador da un mensaje de falta de memoria, utiliza Firefox**

## Índice

- [¿Cómo usarlo?](#cómo-usarlo)
- [Limitaciones conocidas de MDAITex](#limitaciones-conocidas-de-mdaitex)
- [Sintaxis Markdown básica](#sintaxis-markdown-básica)
- [Utilizar con Google Docs](#utilizar-con-google-docs)
- [Utilización con editores de HTML como eXeLearning](#utilización-con-editores-de-html-como-exelearning)
- [Fórmulas LaTeX](#fórmulas-latex)
- [Más sobre LaTeX](#más-sobre-latex)


## ¿Cómo usarlo?

* Utilizando el **botón para copiar** (es decir, sin seleccionar el texto) copia el texto generado por la IA y pégalo directamente en el panel izquierdo.

* Puedes modificarlo aquí mismo o exportarlo para usar en tu procesador de textos favorito. Para usarlo con **Google Docs**, expórtalo en DOCX y súbelo al Drive.

## Limitaciones conocidas de MDAITex

- Con **iOS** (iPhone y iPad) el programa puede no funcionar debido a la forma en que este sistema operativo gestiona la memoria y el tiempo de ejecución.
- En alguna ocasión **Chrome** y **Edge** han dado el error de que falta memoria, en estos casos puedes intentar a utilizar un navegador diferente como Opera o Firefox. 
- En **LibreOffice**, la importación de expresiones como las de los límites o las razones trigonométricas puede no realizarse correctamente, por lo que puede requerir editar las fórmulas. Este es un problema conocido de LibreOffice, no de nuestro programa.
- **Google Docs** no puede representar matrices, por lo que estas aparecerán en una única fila.

## Utilizar con Google Docs

Para poder utilizar el texto con Google Docs, sólo tiene que exportar en formato DOCX, subir al Drive el archivo y luego abrirlo como un documento de Google normal.

## Utilización con editores de HTML como eXeLearning

Para poder pegar el texto en editores HTML como los iDevices de eXeLearning, debes exportar el texto en formato HTML y marcar la opción "Copiar HTML". De esta forma se copiará el contenido que podrás pegar directamente en el editor.

En eXeLearning las fórmulas matemáticas se verán correctamente si has marcado la opción "Modo avanzado" y después: Propiedades > Exportar > Contenido matemático: carga MathJax en páginas con código LaTeX.

## Sintaxis Markdown básica

### Formato

- **Negrita**
- *Cursiva*
- ***Negrita y cursiva***
- ~~Tachado~~

(En Markdown no se puede subrayar)

### Tablas

Las tablas se escriben usando barras verticales (`|`) para separar columnas y guiones (`-`) para definir el encabezado:

| Asignatura     | Profesor   | Aula  |
|----------------|------------|--------|
| Biología       | Javi       | B203   |
| Matemáticas    | Clara      | A101   |
| Digitalización | Marta      | D405   |

### Encabezados

# Título 1  
## Título 2  
### Título 3

### Listas

Lista numerada:

1. Primer elemento  
2. Segundo elemento  
3. Tercer elemento

Lista con viñetas:

- Elemento 1  
- Elemento 2  
- Elemento 3

### Enlaces

[ChatGPT-IA-edu](https://t.me/ChatGPTedu)



## Fórmulas LaTeX

Para insertar fórmulas con ayuda del editor, usa el botón «Insertar/editar ecuación» (EdiCuaTeX) de la barra de herramientas. Se abrirá un editor donde puedes escribir la expresión y pulsar «Insertar»; se pegará en el punto de edición. Si hay texto seleccionado, se sustituirá por la fórmula.

- Fórmula en línea con el texto: $a^2 + b^2 = c^2$
- Fórmula en modo *display*, en una línea aparte y, normalmente, centrada:

$$E = mc^2$$

Fracciones: $\frac{1}{2} + \frac{1}{3} = \frac{5}{6}$

Subíndices: $a_1 + a_2 + a_3 + \ldots + a_n$

Integral definida:
$$\int_{a}^{b} f(x) \, dx = F(b) - F(a)$$

Sumatorio:
$$\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$$

Matriz:
$$A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{pmatrix}$$

Ecuación diferencial:
$$\frac{d^2y}{dx^2} + \frac{dy}{dx} + y = 0$$

Sistema de ecuaciones:
$$\begin{cases}
3x + 5y + z = 0 \\
7x - 2y + 4z = 0 \\
-6x + 3y + 2z = 0
\end{cases}$$

Límite:
$$\lim_{x \to \infty} \frac{1}{x} = 0$$

## Más sobre LaTeX

Para aprender más sobre la sintaxis LaTeX, visita la página creada especialmente para docentes:  
[**Fórmulas matemáticas en LaTeX**](https://latex.bilateria.org/escritura_de_frmulas.html)
