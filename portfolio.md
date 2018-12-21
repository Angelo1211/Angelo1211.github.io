---
layout: page
title: Portfolio
permalink: /portfolio/
description: Selected projects covering my work in Graphics Programming, Aerospace and Machine Learning.
---
<!-- 
{% for project in site.portfolio %}
{% if project.cat == "resume" %}
<p><a href="{{ site.baseurl }}{{ project.url }}"><b>resume</b></a> : cumulative list of work experience, skills, and education.</p>
{% endif %}
{% endfor %} 
--> 
---
<br/>
{% for project in site.portfolio %}
{% if project.redirect %}
<div class="project">
    <div class="thumbnail">
        <a href="{{ project.redirect }}" target="_blank">
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

<div class="project ">
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

