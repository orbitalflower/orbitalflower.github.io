---
title: links page layout
layout: default
---

<!--
  Custom template for links pages including a category from this site.
  Use by giving that page the properties layout: links and includecat: whatever.
  (is this unused?)
-->

{{ content }}

{% assign sortedPosts = site.posts | sort: 'title' %}

<ul>
  {% for post in sortedPosts %}
    {% if post.categories contains page.includecat %}
    {% unless page.slug == post.slug %}
  <li><a href="{{ post.url }}">{{ post.title }}</a>
  {% if post.updated %}&mdash; Updated: {{ post.updated | date_to_string }}
  {% else %}&mdash; {{ post.date | date_to_string }}
  {% endif %}
  </li>
    {% endunless %}
    {% endif %}
  {% endfor %}
</ul>
