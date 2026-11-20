---
layout: page
permalink: /teaching/
title: teaching
description: 
nav: true
nav_order: 6
calendar: true
---
{% assign courses_by_year = site.teachings
  | group_by_exp: "course", "course.year"
  | sort: "name"
  | reverse
%}

{% for year in courses_by_year %}
## {{ year.name }}

<ul>
  {% assign courses = year.items | sort: "title" %}
  {% for course in courses %}
    <li>
      {{ course.title }}
      {% if course.term %} — {{ course.term }}{% endif %}
    </li>
  {% endfor %}
</ul>
{% endfor %}
