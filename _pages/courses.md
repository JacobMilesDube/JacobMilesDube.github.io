---
layout: page
title: courses
permalink: /courses/
description: A collection of courses
nav: true
nav_order: 2
display_categories: [work, fun]
horizontal: false
---

<!-- pages/courses.md -->
<div class="courses">
<!-- Display projects without categories -->
  {%- assign sorted_projects = site.courses | sort: "importance" -%}
  <!-- Generate cards for each project -->
  {% if page.horizontal -%}
  <div class="container">
    <div class="row row-cols-2">
    {%- for project in sorted_projects -%}
      {% include projects_horizontal.html %}
    {%- endfor %}
    </div>
  </div>
  {%- else -%}
  <div class="grid">
    {%- for project in sorted_projects -%}
      {% include projects.html %}
    {%- endfor %}
  </div>
  {%- endif -%}
</div>
