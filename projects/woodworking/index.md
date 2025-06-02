---
title: "Woodworking Projects"
description: "Handmade projects that blend function, form, and the satisfaction of working with wood."
layout: default
language: en-CA
permalink: /projects/woodworking/
---

# Woodworking Projects

Welcome to my collection of woodworking projects.

Each piece here was made by hand — sometimes out of necessity, sometimes for the joy of building, and sometimes just to see if I could pull it off. Some are practical, others experimental, but they all share one thing: they were made with care.

---

<div class="row row-cols-1 row-cols-md-2 g-4 my-3">
  {% assign sorted_projects = site.woodworking | sort: "date" | reverse %}
  {% for post in sorted_projects %}
    <div class="col">
      <div class="card h-100 shadow-sm">
      
        <div class="card-body d-flex">
          {% if post.thumbnail %}
            <img src="{{ post.thumbnail }}"
                class="flex-shrink-0 me-3 rounded"
                alt="Thumbnail for {{ post.title }}"
                style="width: 128px; height: 128px; object-fit: cover;">
          {% endif %}
            
          <div>
            <p class="text-muted small mb-0">{{ post.date | date: "%-d %B %Y" }}</p>
          
            <h5 class="card-title mb-1">
              <a class="stretched-link text-decoration-none" href="{{ post.url }}">{{ post.title }}</a>
            </h5>
            
            {% assign blurb = post.summary | default: post.description %}
            {% if blurb %}
              <p class="card-text mb-1">
                {{ blurb }}
              </p>
            {% endif %}
            
            {% if post.category %}
              <p class="mb-1 small text-muted">
              <strong>Category:</strong> {{ post.category }}
              </p>
            {% endif %}
            
            {% if post.labels %}
              <p class="mb-1 small">
              {% for label in post.labels %}
                <span class="badge bg-secondary me-1">{{ label }}</span>
              {% endfor %}
              </p>
            {% endif %}
          </div>
        </div>
      
      </div>
    </div>
  {% endfor %}
</div>

