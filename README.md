# Markdown Guide

I created this to give myself a refresher on markdown as well as put together a resource for me (or others) to use.

## Table of Contents

* [General Font Formatting](#general-font-formatting)
* [Headings](#headings)
* [Links](#links)
* [Images](#images)
* [Lists](#lists)
* [Line Breaks](#line-breaks)
* [Horizontal Rules](#horizontal-rules)
* [Block Quotes](#block-quotes)
* [Code Blocks](#code-blocks)
* [Tables](#tables)
* [Checkboxes](#checkboxes)

## General Font Formatting

In order to create paragraphs, a full line is needed between lines of text.

        So this sentence will be its own paragraph.

        And this sentence will be its own paragraph.

        But if you try to write this sentence.
        And then put this sentence directly below, it will look like this:

But if you try to write this sentence.
And then put this sentence directly below, it will look like this:

---

Bold and italicized font can be done a few different ways. A single set of `*` or `_` on each side of text will show italics, while a double set on each side will show bold:

        _This is italic_ OR *This is italic* becomes:

_This is italic_ OR *This is italic*

        And similarly, __This is bold__ OR **This is bold** becomes:

And similarly, __This is bold__ OR **This is bold** becomes:

---

A ~~strikethrough~~ can be made like this:

        ~~strikethrough~~

## Headings

Headings are made by placing `#` in front of text. The number of `#` used determines which heading (1-6) appears.

        #### This is an H4

outputs as:

#### This is an H4

Headings appear as:

# This is an H1
## This is an H2
### This is an H3
#### This is an H4
##### This is an H5
###### This is an H6

Alternately, an H1 or H2 can be created by placing at least 3 `-` or `=` under text, and leaving a line empty underneath:

        This is an H1
        ===

        This is an H2
        ---

## Links

If you start a link with `http://`, you can type `<http://danbuda.com>` and get:

<http://danbuda.com>

If you want to show a link name, and not the url, use the syntax `[link name](url)`. So for example, `[Dan's Portfolio](http://danbuda.com)` gives you:

[Dan's Portfolio](http://danbuda.com)

And you can also add a hover title by including quotes around text after the url:

        [Dan's Real Estate Site](http://danbudahomes.com "Dan's Real Estate Site")

[Dan's Real Estate Site](http://danbudahomes.com/ "Dan's Real Estate Website") (<-- try hovering)

Another option is to create a reference to a link instead of plopping the url right next to the link text:

        [Dan's GitHub][1]

        [Also Dan's Github][1]

        And then at the bottom of the file:
        [1]: https://github.com/DanBuda11


[Dan's GitHub][1]

[Also Dan's GitHub][1]

This makes it easy to add links when you have multiple places in your document that need to link to the same place. Common practice is to put all the link references at the bottom of the document. You can see them by clicking [here](#bottom-links)

Finally, you can create intra-document links by taking the name of a heading in a markdown document, placing `-` between words, and putting a `#` in front of the heading name:

        [Link Name](#-heading-name)

Try it here: [Back to Top](#markdown-guide)

## Images

The basic format is: `![]()` where the [] include the alt text (optional) and the () includes the image link. Additionally, you can put hover text inside the () after the image link wrapped in quotes:

```
![Random Unsplash picture](https://source.unsplash.com/random "Random image)
```

![Random picture](https://picsum.photos/200 'Random image')

You can also make references to the image link in the same way you do with a url link:

```
[Cute pup!][pup]
```

And then place the actual link anywhere in the document:

```
[pup]: https://picsum.photos/200
```

You can also use an image as the link itself:

```
[![](https://picsum.photos/200
)](https://picsum.photos/200
)

or

[<img src="https://picsum.photos/200
">](https://picsum.photos/200
)
```

[![](https://picsum.photos/200)](https://picsum.photos/200)

## Lists

Bulleted text can be created by using either a \*, - or + with a space in front of the text:

```
* 1
* 2
* 3
```

outputs as:

- 1
- 2
- 3

An ordered list can be created this way:

```
1. first
2. second
3. third
```

1.  first
1.  second
1.  third

The specific number you use makes no difference. You could use all 1s, go 1-2-3-etc, or 1-6-3-7-5.

You can also create intented lists by tabbing in or using 2+ spaces:

```
* one
  * two
    * three
```

shows up as:

- one
  - two
    - three

And can also create paragraph tags within a list item, and even use images, code blocks, etc. as list items:

````
* one
  * two

  second two

  ![](https://picsum.photos/200)

  ```js
  var x = 100;
````

- one

  - two

    second two

    ![](https://picsum.photos/200)

    ```js
    var x = 100;
    ```

## Line Breaks

```
Sentence one.
Sentence two.

Sentence three.
```

will show up as:

Sentence one.
Sentence two.

Sentence three.

In order to create a line break, simply add a `<br>` after a line:

```
Sentence one.<br>
Sentence two.
```

Sentence one.<br>
Sentence two.

## Horizontal Rules

Create a horizontal line by using at least 3 "-", and remember to leave space between the "-" and above text to avoid them being conveted into H1 tags:

```
Words and stuff

---
Words below
```

will appear as:

Words and stuff

---

Words below

## Block Quotes

```
> Hello this is a quote
```

ends up looking like this:

> Hello this is a quote

## Code Blocks

Create a code block by tabbing in twice to get this:

    var x = 100;
    const dog = 'snickers';

Or use "```" above and below the text to do the same thing. You can also add the name of the language the text is in to make it format even more:

    ```js
    var x = 100;
    const dog = 'snickers';
    ```

will end up looking like:

```js
var x = 100;
const dog = 'snickers';
```

And inline code tags can be done with backticks:

```
Did you try `var x = 100;`?
```

shows up as:

Did you try `var x = 100;`?

`diff` can also be used in place of a language name:

    ```diff
    var x = 100;
    - var y = 200;
    + var y = 300;
    ```

outputs as:

```diff
var x = 100;
- var y = 200;
+ var y = 300;
```

## Tables

Placing vertical lines on both side of content, as well as creating a second line with ":" and dashes, will create a table. Note that the placement of colons determines whether the content is left, right, or center aligned:

    | Dog's Name | Dog's Age | Dog's Color |
    | :--------- | --------: | :---------: |
    | Spot       | 2         | Black       |
    | Rover      | 4         | Brown       |



| Dog's Name | Dog's Age | Dog's Color |
| :--------- | --------: | :---------: |
| Spot       | 2         | Black       |
| Rover      | 4         | Brown       |


## Checkboxes

Create checkboxes by making a list and adding square brackets with a space. Placing an "X" inside the brackets will add the check:

    * [ ] Wake up
    * [X] Brush teeth
    * [ ] Go to work

* [ ] Wake up
* [X] Brush teeth
* [ ] Go to work

# Bottom Links

Where did they go?! They don't show up in the actual document! Ok, head back to the [Links](#links) section.

[1]: https://github.com/DanBuda11