---
layout: layouts/page.njk
title: More
eleventyExcludeFromCollections: true
---

{{ content | safe }}


<ul>
{%- for page in collections.page -%}
<li><a href="{{page.url}}">{{ page.data.title }}</a> › {{ page.data.excerpt }}</li>
{%- endfor -%}
</ul>