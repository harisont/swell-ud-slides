---
title: "Treebanking SweLL"
subtitle: "the Swedish Learner Language Corpus"
author: "Arianna Masciolini"
theme: "lucid"
logo: "gu.png"
date: "22 October 2025"
institute: "SBX, Department of Swedish, Multilingualism, Language technology"
---

## Introducing SweLL
(aka the Swedish Learner Language corpus)

- __genre__: essays (misc topics)
- __learners__: adult L2 Swedish learners with various language backgrounds and proficiency levels
- __annotation__: error tagging, pseudonymization and normalization (minimal edits)

## A look at the data

\vspace{-5.18em} 

### Swedish (SweLL)
\small
```xml
<sentence> <w ref="1">"</w> <w ref="2" target_form="Det" 
correction_label="L-Ref">Den</w> <w ref="3">är</w> 
<w ref="4">en</w> <w ref="5">tredjedel</w> 
<w ref="6">av</w> <w ref="7">din</w> <w ref="8">dag</w> 
<w ref="9">!</w> </sentence>
```

## A look at the data

\bigskip \bigskip \bigskip

### Swedish (SweLL)
\small
```xml
<sentence> <w ref="1">"</w> <w ref="2" target_form="Det" 
correction_label="L-Ref">Den</w> <w ref="3">är</w> 
<w ref="4">en</w> <w ref="5">tredjedel</w> 
<w ref="6">av</w> <w ref="7">din</w> <w ref="8">dag</w> 
<w ref="9">!</w> </sentence>
```

### English (FCE)
\small
```xml
I also suggest that more plays and films should 
<ns type="RV"> <ns type="FV"><i>be taken</i><c>take</c>
</ns> place</ns>.
```

### Italian (VALICO)
\small
```xml
Finse <MC><i>aveva paura</i><c>che aveva paura</c>
</MC> di un <DN><i>rapito</i><c>rapimento</c></DN>.
```

## See problems
- lack of interoperability between corpora
- lots of manual annotation needed
- coarse-grained error labels
- exclusive focus on errors

## The solution: UD
Universal Dependencies

- a __cross-lingually consistent grammatical annotation scheme__, designed to be
  - human- _and_ machine-readable
  - suitabile for both mono- _and_ multilingual use cases <!--uniform morphosyntactic annotation layer complemented by language-specific guidelines; we focus on the former-->
- a growing multilingual collection of dependency treebanks (160+ languages and 600+ contributors!)

## The solution: UD
\bigskip
- adopting a __shared data format__ grants basic interoperability between corpora
- __parsers__ help boostrapping the annotation process
- __fine-grained morphosyntactic annotation__ allows moving beyond error detection/tagging
- __cross-linguistic consistency__\* enables comparisons between:
  - L1 and L2
  - different L2s
  - L2 and TL[^1]

[^1]: especially with __parallel learner treebanks__

## UD treebanks of learner language
\bigskip

| **language** | **name**  | **sentences** | **status**      |
| -----------: | --------  | -------:      | :-----------:   |
| Chinese      | CFL       | 451           | released        |
| English      | ESL       | 5124          | retired         |
| English      | ESLSpok   | 2320          | released        |
| Greek        | GLCII     |               | in progress     |
| Italian      | Valico    | 398           | released        |
| Korean       | KSL       | 12977         | released        |
| Russian      |           | 500           | in progress     |
| **Swedish**  | **SweLL** | **~5000**     | **in progress** |

## \*
UD guidelines do **_not_** cover all relevant interlanguage phenomena and are **_not_** universally adopted across learner treebanks

\bigskip

### Learn more:
Arianna Masciolini, Aleksandrs Berdicevskis, Maria Irena Szawerna, and Elena Volodina. _Annotating second language in Universal Dependencies: a review of current practices and directions for harmonized guidelines_ (2025)

## TL;DR - literal vs. "distributional"
\setlength{\unitlength}{0.45mm}
\begin{picture}(195.0,110.0)
  \put(0.0,0.0){en}
  \put(37.0,0.0){lång}
  \put(83.0,0.0){\bfseries bus}
  \put(129.0,0.0){\bfseries resa}
\end{picture}

## Literal annotation
\setlength{\unitlength}{0.45mm}
\begin{picture}(195.0,110.0)
  \put(0.0,0.0){en}
  \put(37.0,0.0){lång}
  \put(83.0,0.0){\bfseries bus}
  \put(129.0,0.0){\bfseries resa}
  \put(0.0,15.0){{\tiny NUM/DET/...}}
  \put(37.0,15.0){{\tiny ADJ}}
  \put(83.0,15.0){{\tiny NOUN}}
  \put(129.0,15.0){{\tiny NOUN/VERB}}
