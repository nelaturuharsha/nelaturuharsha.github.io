---
title: Publications
layout: default
permalink: /publications/
published: true
order: 3
---

## Publications
<p>
{% for publication in site.data.publications %}
{% for author in publication.authors %}{% 
if author == site.title %}<b>{{ author }}</b>{% else %}{{ author }}{% endif %}{% 
if forloop.last == false %}, {% endif %}{% endfor %}.
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