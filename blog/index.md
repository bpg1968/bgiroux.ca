---
layout: page
title: Blog
permalink: /blog/
---

# Blog

<div class="row row-cols-1 g-4 mt-4">
{% for post in site.posts %}
  <div class="mb-4">
    <div class="d-flex align-items-start">
      {% if post.thumbnail %}
        <img src="{{ post.thumbnail }}" class="flex-shrink-0 me-3 blog-thumbnail" alt="{{ post.title }}">
      {% endif %}

      <div>
        <h2 class="h5 mb-1">
          <a href="{{ post.url }}" class="text-decoration-none">{{ post.title }}</a>
        </h2>

        {% if post.subtitle %}
          <h3 class="h6 text-muted mb-2">{{ post.subtitle }}</h3>
        {% endif %}

        {% if post.excerpt %}
          <p class="mb-0">{{ post.excerpt }}</p>
        {% endif %}
      </div>
    </div>
  </div>
{% endfor %}
</div>

