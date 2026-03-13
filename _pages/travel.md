---
layout: page
title: Travel
permalink: /travels/
# description: A growing collection of your cool travels.
nav: true
nav_order: 5
display_categories: [work, fun]
horizontal: false
---

<!-- pages/travels.md -->
<div class="travels">
{% if site.enable_travel_categories and page.display_categories %}
  <!-- Display categorized travels -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_travels = site.travels | where: "category", category %}
  {% assign sorted_travels = categorized_travels | sort: "importance" %}
  <!-- Generate cards for each travel -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_travels %}
      {% include travels_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_travels %}
      {% include travels.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

<!-- Display travels without categories -->

{% assign sorted_travels = site.travels | sort: "importance" %}

  <!-- Generate cards for each project -->

{% if page.horizontal %}

  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_travels %}
      {% include travels_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_travels %}
      {% include travels.liquid %}
    {% endfor %}
  </div>
  {% endif %}
{% endif %}
</div>
