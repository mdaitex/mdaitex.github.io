# LaTeX euskarria duen Markdown editorea

Editore honek IAk sortutako testuekin lan egitea eta hauek erraz esportatzea ahalbidetzen du, testu-prozesadore guztiekin bateragarriak diren formatuetara. Formula matematikoak ez dira soilik ongi bistaratuko; Word, LibreOffice edo Google Docs-etik ere editatu ahal izango dira.

👉 Txataren "Kopiatu" botoiarekin kopiatu IAren testua; ez hautatu testua eskuz.

⚠️ GARRANTZITSUA: Nabigatzaileak memoria falta dela dioen mezu bat erakusten badu, erabili Firefox.

## Edukia

- [Nola erabili](#nola-erabili)
- [MDAITex-en muga ezagunak](#mdaitex-en-muga-ezagunak)
- [Markdownen oinarrizko sintaxia](#markdownen-oinarrizko-sintaxia)
- [Google Docs-ekin erabiltzea](#google-docs-ekin-erabiltzea)
- [HTML editoreekin erabiltzea (eXeLearning)](#html-editoreekin-erabiltzea-exelearning)
- [LaTeX formulak](#latex-formulak)
- [LaTeXi buruz gehiago](#latex-i-buruz-gehiago)

## Nola erabili

- **Kopiatu** botoia erabiliz (testua hautatu gabe), kopiatu IAk sortutako testua eta itsatsi zuzenean ezkerreko panelean.
- Hemen bertan edita dezakezu edo esportatu zure testu-prozesadore gogokoenean erabiltzeko. **Google Docs**-ekin erabiltzeko, esportatu DOCX formatura eta igo fitxategia Driveryra.

## MDAITex-en muga ezagunak

- **iOS**-en (iPhone eta iPad) aplikazioak baliteke ez ibiltzea, sistema eragile horrek memoria eta exekuzio-denbora nola kudeatzen duen dela eta.
- Batzuetan **Chrome** eta **Edge** nabigatzaileek memoria falta dela adierazten dute; kasu horietan, saiatu beste nabigatzaile batekin, adibidez Opera edo Firefox-ekin.
- **LibreOffice**-en, zenbait adierazpenen (adibidez, muga edo triangelu-funtzioen erlazioen) inportazioak huts egin dezake; ondorioz, formulak eskuz doitzea beharko da. Hau LibreOffice-ren muga ezaguna da, ez gure programarena.
- **Google Docs**-ek ezin ditu matrizeak errendatu, eta lerro bakarrean agertuko dira.

## Google Docs-ekin erabiltzea

Testua Google Docs-en erabiltzeko, esportatu DOCX formatura, igo fitxategia Driveryra eta ireki Google dokumentu arrunt gisa.

## HTML editoreekin erabiltzea (eXeLearning)

HTML editoreetan (adibidez, eXeLearning-eko iDeviceetan) testua itsasteko, esportatu HTML formatuan eta markatu "HTML kopiatu" aukera. Horrela, edukia zuzenean itsatsi ahal izango duzu editorean.

eXeLearning-en formula matematikoak ongi ikusiko dira "Modu aurreratua" gaituta badago eta ondoren: Propietateak > Esportatu > Eduki matematikoa: kargatu MathJax LaTeX kodea duten orrietan.

## Markdownen oinarrizko sintaxia

### Formatua

- **Lodia**
- *Etzana*
- ***Lodi eta etzana***
- ~~Marratua~~

(Markdownen ezin da azpimarratu.)

### Taulak

Taulak barrak (`|`) erabiltzen dituzte zutabeak bereizteko eta marratxoak (`-`) goiburua definitzeko:

| Irakasgaia     | Irakaslea | Gela |
|----------------|-----------|------|
| Biologia       | Javi      | B203 |
| Matematika     | Clara     | A101 |
| Digitalizazioa | Marta     | D405 |

### Izenburuak

# 1. titulua  
## 2. titulua  
### 3. titulua

### Zerrendak

Zenbakitutako zerrenda:

1. Lehen elementua  
2. Bigarren elementua  
3. Hirugarren elementua

Buletdun zerrenda:

- 1. elementua  
- 2. elementua  
- 3. elementua

### Estekak

[ChatGPT-IA-edu](https://t.me/ChatGPTedu)

## LaTeX formulak

Formulak laguntzailearekin txertatzeko, erabili tresna‑barrako «Ekuazioa txertatu» (EdiCuaTeX) botoia. Editorea irekiko da; adierazpena idatzi eta «Txertatu» sakatu, eta kurtsorearen kokalekuan itsatsiko da. Testua hautatuta badago, ordezkatuko da formularekin.

- Lerro barruko formula: $a^2 + b^2 = c^2$
- "Display" moduko formula (lerro bereizian eta, normalean, erdian):

$$E = mc^2$$

Frakzioak: $\frac{1}{2} + \frac{1}{3} = \frac{5}{6}$

Azpiindizeak: $a_1 + a_2 + a_3 + \ldots + a_n$

Integral mugatua:
$$\int_{a}^{b} f(x) \, dx = F(b) - F(a)$$

Batura:
$$\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$$

Matrizea:
$$A = \begin{pmatrix}
a_{11} & a_{12} & a_{13} \\
a_{21} & a_{22} & a_{23} \\
a_{31} & a_{32} & a_{33}
\end{pmatrix}$$

Ekuazio diferentziala:
$$\frac{d^2y}{dx^2} + \frac{dy}{dx} + y = 0$$

Ekuazio-sistema:
$$\begin{cases}
3x + 5y + z = 0 \\
7x - 2y + 4z = 0 \\
-6x + 3y + 2z = 0
\end{cases}$$

Muga:
$$\lim_{x \to \infty} \frac{1}{x} = 0$$

## LaTeXi buruz gehiago

LaTeX sintaxiari buruz gehiago jakiteko, irakasleentzat bereziki sortutako orri hau bisitatu:  
[**LaTeX-eko formula matematikoak**](https://latex.bilateria.org/escritura_de_frmulas.html)
