---
title: Notes
layout: layouts/base.njk
---

{{ content | safe }}
<span>1985 - today</span>
					<img src="https://v1.sparkline.11ty.dev/500x20/{{ collections.posts | getYearlyPostCount }}/" height="20" alt="Sparkline representing frequency of posts written from 2007 to {{ currentYear }}" loading="lazy" decoding="async" class="spark-img">
<hr/>

{% set postslist = collections.posts | head(-1 * numberOfLatestPostsToShow) %}
{% set postslistCounter = postsCount %}
{% include "postslist.njk" %}