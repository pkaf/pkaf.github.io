---
layout: archive
title: "Diary"
permalink: /diary/
author_profile: true
---

With the intention of sharing knowledge more widely—and, importantly, keeping a record for myself—I’m starting to jot down thoughts here. 

My plan is to write at least three working days a week. 

Everything shared here should be considered personal reflections and hypothetical scenarios based on what I hear, learn, or recall from day-to-day life and past experiences. Any resemblance to real events is purely coincidental.

{% assign diary_posts = site.diary | sort: 'date' | reverse %}

{% assign current_week = "" %}
{% for post in diary_posts %}
  {% assign post_week = post.date | date: "%Y-%U" %}  {# %U = week number (Sunday as first day) #}
  
  {% if post_week != current_week %}
    {% if current_week != "" %}
      </ul>
    {% endif %}
    {% assign current_week = post_week %}
    {% assign week_year = post.date | date: "%Y" %}
    {% assign week_number = post.date | date: "%U" %}
    <h2>Week {{ week_number }}, {{ week_year }}</h2>
    <ul>
  {% endif %}
  
  <li>
    <a href="{{ post.url }}">{{ post.title }}</a> — {{ post.date | date: "%d %b %Y" }}
  </li>
{% endfor %}
</ul>
