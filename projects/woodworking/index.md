---
title: "Woodworking Projects"
layout: default
permalink: /projects/woodworking/
summary: "Handmade projects that blend function, form, and the satisfaction of working with wood."
---

# Woodworking Projects

Welcome to my collection of woodworking projects.

Each piece here was made by hand — sometimes out of necessity, sometimes for the joy of building, and sometimes just to see if I could pull it off. Some are practical, others experimental, but they all share one thing: they were made with care.

---

## Project Gallery

<div class="row row-cols-1 row-cols-md-2 g-4 my-3">

{% assign sorted_wood_projects = site.woodworking | sort: "date" | reverse %}
{% for post in sorted_wood_projects %}
  <div class="col">
    <div class="card h-100 shadow-sm">
      <div class="card-body">
        <h5 class="card-title">
          <a class="stretched-link text-decoration-none" href="{{ post.url }}">{{ post.title }}</a>
        </h5>
        {% if post.summary %}
          <p class="card-text">{{ post.summary }}</p>
        {% endif %}
        <p class="text-muted small mb-0">{{ post.date | date: "%-d %B %Y" }}</p>
      </div>
    </div>
  </div>
{% endfor %}

</div>

