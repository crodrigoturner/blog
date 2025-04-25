---
title: Notes
layout: layouts/base.njk
---
<section class="posts">
{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<article>

<img src="{{post.data.cover}}" alt="cover image" class="cover"/>
<h4><a href="{{ post.url }}">{{ post.data.title }}</a></h4>

{{ post.content | safe}}

</article>
{%- endfor %}
</section>

