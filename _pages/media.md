---
title: Media Consumption
layout: default
permalink: /media-consumption/
published: true
order: 5
---

{% assign media = site.data.media %}

## Books (Currently Reading)

{% for book in media.books %}

- *{{ book.title }}* by {{ book.author }}

{% endfor %}

---

## Music Recommendations

---

### Albums

{% for album in media.music.albums %}

- *{{ album.title }}* by {{ album.artist }}

{% endfor %}

### Songs

{% for song in media.music.songs %}

- *{{ song.title }}* by {{ song.artist }}

{% endfor %}
