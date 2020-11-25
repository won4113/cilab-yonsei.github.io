---
title: "CILAB - Domestic Conference"
layout: gridlay
excerpt: "CILAB -- Domestic Conference."
sitemap: false
permalink: /dom_conference/
---

# Domestic Conference

{% assign last_year = site.data.year_information.current_year %}
{% assign first_year = site.data.year_information.pub_first_showing_year %}

Jump to
{% for current_year in (first_year..last_year) reversed -%}
[{{ current_year }}](#{{ current_year }}),
{% endfor -%}
[Before {{ first_year }}](#before-{{ first_year }}).<br />

{% for current_year in (first_year..last_year) reversed %}
  {% assign data_exist = false %}
  {% for publi in site.data.publications.dom_conference_list %}
    {% if publi.year == current_year %}
      {% assign data_exist = true %}
    {% endif %}
  {% endfor %}

  {% if data_exist %}
## {{ current_year }}
    {% for publi in site.data.publications.dom_conference_list %}

      {% if publi.year == current_year %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.conference }}</em> {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}, vol. {{ publi.vol }}, no. {{ publi.issue }}.<br />
      {% endif %}

    {% endfor %}
  {% endif %}
{% endfor %}

## Before {{ first_year }}
{% for publi in site.data.publications.dom_conference_list %}

  {% if publi.year < first_year %}

  <strong>{{ publi.title }}</strong> <br />
  <em>{{ publi.authors }}</em> <br />
  <em>{{ publi.conference }}</em>, {{ publi.venue }}, {{ publi.month }}, {{ publi.year }}, vol. {{ publi.vol }}, no. {{ publi.issue }},.<br />

  {% endif %}

{% endfor %}