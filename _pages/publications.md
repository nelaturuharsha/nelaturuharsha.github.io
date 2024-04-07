---
title: Publications
layout: default
permalink: /publications/
published: true
order: 3
---

## Projects
---

{% for project in site.data.projects %}
{% if project.url %}

#### [{{ project.title }}]({{ project.url }})

{% else %}
#### {{ project.title }}
{% endif %}

* {{ project.description }}

{% if project.code %}

* Code: [{{ project.code }}]({{ project.code }})

{% endif %}

---
{% endfor %}

---
## Talks
---

{% for talk in site.data.talks %}
{% if talk.url %}

* [{{ talk.title }}]({{ talk.url }})

{% else %}

* {{ talk.title }}

{% endif %}
{% endfor %}
