# Typst cheatsheet

## Syntax

### Markup

| Name | Code |
| --- | --- |
| Paragrahph break | Blank line |
| Strong emphasis | `*strong*` |
| Emphasis | `_emphasis_` |
| Raw text | `` `print(1)` `` |
| Link | `https://johzu.com/` |
| Label | `<intro>` |
| Reference | `@intro` |
| Heading | `= Heading` |
| Bullet list | `- item` |
| Numbered list | `+ item` |
| Term list | `/Term: description` |
| Math | `$x^2$` |
| Line break | `\` |
| Smart quote | `'single'` or `'double'` |
| Symbol shorthand | `~`,  `---` |
| Code expression | `#rect(width: 1cm)` |
| Character escape | `Tweet at us \#ad`  |
| Comment | `/* block */`, `//line` |

### Math mode

| Name | Code |
| --- | --- |
| Inline math | `$x^2$` |
| Block-level math | `$ x^2 $` |
| Bottom attachment | `$x_(1)$` |
| Top attachment | `$x^(2)$` |
| Fraction | `$1 + (a+b)/5$` |
| Line break | `$x \ y$` |
| Alignment point | `$x &= 2 \ &= 3$` |
| Variable access | `$pi$` |
| Field access | `$arrow.r.long$` |
| Implied multiplication | `$x y$` |
| Symbol shorthand | `$->, !=$` |
| Text/string in math | `$a "is natural"$` |
| Math function call | `$floor(x)$` |
| Code expression | `$#rect(width: 1cm)$` |
| Character escape | `x\^2` |
| Comment | `$/* comment */$` |

### Code mode

| Name | Code |
| --- | --- |
| Variable access | `x` |
| Any literal | `1pt`, `"hey"` |
| Code block | `{ let x = 1; x + 2 }` |
| Content block | `[*Hello*]` |
| Parenthesized expression | `(1 + 2)` |
| Array | `(1, 2, 3)` |
| Dictionary | `(a: "hi", b: 2)` |
| Unary operator | `-x` |
| Binary operator | `x + y` |
| Assignment | `x = 1` |
| Field access | `x.y` |
| Method call | `x.flatten()` |
| Function call | `min(x, y)` |
| Unnamed function | `(x, y) => x + y` |
| Let binding | `let x = 1` |
| Named function | `let f(x) = 2 * x` |
| Set rule | `set text(14pt)` |
| Set-if rule | `set text(..) if ..` |
| Show-set rule | `show par: set block(..)` |
| Show rule with function | `show raw: it => {..}` |
| Show-everything rule | `show: columns.with(2)` |
| Conditional | `if x == 1 {..} else {..}` |
| For loop | `for x in (1, 2, 3) {..}` |
| While loop | `while x < 10 {..}` |
| Loop control flow | `break`, `continue` |
| Return from function | `return x` |
| Include module | `include "bar.typ"` |
| Import module | `import "bar.typ"` |
| Import items from module | `import "bar.typ": a, b, c` |
| Comment | `/* block */`, `// line` |

## Styling

### Set rules

| Name | Code |
| --- | --- |
|  |  |
