# Editor Markdown amb suport LaTeX



Aquest editor permet treballar amb **textos generats per IA** i exportar-los fàcilment en diversos formats compatibles amb tots els processadors de text. Les fórmules matemàtiques no només es mostraran correctament, sinó que es podran editar des de Word, LibreOffice o Google Docs.


👉 Has de copiar el text de la IA amb el botó "Copiar" del xat, no seleccionis manualment el text.

⚠️ **IMPORTANT: Si el navegador mostra un missatge de manca de memòria, utilitza Firefox**.

## Índex

- [Com s’utilitza?](#com-sutilitza)
- [Limitacions conegudes de MDAITex](#limitacions-conegudes-de-mdaitex)
- [Sintaxi bàsica de Markdown](#sintaxi-bàsica-de-markdown)  
- [Utilitzar amb Google Docs](#utilitzar-amb-google-docs)
- [Utilització amb editors d'HTML com eXeLearning](#utilització-amb-editors-dhtml-com-exelearning)
- [Fórmules LaTeX](#fórmules-latex)
- [Més sobre LaTeX](#més-sobre-latex)

## Com s’utilitza?

* Utilitza el **botó per copiar** (és a dir, sense seleccionar el text) per copiar el text generat per la IA i enganxar-lo directament al panell de l'esquerra.

* Pots modificar-lo aquí mateix o exportar-lo per fer-lo servir al teu processador de textos preferit. Per fer-lo servir amb **Google Docs**, exporta’l en format DOCX i puja’l al Drive.

## Limitacions conegudes de MDAITex

- Amb **iOS** (iPhone i iPad) el programa pot no funcionar per la manera com aquest sistema operatiu gestiona la memòria i el temps d’execució.
- A **LibreOffice**, la importació d’expressions com ara els límits o les raons trigonomètriques pot no fer-se correctament, i pot ser necessari editar les fórmules. Aquest és un problema conegut de LibreOffice, no del nostre programa.
- En alguna ocasió **Chrome** i **Edge** han donat l'error que falta memòria, en aquests casos pots intentar utilitzar un navegador diferent com Opera o Firefox.
- **Google Docs** no pot representar matrius, per tant, aquestes apareixeran en una sola fila.

## Utilitzar amb Google Docs

Per poder utilitzar el text amb Google Docs, només heu d'exportar en format DOCX, pujar al Drive i després obrir com un document de Google normal.

## Utilització amb editors d'HTML com eXeLearning

Per poder enganxar el text en editors HTML com els iDevices de eXeLearning, heu d'exportar el text en format HTML i marcar l'opció "Copiar HTML". D'aquesta forma es copiarà el contingut que podreu enganxar directament a l'editor. 

En eXeLearning les fórmules matemàtiques es veuran correctament si heu marcat l'opció "Mode avançat" i després: Propietats > Exporta > Contingut matemàtic: carrega MathJax en pàgines amb codi LaTeX.

## Sintaxi bàsica de Markdown

### Format

- **Negreta**
- *Cursiva*
- ***Negreta i cursiva***
- ~~Ratllat~~

(A Markdown no es pot subratllar)

### Taules

Les taules s'escriuen amb barres verticals (`|`) per separar columnes i guions (`-`) per definir l'encapçalament:

| Assignatura     | Professor/a | Aula  |
|------------------|-------------|--------|
| Biologia         | Javi        | B203   |
| Matemàtiques     | Clara       | A101   |
| Digitalització   | Marta       | D405   |

### Encapçalaments

# Títol 1  
## Títol 2  
### Títol 3

### Llistes

Llista numerada:

1. Primer element  
2. Segon element  
3. Tercer element

Llista amb vinyetes:

- Element 1  
- Element 2  
- Element 3

### Enllaços

[ChatGPT-IA-edu](https://t.me/ChatGPTedu)



## Fórmules LaTeX

Per inserir fórmules amb l’editor, fes servir el botó «Insereix equació» (EdiCuaTeX) de la barra d’eines. S’obrirà un editor on pots escriure l’expressió i prémer «Insereix»; s’enganxarà al punt d’edició. Si hi ha text seleccionat, se substituirà per la fórmula.

- Fórmula en línia amb el text: $a^2 + b^2 = c^2$
- Fórmula en mode *display*, en una línia separada i, normalment, centrada:

$$E = mc^2$$

Fraccions: $\frac{1}{2} + \frac{1}{3} = \frac{5}{6}$

Subíndexs: $a_1 + a_2 + a_3 + \ldots + a_n$

Integral definida:
$$\int_{a}^{b} f(x) \, dx = F(b) - F(a)$$

Sumatori:
$$\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$$

Matriu:
$$A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{pmatrix}$$

Equació diferencial:
$$\frac{d^2y}{dx^2} + \frac{dy}{dx} + y = 0$$

Sistema d’equacions:
$$\begin{cases}
3x + 5y + z = 0 \\
7x - 2y + 4z = 0 \\
-6x + 3y + 2z = 0
\end{cases}$$

Límit:
$$\lim_{x \to \infty} \frac{1}{x} = 0$$

## Més sobre LaTeX

Per aprendre més sobre la sintaxi de LaTeX, visita la pàgina creada especialment per a docents:  
[**Fórmules matemàtiques en LaTeX**](https://calatex.bilateria.org/escriptura_de_frmules.html)

