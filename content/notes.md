---js
const numberOfLatestPostsToShow = 1000;
layout: layouts/base.njk
title: Notes
---
<section class="posts">
{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<article>
<a href="{{ post.url }}">
<img src="{{post.data.cover}}" alt="cover image" class="cover"/>
<h4>{{ post.data.title }}</h4></a>

{{ post.content | safe}}

</article>
{%- endfor %}
</section>

