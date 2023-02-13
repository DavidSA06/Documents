# Markdown Cheatsheet

## Contents

| Basic Syntax | Extended Syntax |
| --- | --- |
| [Headings](#headings) | [Tables](#tables) |
| [Emphasis](#emphasis) | [Fenced Code Blocks](#fenced-code-blocks) |
| [Blockquotes](#blockquotes) | [Footnotes](#footnotes) |
| [Lists](#lists) | [Heading IDs](#heading-ids) |
| [Code](#code) | [Definition Lists](#definition-lists) |
| [Horizontal Rules](#horizontal-rules) | [Strikethrough](#strikethrough) |
| [Links](#links) | [Task Lists](#task-lists) |
| [Images](#images) | [Automatic URL Linking](#automatic-url-linking) |
| [Links](#links) |  |
| [Escaping Characters](#escaping-characters) |  |

## Basic Syntax 
### Headings 
[🔝](#markdown-cheatsheet)
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

***

## Extended Syntax

### Tables

Go to [Markdown Tables Generator](https://www.tablesgenerator.com/markdown_tables)

```
| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |
```

| Syntax | Description |
| ----------- | ----------- |
| Header | Title |
| Paragraph | Text |

#### Alignment

```
| Syntax | Description | Test Text |
| :--- | :----: | ---: |
| Header | Title | Here's this |
| Paragraph | Text | And more |
```

| Syntax | Description | Test Text |
| :--- | :----: | ---: |
| Header | Title | Here's this |
| Paragraph | Text | And more |

#### Formatting Text in Tables

You can format the text within tables. For example, you can add links, code (words
or phrases in tick marks (\`) only, not code blocks), and emphasis.

You can’t add headings, blockquotes, lists, horizontal rules, images, or HTML tags.

#### Colspan and Rowspan (doesn't work in GitHub)

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

***

### Fenced Code Blocks

\`\`\`
<br>
{
<br>
"firstName": "John",
<br>
"lastName": "Smith",
<br>
"age": 25
<br>
}
<br>
\`\`\`

```
{
"firstName": "John",
"lastName": "Smith",
"age": 25
}
```

#### Syntax Highlighting

\`\`\`json
<br>
{
<br>
"firstName": "John",
<br>
"lastName": "Smith",
<br>
"age": 25
<br>
}
<br>
\`\`\`

```json
{
"firstName": "John",
"lastName": "Smith",
"age": 25
}
```

***

### Footnotes

```
Here's a simple footnote,[^1] and here's a longer one.[^bignote] 

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

```


Here's a simple footnote,[^1] and here's a longer one.[^bignote]

[^1]: This is the first footnote.

[^bignote]: Here's one with multiple paragraphs and code.

(Look the bottom).

***

### Heading IDs

```
### My Great Heading {#custom-id}
```

### My Great Heading {#custom-id}

#### Linking to Heading IDs

[Heading IDs](#custom-id)

You can use `[Heading IDs](https:/www.eff.org/page#heading-ids)`

***

### Definition Lists

```
First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.
```

First Term
: This is the definition of the first term.

Second Term
: This is one definition of the second term.
: This is another definition of the second term.

***

### Strikethrough

`The world is ~~flat~~ round.`

The world is ~~flat~~ round.

***

### Task Lists

```
- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media
```

- [x] Write the press release
- [ ] Update the website
- [ ] Contact the media

***

### Automatic URL Linking

http://example.com

#### Disabling Automatic URL Linking

\`http://www.example.com \`

`http://www.example.com`
