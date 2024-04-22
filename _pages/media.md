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

Media I'm currently consuming :)

## Books
---
{% for book in media.books %}

<div style="display: flex; align-items: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/media/{{ book.image }}" alt="{{ book.title }}" style="width: 80px; height: 100px; margin-right: 20px;">
  <p><span style="color: #FFD64D;">{{ book.title }}</span> by {{ book.author }}</p>
</div>

<hr> <!-- Horizontal rule between entries -->

{% endfor %}

<br>

## Music

---

### Albums

---

{% for album in media.music.albums %}

<div style="display: flex; align-items: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/media/{{ album.image }}" alt="{{ album.title }}" style="width: 80px; height: 100px; margin-right: 20px;">
  <p><span style="color: #FFD64D;">{{ album.title }}</span> by {{ album.artist }}</p>
</div>

<hr> <!-- Horizontal rule between entries -->

{% endfor %}

### Songs

---

{% for song in media.music.songs %}

<div style="display: flex; align-items: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/media/{{ song.image }}" alt="{{ song.title }}" style="width: 80px; height: 100px; margin-right: 20px;">
  <p><span style="color: #FFD64D;">{{ song.title }}</span> by {{ song.artist }}</p>
</div>

<hr> <!-- Horizontal rule between entries -->

{% endfor %}

<br>

## Movies

---

{% for movie in media.movies %}

<div style="display: flex; align-items: center; margin-bottom: 20px;">
  <img src="{{ site.baseurl }}/assets/images/media/{{ movie.image }}" alt="{{ movie.title }}" style="width: 80px; height: 100px; margin-right: 20px;">
  <p><span style="color: #FFD64D;">{{ movie.title }}</span>, {{ movie.year }}</p>
</div>

<hr> <!-- Horizontal rule between entries -->

{% endfor %}
