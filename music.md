---
layout: page
title: Music
permalink: /music/
description: What I do the other half of my life.
---

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
