---
title: Media
layout: default
permalink: /media/
published: true
order: 5
profile:
  align: right
  image: profile.png
---

{% assign media = site.data.media %}

## Books (Currently Reading)

{% for book in media.books %}

<div style="display: flex; align-items: center;">
  <img src="{{ site.baseurl }}/assets/images/media/{{ book.image }}" alt="{{ book.title }}" style="width: 60px; height: 60px; margin-right: 10px;">
  <p><i>{{ book.title }}</i> by {{ book.author }}</p>
</div>

{% endfor %}

---

## Music Recommendations

---

### Albums

{% for album in media.music.albums %}

<div style="display: flex; align-items: center;">
  <img src="{{ site.baseurl }}/assets/images/media/{{ album.image }}" alt="{{ album.title }}" style="width: 60px; height: 60px; margin-right: 10px;">
  <p><i>{{ album.title }}</i> by {{ album.artist }}</p>
</div>

{% endfor %}

### Songs

{% for song in media.music.songs %}

<div style="display: flex; align-items: center;">
  <img src="{{ site.baseurl }}/assets/images/media/{{ song.image }}" alt="{{ song.title }}" style="width: 60px; height: 60px; margin-right: 10px;">
  <p><i>{{ song.title }}</i> by {{ song.artist }}</p>
</div>

{% endfor %}

---

## Movies

---

{% for movie in media.movies %}

<div style="display: flex; align-items: center;">
  <img src="{{ site.baseurl }}/assets/images/media/{{ movie.image }}" alt="{{ movie.title }}" style="width: 60px; height: 60px; margin-right: 10px;">
  <p><i>{{ movie.title }}</i>, {{ movie.year }}</p>
</div>

{% endfor %}