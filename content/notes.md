---
title: Notes
const numberOfLatestPostsToShow = 1000;
---

{% set postsCount = collections.posts | length %}

{% set postslist = collections.posts | head(-1 * numberOfLatestPostsToShow) %}
{% set postslistCounter = postsCount %}
{%- for post in postslist | reverse %}
<p><a href="{{post.url}}">{{ post.data.title }}</a> › {{ post.data.excerpt | safe }}</p>
<hr/>

{%- endfor %}
