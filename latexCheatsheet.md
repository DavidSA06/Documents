# $\LaTeX{}$ Cheatsheet

## Contents

| [Document classes](#document-classes) | [Document Structure](#document-structure) | [Text properties](#text-properties) | [Text-mode symbols](#text-mode-symbols)| [Tabular environments](#tabular-environments) | [Math mode](#math-mode) | [Bibliography and citations](#bibliography-and-citations) |
| --- | --- | --- | --- | --- | --- | --- |
|  |  |  | [Symbols](#symbols) |  | [Sensible size examples](#sensible-size-examples) |  |
|  |  |  | [Accents](#accents) |  | [Greek alphabet](#greek-alphabet)  |  |
|  |  |  | |  | [Symbols of Type Ord](#symbols-of-type-ord) |  |
|  |  |  |  |  | [Large Operators](#large-operators) |  |
|  |  |  |  |  | [Binary Operations](#binary-operations) |  |
|  |  |  |  |  | [Relations](#relations) |  |
|  |  |  |  |  | [Arrows](#arrows) |  |
|  |  |  |  |  | [Delimiters](#delimiters) |  |
|  |  |  |  |  | [Accents](#accents) |  |
|  |  |  |  |  | [Elementary Math Control Sequences](#elementary-math-control-sequences) |  |
|  |  |  |  |  | [Non-Italic Function Names](#non-italic-function-names) |  |


### Document classes

***

### Document Structure

***

### Text properties

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

#### Large Operators

| Name | Code | Symbol | Name | Code | Symbol | Name | Code | Symbol |
| --- | --- | :---: | --- | --- | :---: | --- | --- | :---: |
| summation | `\sum`| $$\sum$$ |  | `\bigcap`| $$\bigcap$$ |  | `\bigodot`| $$\bigodot$$ |
| product | `\prod`| $$\prod$$ |  | `\bigcup`| $$\bigcup$$ |  | `\bigotimes`| $$\bigotimes$$ |
| coproduct | `\prod`| $$\prod$$ |  | `\bigsqcup`| $$\bigsqcup$$ |  | `\bigoplus`| $$\bigoplus$$ |
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



***

### Bibliography and citations
