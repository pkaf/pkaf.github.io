---
title: "Diary"
layout: "archive"
permalink: /diary/
author_profile: True
type: "diary"
---

With the aim of sharing the daily amusements of a data scientist more broadly—and, importantly, keeping a personal record of progress—I’m beginning to jot down my thoughts here.

My plan is to write at least three working days a week. 

Everything shared should be taken as personal reflections and hypothetical scenarios based on what I hear, learn, or recall from by day-to-day but also past experiences; any resemblance to real events is purely coincidental.

{% assign sorted_diary = site.diary | sort: "date" | reverse %}
{% for entry in sorted_diary %}
- [{{ entry.title }}]({{ entry.url }}) — {{ entry.date | date: "%B %d, %Y" }}
{% endfor %}