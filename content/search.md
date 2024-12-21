<img class="hero" src="/img/sitemap.png" alt="storr"/> 

## Search

<form action="https://duckduckgo.com">
  <input name="q" id="search" />
  <input type="hidden" name="sites" value="oliverjam.es" />
  <input type="hidden" name="ko" value="-2" />
  <input type="hidden" name="k1" value="-1" />
  <input type="hidden" name="kz" value="-1" />
  <input type="hidden" name="km" value="m" />
  <input type="hidden" name="k7" value="#fafef5" />
</form>

### Tags

<ul class="tags">
{% for tag in collections | getKeys | filterTagList %}
	{% set tagUrl %}/tags/{{ tag | slugify }}/{% endset %}
	<li><a href="{{ tagUrl }}" class="post-tag">{{ tag }}</a></li>
{% endfor %}
</ul>

### Index

<ul>
	{%- for entry in collections.all %}
	<li><a href="{{ entry.url }}">{{entry.url}}</a></li>
	{%- endfor %}
</ul>