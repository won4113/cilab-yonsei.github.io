---
title: "News"
layout: textlay
excerpt: "CILAB in Yonsei University."
sitemap: false
permalink: /allnews.html
---

# News
{% for article in site.data.news %}
<p><strong>{{ article.category}}</strong><br>
{{ article.date }} <br>
<em>{{ article.headline }}</em></p>
{% endfor %}
