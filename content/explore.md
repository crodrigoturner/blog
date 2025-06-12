---
layout: layouts/page.njk
title: Explore
eleventyExcludeFromCollections: true
---

{{ content | safe }}


<ol>
{%- for page in collections.page -%}
<li><a href="{{page.url}}">{{ page.data.title }}</a> › {{ page.data.excerpt }}</li>
{%- endfor -%}
</ol>