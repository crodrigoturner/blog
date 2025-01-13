---
title: Notes
layout: layouts/base.njk
---

{{ content | safe }}

{% set postslist = collections.posts | head(-1 * numberOfLatestPostsToShow) %}
{% set postslistCounter = postsCount %}
{% include "postslist.njk" %}