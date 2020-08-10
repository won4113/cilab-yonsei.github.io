---
title: "CILAB - Patents - Registration"
layout: gridlay
excerpt: "CILAB -- Patents - Registration."
sitemap: false
permalink: /patents_registration/
---

# Registration

{% assign last_year = site.data.year_information.current_year %}
{% assign first_year = site.data.year_information.pub_first_showing_year %}

Jump to
{% for current_year in (first_year..last_year) reversed -%}
[{{ current_year }}](#{{ current_year }}),
{% endfor -%}
[Before {{ first_year }}](#before-{{ first_year }}).<br />

{% for current_year in (first_year..last_year) reversed %}
## {{ current_year }}
{% for publi in site.data.patents.registration_list %}

  {% if publi.year == current_year %}

  <strong>{{ publi.title }}</strong> <br />
  <em>{{ publi.authors }}</em> <br />
  <em>{{ publi.registration_number }}</em>, {{ publi.month }}, {{ publi.year }}.<br />

  {% endif %}

{% endfor %}
{% endfor %}

## Before {{ first_year }}
{% for publi in site.data.patents.registration_list %}

  {% if publi.year < current_year %}

  <strong>{{ publi.title }}</strong> <br />
  <em>{{ publi.authors }}</em> <br />
  <em>{{ publi.registration_number }}</em>, {{ publi.month }}, {{ publi.year }}.<br />

  {% endif %}

{% endfor %}