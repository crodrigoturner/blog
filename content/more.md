---
layout: layouts/page.njk
title: More
class: more
---

<ul>
<li>Now</li>
<li>Colophon</li>
<li>Blogroll</li>
</ul>
<ul>
	{%- for entry in collections.all %}
	<li><a href="{{ entry.url }}">{{ entry.data.title }}</a></li>
	{%- endfor %}
</ul>

</ul>
{% set postslist = collections.posts %}
{%- for post in postslist | reverse %}
<li><a href="{{ post.url }}">{{ post.data.title }}</a> {{ post.data.excerpt | safe}}</li>
{%- endfor %}
</ul>