---
layout: archive
title: "Diary"
permalink: /diary/
author_profile: true
---

With the intention of sharing knowledge more widely—and, importantly, keeping a record for myself—I’m starting to jot down thoughts here. 

My plan is to write at least three working days a week. 

Naturally, everything shared will be personal reflections and hypothetical scenarios based on what I hear, learn, or recall from past experiences; any resemblance to real events is purely coincidental.


{% assign diary_posts = site.diary | sort: 'date' | reverse %}

{% assign current_month = "" %}
{% for post in diary_posts %}
  {% assign post_month = post.date | date: "%B %Y" %}
  
  {% if post_month != current_month %}
    {% if current_month != "" %}
      </ul>
    {% endif %}
    <h2>{{ post_month }}</h2>
    <ul>
    {% assign current_month = post_month %}
  {% endif %}
  
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%d %b %Y" }}
  </li>
{% endfor %}
</ul>