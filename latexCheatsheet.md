# $\LaTeX{}$ Cheatsheet

## Contents

| [Document classes](#document-classes) | [Document Structure](#document-structure) | [Text properties](#text-properties) | [Text-mode symbols](#text-mode-symbols)| [Tabular environments](#tabular-environments) | [Math mode](#math-mode) | [Bibliography and citations](#bibliography-and-citations) |
| --- | --- | --- | --- | --- | --- | --- |
| [Common documentclass options](#common-documentclass-options) | [Text environments](#text-environments) | [Font face](#font-face) | [Symbols](#symbols) |  | [Sensible size examples](#sensible-size-examples) | [Citation types](#citation-types) |
| [Packages](#packages) | [Lists](#lists) | [Font size](#font-size) | [Accents](#accents) |  | [Greek alphabet](#greek-alphabet) | [BibTex entry types](#bibtex-entry-types) |
| [Title](#title) | [References](#references) | [Verbatim text](#verbatim-text) | [Dashes](#dashes) |  | [Symbols of Type Ord](#symbols-of-type-ord) | [Bibtex fields](#bibtex-fields) |
| [Miscellaneous documents classes](#miscellaneous-documents-classes) | [Floating bodies](#floating-bodies) | [Justification](#justification) |  |  | [Large Operators](#large-operators) | [Common BibTeX style files](#common-bibtex-style-files) |
|  |  | [Miscellaneous text properties](#miscellaneous-text-properties) |  |  | [Binary Operations](#binary-operations) | [BibTex example](#bibtex-example) |
|  |  |  |  |  | [Relations](#relations) |  |
|  |  |  |  |  | [Arrows](#arrows) |  |
|  |  |  |  |  | [Delimiters](#delimiters) |  |
|  |  |  |  |  | [Accents](#accents) |  |
|  |  |  |  |  | [Elementary Math Control Sequences](#elementary-math-control-sequences) |  |
|  |  |  |  |  | [Non-Italic Function Names](#non-italic-function-names) |  |
|  |  |  |  |  | [Fills, Leaders and Ellipses](#fills-leaders-and-ellipses) |  |

### Document classes

| Class | Effect |
| --- | --- |
| $\texttt{book}$ | Default is two sided |
| $\texttt{report}$ | No $\backslash\texttt{part}$ divisions. |
| $\texttt{article}$ | No $\backslash\texttt{part}$ or $\backslash\texttt{chapter}$ divisions. |
| $\texttt{letter}$ | Letter (?). |
| $\texttt{slides}$ | Large sans-serif font. |

Used at the very beginning of a document: <br>
$\backslash\texttt{documentclass} \lbrace class \rbrace$. Use $\backslash\texttt{begi}\texttt{n} \lbrace document \rbrace$ to start contents and $\backslash\texttt{end}\lbrace document \rbrace$ to end the document.

#### Common documentclass options

| Option | Code |
| --- | --- |
| Font size | $\texttt{10pt/11pt/12pt}$ |
| Paper size | $\texttt{letterpaper/a4paper}$ |
| Use two columns | $\texttt{twocolumn}$ |
| Set margins for two-sided | $\texttt{twoside}$ |
| Landscape orientation. <br> Must use $\texttt{dvips-t landscape.}$ | $\texttt{landscape}$ |
| Double-space lines. | $\texttt{draft}$ |

Usage: $\backslash \texttt{documentclass}[opt,opt]\lbrace class \rbrace$

#### Packages

| Effect | Package |
| --- | :---: |
| Use 1 inch margins | $\texttt{fullpage}$ |
| Set margins with $\backslash\texttt{marginsize}\lbrace l \rbrace\lbrace r\rbrace\lbrace t\rbrace\lbrace b\rbrace$. | $\texttt{anysize}$ |
| Use $n$ columns with $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{multicols} \rbrace \lbrace n \rbrace.$ | $\texttt{multicol}$ |
| Use $\LaTeX{}$ symbol font. | $\texttt{latexsym}$ |

Use before $\backslash\texttt{begi}\texttt{n}\lbrace document\rbrace$. Usage: $\backslash\texttt{usepackage}\lbrace package\rbrace$.

#### Title

| Effect | Package |
| --- | :---: |
| Author of document | $\backslash\texttt{author}\lbrace text\rbrace$ |
| Title of document | $\backslash\texttt{title}\lbrace text\rbrace$ |
| Date | $\backslash\texttt{date}\lbrace text\rbrace$ |

These commands go before $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{document} \rbrace$. The declaration $\backslash\texttt{maketitle}$ goes at the top of the document.

#### Miscellaneous documents classes

$\backslash \texttt{pagestyle}\lbrace empty\rbrace$ Empty header, footer and no page numbers.

***

### Document Structure

$\backslash\texttt{part}\lbrace title \rbrace$<br>
$\backslash\texttt{chapter}\lbrace title \rbrace$<br>
$\backslash\texttt{section}\lbrace title \rbrace$<br>
$\backslash\texttt{subsection}\lbrace title \rbrace$<br>
$\backslash\texttt{subsubsection}\lbrace title \rbrace$<br>
$\backslash\texttt{paragraph}\lbrace title \rbrace$<br>
$\backslash\texttt{subparagraph}\lbrace title \rbrace$

Section commands can be followed with an \*, like $\backslash\texttt{section*}\lbrace title \rbrace$, to supress heading numbers.
$\backslash\texttt{setcounter}\lbrace \texttt{secnumdepth} \rbrace \lbrace x\rbrace$ supresses heading numbers of
depth > $x$, where $\texttt{chapter}$ has depth 0.

#### Text environments

$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{comment} \rbrace$ Comment block (not printed).<br>
$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{quote} \rbrace$ Indented quotation block.<br>
$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{quotation} \rbrace$ Like $\texttt{quote}$ with indented paragraphs.<br>
$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{verse} \rbrace$ Quotation block for verse.

#### Lists

$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{enumerate} \rbrace$ Numbered list.<br>
$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{itemize} \rbrace$ Bulleted list.<br>
$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{description} \rbrace$ Description list.<br>
$\backslash\texttt{item} \\; text$ Add an item.<br>
$\backslash\texttt{item}\lbrack x \rbrack \\; text$ Use $x$ instead of normal bullet or number.
Required for descriptions.

#### References

$\backslash\texttt{label}\lbrace marker \rbrace$ Set a marker for cross-reference, often of the form $\backslash\texttt{label}\lbrace\texttt{sec:item}\rbrace$.<br>
$\backslash\texttt{ref}\lbrace marker \rbrace$ Give section/body number of marker.<br>
$\backslash\texttt{pageref}\lbrace marker \rbrace$ Give page number of marker.<br>
$\backslash\texttt{footnote}\lbrace text \rbrace$ Print footnote at bottom of page.

#### Floating bodies

$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{table} \rbrace \lbrack place \rbrack$ Add numbered table.<br>
$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{figure} \rbrace \lbrack place \rbrack$ Add numbered figure.<br>
$\backslash\texttt{begi}\texttt{n}\lbrace \texttt{equation} \rbrace \lbrack place \rbrack$ Add numbered equation.<br>
$\backslash\texttt{caption}\lbrace text \rbrace$ Caption for the body.

The $place$ is a list valid placements for the body. $\texttt{t}$=top, $\texttt{h}$=here, $\texttt{b}$=bottom, $\texttt{p}$=separate page, $\texttt{!}$=place even if ugly. Captions and label markers should be within the environment.

***

### Text properties

#### Font face

| Command | Declaration | Effect |
| --- | --- | --- |
| $\backslash\texttt{textrm}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{rm} \\; text \rbrace$ | $\textrm{Roman family}$ |
| $\backslash\texttt{textsf}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{sf} \\; text \rbrace$ | $\textsf{Sans serif family}$ |
| $\backslash\texttt{texttt}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{tt} \\; text \rbrace$ | $\texttt{Typewriter family}$ |
| $\backslash\texttt{textmd}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{md} \\; text \rbrace$ | $\textmd{Medium series}$ |
| $\backslash\texttt{textbf}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{bf} \\; text \rbrace$ | $\textbf{Bold series}$ |
| $\backslash\texttt{textup}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{up} \\; text \rbrace$ | $\textup{Upright shape}$ |
| $\backslash\texttt{textup}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{it} \\; text \rbrace$ | $\textit{Italic shape}$ |
| $\backslash\texttt{textsl}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{sl} \\; text \rbrace$ | $\textsl{Slanted shape}$ |
| $\backslash\texttt{textsc}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{sc} \\; text \rbrace$ | $\textsc{small caps shape}$ |
| $\backslash\texttt{emph}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{em} \\; text \rbrace$ | $\emph{Emphasized}$ |
| $\backslash\texttt{textnormal}\lbrace text\rbrace$ | $\lbrace \backslash\texttt{normalfont} \\; text \rbrace$ | $\textnormal{Document font}$ |
| $\backslash\texttt{underline}\lbrace text\rbrace$ |  | $\underline{Underline}$ |

#### Font size

| Size | Example |
| --- | --- |
| $\backslash\texttt{tiny}$ | ${\tiny tiny}$ |
| $\backslash\texttt{scriptsize}$ | ${\scriptsize scriptsize}$ |
| $\backslash\texttt{footnotesize}$ | ${\footnotesize footnotesize}$ |
| $\backslash\texttt{small}$ | ${\small small}$ |
| $\backslash\texttt{normalsize}$ | ${\normalsize normalsize}$ |
| $\backslash\texttt{large}$ | ${\large large}$ |
| $\backslash\texttt{Large}$ | ${\Large Large}$ |
| $\backslash\texttt{LARGE}$ | ${\LARGE LARGE}$ |
| $\backslash\texttt{huge}$ | ${\huge huge}$ |
| $\backslash\texttt{Huge}$ | ${\Huge Huge}$ |

These are declarations and should be used in the form $\lbrace \texttt{small} \ldots \rbrace$ or without braces to affect the entire document.

#### Verbatim text

$\backslash\texttt{begi}\texttt{n}\lbrace\texttt{verbatim}\rbrace$ Verbatim environment.<br>
$\backslash\texttt{begi}\texttt{n}\lbrace\texttt{verbatim*}\rbrace$ Spaces are shown as $\textvisiblespace$.<br>
$\backslash\texttt{verb!}\texttt{text!}$ Text between the delimiting characters (in this case $\texttt{!}$) is verbatim.

#### Justification

| Environment | Declaration |
| --- | --- |
| $\backslash\texttt{begi}\texttt{n}\lbrace\texttt{center}\rbrace$ | $\backslash\texttt{centering}$ |
| $\backslash\texttt{begi}\texttt{n}\lbrace\texttt{flushleft}\rbrace$ | $\backslash\texttt{raggedright}$ |
| $\backslash\texttt{begi}\texttt{n}\lbrace\texttt{flushright}\rbrace$ | $\backslash\texttt{raggedleft}$ |

#### Miscellaneous text properties

$\backslash\texttt{linespread}\lbrace x\rbrace$ changes the line spacing by the multiplier $x$.

***

### Text-mode symbols

#### Symbols

| Name | Code | Symbol |
| --- | --- | :---: |
| ampersand | `\&` | $\\&$ |
| backslash | `\backslash` | $\backslash $ |
| bullet symbol | `\bullet` | $\bullet $ |
| circumflex | `\^{}`, `\textasciicircum{}` | $\textasciicircum{}$ |
| dollar sign | `\$` | $\\$ $ |
| ellipsis | `\ldots` | $\ldots $ |
| number sign | `\#` | $\\# $ |
| percentage sign | `\%` | $\\% $ |
| section sign | `\S` | $\\S $ |
| tilde | `\~{}`, `\textasciitilde{}` | $\textasciitilde{}$ |
| underscore | `\_` | $\\_ $ |
| vertical bar (pipe) | `\|`, `\mid`, `\textpipe`, `\textbar` | $\\|$ |

#### Accents

| Name | Code | Symbol |
| --- | --- | :---: |
|  | `\‘o` | $\textnormal{\\\`o}$ |
|  | `\’o` | $\textnormal{\\'o}$ |
|  | `\^{}` | $\textnormal{\\^{}}$ |
|  | `\~{o}` | $\textnormal{\\~{o}}$ |
|  | `\={o}` | $\textnormal{\\={o}}$ |
|  | `\.{o}` | $\textnormal{\\.{o}}$ |
|  | `\"{o}` | $\textnormal{\\"{o}}$ |
|  | `\co` | $\textnormal{\\co}$ |
|  | `\v{o}` | $\textnormal{\\v{o}}$ |
|  | `\H o ` | $\textnormal{\\H{o}}$ |
|  | `\c c` | $\textnormal{\\c{c}}$ |
|  | `\d o ` | $\textnormal{\\d{o}}$ |
|  | `\b o` | $\textnormal{\\b{o}}$ |
|  | `\t oo` | $\textnormal{\\t{oo}}$ |
|  | `\oe` | $\textnormal{\\oe}$ |
|  | `\OE` | $\textnormal{\\OE}$ |
|  | `\ae` | $\textnormal{\\ae}$ |
|  | `\AE` | $\textnormal{\\AE}$ |
|  | `\aa` | $\textnormal{\\aa}$ |
|  | `\AA` | $\\textnormal{\AA}$ |
|  | `\o` | $\\textnormal{\o}$ |
|  | `\O ` | $\\textnormal{\O}$ |
|  | `\l` | $\\textnormal{\l}$ |
|  | ` \L` | $\\textnormal{\L}$ |
|  | `\i ` | $\\textnormal{\i}$ |
|  | `\j ` | $\\textnormal{\j}$ |
|  | `~‘` | $\textnormal{~\`}$ |
|  | `?‘` | $\textnormal{?\`}$ |

#### Dashes

| Name | Source | Example | Usage |
| --- | --- | --- | --- |
| hyphen | - | X $\textnormal{-}$ ray | In words. |
| en-dash | -- | 1 $\textnormal{--}$ 5 | Between numbers. |
| em-dash | --- | Yes $\textnormal{---}$ or no? | Punctuation. |

#### Line and page breaks

| Code | Description |
| --- | --- |
| `\\` | Begin new line without new paragraph |
| `\\*` | Prohibit pagebreak after linebreak |
| $\backslash\texttt{kill}$ | Don't print current line |
| $\backslash\texttt{pagebreak}$ | Start new page |
| $\backslash\texttt{noindent}$ | Do not indent current line |

#### Miscellaneous text-mode symbols

| Code | Description |
| --- | --- |
| $\backslash\texttt{today}$ | February 17, 2023 |
| $ \$ \backslash\texttt{sim} \$ $ |  |

***

### Tabular environments

***

### Math mode

| Inline math | Displayed math |
| --- | --- |
| `\(...\)` | `\[...\]` |
| `$...$` | `$$...$$` |
|  | `\begin{equation}` <br> `...` <br> `\end{equation}` |
|  | `\begin{equation*}` <br> `...` <br> `\end{equation*}` |

#### Sensible size examples

| name | code | inline | displayed |
| --- | --- | --- | :---: |
| fraction | `\frac{x}{y}` | $\frac{x}{y} $ | $$\frac{x}{y} $$ |
| product | `\prod_{k=1}^{n}` | $\prod_{k=1}^{n} $ | $$\prod_{k=1}^{n} $$ |
| radical symbol | `\sqrt[n]{x}` | $\sqrt[n]{x} $ | $$\sqrt[n]{x} $$ |
| subscript | `s_{x}` | $s_{x}$ | $$s_{x} $$ |
| summation | `\sum_{k=1}^{n}` | $\sum_{k=1}^{n} $ | $$\sum_{k=1}^{n} $$ |
| superscript | `s^{x}` | $s^{x} $ | $$s^{x} $$ |

#### Greek alphabet

| name | code | upppercase | lowercase | variant |
| --- | --- | :---: | :---: | :---: |
| alpha | `\alpha` |  | $\alpha $ |  |
| beta | `\beta` |  | $\beta $ |
| gamma | `\Gamma`, `\gamma` | $\Gamma $ | $\gamma $ |  |
| delta | `\Delta`, `\delta` | $\Delta $ | $\delta $ |  |
| epsilon | `\epsilon`, `\varepsilon` |  | $\epsilon $ | $\varepsilon $ |
| zeta | `\zeta` |  | $\zeta $ |  |
| eta | `\eta` |  | $\eta $ |  |
| theta | `\Theta`, `\theta`, `\vartheta` | $\Theta$ | $\theta$ | $\vartheta $ |
| iota | `\iota` |  | $\iota $ |  |
| kappa | `\kappa` |  | $\kappa$ |  |
| lambda | `\Lambda`, `\lambda` | $\Lambda$ | $\lambda$ |  |
| mu | `\mu` |  | $\mu$ |  |
| nu | `\nu` |  | $\nu$ |  |
| xi | `\Xi`, `\xi` | $\Xi$ | $\xi$ |  |
| omicron | `\omicron` |  | $\omicron$ |  |
| pi | `\Pi`, `\pi` | $\Pi$ | $\pi$ |  |
| rho | `\rho` |  | $\rho$ |  |
| sigma | `\Sigma`, `\sigma` | $\Sigma$ | $\sigma$ |  |
| tau | `\tau` |  | $\tau$ |  |
| upsilon | `\Upsilon`, `\upsilon` | $\Upsilon$ | $\upsilon$ |  |
| phi | `\Phi`, `\phi` | $\Phi$ | $\phi$ | $\varphi $ |
| chi | `\chi` |  | $\chi$ |  |
| psi | `\Psi`, `\psi` | $\Psi$ | $\psi$ |  |
| omega | `\Omega`, `\omega` | $\Omega$ | $\omega$ |  |

#### Symbols of Type Ord

| Name | Code | Symbol | Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: | --- | --- | :---: |
| aleph | `\aleph`| $\aleph$ |  | `\prime` | $\prime$ |  | `\forall` | $\forall$ |
| h-bar | `\hbar`| $\hbar$ |  | `\emptyset` | $\emptyset$ |  | `\exists` | $\exists$ |
|  | `\imath` | $\imath$ |  | `\nabla` | $\nabla$ |  | `\neg`, `\lnot` | $\neg$, $\lnot$ |
|  | `\jmath` | $\jmath$ |  | `\surd` | $\surd$ |  | `\flat` | $\flat$ |
|  | `\ell` | $\ell$ |  | `\top` | $\top$ |  | `\natural` | $\natural$ |
|  | `\wp` | $\wp$ |  | `\bot` | $\bot$ |  | `\sharp` | $\sharp$ |
|  | `\jmath` | $\hbar$ |  | `\\|` | $\\\|$ |  | `\clubsuit` | $\clubsuit$ |
|  | `\Re` | $\Re$ |  | `\angle` | $\angle$ |  | `\diamondsuit` | $\diamondsuit$ |
|  | `\Im` | $\Im$ |  | `\triangle` | $\triangle$ |  | `\heartsuit` | $\heartsuit$ |
|  | `\infty` | $\infty$ |  | `\backslash` | $\backslash$ |  | `\spadesuit` | $\spadesuit$ |
|  | `\textvisiblespace` | $\textvisiblespace$ |  |  |  |

#### Special symbols

Degree: 

^{\circ} $Ex: `22^{\circ}\mathrm{C}`: $22^{\circ}\mathrm{C}$.

#### Large Operators

| Name | Code | Symbol | Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: | --- | --- | :---: |
| summation | `\sum`| $$\sum$$ |  | `\bigcap`| $$\bigcap$$ |  | `\bigodot`| $$\bigodot$$ |
| product | `\prod`| $$\prod$$ |  | `\bigcup`| $$\bigcup$$ |  | `\bigotimes`| $$\bigotimes$$ |
| coproduct | `\coprod`| $$\coprod$$ |  | `\bigsqcup`| $$\bigsqcup$$ |  | `\bigoplus`| $$\bigoplus$$ |
|  | `\int`| $$\int$$ |  | `\bigvee`| $$\bigvee$$ |  | `\biguplus`| $$\biguplus$$ |
|  | `\oint`| $$\oint$$ |  | `\bigwedge`| $$\bigwedge$$ |

#### Binary Operations

| Name | Code | Symbol | Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: | --- | --- | :---: |
| plus-minus sign | `\pm`| $\pm$ |  | `\cap`| $\cap$ |  | `\vee`, `\lor` | $\vee$, $\lor$ |
| minus-plus sign | `\mp`| $\mp$ | | `\cup`| $\cup$ |  | `\wedge`, `\land` | $\wedge$, $\land$ |
|  | `\setminus`| $\setminus$ |  | `\uplus`| $\uplus$ |  | `\oplus`| $\oplus$ |
|  | `\cdot`| $\cdot$ |  | `\sqcap`| $\sqcap$ |  | `\ominus`| $\ominus$ |
|  | `\times`| $\times$ |  | `\sqcup`| $\sqcup$ |  | `\otimes`| $\otimes$ |
|  | `\ast`| $\ast$ |  | `\triangleleft`| $\triangleleft$ |  | `\oslash`| $\oslash$ |
|  | `\star`| $\star$ |  | `\triangleright`| $\triangleright$ |  | `\odot`| $\odot$ |
|  | `\diamond`| $\diamond$ |  | `\wr`| $\wr$ |  | `\dagger`| $\dagger$ |
|  | `\circ`| $\circ$ |  | `\bigcirc`| $\bigcirc$ |  | `\ddagger`| $\ddagger$ |
|  | `\bullet`| $\bullet$ |  | `\bigtriangleup`| $\bigtriangleup$ |  | `\amalg`| $\amalg$ |
|  | `\div`| $\div$ |  | `\bigtriangledown`| $\bigtriangledown$ |

#### Relations

| Name | Code | Symbol | Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: | --- | --- | :---: |
|  | `\leq`, `\le` | $\leq$, $\le$ |  | `\geq`, `\ge` | $\geq$, $\ge$ |  | `\equiv` | $\equiv$ |
|  | `\prec` | $\prec$ |  | `\succ` | $\succ$ |  | `\sim` | $\sim$ |
|  | `\preceq` | $\preceq$ |  | `\succeq` | $\succeq$ |  | `\simeq` | $\simeq$ |
|  | `\ll` | $\ll$ |  | `\gg` | $\gg$ |  | `\asymp` | $\asymp$ |
|  | `\subset` | $\subset$ |  | `\supset` | $\supset$ |   | `\approx` | $\approx$ |
|  | `\subseteq` | $\subseteq$ |   | `\supseteq` | $\supseteq$ |  | `\cong` | $\cong$ |
|  | `\sqsubseteq` | $\sqsubseteq$ |  | `\sqsupseteq` | $\sqsupseteq$ |  | `\bowtie` | $\bowtie$ |
|  | `\in` | $\in$ |  | `\notin` | $\notin$ |  | `\ni`, `\owns` | $\ni$, $\owns$ |
|  | `\vdash` | $\vdash$ |  | `\dashv` | $\dashv$ |  | `\models` | $\models$ |
|  | `\smile` | $\smile$ |  | `\mid` | $\mid$ |  | `\doteq` | $\doteq$ |
|  | `\frown` | $\frown$ |  | `\parallel` | $\parallel$ |  | `\perp` | $\perp$ |
|  | `\propto` | $\propto$ |

Most relations can be negated by prefixing them with $\backslash\texttt{not}$.

| Name | Code | Symbol | Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: | --- | --- | :---: |
|  | `\not\equiv` | $\not\equiv$ |  | `\notin` | $\notin$ |  | `\ne` | $\ne$ |

#### Arrows

| Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: |
|  | `\leftarrow`, `\gets` | $\leftarrow$, $\gets$ |  | `\longleftarrow` | $\longleftarrow$ |
|  | `\Leftarrow` | $\Leftarrow$ |  | `\Longleftarrow` | $\Longleftarrow$ |
|  | `\rightarrow`, `\to` | $\rightarrow$, $\to$ |  | `\longrightarrow` | $\longrightarrow$ |  
|  | `\Rightarrow` | $\Rightarrow$ |  | `\Longrightarrow` | $\Longrightarrow$ |
|  | `\leftrightarrow` | $\leftrightarrow$ |  | `\longleftrightarrow` | $\longleftrightarrow$ | 
|  | `\Leftrightarrow` | $\Leftrightarrow$ |  | `\Longleftrightarrow` | $\Longleftrightarrow$ |
|  | `\mapsto` | $\mapsto$ |  | `\longmapsto` | $\longmapsto$ |
|  | `\hookleftarrow` | $\hookleftarrow$ |  | `\hookrightarrow` | $\hookrightarrow$ |
|  | `\uparrow` | $\uparrow$ |  | `\Uparrow` | $\Uparrow$ |
|  | `\downarrow` | $\downarrow$ |  | `\Downarrow` | $\Downarrow$ |
|  | `\updownarrow` | $\updownarrow$ |  | `\Updownarrow` | $\Updownarrow$ |
|  | `\nearrow` | $\nearrow$ |  | `\searrow` | $\searrow$ |
|  | `\nwarrow` | $\nwarrow$ |  | `\swarrow` | $\swarrow$ |

The $\backslash\texttt{buildrel}$ macro puts one symbol over another. The format is $\backslash\texttt{buildrel}\langle\textnormal{superscript}\rangle\backslash\texttt{over}\langle\textnormal{relation}\rangle$.

`\buildrel\alpha\beta\over\longrightarrow` $\buildrel\alpha\beta\over\longrightarrow$

`f(x) \; {\buildrel\rm def\over=} \; x+1`
$f(x) \\; {\buildrel\rm def\over=} \\; x+1$

#### Delimiters

| Name | Code | Symbol | Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: | --- | --- | :---: |
|  | `\lbrack`, `[` | $\lbrack$, $[$ |  | `\lbrace`, `\{` | $\lbrace$, $\\{$ |  | `\langle` | $\langle$ |
|  | `\rbrack`, `[` | $\rbrack$, $]$ |  | `\rbrace`, `\}` | $\rbrace$, $\\}$ |  | `\rangle` | $\rangle$ |
|  | `\vert`, `\|` | $\vert$, $\\|$ |  | `\lfloor` | $\lfloor$ |  | `\lceil` | $\lceil$ |
|  | `\Vert`, `\\|` | $\Vert$, $\\\|$ |  | `\rfloor` | $\rfloor$ |  | `\rceil` | $\rceil$ |
|  | `[\![` | $[\\![$ |  | `(\!(` | $(\\!($ |  | `\langle\!\langle` | $\langle\\!\langle$ |
|  | `]\!]` | $]\\!]$ |  | `)\!)` | $)\\!)$ |  | `\rangle\!\rangle` | $\rangle\\!\rangle$ |

Left and right delimeters will be enlarged if they are prefixed with $\backslash\mathtt{left}$ or $\backslash\mathtt{right}$. Each $\backslash\mathtt{left}$ must have a matching $\backslash\mathtt{right}$, one of which may be an empty delimeter ($\backslash\mathtt{left.}$ or $\backslash\mathtt{right.}$). To specify a particular size, use the following:
$\backslash\mathtt{bigl}$, $\backslash\mathtt{bigr}$
$\backslash\mathtt{Bigl}$, $\backslash\mathtt{Bigr}$ 
$\backslash\mathtt{biggl}$, $\backslash\mathtt{biggr}$
\biggl, \biggr
You can also say $\backslash\mathtt{bigm}$ for a large delimenter in the middle of a formula, or just $\backslash\mathtt{big}$ for one that acts as an ordinary symbol.

#### Accents

| Name | Text mode | Math mode | Symbol |
| --- | --- | --- | :---: |
| hat | `\^` | `\hat` | $\hat{a}$ |
| expanding hat |  | `\widehat` | $\widehat{abc}$ |
| check | `\v` | `\check` | $\check{a}$ |
| tilde | `\~` | `\tilde` | $\tilde{a}$ |
| expanding tilde |  | `\widetilde` | $\widetilde{abc}$ |
| acute | `\'` | `\acute` | $\acute{a}$ |
| grave | `\’` | `\grave` | $\grave{a}$ |
| dot | `\.` | `\dot` | $\dot{a}$ |
| double dot | `\"` | `\ddot` | $\ddot{a}$ |
| breve | `\u` | `\breve` | $\breve{a}$ |
| bar | `\=` | `\bar` | $\bar{a}$ |
| vector |  | `\vec` | $\vec{a}$ |

The $\backslash\texttt{skew}\langle$number$\rangle$ command shifts accents for proper positioning,the larger the $\langle$number$\rangle$, the more right the shift. Compare

`\hat{\hat{A}}` gives $\hat{\hat{A}}$, `skew6\hat{\hat{A}}` gives $\skew6\hat{\hat{A}}$.

#### Elementary Math Control Sequences

| Name | Code | Example |
| --- | --- | :---: |
| overline a formula | `\overline{x+y}` | $$\overline{x+y}$$ |
| underline a formula | `\underline{x+y}` | $$\underline{x+y}$$ |
| square root | `\sqrt{x+y}` | $$\sqrt{x+y}$$ |
| higher order roots | `\root n\of{x+y}` | $$\root n\of{x+y}$$ |
| fraction | `{n+1\over 3}` | $${n+1\over 3}$$ |
| fraction, no line | `{n+1\atop 3}` | $${n+1\atop 3}$$ |
| binomial coeff. | `{n+1\choose 3}` | $${n+1\choose 3}$$ |
| braced fraction | `{n+1\brace 3}` | $${n+1\brace 3}$$ |
| bracketed fraction | `{n+1\brack 3}` | $${n+1\brack 3}$$ |

The following specify a style for typesetting formulas.
$\backslash\texttt{displaystyle}\\; \backslash\texttt{textstyle}\\; \backslash\texttt{scriptstyle}\\; \backslash\texttt{scriptscriptstyle}$

#### Non-Italic Function Names

| Name | Code | Example |
| --- | --- | :---: |
|  | `\arccos` | $\arccos$ |
|  | `\arcsin` | $\arcsin$ |
|  | `\arctan` | $\arctan$ |
|  | `\arg` | $\arg$ |
|  | `\cos` | $\cos$ |
|  | `\cosh` | $\cosh$ |
|  | `\cot` | $\cot$ |
|  | `\coth` | $\coth$ |
|  | `\csc` | $\csc$ |
|  | `\deg` | $\deg$ |
|  | `\det` | $\det$ |
|  | `\dim` | $\dim$ |
|  | `\exp` | $\exp$ |
|  | `\gcd` | $\gcd$ |
|  | `\hom` | $\hom$ |
|  | `\inf` | $\inf$ |
|  | `\ker` | $\ker$ |
|  | `\lg` | $\lg$ |
|  | `\lim` | $\lim$ |
|  | `\liminf` | $\liminf$ |
|  | `\limsup` | $\limsup$ |
|  | `\ln` | $\ln$ |
|  | `\log` | $\log$ |
|  | `\max` | $\max$ |
|  | `\min` | $\min$ |
|  | `\Pr` | $\Pr$ |
|  | `\sec` | $\sec$ |
|  | `\sin` | $\sin$ |
|  | `\sinh` | $\sinh$ |
|  | `\sup` | $\sup$ |
|  | `\tan` | $\tan$ |
|  | `\tanh` | $\tanh$ |


mod with parentheses `a \pmod{m}` $a \pmod{m}$

mod without parentheses `a \bmod m` $a \bmod m$

The following examples use \mathop to create function names.

| Example | Command | Plain $\TeX{}$ Definition |
| --- | --- | :---: |
| `\def\lim{\mathop{\rm lim}}` | `\lim_{x\to2}` | $\lim_{x\to2}$ |
| `\def\log{\mathop{\rm log}\nolimits}` | `\log_2` | $\log_{2}$ |

#### Fills, Leaders and Ellipses

Text or Math mode: `\dots` $\dots$ 

Math mode:

| Code | Example |
| --- | :---: |
| `\ldots` | $\ldots$ |
| `\cdots` | $\cdots$ |
| `\vdots` | $\vdots$ |
| `\ddots` | $\ddots$ |

The following fill space with the indicated item.
$\backslash\texttt{hrulefill} \\; \backslash\texttt{rightarrowfill}  \\; \backslash\texttt{leftarrowfill} \\; \backslash\texttt{dotfill}$

The general format for constructing leaders is <br>
$\backslash\texttt{leaders}\langle box \\; or \\; rule \rangle \backslash \texttt{hskip}\langle glue\rangle$ repeat box or rule <br>
$\backslash\texttt{leaders}\langle box \\; or \\; rule \rangle \backslash \texttt{hfill}$ fill space with box or rule

***

### Bibliography and citations

When using $\mathrm{B\scriptstyle IB}\TeX{}$, you need to run latex, bibtex, and latex twice more to resolve dependencies.

#### Citation Types

`\cite{key}` Full author list and year. (Watson and Crick 1953)

`\citeA{key}` Full author list. (Watson and Crick)

`\citeN{key}` Full author list and year. Watson and Crick (1953)

`\shortcite{key}` Abbreviated author list and year.

`\shortciteA{key}` Abbreviated author list.

`\shortciteN{key}` Abbreviated author list and year.

`\citeyear{key}` Cite year only. (1953)

All the above have an $\texttt{NP}$ variant without parentheses; Ex. `\citeNP`.

#### Bibtex entry types

`@article` Journal or magazine article.

`@book`Book with publisher.

`@booklet` Book without publisher.

`@conference` Article in conference proceedings.

`@inbook` A part of a book and/or range of pages.

`@incollection`A part of book with its own title.

`@manual` Technical documentation.

`@mastersthesis` Master's thesis.

`@misc`If nothing else fits.

`@phdthesis` PhD. thesis.

`@proceedings` Proceedings of a conference.

`@techreport` Tech report, usually numbered in series.

`@unpublished` Unpublished.

#### Bibtex fields

`address` Address of publisher. Not necessary for major publishers.

`author` Names of authors, of format ...

`booktitle` Title of book when part of it is cited.

`chapter` Chapter or section number.

`edition` Edition of a book.

`editor` Names of editors.

`institution` Sponsoring institution of tech. report.

`journal` Journal name.

`key` Used for cross ref. when no author.

`month` Month published. Use 3-letter abbreviation.

`note` Any additional information.

`number` Number of journal or magazine.

`organization` Organization that sponsors a conference.

`pages` Page range (2,6,9--12).

`publisher` Publisher's name.

`school` Name of school (for thesis).

`series` Name of series of books.

`title` Title of work.

`type` Type of tech. report, ex. \\Research Note".

`volume` Volume of a journal or book.

`year` Year of publication.

Not all fields need to be filled.

#### Common BibTeX style files

`abbrv` Standard
`alpha` Standard
`plain` Standard
`abstract` $\texttt{alpha}$ with abstract
`apa` APA
`unsrt` Unsorted

The $\LaTeX{}$ document should have the following two lines just
before \end{document}, where $\texttt{bibfile.bib}$ is the name of the
$\mathrm{B\scriptstyle IB}\TeX{}$ file.

`\bibliographystyle{plain}`
`\bibliography{bibfile}`

#### BibTeX example

The $\mathrm{B\scriptstyle IB}\TeX{}$ database goes in a file called $\textit{file}\texttt{.bib}$, which is processed with $\texttt{bibtex file}$.

```
@String{N = {Na\-ture}}
@Article{WC:1953,
  author = {James Watson and Francis Crick},
  title = {A structure for Deoxyribose Nucleic Acid},
  journal = N,
  volume = {171},
  pages = {737},
  year = 1953
}
```
