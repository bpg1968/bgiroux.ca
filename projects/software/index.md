---
layout: page
title: Software Projects
permalink: /projects/software/
---

# Software Projects

{% for project in site.software %}
- [{{ project.title }}]({{ project.url }})
{% endfor %}

