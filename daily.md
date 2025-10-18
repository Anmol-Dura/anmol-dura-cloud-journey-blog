---
layout: page
title: Daily
permalink: /daily/
---

Short, raw logs of what I'm doing or learning.

<ul>
  {% assign items = site.daily | sort: 'date' | reverse %}
  {% for entry in items %}
    <li>
      <a href="{{ entry.url | relative_url }}">{{ entry.title }}</a>
      <small>— {{ entry.date | date: "%B %d, %Y" }}</small>
    </li>
  {% endfor %}
</ul>
