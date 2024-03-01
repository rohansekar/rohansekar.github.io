---
layout: page
title: research
permalink: /research/
description: 
nav: true
nav_order: 2
horizontal: false
---

<div class="research">
{%- if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized research -->
  {%- for category in page.display_categories %}
  <h2 class="category">{{ category }}</h2>
  {%- assign categorized_research = site.research | where: "category", category -%}
  {%- assign sorted_research = categorized_research | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_research -%}
      {% include research_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <!-- <div class="grid"> -->
  <div class="row row-cols-1">
    {%- for project in sorted_research -%}
      {% include research_horizontal.html %}
      <!-- { include research.html } -->
    {%- endfor %}
  </div>
  {%- endif -%}
  {% endfor %}

{%- else -%}
<!-- Display research without categories -->
  {%- assign sorted_research = site.research | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_research -%}
      {% include research_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <!-- <div class="grid"> -->
  <div class="row row-cols-1">
    {%- for project in sorted_research -%}
      {% include research_horizontal.html %}
      <!-- { include research.html } -->
    {%- endfor %}
  </div>
  {%- endif -%}
{%- endif -%}
</div>

