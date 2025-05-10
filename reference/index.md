---
layout: page
title: Reference
permalink: /reference/
---

# Reference

A growing collection of notes and quick lookups.

{% for note in site.reference %}
- [{{ note.title }}]({{ note.url }})
{% endfor %}

