---
title: "CILAB - Patents - Application"
layout: gridlay
excerpt: "CILAB -- Patents - Application."
sitemap: false
permalink: /patents_application/
---


# Application

{% assign last_year = site.data.year_information.current_year %}
{% assign first_year = site.data.year_information.pub_first_showing_year %}
{% assign first_year_plus_one = {{ first_year | plus : 1}} %}

Jump to
{% for current_year in (first_year_plus_one..last_year) reversed -%}
[{{ current_year }}](#{{ current_year }}),
{% endfor -%}
[{{ first_year }}](#{{ first_year }}).<br />

{% for current_year in (first_year..last_year) reversed %}
  {% assign data_exist = false %}
  {% for publi in site.data.patents.application_list %}
    {% if publi.year == current_year %}
      {% assign data_exist = true %}
    {% endif %}
  {% endfor %}
  
  {% if data_exist %}
## {{ current_year }}
    {% for publi in site.data.patents.application_list %}

      {% if publi.year == current_year %}
<strong>{{ publi.title }}</strong> <br />
<em>{{ publi.authors }}</em> <br />
<em>{{ publi.application_number }}</em>, {{ publi.month }}, {{ publi.year }}.<br />
      {% endif %}
    {% endfor %}
  {% endif %}
{% endfor %}