## Sitemap

<ul>
	{%- for entry in collections.all %}
	<li><a href="{{ entry.url }}">{{entry.url}}</a></li>
	{%- endfor %}
</ul>