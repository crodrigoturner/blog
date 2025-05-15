---
title: Notes
layout: layouts/page.njk
class: notes
---

{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<article>
<h3><a href="{{ post.url }}">{{ post.data.title }}</a></h3> 
{{ post.data.excerpt | safe}}
</article>
{%- endfor %}
