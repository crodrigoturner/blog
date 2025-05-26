---
layout: layouts/page.njk
title: More
eleventyExcludeFromCollections: true
---

<ul>
	{%- for entry in collections.all %}
	<li><a href="{{ entry.url }}">{{ entry.data.title }}</a></li>
	{%- endfor %}
</ul>



<h2>{{title}}</h2>

{{ content | safe }}


<ul>
{%- for page in collections.page -%}
<li><a href="{{page.url}}">{{ page.data.title }}</a> {{ page.data.excerpt }}</li>
{%- endfor -%}
</ul>