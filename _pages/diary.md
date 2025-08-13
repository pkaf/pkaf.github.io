---
layout: archive
title: "Diary"
permalink: /diary/
author_profile: true
---

{% for entry in site.diary %}
- [{{ entry.title }}]({{ entry.url }}) — {{ entry.date | date: "%B %d, %Y" }}
{% endfor %}