\end{picture}

## Literal annotation
\setlength{\unitlength}{0.45mm}
\begin{picture}(195.0,110.0)
  \put(0.0,0.0){en}
  \put(37.0,0.0){lång}
  \put(83.0,0.0){\bfseries bus}
  \put(129.0,0.0){\bfseries resa}
  \put(0.0,15.0){{\tiny DET}}
  \put(37.0,15.0){{\tiny ADJ}}
  \put(83.0,15.0){{\tiny NOUN}}
  \put(129.0,15.0){{\tiny NOUN}}
  \put(0.0,-13.0){{\scriptsize {\slshape a}}}
  \put(37.0,-13.0){{\scriptsize {\slshape long}}}
  \put(83.0,-13.0){{\scriptsize {\slshape ?}}}
  \put(129.0,-13.0){{\scriptsize {\slshape trip}}}
\end{picture}

## Correction-aware annotation
\setlength{\unitlength}{0.45mm}
\begin{picture}(195.0,110.0)
  \put(0.0,0.0){en}
  \put(37.0,0.0){lång}
  \put(129.0,0.0){\bfseries bussresa}
  \put(0.0,15.0){{\tiny DET}}
  \put(37.0,15.0){{\tiny ADJ}}
  \put(129.0,15.0){{\tiny NOUN}}
  \put(0.0,-13.0){{\scriptsize {\slshape a}}}
  \put(37.0,-13.0){{\scriptsize {\slshape long}}}
  \put(129.0,-13.0){{\scriptsize {\slshape bus.trip}}}
\end{picture}

## Correction-aware annotation
\setlength{\unitlength}{0.45mm}
\begin{picture}(195.0,110.0)
  \put(0.0,0.0){en}
  \put(37.0,0.0){lång}
  \put(129.0,0.0){\bfseries bussresa}
  \put(0.0,15.0){{\tiny DET}}
  \put(37.0,15.0){{\tiny ADJ}}
  \put(129.0,15.0){{\tiny NOUN}}
  \put(0.0,-13.0){{\scriptsize {\slshape a}}}
  \put(37.0,-13.0){{\scriptsize {\slshape long}}}
  \put(129.0,-13.0){{\scriptsize {\slshape bus.trip}}}
  \put(74.5,30.0){\oval(126.67441860465117,100.0)[t]}
  \put(11.162790697674417,35.0){\vector(0,-1){5.0}}
  \put(67.75,83.0){{\tiny det}}
  \put(93.0,30.0){\oval(88.73913043478261,66.66666666666667)[t]}
  \put(48.630434782608695,35.0){\vector(0,-1){5.0}}
  \put(84.0,66.33333333333334){{\tiny amod}}
  \put(144.0,110.0){\vector(0,-1){80.0}}
  \put(149.0,100.0){{\tiny root}}
\end{picture}

## Correction-aware annotation
\setlength{\unitlength}{0.45mm}
\begin{picture}(195.0,110.0)
  \put(0.0,0.0){en}
  \put(37.0,0.0){lång}
  \put(83.0,0.0){\bfseries bus}
  \put(129.0,0.0){\bfseries resa}
  \put(0.0,15.0){{\tiny DET}}
  \put(37.0,15.0){{\tiny ADJ}}
  \put(83.0,15.0){{\tiny NOUN}}
  \put(129.0,15.0){{\tiny NOUN}}
  \put(0.0,-13.0){{\scriptsize {\slshape a}}}
  \put(37.0,-13.0){{\scriptsize {\slshape long}}}
  \put(83.0,-13.0){{\scriptsize {\slshape bus}}}
  \put(129.0,-13.0){{\scriptsize {\slshape trip}}}
\end{picture}

