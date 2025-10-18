---
layout: page
title: Blog
permalink: /blog/
---

<ul>
  {% for post in site.posts %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <small>— {{ post.date | date: "%B %d, %Y" }}</small>
      {% if post.excerpt %}<br><em>{{ post.excerpt | strip_html }}</em>{% endif %}
    </li>
  {% endfor %}
</ul>
