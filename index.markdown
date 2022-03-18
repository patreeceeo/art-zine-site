---
author_profile: true
layout: collection
entries_layout: grid
title: "issue #1: _Folklore_"
tagline: is here
header:
  overlay_image: assets/issues/01-folklore/Jun.png
  overlay_filter: 0.5
  actions:
    - label: "Check it out!"
      url: "/issues/01-folklore/00-cover.html"
---

<h3 class="archive__subtitle">{{ site.data.ui-text[site.locale].recent_posts | default: "All issues" }}</h3>

{% if paginator %}
  {% assign posts = paginator.posts %}
{% else %}
  {% assign posts = site.posts %}
{% endif %}

{% assign entries_layout = page.entries_layout | default: 'list' %}
<div class="entries-{{ entries_layout }}">
{% for post in site.issues %}
  {% if post.is_cover %}
  {% include archive-single.html type=entries_layout %}
  {% endif %}
{% endfor %}
<div class="entries-{{ entries_layout }}">

{% include paginator.html %}
