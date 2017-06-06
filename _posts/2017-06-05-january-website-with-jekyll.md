---
layout: post-doc
title:  "January Website with Jekyll"
date:   2017-06-05 11:15:03 +0100
categories: docs
img:    "uploads/basic.jpg"
---

In this post, we will explain how to maintain the January website.

## Requirements

* Install Jekyll (find how to install **[here](https://jekyllrb.com/docs/installation/)**).

* Knowing how to code in HTML.

* Knowing how to write a markown file.

* Know basics of programation (control structure)

* Knowing Liquid language help

----

## Folders

Here you have all folders:

![main folder](https://raw.githubusercontent.com/Jdarroy/Internship/master/blogpost/arborescance.PNG)

I will not explain what's in css, fonts, img and js ; it's normal folders. There is not any specialities.

----

## Includes

In this folder you have 2 differents types.

footer.html, head.html, header.html contain code that will be written in all HTML files after the Jekyll's generation. They are called by layouts files.

categories.html and category.html are used to class posts but we will explain them later.

----

## Layouts

Files in layouts folder define the structure of the final page.

![layouts folder](https://raw.githubusercontent.com/Jdarroy/Internship/master/blogpost/layouts.png)

#### default.html && docs.html

defaults.html and docs.html define the main structure of the generated files. They include the head, header, content of the file who call it and the footer. There is just one difference between defaults.html and docs.html, just after the include of head.html  and before the body balise, they have a different link to css.

So when Jekyll do the generation he put each file with this structure.

layouts/docs.html :
{% raw %}
```
<!DOCTYPE html>
<html>

  {% include head.html %}
  <link rel="stylesheet" href="{{ "/css/app1.css" | prepend: site.baseurl }}">

    <body>

    {% include header.html %}

    {{ content }}

    {% include footer.html %}

    </body>
</html>
```
Link to the [file](https://github.com/Jdarroy/Jdarroy.github.io/blob/master/_layouts/docs.html)

Note:


The line "{{ content }}" means the all file which is called.

{% endraw %}

For example, the file news.html call default as layout, so the content will be what's written in news.html.

----

#### post-doc.html && post.html

post.html has no loop, it print only the content and the title of the page which call it. It's use only by about.md

post-doc.html has two loop with a condition. This file define which file you want to read.
The two loops write links to posts.

{% raw %}
```
<div class="posts">
  <div class="title">
    ______________________
    <br>
    <b>Getting Started</b>
  </div>
  {% for post in site.posts %}
  {% if post.categories contains 'getting-started' %}
  <div class="post">
    <div class="post-content">
      <h2 class="post-title"><a href="{{ post.url }}"><b>- </b>{{ post.title }}</a></h2>
    </div>
  </div>
  {% endif %}
  {% endfor %}

  <div class="title">
    ______________________
    <br>
    <b>News</b>
  </div>
  {% for post in site.posts limit:5 %}
  {% if post.categories contains 'docs' %}
  <div class="post">
    <div class="post-content">
      <h2 class="post-title"><a href="{{ post.url }}"><b>- </b>{{ post.title }}</a></h2>
    </div>
  </div>
  {% endif %}
  {% endfor %}
  <h2 class="post-title"><a href="{{site.url}}/docs/news/">See more ...</a></h2>
</div>

```
Link to the [file](https://github.com/Jdarroy/Jdarroy.github.io/blob/master/_layouts/post-doc.html)

For the first loop we got two instruction in liquid.
The instruction "{% for post in site.posts %}" process all posts, then the instruction
"{% if post.categories contains 'getting-started' %}" filter them by categories.

What's inside theese two instruction print the result.

For the second loop it's the same but we add a limit to show only the last 5 posts.

Here is the result:

![result](https://raw.githubusercontent.com/Jdarroy/Internship/master/blogpost/showPostDoc1.png)

----

## Categories

In this folder you have to create a new file each time you want to create a new category. Then you give a category to your posts and you can filter them.

You just have to give him the same name and title, for docs.html for example you have that:
```
---
layout: default
title: docs
---

{% include category.html %}

----
```
## Posts

Here you store all your posts as markdown files. It's normal mardown files, you just have to write some information before.

For this post for example it's wrote that:

```
---
layout: post-doc
title:  "January Website with Jekyll"
date:   2017-06-05 11:15:03 +0100
categories: docs
img:    "uploads/basic.jpg"
---
```

{% endraw %}

The Layout is really important because it will descibe how your post will be print.

Give it the title, this is what user will see as a link.

The date is important too because posts are order by date, so if you want to order them you have to give to your posts the real date.

The img is used by the the "news" page, if you don't want to put an img just put "uploads/basic.jpg"

!!! Don't forgot to put the three dash the line before and the line after theese informations !!!
