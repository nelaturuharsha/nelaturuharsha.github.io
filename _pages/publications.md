---
title: Publications
layout: default
permalink: /publications/
published: true
order: 3
profile:
  align: right
  image: profile.png
---

## Publications
{% for publication in site.data.publications %}
{% if publication.url %}
<b><a href="{{ publication.url }}">{{ publication.title }}</a></b>{% 
else %}
<em>{{ publication.title }}</em>{% 
endif %}

{% for author in publication.authors %}{% 
if author == site.title %}<b>{{ author }}</b>{% else %}{{ author }}{% endif %}{% 
if forloop.last == false %}, {% endif %}{% endfor %}.

{% if publication.description %}
{{ publication.description }}{% endif %}{%
if publication.year %}, {{ publication.year }}{% endif %}.
<hr>
{% endfor %}