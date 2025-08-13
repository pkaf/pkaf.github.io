---
title: "Diary"
layout: "archive"
permalink: /diary/
type: "diary"
---

With the aim of sharing the daily amusements of a data scientist more broadly—and, importantly, keeping a personal record of progress—I’m beginning to jot down my thoughts here.

My plan is to write at least three working days a week. 

Everything shared should be taken as personal reflections and hypothetical scenarios based on what I hear, learn, or recall from by day-to-day but also past experiences; any resemblance to real events is purely coincidental.

{% for entry in site.diary %}
- [{{ entry.title }}]({{ entry.url }}) — {{ entry.date | date: "%B %d, %Y" }}
{% endfor %}