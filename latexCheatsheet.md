# $\LaTeX{}$ Cheatsheet

## Contents

| [Document classes](#document-classes) | [Document Structure](#document-structure) | [Text properties](#text-properties) | [Text-mode symbols](#text-mode-symbols)| [Tabular environments](#tabular-environments) | [Math mode](#math-mode) | [Bibliography and citations](#bibliography-and-citations) |
| --- | --- | --- | --- | --- | --- | --- |
| [Common documentclass options](#common-documentclass-options) | [Text environments](#text-environments) | [Font face](#font-face) | [Symbols](#symbols) | [tabbing environment](#tabbing-environment) | [Sensible size examples](#sensible-size-examples) | [Citation types](#citation-types) |
| [Packages](#packages) | [Lists](#lists) | [Font size](#font-size) | [Accents](#accents) | [tabular environment](#tabular-environment) | [Letters](#letters) | [BibTex entry types](#bibtex-entry-types) |
| [Title](#title) | [References](#references) | [Verbatim text](#verbatim-text) | [Dashes](#dashes) | [tabular column specification](#tabular-column-specification) | [Symbols of Type Ord](#symbols-of-type-ord) | [Bibtex fields](#bibtex-fields) |
| [Miscellaneous documents classes](#miscellaneous-documents-classes) | [Floating bodies](#floating-bodies) | [Justification](#justification) |  | [tabular elements](#tabular-elements) | [Large Operators](#large-operators) | [Common BibTeX style files](#common-bibtex-style-files) |
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

| Command | Description |
| :---: | --- |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{comment} \rbrace$ | Comment block (not printed) |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{quote} \rbrace$ | Indented quotation block |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{quotation} \rbrace$ Like $\texttt{quote}$ | with indented paragraphs |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{verse} \rbrace$ | Quotation block for verse |

#### Lists

| Command | Description |
| :---: | --- |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{enumerate} \rbrace$ | Numbered list |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{itemize} \rbrace$ | Bulleted list |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{description} \rbrace$ | Description list |
| $\backslash\texttt{item} \\; text$ | Add an item |
| $\backslash\texttt{item}\lbrack x \rbrack \\; text$ | Use $x$ instead of normal bullet or number<br>Required for descriptions |

#### References

| Command | Description |
| :---: | --- |
| $\backslash\texttt{label}\lbrace marker \rbrace$ | Set a marker for cross-reference, often of the form $\backslash\texttt{label}\lbrace\texttt{sec:item}\rbrace$ |
| $\backslash\texttt{ref}\lbrace marker \rbrace$ | Give section/body number of marker |
| $\backslash\texttt{pageref}\lbrace marker \rbrace$ | Give page number of marker |
| $\backslash\texttt{footnote}\lbrace text \rbrace$ | Print footnote at bottom of page |

#### Floating bodies

| Command | Description |
| :---: | --- |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{table} \rbrace \lbrack place \rbrack$ | Add numbered table |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{figure} \rbrace \lbrack place \rbrack$ | Add numbered figure |
| $\backslash\texttt{begi}\texttt{n}\lbrace \texttt{equation} \rbrace \lbrack place \rbrack$ | Add numbered equation |
| $\backslash\texttt{caption}\lbrace text \rbrace$ | Caption for the body |

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

| Command | Description |
| :---: | --- |
| $\backslash\texttt{begi}\texttt{n}\lbrace\texttt{verbatim}\rbrace$ | Verbatim environment |
| $\backslash\texttt{begi}\texttt{n}\lbrace\texttt{verbatim*}\rbrace$ | Spaces are shown as $\textvisiblespace$ |
| $\backslash\texttt{verb!}\texttt{text!}$ | Text between the delimiting characters (in this case $\texttt{!}$) is verbatim |

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

| Symbol | Command | Name |
| :---: | --- | --- |
| $\\&$ | `\&` | ampersand |
| $\backslash$ | `\backslash` | backslash |
| $\bullet$ | `\bullet` | bullet symbol |
| $\textasciicircum{}$ | `\^{}`, `\textasciicircum{}` | circumflex |
| $\copyright$ | `\copyright` | copyright symbol/sign |
| $\dag$ | `\dag` | dagger, obelisk, obelus |
| $\\$ $ | `\$` | dollar sign |
| $\ddag$ | `\ddag` | double dagger, diesis |
| $\ldots$ | `\ldots` | ellipsis |
| $\\# $ | `\#` | number sign |
| $\\% $ | `\%` | percentage sign |
| $\P$ | `\P` | pilcrow |
| $\pounds$ | `\pounds` | pound sign |
| $\\S $ | `\S` | section sign |
| $\textasciitilde{}$ | `\~{}`, `\textasciitilde{}` | tilde |
| $\\_ $ | `\_` | underscore |
| $\\|$ | `\|`, `\mid`, `\textpipe`, `\textbar` | vertical bar (pipe) |

#### Accents

| Symbol | Command | Name |
| :---: | --- | --- |
| $\textnormal{\\\`o}$ | `\‘o` |  |
| $\textnormal{\\'o}$ | `\’o` |  |
| $\textnormal{\\^{}}$ | `\^{}` |  |
| $\textnormal{\\~{o}}$ | `\~{o}` |  |
| $\textnormal{\\\={o}}$ | `\={o}` |  |
| $\textnormal{\\\.{o}}$ | `\.{o}` |  |
| $\textnormal{\\\"{o}}$ | `\"{o}` |  |
| $\textnormal{\\co}$ | `\c{o}` |  |
| $\textnormal{\\v{o}}$ | `\v{o}` |  |
| $\textnormal{\\H{o}}$ | `\H{o}` |  |
| $\textnormal{\\c{c}}$ | `\c{c}` |  |
| $\textnormal{\\d{o}}$ | `\d{o}` |  |
| $\textnormal{\\b{o}}$ | `\b{o}` |  |
| $\textnormal{\\t{oo}}$ | `\t{oo}` |  |
| $\textnormal{\\oe}$ | `\oe` |  |
| $\textnormal{\\OE}$ | `\OE` |  |
| $\textnormal{\\ae}$ | `\ae` |  |
| $\textnormal{\\AE}$ | `\AE` |  |
| $\textnormal{\\aa}$ | `\aa` |  |
| $\\textnormal{\\AA}$ | `\AA` |  |
| $\\textnormal{\\o}$ | `\o` |  |
| $\\textnormal{\\O}$ | `\O ` |  |
| $\\textnormal{\\l}$ | `\l` |  |
| $\\textnormal{\\L}$ | `\L` |  |
| $\\textnormal{\\i}$ | `\i ` |  |
| $\\textnormal{\\j}$ | `\j ` |  |
| $\\textnormal{\\\ss}$ | `\ss` |  |
| $\textnormal{\~\`}$ | `~‘` |  |
| $\textnormal{\?\`}$ | `?‘` |  |

#### Dashes

| Name | Source | Example | Usage |
| --- | :---: | :---: | --- |
| hyphen | - | X $\textnormal{-}$ ray | In words. |
| en-dash | -- | 1 $\textnormal{--}$ 5 | Between numbers. |
| em-dash | --- | Yes $\textnormal{---}$ or no? | Punctuation. |

#### Line and page breaks

| Command | Description |
| :---: | --- |
| `\\` | Begin new line without new paragraph |
| `\\*` | Prohibit pagebreak after linebreak |
| $\backslash\texttt{kill}$ | Don't print current line |
| $\backslash\texttt{pagebreak}$ | Start new page |
| $\backslash\texttt{noindent}$ | Do not indent current line |

#### Miscellaneous text-mode symbols

| Command | Description |
| --- | --- |
| $\backslash\texttt{today}$ | February 17, 2023 |
| $\\$\backslash\texttt{sim}\\$$ | Prints $\sim$ instead of `\~{}`, which makes $\textnormal{\\~{ }}$. |
| $\texttt{\\~{ }}$ | Space, disallow linebreak $\texttt{(W.J.\\~{ }Clinton)}$. |
| $\backslash\texttt{@.}$ | Indicate that the $\texttt{.}$ ends a sentence when following an uppercase letter. |
| $\backslash\texttt{hspace \\{ l \\}}$ | Horizontal space of length $l$ (Ex: l = $\texttt{20pt}$). |
| $\backslash\texttt{vspace \\{ l \\}}$ | Vertical space of length $l$. |
 $\backslash\texttt{vspace \\{ w \\}\\{ h \\}}$ | Line of width $w$ and height $h$. |

***

### Tabular environments

#### tabbing environment

$\backslash\texttt{=}$ Set tab stop.<br>
$\backslash\texttt{>}$ Go to tab stop.<br>
Tab stops can be set on "invisible" lines with $\backslash\texttt{kill}$ at the end of the line. Normally $\backslash\backslash$ is used to separate lines.

#### tabular environment

$\backslash\texttt{begi}\texttt{n}\lbrace\texttt{array}\rbrace\lbrack pos \rbrack\lbrace cols \rbrace$<br>
$\backslash\texttt{begi}\texttt{n}\lbrace\texttt{tabular}\rbrace\lbrack pos \rbrack\lbrace cols \rbrace$<br>
$\backslash\texttt{begi}\texttt{n}\lbrace\texttt{tabular*}\rbrace\lbrace width \rbrace\lbrack pos \rbrack\lbrace cols \rbrace$

#### tabular column specification

| Command | Description |
| :---: | --- |
| $\texttt{l}$ | Left-justified column. |
| $\texttt{c}$ | Centered column. |
| $\texttt{r}$ | Right-justified column. |
| $\texttt{p}\texttt{\\{ width \\}}$ | Same as $\backslash\texttt{parbox[t]\\{width\\}}$. |
| $\texttt{@}\texttt{\\{ decl \\}}$ | Insert $decl$ instead of inter-column space. |
| $\texttt{\\|}$ | Inserts a vertical line between columns. |

#### tabular elements

$\backslash\texttt{hline}$ Horizontal line between rows.<br>
$\backslash\texttt{cline \\{ x-y \\}}$ Horizontal line across columns $x$ through $y$.<br>
$\backslash\texttt{multicolumn}\lbrace n \rbrace\lbrace cols \rbrace\lbrace text \rbrace$ A cell that spans $n$ columns, with $cols$ column specification.

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


#### letters

##### Greek alphabet

| name | code | upppercase | lowercase | variant |
| --- | --- | :---: | :---: | :---: |
| alpha | `\alpha` |  | $\alpha$ |  |
| beta | `\beta` |  | $\beta$ |
| gamma | `\Gamma`, `\gamma` | $\Gamma$ | $\gamma$ |  |
| delta | `\Delta`, `\delta` | $\Delta$ | $\delta$ |  |
| epsilon | `\epsilon`, `\varepsilon` |  | $\epsilon$ | $\varepsilon$ |
| zeta | `\zeta` |  | $\zeta$ |  |
| eta | `\eta` |  | $\eta$ |  |
| theta | `\Theta`, `\theta`, `\vartheta` | $\Theta$ | $\theta$ | $\vartheta$ |
| iota | `\iota` |  | $\iota$ |  |
| kappa | `\kappa`, `\varkappa` |  | $\kappa$ | $\varkappa$ |
| lambda | `\Lambda`, `\lambda` | $\Lambda$ | $\lambda$ |  |
| mu | `\mu` |  | $\mu$ |  |
| nu | `\nu` |  | $\nu$ |  |
| xi | `\Xi`, `\xi` | $\Xi$ | $\xi$ |  |
| omicron | `\omicron` |  | $\omicron$ |  |
| pi | `\Pi`, `\pi`, `\varpi` | $\Pi$ | $\pi$ | $\varpi$ |
| rho | `\rho`, `varrho` |  | $\rho$ | $\varrho$ |
| sigma | `\Sigma`, `\sigma`, `\varsigma` | $\Sigma$ | $\sigma$ | $\varsigma$ |
| tau | `\tau` |  | $\tau$ |  |
| upsilon | `\Upsilon`, `\upsilon` | $\Upsilon$ | $\upsilon$ |  |
| phi | `\Phi`, `\phi`, `\varphi` | $\Phi$ | $\phi$ | $\varphi$ |
| chi | `\chi` |  | $\chi$ |  |
| psi | `\Psi`, `\psi` | $\Psi$ | $\psi$ |  |
| omega | `\Omega`, `\omega` | $\Omega$ | $\omega$ |  |

##### Archaic Greek

| name | code | upppercase | lowercase | variant |
| --- | --- | :---: | :---: | :---: |
| digamma | `\digamma` |  | $\digamma$ |  |

##### Hebrew letters

| Name | Command | Symbol |
| --- | --- | :---: |
| aleph | `\aleph` | $\aleph$ |
| beth | `\beth` | $\beth$ |
| gimel | `\gimel` | $\gimel$ |
| daleth | `\daleth` | $\daleth$ |

##### Other letters

| Name | Command | Symbol |
| --- | --- | :---: |
|  | `\complement` | $\complement$ |
|  | `\ell` | $\ell$ |
|  | `\eth` | $\eth$ |
|  | `\Finv` | $\Finv$ |
| h-bar, reduced Plancks's constant | `\hbar` | $\hbar$ |
|  | `\hslash` | $\hslash$ |
|  | `\Bbbk` | $\Bbbk$ |
|  | `\mho` | $\mho$ |
| partial derivative | `\partial` | $\partial$ |
|  | `\circledS` | $\circledS$ |
| [Weierstrass] powerset | `\wp` | $\wp$ |

#### Symbols of Type Ord

| Symbol | Command | Name | Symbol | Command | Name | Symbol | Command | Name |
| :---: | --- | --- | :---: | --- | --- | :---: | --- | --- |
| $\forall$ | `\forall` | for all | $\prime$ | `\prime` |  |  |  |  |
| $\exists$ | `\exists` | there exists at least one | $\emptyset$ | `\emptyset` |  |  |  |  |
| $\exists!$ | `\exists!` | there exists one and only one | $\nabla$ | `\nabla` | del, nabla |  |  |  |
| $\nexists$ | `\nexists` | there is no | $\surd$ | `\surd` |  |  |  |  |
| $\imath$ | `\imath` |  | $\flat$ | `\flat` |  | $\neg$, $\lnot$ | `\neg`, `\lnot` | logical not |
| $\jmath$ | `\jmath` |  | $\natural$ | `\natural` |  | $\top$ | `\top` |  |
| $\Re$ | `\Re` | real part | $\sharp$ | `\sharp` |  | $\bot$ | `\bot` |  |
| $\Im$ | `\Im` | imaginary part | $\\\|$ | `\\|` |  | $\clubsuit$ | `\clubsuit` |  |
|  |  |  | $\angle$ | `\angle` |  | $\diamondsuit$ | `\diamondsuit` |  |
| $\infty$ | `\infty` | infinity | $\triangle$ | `\triangle` |  | $\heartsuit$ | `\heartsuit` |  |
| $\textvisiblespace$ | `\textvisiblespace` |  | $\backslash$ | `\backslash` |  | $\spadesuit$ | `\spadesuit` |  |

#### Special symbols

Degree: 

^{\circ} $Ex: `22^{\circ}\mathrm{C}`: $22^{\circ}\mathrm{C}$.

#### Large Operators

| Symbol | Code | Name | Symbol | Code | Name | Symbol | Code | Name |
| :---: | --- | --- | :---: | --- | --- | :---: | --- | --- |
| $$\sum$$ | `\sum`| summation | $$\bigcap$$ | `\bigcap`| set intersection | $$\bigodot$$ | `\bigodot`|  |
| $$\prod$$ | `\prod`| product | $$\bigcup$$ | `\bigcup`| set union | $$\bigotimes$$ | `\bigotimes`|  |
| $$\coprod$$ | `\coprod`| coproduct | $$\bigsqcup$$ | `\bigsqcup`|  | $$\bigoplus$$ | `\bigoplus`|  |
| $$\int$$ | `\int`|  | $$\bigvee$$ | `\bigvee`|  | $$\biguplus$$ | `\biguplus`| multiset addition |
| $$\oint$$ | `\oint`|  | $$\bigwedge$$ | `\bigwedge`|  |  |  |  |

#### Binary Operations

| Symbol | Code | Name | Symbol | Code | Name | Symbol | Code | Name |
| :---: | --- | --- | :---: | --- | --- | :---: | --- | --- |
| $\pm$ | `\pm`| plus-minus sign | $\cap$ | `\cap`| set intersection | $\vee$, $\lor$ | `\vee`, `\lor` |  |
| $\mp$ | `\mp`| minus-plus sign | $\cup$ | `\cup`| set union | $\wedge$, $\land$ | `\wedge`, `\land` |  |
| $\setminus$ | `\setminus`| set diference | $\uplus$ | `\uplus`| multiset addition | $\oplus$ | `\oplus`|  |
| $\cdot$ | `\cdot`|  | $\sqcap$ | `\sqcap`|  | $\ominus$ | `\ominus`|  |
| $\times$ | `\times`|  | $\sqcup$ | `\sqcup`|  | $\otimes$ | `\otimes`|  |
| $\ast$ | `\ast`|  | $\triangleleft$ | `\triangleleft`|  | $\oslash$ | `\oslash`|  |
| $\star$ | `\star`|  | $\triangleright$ | `\triangleright`|  | $\odot$ | `\odot`|  |
| $\diamond$ | `\diamond`|  | $\wr$ | `\wr`|  | $\dagger$ | `\dagger`| dagger, obelisk, obelus |
| $\circ$ | `\circ`|  | $\bigcirc$ | `\bigcirc`|  | $\ddagger$ | `\ddagger`| double dagger, diesis |
| $\bullet$ | `\bullet`|  | $\bigtriangleup$ | `\bigtriangleup`|  | $\amalg$ | `\amalg`|  |
| $\div$ | `\div`|  | $\bigtriangledown$ | `\bigtriangledown`|  |

#### Relations

| Symbol | Code | Name | Symbol | Code | Name |
| :---: | --- | --- | :---: | --- | --- |
| $<$ | `<` | is less than | $>$ | `>` | is greater than |
| $\nless$ | `\nless` | is not less than | $\ngtr$ | `\ngtr` | is not greater than |
| $\leq$, $\le$ | `\leq`, `\le` | is less than or equal to | $\geq$, $\ge$ | `\geq`, `\ge` | is greater than or equal to |
| $\leqslant$ | `\leqslant` | is less than or equal to | $\geqslant$ | `\geqslant` | is greater than or equal to |
| $\nleq$ | `\nleq` | is neither less than nor equal to | $\ngeq$ | `\ngeq` | is neither greater than nor equal to |
| $\nleqslant$ | `\nleqslant` | is neither less than nor equal to | $\ngeqslant$ | `\ngeqslant	` | is neither greater than nor equal to |
| $\prec$ | `\prec` | precedes | $\succ$ | `\succ` | succeeds |
| $\nprec$	| `\nprec` | doesn't precede | $\nsucc$ | `\nsucc` | doesn't succeed |
| $\preceq$ | `\preceq` | precedes or equals | $\succeq$ | `\succeq` | succeeds or equals |
| $\npreceq$ | `\npreceq` | neither precedes nor equals | $\nsucceq$ | `\nsucceq` | neither succeeds nor equals |
| $\ll$ | `\ll` |  | $\gg$ | `\gg` |  |
| $\lll$, $\llless$ | `\lll`, `\llless` |  | $\ggg$, $\gggtr$ | `\ggg`, `\gggtr` |  |
| $\subset$ | `\subset` | is a proper subset of | $\supset$ | `\supset` | is a proper superset of |
| $\not\subset	$ | `\not\subset	` | is not a proper subset of | $\not\supset$ | `\not\supset	` | is not a proper superset of |
| $\subseteq$ | `\subseteq` | is a subset of$ | $\supseteq$ | `\supseteq` | is a superset of |
| $\sqsubset$ | `\sqsubset` |  | $\sqsupset$ | `\sqsupset` |  |
| $\sqsubseteq$ | `\sqsubseteq` |  | $\sqsupseteq$ | `\sqsupseteq` |  |

| Symbol | Code | Name |
| :---: | --- | --- |
| $=$ | `=` | is equal to |
| $\doteq$ | `\doteq` |  |
| $\equiv$ | `\equiv` | is equivalent to |
| $\approx$ | `\approx` | is approximately |
| $\cong$ | `\cong` | is congruent to |
| $\simeq$ | `\simeq` | is similar or equal to |
| $\sim$ | `\sim` | is similar to |
| $\propto$ | `\propto` | is proportional to |
| $\neq$, $\ne$ | `\neq`, `\ne` | is not equal to |

| Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: |
| $\parallel$ | `\parallel` | is parallel with | $\nparallel$ | `\nparallel` | is not parallel with |
| $\asymp$ | `\asymp` | is asymptotic to | $\bowtie$ | `\bowtie` |  |
| $\vdash$ | `\vdash` |  | $\dashv$ | `\dashv` |  |
| $\in$ | `\in` | is member of | $\ni$, $\owns$ | `\ni`, `\owns` | has member, owns |
| $\smile$ | `\smile` |  | $\frown$ | `\frown` |  |
| $\models$ | `\models` | models | $\notin$ | `\notin` | is not member of |
| $\perp$ | `\perp` | is perpendicular with | $\mid$ | `\mid` | divides |

| Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: |
| $\neq$, $\ne$ | `\neq`,  `\ne` | is not equal to | $\notin	$ | `\notin	` | is not member of |
| $\nless$ | `\nless` | is not less than | $\ngtr$ | `\ngtr` | is not greater than |
| $\nleq$ | `\nleq` | is not less than or equal to | $\ngeq$ | `\ngeq` | is not greater than or equal to |
| $\nleqslant	$ | `\nleqslant` |  | $\ngeqslant$ | `\ngeqslant` |  |
| $\nleqq	$ | `\nleqq` |  | $\ngeqq$ | `ngeqq` |  |
| $\lneq	$ | `\lneq` |  | $\gneq$ | `gneq` |  |
| $\lneqq	$ | `\lneqq` |  | $\gneqq$ | `\gneqq` |  |
| $\lvertneqq	$ | `\lvertneqq` |  | $\gvertneqq$ | `\gvertneqq` |  |
| $\lnsim	$ | `\lnsim` |  | $\gnsim$ | `\gnsim` |  |
| $\lnapprox	$ | `\lnapprox` |  | $\gnapprox$ | `\gnapprox` |  |
| $\nprec$ | `\nprec` | does not precede | $\nsucc$ | `\nsucc` | does not succeed |
| $\npreceq$ | `\npreceq` | neither precedes nor equals | $\nsucceq$ | `\nsucceq` | neither succedes nor equals |
| $\precneqq$ | `\precneqq` |  | $\succneqq$ | `\succneqq` |  |
| $\precnsim$ | `\precnsim` |  | $\succnsim$ | `\succnsim` |  |
| $\precnapprox$ | `\precnapprox` |  | $\succnapprox$ | `\succnapprox` |  |
| $\nsim$ | `\nsim	` | is not similar to	| $\ncong$ | `\ncong` | is not congruent to |
| $\nshortmid$	 | `\nshortmid` |  | $\nshortparallel$ | `\nshortparallel` |  |
| $\nmid$ | `\nmid` |  | $\nparallel$ | `\nparallel	` | is not parallel with |
| $\nvdash$ | `\nvdash` |  | $\nvDash$ | `\nvDash` |  |
| $\nVdash$ | `\nVdash` |  | $\nVDash$ | `\nVDash` |  |
| $\ntriangleleft$ | `\ntriangleleft` |  | $\ntriangleright$ | `\ntriangleright` |  |
| $\ntrianglelefteq$ | `\ntrianglelefteq` |  | $\ntrianglerighteq$ | `\ntrianglerighteq` |  |
| $\nsubseteq$ | `\nsubseteq` |  | $\nsupseteq$ | `\nsupseteq` |  |
| $\nsubseteqq$ | `\nsubseteqq` |  | $\nsupseteqq$ | `\nsupseteqq` |  |
| $\subsetneq$ | `\subsetneq` |  | $\supsetneq$ | `\supsetneq` |  |
| $\varsubsetneq$ | `\varsubsetneq` |  | $\varsupsetneq$ | `\varsupsetneq` |  |
| $\subsetneqq$| `\subsetneqq` |  | $\supsetneqq$ | `\supsetneqq` |  |
| $\varsubsetneqq$ | `\varsubsetneqq` |  | $\varsupsetneqq$ | `\varsupsetneqq` |  |

Most relations can be negated by prefixing them with $\backslash\texttt{not}$.

| Symbol | Code | Name | Symbol | Code | Name | SymbolName | Code | Name |
| --- | --- | :---: | --- | --- | :---: | --- | --- | :---: |
|  | `\not\equiv` | $\not\equiv$ |  | `\notin` | $\notin$ |  | `\ne` | $\ne$ |

#### Arrows

| Symbol | Code | Name | Symbol | Code | Name |
| :---: | --- | --- | :---: | --- | --- |
| $\circlearrowleft$ | `\circlearrowleft` |  | $\circlearrowright$ | `\circlearrowright` |  |
| $\leftarrow$, $\gets$ | `\leftarrow`, `\gets` |  | $\longleftarrow$ | `\longleftarrow` |  |
| $\curvearrowleft$ | `\curvearrowleft` |  | $\curvearrowright$ | `\curvearrowright` |  |
| $\upuparrows$ | `\upuparrows` |  | $\downdownarrows$ | `\downdownarrows` |  |
| $\downharpoonleft$ | `\downharpoonleft` |  | $\downharpoonright$ | `\downharpoonright` |  |
| $\leftarrowtail$ | `\leftarrowtail` |  | $\rightarrowtail$ | `\rightarrowtail` |  |
| $\leftharpoondown$ | `\leftharpoondown` |  | $\leftharpoonup$ | `\leftharpoonup` |  |
| $\leftleftarrows$ | `\leftleftarrows` |  | $\rightrightarrows$ | `\rightrightarrows` |  |
| $\leftrightarrows$ | `\leftrightarrows` |  | $\rightleftarrows$ | `\rightleftarrows` |  |
| $\Lleftarrow$ | `\Lleftarrow` |  | $\Rrightarrow$ | `\Rrightarrow` |  |
| $\Lsh$ | `\Lsh` |  | $\Rsh$ | `\Rsh` |  |
| $\upharpoonleft$ | `\upharpoonleft` |  | $\upharpoonright$, $\restriction$ | `\upharpoonright`, `\restriction` |  |
| $\twoheadleftarrow$ | `\twoheadleftarrow` |  | $\twoheadrightarrow$ | `\twoheadrightarrow` |  |
| $\leftrightsquigarrow$ | `\leftrightsquigarrow` |  | $\rightsquigarrow$ | `\rightsquigarrow` |  |
| $\leftrightharpoons$ | `$\leftrightharpoons$` |  | $\rightleftharpoons$ | `\rightleftharpoons` |  |
| $\rightharpoondown$ | `\rightharpoondown` |  | $\rightharpoonup$ | `\rightharpoonup` |  |
| $\nLeftarrow$ | `\nLeftarrow` |  | $\nRightarrow$ | `\nRightarrow` |  |
| $\looparrowleft$ | `\looparrowleft` |  | $\looparrowright$ | `\looparrowright` |  |
| $\nleftarrow$ | `\nleftarrow` |  | $\nrightarrow$ | `\nrightarrow` |  |
| $\nleftrightarrow$ | `\nleftrightarrow` |  | $\multimap$ | `\multimap` |  |
| $\Leftarrow$ | `\Leftarrow` |  | $\Longleftarrow$ | `\Longleftarrow` |  |
| $\rightarrow$, $\to$ | `\rightarrow`, `\to` |  | $\longrightarrow$ | `\longrightarrow` |  |  
| $\Rightarrow$ | `\Rightarrow` |  | $\Longrightarrow$, $\implies$ | `\Longrightarrow`, `\implies` |  |
| $\leftrightarrow$ | `\leftrightarrow` |  | $\longleftrightarrow$ | `\longleftrightarrow` |  | 
| $\Leftrightarrow$ | `\Leftrightarrow` |  | $\Longleftrightarrow$ | `\Longleftrightarrow` |  |
| $\mapsto$ | `\mapsto` |  | $\longmapsto$ | `\longmapsto` |  |
| $\hookleftarrow$ | `\hookleftarrow` |  | $\hookrightarrow$ | `\hookrightarrow` |  |
| $\uparrow$ | `\uparrow` |  | $\Uparrow$ | `\Uparrow` |  |
| $\downarrow$ | `\downarrow` |  | $\Downarrow$ | `\Downarrow` |  |
| $\updownarrow$ | `\updownarrow` |  | $\Updownarrow$ | `\Updownarrow` |  |
| $\nearrow$ | `\nearrow` |  | $\searrow$ | `\searrow` |  |
| $\nwarrow$ | `\nwarrow` |  | $\swarrow$ | `\swarrow` |  |

The $\backslash\texttt{buildrel}$ macro puts one symbol over another. The format is $\backslash\texttt{buildrel}\langle\textnormal{superscript}\rangle\backslash\texttt{over}\langle\textnormal{relation}\rangle$.

`\buildrel\alpha\beta\over\longrightarrow` $\buildrel\alpha\beta\over\longrightarrow$

`f(x) \; {\buildrel\rm def\over=} \; x+1`
$f(x) \\; {\buildrel\rm def\over=} \\; x+1$

#### Delimiters

| Symbol | Code | Name | Symbol | Code | Name | Symbol | Code | Name |
| :---: | --- | --- | :---: | --- | --- | :---: | --- | --- |
| $\lbrack$, $[$ | `\lbrack`, `[` |  | $\lbrace$, $\\{$ | `\lbrace`, `\{` |  | $\langle$ | `\langle` |  |
| $\rbrack$, $]$ | `\rbrack`, `[` |  | $\rbrace$, $\\}$ | `\rbrace`, `\}` |  | $\rangle$ | `\rangle` |  |
| $\vert$, $\\|$ | `\vert`, `\|` |  | $\lfloor$ | `\lfloor` |  | $\lceil$ | `\lceil` |  |
| $\Vert$, $\\\|$ | `\Vert`, `\\|` |  | $\rfloor$ | `\rfloor` |  | $\rceil$ | `\rceil` |  |
| $[\\![$ | `[\![` |  | $(\\!($ | `(\!(` |  | $\langle\\!\langle$ | `\langle\!\langle` |  |
| $]\\!]$ | `]\!]` |  | $)\\!)$ | `)\!)` |  | $\rangle\\!\rangle$ | `\rangle\!\rangle` |  |

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
|  |  | `\overset{*}{X}` | $\overset{\*}{X}$ |
|  |  | `\underset{*}{X}` | $\underset{\*}{X}$ |
|  |  | `\sideset{}{'}\sum` | $\sideset{}{'}\sum$ |
|  |  | `\sideset{_1^2}{_3^4}\sum` | $\sideset{\_1^2}{\_3^4}\sum$ |
| overline |  | `\overline{abc}` | $\overline{abc}$ |
| underline |  | `\underline{abc}` | $\underline{abc}$ |
| overbrace |  | `\overbrace{abc}` | $\overbrace{abc}$ |
| underbrace |  | `\underbrace{abc}` | $\underbrace{abc}$ |
|  |  | `\overleftarrow{abc}` | $\overleftarrow{abc}$ |
|  |  | `\overrightarrow{abc}` | $\overrightarrow{abc}$ |
|  |  | `\overleftrightarrow{abc}` | $\overleftrightarrow{abc}$ |
|  |  | `\xleftarrow[under]{over}` | $\xleftarrow[under]{over}$ |
|  |  | `\xrightarrow[under]{over}` | $\xrightarrow[under]{over}$ |

The $\backslash\texttt{skew}\langle$number$\rangle$ command shifts accents for proper positioning,the larger the $\langle$number$\rangle$, the more right the shift. Compare

`\hat{\hat{A}}` gives $\hat{\hat{A}}$, `skew6\hat{\hat{A}}` gives $\skew6\hat{\hat{A}}$.

#### Elementary Math Control Sequences

| Example | Code | Name |
| :---: | --- | --- |
| $$\overline{x+y}$$ | `\overline{x+y}` | overline a formula |
| $$\underline{x+y}$$ | `\underline{x+y}` | underline a formula |
| $$\sqrt{x+y}$$ | `\sqrt{x+y}` | square root |
| $$\root n\of{x+y}$$ | `\root n\of{x+y}` | higher order roots |
| $${n+1\over 3}$$ | `{n+1\over 3}` | fraction |
| $${n+1\atop 3}$$ | `{n+1\atop 3}` | fraction, no line |
| $${n+1\choose 3}$$ | `{n+1\choose 3}` | binomial coeff. |
| $${n+1\brace 3}$$ | `{n+1\brace 3}` | braced fraction |
| $${n+1\brack 3}$$ | `{n+1\brack 3}` | bracketed fraction |

The following specify a style for typesetting formulas.
$\backslash\texttt{displaystyle}\\; \backslash\texttt{textstyle}\\; \backslash\texttt{scriptstyle}\\; \backslash\texttt{scriptscriptstyle}$

#### Non-Italic Function Names

| Example | Code | Name |
| :---: | --- | --- |
| $\arccos$ | `\arccos` | arccosine |
| $\arcsin$ | `\arcsin` | arcsine |
| $\arctan$ | `\arctan` | arctangent |
| $\arg$ | `\arg` | argument of |
| $\cos$ | `\cos` | cosine |
| $\cosh$ | `\cosh` | hyperbolic cosine |
| $\cot$ | `\cot` | cotangent |
| $\coth$ | `\coth` | hyperbolic cotangent |
| $\csc$ | `\csc` | cosecant |
| $\deg$ | `\deg` | degree |
| $\det$ | `\det` | determinant |
| $\dim$ | `\dim` | dimension |
| $\exp$ | `\exp` | exponential function |
| $\gcd$ | `\gcd` | greatest common divisor |
| $\hom$ | `\hom` | hom-class |
| $\inf$ | `\inf` | infimum of a set |
| $\ker$ | `\ker` | kernel |
| $\lg$ | `\lg` | common logarithm ($\log_{10}$, $\log_{2}$) |
| $\lim$ | `\lim` | limit (sequence, function) |
| $\varinjlim$ | `\varinjlim` |  |
| $\varprojlim$ | `\varprojlim` |  |
| $\varliminf$ | `\varliminf` |  |
| $\varliminf$ | `\varliminf` |  |
| $\varlimsup$ | `\varlimsup` |  |
| $\liminf$ | `\liminf` | limit inferior |
| $\limsup$ | `\limsup` | limit superior |
| $\ln$ | `\ln` | natural logarithm ($\log_{e}$) |
| $\log$ | `\log` | logarithm ($\log_{10}$, $\log_{e}$) |
| $\max$ | `\max` | maximum of a set |
| $\min$ | `\min` | minimum of a set |
| $\Pr$ | `\Pr` | probability of an event |
| $\sec$ | `\sec` | secant |
| $\sin$ | `\sin` | sine |
| $\sinh$ | `\sinh` | hyperbolic sine |
| $\sup$ | `\sup` | supremum of a set |
| $\tan$ | `\tan` | tangent |
| $\tanh$ | `\tanh` | hyperbolic tangent |
| $\operatorname{zzz}\_{0}^{1}$ | `\operatorname{zzz}\_{0}^{1}` | generic operator |


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

| Example | Command |
| :---: | --- |
| $\ldots$ | `\ldots` |
| $\cdots$ | `\cdots` |
| $\vdots$ | `\vdots` |
| $\ddots$ | `\ddots` |

The following fill space with the indicated item.
$\backslash\texttt{hrulefill} \\; \backslash\texttt{rightarrowfill}  \\; \backslash\texttt{leftarrowfill} \\; \backslash\texttt{dotfill}$

The general format for constructing leaders is <br>
$\backslash\texttt{leaders}\langle box \\; or \\; rule \rangle \backslash \texttt{hskip}\langle glue\rangle$ repeat box or rule <br>
$\backslash\texttt{leaders}\langle box \\; or \\; rule \rangle \backslash \texttt{hfill}$ fill space with box or rule

***

### Bibliography and citations

When using $\mathrm{B\scriptstyle IB}\TeX{}$, you need to run latex, bibtex, and latex twice more to resolve dependencies.

#### Citation Types

| Entry | Description |
| --- | --- |
| `\cite{key}` | Full author list and year. (Watson and Crick 1953) |
| `\citeA{key}` | Full author list. (Watson and Crick) |
| `\citeN{key}` | Full author list and year. Watson and Crick (1953) |
| `\shortcite{key}` | Abbreviated author list and year. |
| `\shortciteA{key}` | Abbreviated author list. |
| `\shortciteN{key}` | Abbreviated author list and year. |
| `\citeyear{key}` | Cite year only. (1953) |

All the above have an $\texttt{NP}$ variant without parentheses; Ex. `\citeNP`.

#### Bibtex entry types

| Entry | Description |
| --- | --- |
| `@article` | Journal or magazine article. |
| `@book` | Book with publisher. |
| `@booklet` | Book without publisher. |
| `@conference` | Article in conference proceedings. |
| `@inbook` | A part of a book and/or range of pages. |
| `@incollection` | A part of book with its own title. |
| `@manual` |  Technical documentation. |
| `@mastersthesis` | Master's thesis. |
| `@misc` | If nothing else fits. |
| `@phdthesis` | PhD. thesis. |
| `@proceedings` | Proceedings of a conference. |
| `@techreport` | Tech report, usually numbered in series. |
| `@unpublished` | Unpublished. | 

#### Bibtex fields

| Entry | Description |
| --- | --- |
| `address` | Address of publisher. Not necessary for major publishers. |
| `author` | Names of authors, of format ... |
| `booktitle` | Title of book when part of it is cited. |
| `chapter` | Chapter or section number. |
| `edition` | Edition of a book. |
| `editor` | Names of editors. |
| `institution` | Sponsoring institution of tech. report. |
| `journal` | Journal name. |
| `key` | Used for cross ref. when no author. |
| `month` | Month published. Use 3-letter abbreviation. |
| `note` | Any additional information. |
| `number` | Number of journal or magazine. |
| `organization` | Organization that sponsors a conference. |
| `pages` | Page range (2,6,9--12). | 
| `publisher` | Publisher's name. |
| `school` | Name of school (for thesis). |
| `series` | Name of series of books. |
| `title` | Title of work. |
| `type` | Type of tech. report, ex. \\Research Note". |
| `volume` | Volume of a journal or book. | 
| `year` | Year of publication. |

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
