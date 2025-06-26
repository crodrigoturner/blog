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
<li><a href="/tag/uses/">Uses</a>  › Tools and apps for a semi-productive life</li>
<li><a href="/tag/projects/">Projects</a>  › Things to keep me busy</li>

</ol>

<h5>Tags</h5>
<ul class="tagcloud">
<li><a href="/blog/">all</a></li>
{% for tag in collections | getKeys | filterTagList %}
{% set tagUrl %}/tag/{{ tag | slugify }}/{% endset %}
<li><a href="/tag/{{tag}}" >{{ tag }}</a></li>
{% endfor %}</ul>

<h5>Elsewhere</h5>

<ol>
<li><a href="https://www.imdb.com/user/ur178111487/?ref_=ext_shr_lnk">Imdb</a> </li>
<li><a href="https://github.com/crodrigoturner"></a>Github </li>
<li><a href="https://www.goodreads.com/user/show/190088576-carlos-rodrigo-turner">Goodreads</a> </li>
</ol>