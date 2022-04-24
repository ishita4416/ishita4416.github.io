---
layout: post
title: Learning Markdown 
---

Esentially, I wanted to use this blog to just be able to keep track of my progress while I am studying for Cybersec, or anything for that matter, but since it has been a rather long time since I did something even slightly Webdev centric, I thought it would be nice to start using this initially for learning how to use it itself.

## Headers

# H1
## H2
### H3
#### H4
##### H5
###### H6

Underlined style Alt-H1
=======

Underlined style Alt-H2
------

## Emphasis

Italics with * single asterisk* or _single underscore_

Bold with **double asterisk** or __double underscore__

Combined emphasis with **asterisk at beginning and _underscore at beginning and astersik at end_**

Strikethrough using tilde ~~two tildes~~


## Lists

1. Just number and list item
2. another item etc
..* Unordered sub-list
..1. Ordered sub-list
4. and different numbers will still give the reqd list

   Properly indented paragraphs within list items using a blank line and leading spaces to align the raw markdown

   to break a line without using the paragraph, two trailing spaces need to be used  
   this next line would be in the next line, but also in the same paragraph

* unordered lists can use asterisks
+ as well as pluses
- and minuses

## Links

[inline-style link](https://www.google.com)
[inline-style link with title](https://www.google.com "Google's Homepage")

## Images

Hover to see the title text

Inline-style:
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style:

![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"


## Code and Syntax Highlighting

Inline `code` has `back-ticks` around it

Block code has 3 back-ticks around it

```python
s = "Python Syntax Highlighting"
print s
```
## Footnotes

A simple footnote[^1]
A footnote can also have multiple lines[^2]
words can also be used instead of numbers[^note]

[^1]: Reference used  
[^2]: Every new line should be prefixed with 2 spaces  
  this allows for a footnote to have multiple lines  
[^note]: Named footnotes begin with numbers too instead of text but allow easier identification and linking

## Tables

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 | 

Markdown | Less | Pretty  
--- | --- | ---  
*Still* | `renders` | **nicely**
1 | 2 | 3

## Blockquotes

> Blockquotes are very handy in email to emulate reply text.
> This line is a part of the same quote

Quote Break

> This is a very long like that will still be quoted properly when it wraps. And also **Markdown** can be put into _blockquote_ as well. This is very nice to highlight text within text too

## Inline HTML

<dl>
   <dt> Heading sort </dt>
   <dd> raw HTML can be made in your Markdown, and it usually works really well </dd>
   
   <dt> Markdown in HTML </dt>
   <dd> Does *not* work **very** well. Use HTML <em>tags</em></dd>
</dl>
   
## Horizontal Rule

3 or more...
---
Hyphens
***
Asterisk
___
underscores
