---
layout: page
permalink: /teaching/
title: teaching
description: 
nav: true
nav_order: 6
calendar: true
---
<!-- {% assign courses_by_year = site.teachings
  | group_by_exp: "course", "course.year"
  | sort: "name"
  | reverse
%} -->

<!-- {% for year in courses_by_year %}
  <h2 class="year">{{ year.name }}</h2>
  <hr>

  <ul class="teaching-list">
    {% assign courses = year.items | sort: "title" %}
    {% for course in courses %}
      <li>
        <strong>{{ course.title }}</strong>
        {% if course.term %}<span> — {{ course.term }}</span>{% endif %}
      </li>
    {% endfor %}
  </ul>
{% endfor %} -->

{% include courses.liquid %}
