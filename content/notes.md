---
title: Notes
layout: layouts/page.njk
class: notes
---

<p>{% for tag in collections | getKeys | filterTagList %}
{% set tagUrl %}/tag/{{ tag | slugify }}/{% endset %}
<span class="tag-item"><a href="/tag/{{tag}}" >{{ tag }}</a></span>
{% endfor %}</p>

{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<article>
<h3><a href="{{ post.url }}">{{ post.data.title }}</a></h3> 
{{ post.data.excerpt | safe}}
</article>
{%- endfor %}
