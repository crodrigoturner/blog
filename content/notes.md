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

<ul>
	{%- for post in postslist | reverse %}
<li class="postlist-item{% if post.url == url %} postlist-item-active{% endif %}">
{% for tag in post.data.tags %}
        {% if tag != "posts" %}
<a href="{{ post.url }}" class="{{tag}}"><span class="{{tag}}"></span> {{ post.data.title }}</a>
   

        {% endif %}
      {% endfor %}

</li>
{%- endfor %}
</ul>

<span>1985 - today</span>
					<img src="https://v1.sparkline.11ty.dev/500x20/{{ collections.posts | getYearlyPostCount }}/" height="20" alt="Sparkline representing frequency of posts written from 2007 to {{ currentYear }}" loading="lazy" decoding="async" class="spark-img">