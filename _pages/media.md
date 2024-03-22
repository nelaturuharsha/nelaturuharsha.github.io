---
title: Media Consumption
layout: default
permalink: /media-consumption/
published: true
order: 2
---

{% assign media = site.pages | where: "category", "media-consumption" %}
{% for project in media %}

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