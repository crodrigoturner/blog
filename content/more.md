---
layout: layouts/page.njk
title: More
class: more
---

<ul>
	{%- for entry in collections.pages %}
	<li><a href="{{ entry.url }}">{{ entry.data.title }}</a></li>
	{%- endfor %}
</ul>


<ul>
	{%- for entry in collections.all %}
	<li><a href="{{ entry.url }}">{{ entry.data.title }}</a></li>
	{%- endfor %}
</ul>
