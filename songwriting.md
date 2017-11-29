---
layout: page
permalink: /songwriting/
title: songwriting
description: songwriting is an inactive hobby. back to it someday! here are some old songs.
---

<ul class="post-list">
{% for song in site.songwriting reversed %}
    <li>
        <h2><a class="song-title" href="{{ song.url | prepend: site.baseurl }}">{{ song.title }}</a></h2>
        <p class="post-meta">{{ song.date | date: '%Y' }}</p>
      </li>
{% endfor %}
</ul>
