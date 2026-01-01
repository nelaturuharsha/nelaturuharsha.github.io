---
title: Projects
layout: page
permalink: /projects/
description: Selected projects and talks
---

## Projects

<div class="grid grid-auto">
{% for project in site.data.projects %}
<div class="card card-interactive">
  <div class="card-header">
    <h3 class="card-title">
      {% if project.url %}
      <a href="{{ project.url }}" target="_blank" rel="noopener">{{ project.title }}</a>
      {% else %}
      {{ project.title }}
      {% endif %}
    </h3>
  </div>
  <div class="card-body">
    <p>{{ project.description }}</p>
  </div>
  {% if project.url %}
  <div class="card-footer">
    <a href="{{ project.url }}" class="btn btn-sm btn-secondary" target="_blank" rel="noopener">
      View Project &rarr;
    </a>
  </div>
  {% endif %}
</div>
{% endfor %}
</div>

---

## Talks

<div class="talks-list">
{% for talk in site.data.talks %}
<div class="talk-item">
  <h4 class="talk-title">{{ talk.title }}</h4>
  <div class="talk-links">
    {% if talk.slides %}
    <a href="{{ talk.slides }}" class="btn btn-sm btn-secondary" target="_blank" rel="noopener">
      Slides
    </a>
    {% endif %}
    {% if talk.video %}
    <a href="{{ talk.video }}" class="btn btn-sm btn-secondary" target="_blank" rel="noopener">
      Video
    </a>
    {% endif %}
    {% if talk.code %}
    <a href="{{ talk.code }}" class="btn btn-sm btn-secondary" target="_blank" rel="noopener">
      Code
    </a>
    {% endif %}
  </div>
</div>
{% endfor %}
</div>

<style>
.talks-list {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.talk-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
  border-bottom: 1px solid var(--border-color, #e2e8f0);
  flex-wrap: wrap;
  gap: 1rem;
}

.talk-item:last-child {
  border-bottom: none;
}

.talk-title {
  margin: 0;
  font-size: 1rem;
  font-weight: 500;
}

.talk-links {
  display: flex;
  gap: 0.5rem;
}
</style>
