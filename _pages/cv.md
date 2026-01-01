---
title: CV
layout: page
permalink: /cv/
description: Curriculum Vitae
---

<div class="cv-header">
  <h2>Sree Harsha Nelaturu</h2>
  <p class="cv-subtitle">Deep Learning Researcher</p>
  <p class="cv-contact">
    <a href="mailto:{{ site.email }}">{{ site.email }}</a> |
    <a href="https://github.com/{{ site.github }}" target="_blank">GitHub</a> |
    <a href="https://linkedin.com/in/{{ site.linkedin }}" target="_blank">LinkedIn</a>
  </p>
</div>

---

## Education

**MSc Visual Computing**
Saarland University, Germany
*Current*

---

## Research Interests

- Systems-aware efficient training and inference for deep learning
- Model Compression (Sparsity, Pruning, Quantization, Knowledge Distillation)
- Communication efficiency in distributed and federated learning
- Interpretability, fairness, and privacy in ML systems

---

## Experience

*Add your experience here...*

---

## Publications

{% for pub in site.data.publications limit: 3 %}
- **{{ pub.title }}**
  {{ pub.authors | join: ", " }}
  {% if pub.description %}*{{ pub.description }}*{% endif %}{% if pub.year %}, {{ pub.year }}{% endif %}
{% endfor %}

[View all publications &rarr;](/publications/)

---

## Projects

{% for project in site.data.projects limit: 3 %}
- **{{ project.title }}** - {{ project.description | truncate: 100 }}
{% endfor %}

[View all projects &rarr;](/projects/)

---

## Skills

- **Languages**: Python, C++, CUDA
- **Frameworks**: PyTorch, TensorFlow, JAX
- **Tools**: Git, Docker, Linux

---

<div class="cv-download">
  <a href="/assets/cv.pdf" class="btn btn-primary" target="_blank">
    Download PDF Version
  </a>
</div>

<style>
.cv-header {
  text-align: center;
  margin-bottom: 2rem;
}

.cv-header h2 {
  margin-bottom: 0.25rem;
}

.cv-subtitle {
  font-size: 1.125rem;
  color: var(--text-muted, #718096);
  margin-bottom: 0.5rem;
}

.cv-contact {
  font-size: 0.875rem;
}

.cv-contact a {
  color: var(--primary, #5b9cad);
}

.cv-download {
  text-align: center;
  margin-top: 3rem;
  padding-top: 2rem;
  border-top: 1px solid var(--border-color, #e2e8f0);
}
</style>
