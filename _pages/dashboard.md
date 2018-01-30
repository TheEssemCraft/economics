---
title: "Dashboard"
permalink: "/dashboard.html"
layout: archive
categories: "site"
---

<div class="grid__wrapper">
  {% for post in site.pages %}
    {% unless page.categories contains 'site' %}
      {% include archive-single.html type="grid" %}
    {% endif %}
  {% endfor %}
</div>

{% comment %}
{{ site.pages }}
{% endcomment %}

{% for post in site.pages %}
  {{ page.categories }}
{% endfor %}
