---
layout: page
title: works
permalink: /works/
---

{% for works in site.works %}

{% if works.redirect %}
<div class="works">
    <div class="thumbnail">
        <a href="{{ works.redirect }}" target="_blank">
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
{% else %}

<div class="works ">
    <div class="thumbnail">
        <a href="{{ site.baseurl }}{{ works.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ works.img }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ works.title }}</h1>
            <br/>
            <p>{{ works.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
