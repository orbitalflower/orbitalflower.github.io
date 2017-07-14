---
title: links page layout
layout: default
---

{{ content }}

{% assign sortedPosts = site.posts | sort: 'title' %}

<ul>
  {% for post in sortedPosts %}
    {% if post.categories contains post.includecat %}
  <li><a href="{{ post.url }}">{{ post.title }}</a>
  {% if post.updated %}&mdash; Updated: {{ post.updated | date_to_string }}
  {% else %}&mdash; {{ post.date | date_to_string }}
  {% endif %}
  </li>
    {% endif %}
  {% endfor %}
</ul>
