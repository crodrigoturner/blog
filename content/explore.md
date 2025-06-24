---
layout: layouts/page.njk
title: Explore
eleventyExcludeFromCollections: true
---

{{ content | safe }}

<h5>Other pages on this site</h5>
<ol>
{%- for page in collections.page -%}
<li><a href="{{page.url}}">{{ page.data.title }}</a> › {{ page.data.excerpt }}</li>
{%- endfor -%}
</ol>

<h5>Tags</h5>
<ul class="tagcloud">
<li><a href="/notes/">all</a></li>
{% for tag in collections | getKeys | filterTagList %}
{% set tagUrl %}/tag/{{ tag | slugify }}/{% endset %}
<li><a href="/tag/{{tag}}" >{{ tag }}</a></li>
{% endfor %}</ul>