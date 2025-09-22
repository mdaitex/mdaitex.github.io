# Editor Markdown con soporte LaTeX

Este editor permite traballar con textos xerados pola IA e exportalos facilmente a varios formatos compatibles con todos os procesadores de texto. As fórmulas matemáticas non só se verán correctamente, senón que tamén se poderán editar desde Word, LibreOffice ou Google Docs.

👉 Copia o texto da IA co botón "Copiar" do chat; non selecciones o texto manualmente.

⚠️ IMPORTANTE: Se o navegador mostra unha mensaxe de falta de memoria, utiliza Firefox.

## Índice

- [Como usalo](#como-usalo)
- [Limitacións coñecidas de MDAITex](#limitacións-coñecidas-de-mdaitex)
- [Sintaxe básica de Markdown](#sintaxe-básica-de-markdown)
- [Usar con Google Docs](#usar-con-google-docs)
- [Uso con editores HTML como eXeLearning](#uso-con-editores-html-como-exelearning)
- [Fórmulas LaTeX](#fórmulas-latex)
- [Máis sobre LaTeX](#máis-sobre-latex)

## Como usalo

- Usando o **botón Copiar** do chat (é dicir, sen seleccionar o texto), copia o texto xerado pola IA e pégano directamente no panel esquerdo.
- Podes editalo aquí mesmo ou exportalo para usalo no teu procesador de textos favorito. Para usalo con **Google Docs**, expórtao en DOCX e súbeo a Drive.

## Limitacións coñecidas de MDAITex

- En **iOS** (iPhone e iPad) a aplicación pode non funcionar debido a como ese sistema xestiona a memoria e o tempo de execución.
- En ocasións **Chrome** e **Edge** mostran un erro de falta de memoria; nese caso, proba con outro navegador como Opera ou Firefox.
- En **LibreOffice**, a importación de certas expresións (por exemplo, límites ou razóns trigonométricas) pode non realizarse correctamente, polo que as fórmulas poden requirir edición manual. Isto é unha limitación coñecida de LibreOffice, non do noso programa.
- **Google Docs** non pode representar matrices, polo que aparecen nunha única fila.

## Usar con Google Docs

Para usar o texto con Google Docs, simplemente expórtao en formato DOCX, súbeo a Drive e ábreo como un documento de Google normal.

## Uso con editores HTML como eXeLearning

Para pegar o texto en editores HTML como os iDevices de eXeLearning, expórtao en formato HTML e marca a opción "Copiar HTML". Deste modo copiarase o contido para poder pegalos directamente no editor.

En eXeLearning as fórmulas matemáticas veranse correctamente se activas o "Modo avanzado" e despois: Propiedades > Exportar > Contido matemático: cargar MathJax nas páxinas con código LaTeX.

## Sintaxe básica de Markdown

### Formato

- **Negra**
- *Cursiva*
- ***Negra e cursiva***
- ~~Riscado~~

(En Markdown non se pode subliñar.)

### Táboas

As táboas escríbense usando barras verticais (`|`) para separar columnas e guións (`-`) para definir a cabeceira:

| Materia        | Profesorado | Aula |
|----------------|-------------|------|
| Bioloxía       | Javi        | B203 |
| Matemáticas    | Clara       | A101 |
| Dixitalización | Marta       | D405 |

### Títulos

# Título 1  
## Título 2  
### Título 3

### Listas

Lista numerada:

1. Primeiro elemento  
2. Segundo elemento  
3. Terceiro elemento

Lista con viñetas:

- Elemento 1  
- Elemento 2  
- Elemento 3

### Ligazóns

[ChatGPT-IA-edu](https://t.me/ChatGPTedu)

## Fórmulas LaTeX

Para inserir fórmulas co asistente, usa o botón «Inserir ecuación» (EdiCuaTeX) da barra de ferramentas. Abrirase un editor onde podes escribir a expresión e premer «Inserir»; pegarase no punto de edición. Se hai texto seleccionado, substituirase pola fórmula.

- Fórmula en liña: $a^2 + b^2 = c^2$
- Fórmula en modo "display" (nunha liña aparte e, normalmente, centrada):

$$E = mc^2$$

Fraccións: $\frac{1}{2} + \frac{1}{3} = \frac{5}{6}$

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

Sistema de ecuacións:
$$\begin{cases}
3x + 5y + z = 0 \\
7x - 2y + 4z = 0 \\
-6x + 3y + 2z = 0
\end{cases}$$

Límite:
$$\lim_{x \to \infty} \frac{1}{x} = 0$$

## Máis sobre LaTeX

Para aprender máis sobre a sintaxe de LaTeX, visita a páxina creada especialmente para docentes:  
[**Fórmulas matemáticas en LaTeX**](https://latex.bilateria.org/escritura_de_frmulas.html)
