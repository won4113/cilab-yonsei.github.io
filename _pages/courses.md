---
title: "CILAB - Courses"
layout: gridlay
excerpt: "CILAB -- Courses"
sitemap: false
permalink: /courses/
---

# Courses

{% assign last_year = site.data.year_information.current_year %}
{% assign first_year = site.data.year_information.course_first_showing_year %}

{% for current_year in (first_year..last_year) reversed %}
{% for current_semester in site.data.year_information.semester_list reversed %}
{% assign initial_state = 0 %}

{% for publi in site.data.course_list %}
{% if publi.year == current_year %}
{% if publi.semester == current_semester %}

{% if initial_state == 0 %}
## {{  current_year }} {{ current_semester }}
{% assign initial_state == 1 %}
{% endif %}

<strong>{{ publi.number }}</strong><br /> [{{ publi.title }}]<br />

{% endif %}
{% endif %}

{% endfor %}

{% endfor %}
{% endfor %}

