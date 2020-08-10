---
title: "CILAB - Patents"
layout: gridlay
excerpt: "CILAB -- Patents."
sitemap: false
permalink: /patents/
---

# Patents

Jump to [Registration](#registration), [Application](#application).

## Registration

{% for publi in site.data.patent_registration_list %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}

## Application

{% for publi in site.data.patent_application_list %}

  {{ publi.title }} <br />
  <em>{{ publi.authors }} </em><br /><a href="{{ publi.link.url }}">{{ publi.link.display }}</a>

{% endfor %}


