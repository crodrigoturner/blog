## Sitemap

<img class="hero" src="/img/sitemap.png" alt="storr"/> 

<ul>
	{%- for entry in collections.all %}
	<li><a href="{{ entry.url }}">{{entry.url}}</a></li>
	{%- endfor %}
</ul>