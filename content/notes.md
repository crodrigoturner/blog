---
title: Notes
layout: layouts/base.njk
---
<section class="posts">
{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<article>

<img src="{{post.data.cover}}" alt="cover image" class="cover"/>
<a href="{{ post.url }}"><h4>{{ post.data.title }}</h4></a>

{{ post.content | safe}}

</article>
{%- endfor %}
</section>

