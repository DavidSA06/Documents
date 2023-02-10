# Markdown Cheatsheet

## Basic Syntax

### Headings

```
# H1
## H2
### H3
#### H4
##### H5
###### H6
```

#### Alternate Syntax

```
Heading level 1 <h1>Heading level 1</h1>
===============
Heading level 2 <h2>Heading level 2</h2>
---------------
```

***

### Emphasis

#### Bold

`**bold text**` **bold text**

`__bold text__` __bold text__

#### Italic

`*italicized text*` *italicized text*

`_italicized text_` _italicized text_

#### Bold and Italic

`***Important*** text.` ***Important*** text.

`___Important___ text.` ___Important___ text.

`__*Important*__ text.` __*Important*__ text.

`__*Important*__ text.` __*Important*__ text.

***

### Blockquotes

`> blockquote`

> blockquote

#### Blockquotes with Multiple Paragraphs

```
> This the first paragraph.
>
> And this is the second paragraph.
```

> This the first paragraph.
>
> And this is the second paragraph.

#### Nested Blockquotes

```
> This the first paragraph.
>
>> And this is the nested paragraph.
```

> This the first paragraph.
>
>> And this is the nested paragraph

#### Blockquotes with Other Elements

```
##### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
> *Everything* is going **well**.
```

##### The quarterly results look great!
>
> - Revenue was off the chart.
> - Profits were higher than ever.
>
> *Everything* is going **well**.
> 
***

### Lists

#### Ordered Lists

```
1. First item
2. Second item
3. Third item
4. Fourth item

1. First item
1. Second item
1. Third item
1. Fourth item

1. First item
8. Second item
3. Third item
5. Fourth item
```

1. First item
2. Second item
3. Third item
4. Fourth item
<br>

1. First item
1. Second item
1. Third item
1. Fourth item
<br>

1. First item
8. Second item
3. Third item
5. Fourth item

##### Nesting List Items (4 spaces, 1 tab)

```
1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item
```

1. First item
2. Second item
3. Third item
    1. Indented item
    2. Indented item
4. Fourth item

#### Unordered List

```
- First item
- Second item
- Third item
- Fourth item

* First item
* Second item
* Third item
* Fourth item

+ First item
* Second item
- Third item
+ Fourth item
```

- First item
- Second item
- Third item
- Fourth item

* First item
* Second item
* Third item
* Fourth item

+ First item
* Second item
- Third item
+ Fourth item

##### Nesting List Items (4 spaces, 1 tab)

```
- First item
- Second item
- Third item
    - Indented item
    - Indented item
- Fourth item
```

- First item
- Second item
- Third item
    - Indented item
    - Indented item
- Fourth item

#### Adding Elements in Lists

##### Paragraphs

```

* This is the first list item.
* Here's the second list item.

I need to add another paragraph below the second list item.

* And here's the third list item.
```

* This is the first list item.
* Here's the second list item.

I need to add another paragraph below the second list item.

* And here's the third list item.

##### Blockquotes

```
* This is the first list item.
* Here's the second list item.

> A blockquote would look great here.

* And here's the third list item.
```

* This is the first list item.
* Here's the second list item.

> A blockquote would look great here.

* And here's the third list item.

##### Code Blocks (4 spaces, 1 tab), List (8 spaces, 2 tabs)

```
1. Open the file.
2. Find the following code block on line 21:

        <html>
            <head>
                <title>Test</title>
        </head>

3. Update the title to match the name of your website.
```

1. Open the file.
2. Find the following code block on line 21:

        <html>
            <head>
                <title>Test</title>
        </head>

3. Update the title to match the name of your website.

##### Images

```
1. Open the file containing Tux, the Linux mascot.
2. Marvel at its beauty.

![Tux](images/tux.png)

3. Close the file.
```

1. Open the file containing Tux, the Linux mascot.
2. Marvel at its beauty.

![Tux](images/tux.png)

3. Close the file.

***

### Code


``At the command prompt, type `nano`.``


At the command prompt, type `nano`.

#### Escaping Tick Marks

```
``Use `code` in your Markdown file.``
```

``Use `code` in your Markdown file.``

#### Code Blocks (4 spaces, 1 tab)

```
    <html>
        <head>
        </head>
    </html>
```

    <html>
        <head>
        </head>
    </html>

***

### Horizontal Rules

```
***

---

_________________
```

***

---

_________________

<br>

***

### Links

`Use [Duck Duck Go](https://duckduckgo.com).`

Use [Duck Duck Go](https://duckduckgo.com).

#### Adding Titles

`Use [Duck Duck Go](https://duckduckgo.com "My search engine!").`

Use [Duck Duck Go](https://duckduckgo.com "My search engine!").


#### URLs and Email Addresses

`<https://eff.org> <fake@example.com>`

<https://eff.org> <fake@example.com>

#### Formatting Links

`I love supporting **[EFF](https://eff.org)**. This is the *[EFF](https://eff.org)*.`

I love supporting **[EFF](https://eff.org)**. This is the *[EFF](https://eff.org)*.

#### Reference-style Links

##### Formatting the First Part of the Link

```
[hobbit-hole][1]
[hobbit-hole] [1]
[hobbit-hole][a]
[hobbit-hole][A]
```
[hobbit-hole][1]

[hobbit-hole] [1]

[hobbit-hole][a]

[hobbit-hole][A]

##### Formatting the Second Part of the Link

```
[hobbit-hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle
[hobbit-hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit
lifestyles"
[hobbit-hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit
lifestyles'
[hobbit-hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit
lifestyles)
[hobbit-hole]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit
lifestyles"
[hobbit-hole]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit
lifestyles'
[hobbit-hole]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit
lifestyles)
```

[hobbit-hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle

[hobbit-hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle "Hobbit
lifestyles"

[hobbit-hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle 'Hobbit
lifestyles'

[hobbit-hole]: https://en.wikipedia.org/wiki/Hobbit#Lifestyle (Hobbit
lifestyles)

[hobbit-hole]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> "Hobbit
lifestyles"

[hobbit-hole]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> 'Hobbit
lifestyles'

[hobbit-hole]: <https://en.wikipedia.org/wiki/Hobbit#Lifestyle> (Hobbit
lifestyles)

***

### Images

`![Philadelphia's Magic Gardens. This place was so cool!](images/philly-\
2 magic-garden.png "Philadelphia's Magic Gardens")`

![Philadelphia's Magic Gardens. This place was so cool!](images/philly-\
2 magic-garden.png "Philadelphia's Magic Gardens")

***

### Escaping Characters

`\* Without the backslash, this would be a bullet in an unordered list.`

\* Without the backslash, this would be a bullet in an unordered list.

#### Characters You Can Escape

| Character| Name |
| --- | --- |
| \\ | backslash |
| \` | tickmark |
| \* | asterisk |
| \_ | underscore |
| \{\} | curly braces |
| \[\] | brackets |
| \(\) | parentheses |
| \# | pound sign |
| \+ | plus sign |
| \- | minus sign (hyphen) |
| \. | dot |
| \! | exclamation mark |


## Extended Syntax



| MathJax \|\| Image : |||
| :--- | :--- | :--- |
| A | : A : | A \
| B | B | B \
| O | O | O |
| : Rowspan is 4 : || : How's it? : |
| ^^ A. Peach || 1. ![example][cell-image] |
| ^^ B. Orange || 2. $I=\int \rho R^{2} dV$  |
| ^^ C. Banana || **3. It's OK!** |

[cell-image]: https://jekyllrb.com/img/octojekyll.png "An exemplary image"