## Correction-aware annotation
\setlength{\unitlength}{0.45mm}
\begin{picture}(195.0,110.0)
  \put(0.0,0.0){en}
  \put(37.0,0.0){lång}
  \put(83.0,0.0){\bfseries bus}
  \put(129.0,0.0){\bfseries resa}
  \put(0.0,15.0){{\tiny DET}}
  \put(37.0,15.0){{\tiny ADJ}}
  \put(83.0,15.0){{\tiny NOUN}}
  \put(129.0,15.0){{\tiny NOUN}}
  \put(0.0,-13.0){{\scriptsize {\slshape a}}}
  \put(37.0,-13.0){{\scriptsize {\slshape long}}}
  \put(83.0,-13.0){{\scriptsize {\slshape bus}}}
  \put(129.0,-13.0){{\scriptsize {\slshape trip}}}
  \put(51,30.0){\oval(79.3855421686747,66.66666666666667)[t]}
  \put(11.2,35.0){\vector(0,-1){5.0}}
  \put(44.75,66.33333333333334){{\tiny det}}
  \put(68.2,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(48.630434782608695,35.0){\vector(0,-1){5.0}}
  \put(61.0,49.66666666666667){{\tiny amod}}
  \put(93.0,110.0){\vector(0,-1){80.0}}
  \put(97.0,80.0){{\tiny root}}
  \put(115.5,30.0){\oval(40,33.333333333333336)[t]}
  \put(135.25,35.0){\vector(0,-1){5.0}}
  \put(105.5,49.66666666666667){{\color{SecondaryColor} \tiny goeswith}}
\end{picture}

## Correction-aware annotation
\setlength{\unitlength}{0.45mm}
\begin{picture}(195.0,110.0)
  \put(0.0,0.0){en}
  \put(37.0,0.0){lång}
  \put(83.0,0.0){\bfseries bus}
  \put(129.0,0.0){\bfseries resa}
  \put(0.0,15.0){{\tiny DET}}
  \put(37.0,15.0){{\tiny ADJ}}
  \put(83.0,15.0){{\tiny NOUN}}
  \put(129.0,15.0){{\tiny NOUN}}
  \put(0.0,-13.0){{\scriptsize {\slshape a}}}
  \put(37.0,-13.0){{\scriptsize {\slshape long}}}
  \put(83.0,-13.0){{\scriptsize {\slshape bus}}}
  \put(129.0,-13.0){{\scriptsize {\slshape trip}}}
  \put(74.5,30.0){\oval(126.67441860465117,100.0)[t]}
  \put(11.162790697674417,35.0){\vector(0,-1){5.0}}
  \put(67.75,83.0){{\tiny det}}
  \put(93.0,30.0){\oval(88.73913043478261,66.66666666666667)[t]}
  \put(48.630434782608695,35.0){\vector(0,-1){5.0}}
  \put(84.0,66.33333333333334){{\tiny amod}}
  \put(116.0,30.0){\oval(39.47826086956522,33.333333333333336)[t]}
  \put(96.26086956521739,35.0){\vector(0,-1){5.0}}
  \put(100.5,49.66666666666667){{\tiny \color{SecondaryColor} compound}}
  \put(144.0,110.0){\vector(0,-1){80.0}}
  \put(149.0,100.0){{\tiny root}}
\end{picture}

## Transfer-aware annotation
\setlength{\unitlength}{0.21mm}
\begin{picture}(617.0,130.0)
  \put(0.0,0.0){det}
  \put(46.0,0.0){är}
  \put(83.0,0.0){\bfseries det}
  \put(210.0,0.0){\bfseries samma}
  \put(352.0,0.0){som}
  \put(392.0,0.0){i}
  \put(429.0,0.0){Sverige}
  \put(0.0,15.0){{\tiny PRON}}
  \put(46.0,15.0){{\tiny AUX}}
  \put(83.0,15.0){{\tiny PRON/DET}}
  \put(210.0,15.0){{\tiny ADJ}}
  \put(315.0,15.0){{\tiny PRON/ADP/...}}
  \put(392.0,15.0){{\tiny ADP}}
  \put(429.0,15.0){{\tiny PROPN}}
\end{picture}

## Transfer-aware annotation
\setlength{\unitlength}{0.21mm}
\begin{picture}(617.0,130.0)
  \put(0.0,0.0){det}
  \put(46.0,0.0){är}
  \put(83.0,0.0){\bfseries det}
  \put(210.0,0.0){\bfseries samma}
  \put(352.0,0.0){som}
  \put(392.0,0.0){i}
  \put(429.0,0.0){Sverige}
  \put(0.0,15.0){{\tiny PRON}}
  \put(46.0,15.0){{\tiny AUX}}
  \put(83.0,15.0){{\tiny \color{SecondaryColor} PRON}}
  \put(210.0,15.0){{\tiny \color{SecondaryColor} X}}
  \put(315.0,15.0){{\tiny PRON/ADP/...}}
  \put(392.0,15.0){{\tiny ADP}}
  \put(429.0,15.0){{\tiny PROPN}}
  \put(156.5,30.0){\color{SecondaryColor} \oval(124.63779527559056,33.333333333333336)[t]}
  \put(218.18110236220471,35.0){\color{SecondaryColor}\vector(0,-1){5.0}}
  \put(145.75,49.66666666666667){{\tiny \color{SecondaryColor} goeswith}}
\end{picture}

## Transfer-aware annotation
\setlength{\unitlength}{0.21mm}
\begin{picture}(617.0,130.0)
  \put(0.0,0.0){det}
  \put(46.0,0.0){är}
  \put(83.0,0.0){\bfseries det}
  \put(210.0,0.0){\bfseries samma}
  \put(352.0,0.0){som}
  \put(392.0,0.0){i}
  \put(429.0,0.0){Sverige}
  \put(0.0,15.0){{\tiny PRON}}
  \put(46.0,15.0){{\tiny AUX}}
  \put(83.0,15.0){{\tiny DET}}
  \put(210.0,15.0){{\tiny ADJ}}
  \put(352.0,15.0){{\tiny ADP}}
  \put(392.0,15.0){{\tiny ADP}}
  \put(429.0,15.0){{\tiny PROPN}}
  \put(0.0,-11.0){{\scriptsize {\slshape it}}}
  \put(46.0,-11.0){{\scriptsize {\slshape is}}}
  \put(83.0,-11.0){{\scriptsize {\slshape the}}}
  \put(210.0,-11.0){{\scriptsize {\slshape same}}}
  \put(352.0,-11.0){{\scriptsize {\slshape as}}}
  \put(392.0,-11.0){{\scriptsize {\slshape in}}}
  \put(429.0,-11.0){{\scriptsize {\slshape Sweden}}}
\end{picture}

## Transfer-aware annotation
\setlength{\unitlength}{0.21mm}
\begin{picture}(617.0,130.0)
  \put(0.0,0.0){det}
  \put(46.0,0.0){är}
  \put(83.0,0.0){\bfseries det}
  \put(210.0,0.0){\bfseries samma}
  \put(352.0,0.0){som}
  \put(392.0,0.0){i}
  \put(429.0,0.0){Sverige}
  \put(0.0,15.0){{\tiny PRON}}
  \put(46.0,15.0){{\tiny AUX}}
  \put(83.0,15.0){{\tiny DET}}
  \put(210.0,15.0){{\tiny ADJ}}
  \put(352.0,15.0){{\tiny ADP}}
  \put(392.0,15.0){{\tiny ADP}}
  \put(429.0,15.0){{\tiny PROPN}}
  \put(0.0,-11.0){{\scriptsize {\slshape it}}}
  \put(46.0,-11.0){{\scriptsize {\slshape is}}}
  \put(83.0,-11.0){{\scriptsize {\slshape the}}}
  \put(210.0,-11.0){{\scriptsize {\slshape same}}}
  \put(352.0,-11.0){{\scriptsize {\slshape as}}}
  \put(392.0,-11.0){{\scriptsize {\slshape in}}}
  \put(429.0,-11.0){{\scriptsize {\slshape Sweden}}}
  \put(115.0,30.0){\oval(208.57142857142858,100.0)[t]}
  \put(10.714285714285708,35.0){\vector(0,-1){5.0}}
  \put(103.75,83.0){{\tiny nsubj}}
  \put(138.0,30.0){\oval(162.17073170731706,66.66666666666667)[t]}
  \put(56.91463414634147,35.0){\vector(0,-1){5.0}}
  \put(131.25,66.33333333333334){{\tiny cop}}
  \put(156.5,30.0){\oval(124.63779527559056,33.333333333333336)[t]}
  \put(94.18110236220471,35.0){\vector(0,-1){5.0}}
  \put(149.75,49.66666666666667){{\tiny det}}
  \put(225.0,130.0){\vector(0,-1){100.0}}
  \put(230.0,120.0){{\tiny root}}
  \put(402.0,30.0){\oval(69.94594594594595,66.66666666666667)[t]}
  \put(367.02702702702703,35.0){\vector(0,-1){5.0}}
  \put(393.0,66.33333333333334){{\tiny case}}
  \put(420.5,30.0){\oval(28.89189189189189,33.333333333333336)[t]}
  \put(406.05405405405406,35.0){\vector(0,-1){5.0}}
  \put(411.5,49.66666666666667){{\tiny case}}
  \put(339.5,30.0){\oval(217.63013698630138,100.0)[t]}
  \put(448.3150684931507,35.0){\vector(0,-1){5.0}}
  \put(332.75,83.0){{\tiny obl}}
\end{picture}

## Annotators
- Sasha (L1: Russian)
- Maria (L1: Polish)
- Arianna (L1: Italian)

And soon:

- Caroline (L1: French)

## Where?
\bigskip \bigskip

![](qr-code.png)

\centering `github.com/UniversalDependencies/UD_Swedish-SweLL`[^2]

[^2]: just not yet!

## When?
- test set (500 sentences): first release \color{gray}hopefully \color{black}on November 15 as part of UD 2.17
- dev set (another 500 sentences): as part of UD 2.18
- train set (4000 sentences!): we'll see about that

## Tackar _all_ som hjälpte oss!

\bigskip
\bigskip
\bigskip

![](sbx.png)

\bigskip
\bigskip

![](unidive.png)