---
title: "CILAB - Honor/Award"
layout: gridlay
excerpt: "CILAB -- Honor/Award"
sitemap: false
permalink: /honor_award/
---

# Honor/Award

{% assign last_year = site.data.year_information.current_year %}
{% assign first_year = site.data.year_information.ha_first_showing_year %}

{% for current_year in (first_year..last_year) reversed %}
{% assign initial_state = 0 %}

{% for publi in site.data.honor_award_list %}
{% if publi.year == current_year %}

{% if initial_state == 0 %}
## {{ current_year }}
{% assign initial_state == 1 %}
{% endif %}

<strong>{{ publi.title }}</strong><br /> {{ publi.author }}<br />

{% endif %}

{% endfor %}
{% endfor %}
