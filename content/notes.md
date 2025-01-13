---const numberOfLatestPostsToShow = 1000;
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
<hr/>
{% set postslist = collections.posts | head(-1 * numberOfLatestPostsToShow) %}
{% set postslistCounter = postsCount %}
{% include "postslist.njk" %}
<hr/>
<span>1985 - today</span>
					<img src="https://v1.sparkline.11ty.dev/500x20/{{ collections.posts | getYearlyPostCount }}/" height="20" alt="Sparkline representing frequency of posts written from 2007 to {{ currentYear }}" loading="lazy" decoding="async" class="spark-img">
<hr/>
