---
layout: layouts/page.njk
title: More
class: more
eleventyExcludeFromCollections: true
---

<ul>
	{%- for entry in collections.all %}
	<li><a href="{{ entry.url }}">{{ entry.data.title }}</a></li>
	{%- endfor %}
</ul>
