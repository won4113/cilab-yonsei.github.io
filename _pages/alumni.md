---
title: "CILAB - Alumni"
layout: gridlay
excerpt: "CILAB: Alumni"
sitemap: false
permalink: /alumni/
---

# Alumni

Jump to [PhD Degree](#phd-degree), [Master Degree](#master-degree).

## PhD Degree
{% assign number_printed = 0 %}
{% for member in site.data.members.alumni.phd_list %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

{% if member.cv.exist == 1 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.affiliation }}</i>
  <ul style="overflow: hidden">
  <br>CV: <a href="{{ site.url }}{{ site.baseurl }}/cv/{{ member.cv.url }}">download</a>
  </ul>
</div>
{% endif %}

{% if member.cv.exist == 0 %}
<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.affiliation }}</i>
  <ul style="overflow: hidden">
  <br>
  </ul>
</div>
{% endif %}

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

## Master Degree
{% assign number_printed = 0 %}
{% for member in site.data.members.alumni.ms_list %}

{% assign even_odd = number_printed | modulo: 2 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
  <img src="{{ site.url }}{{ site.baseurl }}/images/teampic/{{ member.photo }}" class="img-responsive" width="25%" style="float: center" />
  <h4>{{ member.name }}</h4>
  <i>{{ member.affiliation }}</i>
  <ul style="overflow: hidden">

  </ul>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}