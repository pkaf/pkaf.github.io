---
layout: archive
title: "Diary"
permalink: /diary/
---

{% for entry in site.diary %}
- [{{ entry.title }}]({{ entry.url }}) — {{ entry.date | date: "%B %d, %Y" }}
{% endfor %}