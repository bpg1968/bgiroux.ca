---
layout: page
title: Home
permalink: /
---

<h2 class="mt-5">Woodworking Projects</h2>
<div class="row row-cols-1 row-cols-md-2 g-4 mb-5">
  {% assign woodworking_projects = site.woodworking | sort: 'date' | reverse | slice: 0, 2 %}
  {% for project in woodworking_projects %}
    <div class="col">
      <div class="card h-100 border-secondary">
        <div class="card-body">
          <h5 class="card-title">{{ project.title }}</h5>
          <p class="card-text">{{ project.summary | strip_html | truncate: 160 }}</p>
          <a href="{{ project.url | relative_url }}" class="btn btn-outline-primary mt-2">Read More</a>
        </div>
      </div>
    </div>
  {% endfor %}
</div>

<h2 class="mt-5">Software Projects</h2>
<div class="row row-cols-1 row-cols-md-2 g-4">
  {% assign software_projects = site.software | sort: 'date' | reverse | slice: 0, 2 %}
  {% for project in software_projects %}
    <div class="col">
      <div class="card h-100 border-primary">
        <div class="card-body">
          <h5 class="card-title">{{ project.title }}</h5>
          <p class="card-text">{{ project.description | strip_html | truncate: 160 }}</p>
          <a href="{{ project.url | relative_url }}" class="btn btn-outline-primary mt-2">Read More</a>
        </div>
      </div>
    </div>
  {% endfor %}
</div>


<!--
Hi, I'm Brian Giroux — a creator, builder, and lifelong learner based in Bathurst, New Brunswick.

I enjoy working at the intersection of creativity and craftsmanship, whether it's through software projects, woodworking, open-source contributions, or thoughtful writing.

This site is where I share my projects, reflections, and stories.

## Explore

- [About](/about/)  
  Learn more about who I am and what drives my work.

- [Projects](/projects/)  
  A collection of programming and woodworking projects I've built.

- [Writing](/writing/)  
  News, essays, and short stories.

- [Contact](/contact/)  
  Get in touch.

---

Thanks for visiting — I hope you find something here that inspires or interests you.
-->
