---
title: "Dashboard"
permalink: "/dashboard.html"
layout: archive
hidden: true
---

<div class="grid__wrapper">
  {% for post in site.concepts %}
    {% unless post.hidden == true %}
      {% include archive-single.html type="grid" %}
    {% endunless %}
  {% endfor %}
</div>

{% comment %}
{{ site.pages }}
{% endcomment %}
