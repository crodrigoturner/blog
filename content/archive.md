---
title: Archive
layout: layouts/base.njk
---
<section class="posts">
{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<article>

<h4><a href="{{ post.url }}">{{ post.title }}</a></h4>

{{ post.data.excerpt | safe}}

</article>
{%- endfor %}


</section>

