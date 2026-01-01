---
title: Media
layout: page
permalink: /media/
description: Books, music, and movies I'm enjoying
---

{% assign media = site.data.media %}

What I'm currently reading, listening to, and watching.

---

## Books

<section class="shelf-section">
  <div class="bookshelf">
    <div class="shelf-row">
      {% for book in media.books %}
      <div class="book-item">
        <div class="book-cover-wrapper">
          <img src="{{ '/assets/images/media/' | append: book.image | relative_url }}"
               alt="{{ book.title }}"
               class="book-cover"
               loading="lazy">
        </div>
        <div class="book-info">
          <p class="book-title">{{ book.title }}</p>
          <p class="book-author">{{ book.author }}</p>
          {% if book.status %}
          <span class="book-status {{ book.status }}">
            {% if book.status == 'reading' %}Currently Reading
            {% elsif book.status == 'completed' %}Finished
            {% elsif book.status == 'want-to-read' %}Want to Read
            {% endif %}
          </span>
          {% endif %}
          {% if book.goodreads %}
          <div class="media-links">
            <a href="{{ book.goodreads }}" class="media-link" target="_blank" rel="noopener">
              Goodreads
            </a>
          </div>
          {% endif %}
        </div>
      </div>
      {% endfor %}
    </div>
    <div class="shelf-edge"></div>
  </div>
</section>

---

## Music

### Albums

<section class="shelf-section">
  <div class="vinyl-shelf">
    {% for album in media.music.albums %}
    <div class="vinyl-item">
      <div class="vinyl-record"></div>
      <div class="vinyl-sleeve">
        <img src="{{ '/assets/images/media/' | append: album.image | relative_url }}"
             alt="{{ album.title }}"
             loading="lazy">
      </div>
      <div class="vinyl-info">
        <p class="vinyl-title">{{ album.title }}</p>
        <p class="vinyl-artist">{{ album.artist }}</p>
        {% if album.spotify %}
        <div class="media-links">
          <a href="{{ album.spotify }}" class="media-link" target="_blank" rel="noopener">
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor" width="12" height="12">
              <path d="M12 0C5.4 0 0 5.4 0 12s5.4 12 12 12 12-5.4 12-12S18.66 0 12 0zm5.521 17.34c-.24.359-.66.48-1.021.24-2.82-1.74-6.36-2.101-10.561-1.141-.418.122-.779-.179-.899-.539-.12-.421.18-.78.54-.9 4.56-1.021 8.52-.6 11.64 1.32.42.18.479.659.301 1.02zm1.44-3.3c-.301.42-.841.6-1.262.3-3.239-1.98-8.159-2.58-11.939-1.38-.479.12-1.02-.12-1.14-.6-.12-.48.12-1.021.6-1.141C9.6 9.9 15 10.561 18.72 12.84c.361.181.54.78.241 1.2zm.12-3.36C15.24 8.4 8.82 8.16 5.16 9.301c-.6.179-1.2-.181-1.38-.721-.18-.601.18-1.2.72-1.381 4.26-1.26 11.28-1.02 15.721 1.621.539.3.719 1.02.419 1.56-.299.421-1.02.599-1.559.3z"/>
            </svg>
            Spotify
          </a>
        </div>
        {% endif %}
      </div>
    </div>
    {% endfor %}
  </div>
</section>

### Songs

<section class="shelf-section">
  <div class="songs-list">
    {% for song in media.music.songs %}
    <div class="song-item">
      <img src="{{ '/assets/images/media/' | append: song.image | relative_url }}"
           alt="{{ song.title }}"
           class="song-cover"
           loading="lazy">
      <div class="song-info">
        <p class="song-title">{{ song.title }}</p>
        <p class="song-artist">{{ song.artist }}</p>
      </div>
      {% if song.spotify %}
      <a href="{{ song.spotify }}" class="song-link" target="_blank" rel="noopener" title="Listen on Spotify">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="currentColor">
          <path d="M12 0C5.4 0 0 5.4 0 12s5.4 12 12 12 12-5.4 12-12S18.66 0 12 0zm5.521 17.34c-.24.359-.66.48-1.021.24-2.82-1.74-6.36-2.101-10.561-1.141-.418.122-.779-.179-.899-.539-.12-.421.18-.78.54-.9 4.56-1.021 8.52-.6 11.64 1.32.42.18.479.659.301 1.02zm1.44-3.3c-.301.42-.841.6-1.262.3-3.239-1.98-8.159-2.58-11.939-1.38-.479.12-1.02-.12-1.14-.6-.12-.48.12-1.021.6-1.141C9.6 9.9 15 10.561 18.72 12.84c.361.181.54.78.241 1.2zm.12-3.36C15.24 8.4 8.82 8.16 5.16 9.301c-.6.179-1.2-.181-1.38-.721-.18-.601.18-1.2.72-1.381 4.26-1.26 11.28-1.02 15.721 1.621.539.3.719 1.02.419 1.56-.299.421-1.02.599-1.559.3z"/>
        </svg>
      </a>
      {% endif %}
    </div>
    {% endfor %}
  </div>
</section>

---

## Movies

<section class="shelf-section">
  <div class="movie-wall">
    {% for movie in media.movies %}
    <div class="movie-item">
      <img src="{{ '/assets/images/media/' | append: movie.image | relative_url }}"
           alt="{{ movie.title }}"
           class="movie-poster"
           loading="lazy">
      <div class="movie-overlay">
        <p class="movie-title">{{ movie.title }}</p>
        <p class="movie-year">{{ movie.year }}</p>
        {% if movie.rating %}
        <div class="movie-rating">
          {% for i in (1..5) %}
            {% if i <= movie.rating %}
            <span class="star">&#9733;</span>
            {% else %}
            <span class="star star-empty">&#9733;</span>
            {% endif %}
          {% endfor %}
        </div>
        {% endif %}
        {% if movie.letterboxd %}
        <div class="media-links" style="margin-top: 0.5rem;">
          <a href="{{ movie.letterboxd }}" class="media-link" target="_blank" rel="noopener" style="background: rgba(255,255,255,0.2); color: white;">
            Letterboxd
          </a>
        </div>
        {% endif %}
      </div>
    </div>
    {% endfor %}
  </div>
</section>
