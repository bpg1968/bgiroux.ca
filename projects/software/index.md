---
title: "Software Projects"
description: "Explore my collection of personal software projects — small utilities, learning experiments, and practical tools built for fun and functionality."
layout: page
permalink: /projects/software/
---

# Software Projects

I enjoy building small, focused software projects — sometimes they're practical tools, and other times they're just fun exercises to sharpen my skills.
Many of these projects were created out of personal curiosity, to solve a real-world need, or simply to explore an idea that interested me.

Here you will find a selection of my software work, ranging from system utilities to algorithmic experiments.

---

<div class="row row-cols-1 row-cols-md-2 g-4">

{% assign sorted_projects = site.software | sort: "date" | reverse %}
{% for project in sorted_projects %}
  <div class="col">
    <div class="card h-100">
      <div class="card-body">
        <h5 class="card-title">{{ project.title }}</h5>
        <p class="card-text">{{ project.description }}</p>
        <a href="{{ project.url }}" class="btn btn-primary">View Project</a>
      </div>
    </div>
  </div>
{% endfor %}

</div>

