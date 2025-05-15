---
title: Notes
layout: layouts/page.njk
class: notes
---
<ul>
{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<li><a href="{{ post.url }}">{{ post.data.title }}</a> {{ post.data.excerpt | safe}}</li>
{%- endfor %}
</ul>