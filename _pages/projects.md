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

{% for talk in site.data.talks %}
{% if talk.url %}

* [{{ talk.title }}]({{ talk.url }})

{% else %}

* {{ talk.title }}

{% endif %}
{% endfor %}
