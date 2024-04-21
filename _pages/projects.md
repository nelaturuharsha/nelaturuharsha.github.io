---
title: Projects
layout: default
permalink: /projects/
published: true
order: 2
profile:
  align: right
  image: profile.png
---

## Projects

---


<div id="newstable" style="
/* padding-left: 0.7em; padding-right: 0.7em; padding-top: 0.7em; padding-bottom: 0.7em; */
border: none;
">
<table style="width:100%">

<col width="23%">
<col width="2%">
<col width="75%">


{% for project in site.data.projects %}

<tr><td><em>{% if project.url %}
<a href="{{ project.url }}">{{ project.title }}</a>
{% else %}
{{ project.title }}
{% endif %}</em></td>
<td></td>
<td>{{ project.description }}</td></tr>
{%- if forloop.last == false -%}
<tr><td colspan="3"><hr></td></tr>
{%- endif -%}
{%- endfor -%}
</table>
</div>

<br>

## Talks
---

<ul>
{% for talk in site.data.talks %}

<li><div style="display: flex; gap: 10px; margin-block-start: 2em; margin-block-end: 2em; align-items: center;
">
{% if talk.url %}<a href="{{ talk.url }}">{{ talk.title }}</a>{% else %}{{ talk.title }}{% endif %}
  {% if talk.slides %}<a href="{{ talk.slides }}" target="_blank" class="button">Slides</a>{% endif %}
  {% if talk.video %}<a href="{{ talk.video }}" target="_blank" class="button">Video</a>{% endif %}
  {% if talk.code %}<a href="{{ talk.code }}" target="_blank" class="button">Code</a>{% endif %}
</div>
</li>

{% endfor %}
</ul>
