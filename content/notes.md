---
title: Notes
layout: layouts/base.njk
---
<section class="posts">
{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<article>

<h4><a href="{{ post.url }}">{{ post.data.title }}</a></h4>

{{ post.data.excerpt | safe}}

</article>
{%- endfor %}


</section>

