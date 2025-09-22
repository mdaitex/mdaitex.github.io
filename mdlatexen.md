# Markdown Editor with LaTeX Support

This editor lets you work with AI‑generated text and export it easily to multiple formats compatible with all word processors. Mathematical formulas will not only render correctly, they can also be edited in Word, LibreOffice, or Google Docs.

👉 Copy the AI text using the chat’s "Copy" button — do not select text manually.

⚠️ IMPORTANT: If the browser reports an out‑of‑memory error, use Firefox.

## Table of contents

- [How to use it](#how-to-use-it)
- [Known limitations of MDAITex](#known-limitations-of-mdaitex)
- [Basic Markdown syntax](#basic-markdown-syntax)
- [Use with Google Docs](#use-with-google-docs)
- [Use with HTML editors like eXeLearning](#use-with-html-editors-like-exelearning)
- [LaTeX formulas](#latex-formulas)
- [More about LaTeX](#more-about-latex)

## How to use it

- Using the chat’s **Copy button** (i.e., without selecting text), copy the AI‑generated text and paste it directly into the left panel.
- You can edit it here or export it to use in your favorite word processor. To use it with **Google Docs**, export to DOCX and upload the file to Drive.

## Known limitations of MDAITex

- On **iOS** (iPhone and iPad) the app may not work due to how that operating system handles memory and execution time.
- Occasionally **Chrome** and **Edge** show an out‑of‑memory error; in such cases try another browser like Opera or Firefox.
- In **LibreOffice**, importing certain expressions (e.g., limits or trigonometric ratios) may not work properly, so formulas might require manual adjustment. This is a known LibreOffice limitation, not an issue in our program.
- **Google Docs** cannot render matrices, so they appear in a single row.

## Use with Google Docs

To use the text with Google Docs, simply export in DOCX format, upload the file to Drive, and then open it as a regular Google document.

## Use with HTML editors like eXeLearning

To paste the text into HTML editors such as eXeLearning’s iDevices, export the text in HTML format and check the "Copy HTML" option. This copies the content so you can paste it directly into the editor.

In eXeLearning, math formulas display correctly if you enable "Advanced mode" and then go to: Properties > Export > Mathematical content: load MathJax on pages with LaTeX code.

## Basic Markdown syntax

### Formatting

- **Bold**
- *Italic*
- ***Bold and italic***
- ~~Strikethrough~~

(Markdown does not support underline.)

### Tables

Tables are written using vertical bars (`|`) to separate columns and dashes (`-`) to define the header:

| Subject        | Teacher | Room |
|----------------|---------|------|
| Biology        | Javi    | B203 |
| Mathematics    | Clara   | A101 |
| Digitalization | Marta   | D405 |

### Headings

# Title 1  
## Title 2  
### Title 3

### Lists

Numbered list:

1. First item  
2. Second item  
3. Third item

Bulleted list:

- Item 1  
- Item 2  
- Item 3

### Links

[ChatGPT-IA-edu](https://t.me/ChatGPTedu)

## LaTeX formulas

To insert formulas with the helper, use the “Insert equation” (EdiCuaTeX) button on the toolbar. An editor opens where you can write the expression and click “Insert”; it will be pasted at the caret. If text is selected, it will be replaced by the formula.

- Inline formula: $a^2 + b^2 = c^2$
- Display formula (on its own line, usually centered):

$$E = mc^2$$

Fractions: $\frac{1}{2} + \frac{1}{3} = \frac{5}{6}$

Subscripts: $a_1 + a_2 + a_3 + \ldots + a_n$

Definite integral:
$$\int_{a}^{b} f(x) \, dx = F(b) - F(a)$$

Summation:
$$\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$$

Matrix:
$$A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{pmatrix}$$

Differential equation:
$$\frac{d^2y}{dx^2} + \frac{dy}{dx} + y = 0$$

System of equations:
$$\begin{cases}
3x + 5y + z = 0 \\
7x - 2y + 4z = 0 \\
-6x + 3y + 2z = 0
\end{cases}$$

Limit:
$$\lim_{x \to \infty} \frac{1}{x} = 0$$

## More about LaTeX

To learn more about LaTeX syntax, visit this page created especially for teachers:  
[**Mathematical formulas in LaTeX**](https://latex.bilateria.org/escritura_de_frmulas.html)
