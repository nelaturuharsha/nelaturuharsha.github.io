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

<div id="newstable" style="
/* padding-left: 0.7em; padding-right: 0.7em; padding-top: 0.7em; padding-bottom: 0.7em; */
border: none;
"><table style="width:100%"><col width="100%">
{% for publication in site.data.publications %}<tr><td><p>
{% if publication.url %}
<em><a href="{{ publication.url }}">{{ publication.title }}</a></em>{% 
else %}
<em>{{ publication.title }}</em>{% 
endif %}
</p>

<p>
{% for author in publication.authors %}{% 
if author == site.title %}<i>{{ author }}</i>{% else %}{{ author }}{% endif %}{% 
if forloop.last == false %}, {% endif %}{% endfor %}.
</p>

<p>
{% if publication.description %}
{{ publication.description }}{% endif %}{%
if publication.year %}, {{ publication.year }}{% endif %}.

<!-- {% if forloop.last == false %}
<tr><td colspan="1"><hr></td></tr>
{% endif %} -->
</p>

{% endfor %}