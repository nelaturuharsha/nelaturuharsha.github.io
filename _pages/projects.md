---
title: Projects
layout: default
permalink: /projects/
published: true
order: 1
---

{% assign projects = site.pages | where: "category", "project" %}
{% for project in projects %}

{% if project.redirect %}
<a href="{{ project.redirect }}" target="_blank"  style="font-size: 1.5em;">
    {{ project.title }}
</a>

{{ project.description }}

{% else %}

<a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}" style="font-size: 1.5em;">
    {{ project.title }}
</a>

{{ project.description }}

{% endif %}

{% endfor %}