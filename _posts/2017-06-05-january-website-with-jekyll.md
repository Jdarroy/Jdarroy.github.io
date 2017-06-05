---
layout: post-doc
title:  "January Website with Jekyll"
date:   2017-06-05 11:15:03 +0100
categories: docs
img:    "uploads/basic.jpg"
---

In this post, we will explain how to maintain the January website.

## Requirements

* Install Jekyll (find how to install [here](https://jekyllrb.com/docs/installation/)).

* Knowing how to code in HTML.

* Knowing how to write a markown file.

## Folders

Here you have all folders:

![main folder](https://raw.githubusercontent.com/Jdarroy/Internship/master/blogpost/arborescance.PNG)

I will not explain what's in css, fonts, img and js ; it's normal folders. There is not any specialities.

## includes

In this folder you have 2 differents types.

footer.html, head.html, header.html contain code that will be written in all HTML files after the Jekyll's generation. They are called by layouts files.

categories.html and category.html are used to class posts but we will explain them later.

## layouts

Files in layouts folder define the structure of the final page.

![layouts folder](https://raw.githubusercontent.com/Jdarroy/Internship/master/blogpost/layouts.png)

### default.html && docs.html

defaults.html and docs.html define the main structure of the generated files. They got html balise, they include the head, header, content of the file who call it and the footer. There is just one difference between defaults.html and docs.html, just after the include of head.html  and before the body balise, they have a different link to css.

So when Jekyll do the generation he put each file with this structure.
