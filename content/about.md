---js
const eleventyNavigation = {
	key: "About",
	order: 1
};
title: About
---

## About

Hi, I'm Carlos, a data specialist with 7+ years of experience in leveraging data to drive businesses forward. I am passionate about helping make data-driven decisions that lead to growth and success. 

I have worked in architecture studios, big energy companies, luxury brands, and small companies. I currently work at <a href="http://tecnicayavance.com">Técnica y Avance</a>.

I live in Madrid with Mar, Lucas, Nicolás and <a href="/blog/pancho.md">Pancho</a>.

{% set posts = collections.posts | contains("data.tags", 'meta') %}
<ul>
{%- for offer in offers %}
    <li><a href="{{ post.url }}">{{ post.title }}</a></li>
{%- endfor -%}
</ul>
