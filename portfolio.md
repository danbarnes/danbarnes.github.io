---
layout: page
title: Photo galleries
permalink: /portfolio/
---

<h4>Hover to see a description.</h4><br>

{% for project in site.portfolio %}

{% if project.redirect %}

<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <h2> 
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% else %}

<div class="project">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ project.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ project.title }}</h1>
            <br/>
            <p>{{ project.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
