# Markdown Cheatsheet

## General Font Formatting

In order to have

paragraph tags

you need a full line between

each line of text.

```
So like this

lalalalalala
```

```
but not like this
lalalalalala
```

Bold and italics can be done 2 ways. A single set of `*` or `_` on each side of text will show italics, while a double set on each side of the text will show bold:

```
**This is bold** becomes:
```

**This is bold**

```
and _This is italic_ becomes:
```

_This is italic_

```
A strikethrough can be done like this: ~~strikethrough~~
```

~~strikethrough~~

## Headings

Headings are made by using 1 to 6 "#" in front of the text. So for example an H1 can be made by typing:

```
# This is a Heading
```

which outputs as:

# This is a Heading

H1 to H6 appears as

# H1

## H2

### H3

#### H4

##### H5

###### H6

Or you can make an H1 or H2 by using equals signs or dashes under text:

```
Heading 1
========= (at least 3)
Heading 2
--------- (at least 3)
```

# Heading 1

## Heading 2

## Links

```
If you start a link with "http://", <http://link.com> will give you:
```

<http://link.com>

Or you can surround text with square brackets followed by the url in curvy brackets (no space between square and curvy brackets):

```
[Link Name](http://danbuda.com/) becomes:
```

[Link Name](http://danbuda.com/)

And you can also add a hover title by including quotes around text after the url:

```
[Link Number Two](http://danbudahomes.com/ "Dan's Real Estate Website")
```

[Link Number Two](http://danbudahomes.com/ "Dan's Real Estate Website")

Another option is to create a reference to a link instead of plopping the url right next to the link text:

```
[Link Three][1]

And then at the bottom of the file:
[1]: https://github.com/DanBuda11
```

[Link Three][1]

[This also goes to the same link][1]

[1]: https://github.com/DanBuda11

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
1. second
1. third
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

Create a horizontal line by using at least 3 "=" or "-" and remember to lease space between them and above text to avoid them being conveted into H1 or H2 tags:

```
Words and stuff

---

===
```

will appear as:

Words and stuff

===

---

---
