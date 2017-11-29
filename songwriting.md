---
layout: page
permalink: /songwriting/
title: songwriting
description: songwriting is an inactive hobby. back to it someday! here are some old songs that i wrote with my friend, <a href=http://www.braddunsemusic.com>brad dunse</a>.
---

<ul class="post-list">
{% for song in site.songwriting reversed %}
    <li>
        <h2><a class="song-title" href="{{ song.url | prepend: site.baseurl }}">{{ song.title }}</a></h2>
        <p class="post-meta">{{ song.date | date: '%Y' }}</p>
      </li>
{% endfor %}
</ul>
