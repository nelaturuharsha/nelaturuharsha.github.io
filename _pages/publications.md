---
title: Publications
layout: default
permalink: /publications/
published: true
order: 3
---

## Publications

{% for publication in site.data.publications %}
{% if publication.authors %}
<p>{{ publication.authors | join: ', ' }}.
{% endif %}
{% if publication.url %}
<em><a href="{{ publication.url }}">{{ publication.title }}</a></em>{% 
else %}
<em>{{ publication.title }}</em>{% 
endif %}{%
if publication.year %}, {{ publication.year }}{% endif %}.
{% if publication.description %}
{{ publication.description }}.
{% endif %}
<hr>
{% endfor %}