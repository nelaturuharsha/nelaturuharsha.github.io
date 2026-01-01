---
title: Publications
layout: page
permalink: /publications/
description: Academic publications and research papers
---

<div class="publications-list">
{% for pub in site.data.publications %}
<article class="publication">
  <h3 class="publication-title">
    {% if pub.url %}
    <a href="{{ pub.url }}" target="_blank" rel="noopener">{{ pub.title }}</a>
    {% else %}
    {{ pub.title }}
    {% endif %}
  </h3>

  <p class="publication-authors">
    {% for author in pub.authors %}{% if author == site.title %}<span class="author-self">{{ author }}</span>{% else %}{{ author }}{% endif %}{% if forloop.last == false %}, {% endif %}{% endfor %}
  </p>

  {% if pub.description %}
  <p class="publication-venue">{{ pub.description }}{% if pub.year %}, {{ pub.year }}{% endif %}</p>
  {% endif %}

  {% if pub.url %}
  <div class="publication-links">
    <a href="{{ pub.url }}" class="btn btn-sm btn-primary" target="_blank" rel="noopener">
      View Paper
    </a>
  </div>
  {% endif %}
</article>
{% endfor %}
</div>
