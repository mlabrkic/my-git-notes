
## HACKS

[(Markdown Guide hacks)](https://www.markdownguide.org/hacks/)<br>
If your Markdown processor supports HTML ...

### Table of Contents:
<!-- vim-markdown-toc GFM -->

  * [Underline](#underline)
  * [Indent (Tab)](#indent-tab)
  * [Line breaks](#line-breaks)
  * [Center](#center)
  * [Color](#color)
  * [Comments](#comments)
  * [Admonitions](#admonitions)
  * [Symbols](#symbols)
  * [GitHub Emoji](#github-emoji)
* [RESOURCES](#resources)
    * [Markdown Cheatsheets / Quick References](#markdown-cheatsheets--quick-references)
    * [Markdown Getting Started Guides / Tutorials](#markdown-getting-started-guides--tutorials)

<!-- vim-markdown-toc -->


### Underline

HTML tag:  `<ins>`
``` html
Some of these words <ins>will be underlined</ins>.
```
The rendered output looks like this: <br>
Some of these words <ins>will be underlined</ins>.


### Indent (Tab)

HTML tag (for non-breaking space):  `&nbsp;`

``` html
&nbsp;&nbsp;&nbsp;&nbsp;This is the first sentence of my indented paragraph.
```
The rendered output looks like this: <br>
&nbsp;&nbsp;&nbsp;&nbsp;This is the first sentence of my indented paragraph.


### Line breaks

[(Markdownguide line breaks)](https://www.markdownguide.org/basic-syntax/#line-breaks)

To create a line break or new line (`<br>`), end a line with "two or more spaces", and then type return.

HTML tag:  `<br>`

``` html
<p>This is the first line.<br>
And this is the second line.</p>
<p>This is the first line.<br>
And this is the second line.</p>
```
The rendered output looks like this: <br>
<p>This is the first line.<br>
And this is the second line.</p>
<p>This is the first line.<br>
And this is the second line.</p>


### Center

HTML tag: `<center>`.

``` html
<center>This text is centered.</center>
```
The rendered output looks like this: <br>
<center>This text is centered.</center>


### Color

HTML tag: `<font>`.<br>
The color attribute allows you to specify the font color using a color’s name or the hexadecimal #RRGGBB code.

``` html
<font color="red">This text is red!</font>
```
The rendered output looks like this:<br>
<font color="red">This text is red!</font>

The `<font>` HTML tag is technically supported but officially deprecated, which means it works for now but you’re not supposed to be using it. Unfortunately, there’s not another pure HTML alternative. You could try using one of the CSS alternatives.<br>
Not all Markdown applications provide CSS support, but if the one you’re using does, here’s an alternative to the `<font>` tag:
``` html
<p style="color:blue">Make this text blue.</p>
```
If this is supported by your Markdown application, the output looks like this:<br>
<p style="color:blue">Make this text blue.</p>


### Comments

Some people need the ability to write sentences in their Markdown files that will not appear in the rendered output. These comments are essentially hidden text. The text is viewable by the author of the document, but it’s not printed on the webpage or PDF. Markdown doesn’t natively support comments, but several enterprising individuals have devised a solution.<br>
To add a comment, place text inside brackets followed by a colon, a space, and a pound sign<br>
(e.g., `[comment]: #`). You should put blank lines before and after a comment.

``` html
Here's a paragraph that will be visible.

[This is a comment that will be hidden.]: #

And here's another paragraph that's visible.
```
The rendered output looks like this:<br>
Here's a paragraph that will be visible.

[This is a comment that will be hidden.]: #

And here's another paragraph that's visible.

This tip comes from [Stack Overflow](https://stackoverflow.com/questions/4823468/comments-in-markdown).


### Admonitions

Admonitions are frequently used in documentation to call attention to warnings, notes, and tips. Markdown doesn’t provide special syntax for admonitions, and most Markdown applications don’t provide support for admonitions (one exception is [MkDocs](https://www.markdownguide.org/tools/mkdocs/)).

However, if you need to add admonitions, you might be able to use [blockquotes](https://www.markdownguide.org/basic-syntax/#blockquotes-1) with [emoji](https://www.markdownguide.org/extended-syntax/#emoji) and [emphasis](https://www.markdownguide.org/basic-syntax/#emphasis) to create something that looks similar to the admonitions you see on other websites.

``` html
> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.
```
The rendered output looks like this:<br>
> :warning: **Warning:** Do not push the big red button.

> :memo: **Note:** Sunrises are beautiful.

> :bulb: **Tip:** Remember to appreciate the little things in life.


### Symbols

Markdown doesn’t provide special syntax for symbols. However, in most cases, you can copy and paste whatever symbol you want to use into your Markdown document. For example, if you need to display Pi (π), just find the symbol on a webpage and copy and paste it into your document. The symbol should appear as expected in the rendered output.

Alternatively, if your Markdown application supports [HTML](https://www.markdownguide.org/basic-syntax/#html), you can use the HTML entity for whatever symbol you want to use. For example, if you want to display the copyright sign (©), you can copy and paste the HTML entity for copyright (&copy;) into your Markdown document.

Here’s a partial list of HTML entities for symbols:
``` html
* Copyright (©) — &copy;
* Registered trademark (®) — &reg;
* Trademark (™) — &trade;
* Euro (€) — &euro;
* Left arrow (←) — &larr;
* Up arrow (↑) — &uarr;
* Right arrow (→) — &rarr;
* Down arrow (↓) — &darr;
* Degree (°) — &#176;
* Pi (π) — &#960;
```
For a complete list of available HTML entities, refer to Wikipedia’s page on [HTML entities](https://en.wikipedia.org/wiki/List_of_XML_and_HTML_character_entity_references).




---

### GitHub Emoji

[Using](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#using-emoji) Emoji <br>
Emoji [cheat sheet](https://github.com/ikatyang/emoji-cheat-sheet)


<br>
<br>

## RESOURCES

[Awesome Markdown.](https://github.com/mundimark/awesome-markdown) A list of Markdown tools and learning resources. <br>


#### Markdown Cheatsheets / Quick References

* [Markdown Cheatsheet :octocat:](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

#### Markdown Getting Started Guides / Tutorials

* [Markdown Tutorial](http://markdowntutorial.com) - [:octocat:](https://github.com/gjtorikian/markdowntutorial.com) An open source website that allows you **to try Markdown** in your web browser.
* [Markdown Guide cheat-sheet](https://www.markdownguide.org/cheat-sheet/) &nbsp; [(and hacks)](https://www.markdownguide.org/hacks/)
* [Writing on Github](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github)







