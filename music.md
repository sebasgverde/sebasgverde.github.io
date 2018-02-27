---
layout: page
title: music
permalink: /music/
description: What I do the other half of my life.
---

{% for project in site.music %}

{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
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

<div class="project ">
    <div class="thumbnail">
        <a href="{{ project.url | prepend: site.baseurl | prepend: site.url }}">
        {% if project.img %}
        <img class="thumbnail" src="{{ project.img | prepend: site.baseurl | prepend: site.url }}"/>
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

{% for mus in site.music %}

{% if mus.redirect %}
<div class="mus">
    <div class="thumbnail">
        <a href="{{ mus.redirect }}" target="_blank">
        {% if mus.img %}
        <img class="thumbnail" src="{{ mus.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox">
        {% endif %}    
        <span>
            <h1>{{ mus.title }}</h1>
            <br/>
            <p>{{ mus.description }}</p>
        </span>
        </div>
        </a>
    </div>
</div>
{% else %}

<div class="mus ">
    <div class="thumbnail">
        <a href="{{ mus.url | prepend: site.baseurl | prepend: site.url }}">
        {% if mus.img %}
        <img class="thumbnail" src="{{ mus.img | prepend: site.baseurl | prepend: site.url }}"/>
        {% else %}
        <div class="thumbnail blankbox"></div>
        {% endif %}    
        <span>
            <h1>{{ mus.title }}</h1>
            <br/>
            <p>{{ mus.description }}</p>
        </span>
        </a>
    </div>
</div>

{% endif %}

{% endfor %}
