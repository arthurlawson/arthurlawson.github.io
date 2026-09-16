---
layout: page
title: PROJECTS
permalink: /projects/
description: A growing collection of my cool projects.
nav: true
nav_order: 3
display_categories: [fun]
horizontal: false
---

<!-- pages/projects.md -->
<div class="projects">
{% if site.enable_project_categories and page.display_categories %}
  <!-- Display categorized projects -->
  {% for category in page.display_categories %}
  <a id="{{ category }}" href=".#{{ category }}">
    <h2 class="category">{{ category }}</h2>
  </a>
  {% assign categorized_projects = site.projects | where: "category", category %}
  {% assign sorted_projects = categorized_projects | sort: "importance" %}
  <!-- Generate cards for each project -->
  {% if page.horizontal %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-2">
    {% for project in sorted_projects %}
      {% include projects_horizontal.liquid %}
    {% endfor %}
    </div>
  </div>
  {% else %}
  <div class="row row-cols-1 row-cols-md-3">
    {% for project in sorted_projects %}
      {% include projects.liquid %}
    {% endfor %}
  </div>
  {% endif %}
  {% endfor %}

{% else %}

  <!-- Display projects without categories (Updated to strictly respect display_categories) -->
  {% assign filtered_projects = "" | split: "" %}
  {% for cat in page.display_categories %}
    {% assign match = site.projects | where: "category", cat %}
    {% assign filtered_projects = filtered_projects | concat: match %}
  {% endfor %}

  {% assign sorted_projects = filtered_projects | sort: "importance" %}

    <!-- Generate cards for each project -->
    {% if page.horizontal %}
    <div class="container">
      <div class="row row-cols-1 row-cols-md-2">
      {% for project in sorted_projects %}
        {% include projects_horizontal.liquid %}
      {% endfor %}
      </div>
    </div>
    {% else %}
    <!-- Centers the single project card beautifully on your screen -->
    <div class="row row-cols-1 row-cols-md-3 justify-content-center">
      {% for project in sorted_projects %}
        {% include projects.liquid %}
      {% endfor %}
    </div>
    {% endif %}
  {% endif %}
</div>
