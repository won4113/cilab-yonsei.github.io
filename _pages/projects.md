---
title: "CILAB - Projects"
layout: gridlay
excerpt: "CILAB -- Projects"
sitemap: false
permalink: /projects/
---

# Projects

{% for publi in site.data.project_list %}

  <strong>{{ publi.title }}</strong><br />
  {{ publi.start }} ~ {{  publi.end  }}<br />
  {{ publi.company }}<br />

{% endfor %}