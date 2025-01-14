---
title: Notes
layout: layouts/base.njk
---

## Notes

{{ content | safe }}

<span class="tags">
{% for tag in collections | getKeys | filterTagList %}
	{% set tagUrl %}/tags/{{ tag | slugify }}/{% endset %}
<a href="{{ tagUrl }}">{{ tag }}</a>
{% endfor %}
</span>


<h2><a href="/">home</a> › {{ tag }}</h2>

{% set postslist = collections[ tag ] %}
<ul>
	{%- for post in postslist | reverse %}
<li class="postlist-item{% if post.url == url %} postlist-item-active{% endif %}">
<a href="{{ post.url }}" class="title">{{ post.data.title }}</a>
</li>
{%- endfor %}
</ul>