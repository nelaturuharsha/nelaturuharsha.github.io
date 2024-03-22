---
title: Media Consumption
layout: default
permalink: /media-consumption/
published: true
order: 2
---

<div class="ProjectContainer">

	<div class="gallery">

  {% assign media = site.pages | where: "category", "media-consumption" %}

  {% for project in media %}

  {% if project.redirect %}
  <p class="projectTile">
          <a href="{{ project.redirect }}" target="_blank">
              <span style="font-size: 1.5em;">
              {{ project.title }}
              </span>
              {{ project.description }}
          </a>
  </p>

  {% else %}

  <p class="projectTile">
          <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
              <span style="font-size: 1.5em;">
              {{ project.title }}
              </span>
              {{ project.description }}
          </a>
  </p>

  {% endif %}

  {% endfor %}

	</div>

</div>
