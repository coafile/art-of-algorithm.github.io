---
layout: page
title: Languages
desc: Nuances of Languages
permalink: /languages/
order: 4
---

<div class="container index-container">
    <div class="row">
         <div class="col s6 in-progress-div">
            <div class="in-progress">IN PROGRESS</div>
            <div class="desc-menu">Work in progress on GitHub</div>
            <ul>
            {%  for post in site.posts %}
                {% if post.tag == "wip" %}
                {% if post.categories contains "languages" %}
                <li class="post-title-li"><a class="post-title" href="{{post.url | prepend:site.baseurl }}" > {{ post.title }}</a></li>
                {% endif %}
                {% endif %}
            {% endfor %}
            </ul>
        </div>
        
        <div class="col s6 complete-div">
            <ul>
            {%  for post in site.posts %}
                {% if post.tag != "wip" %}
                {% if post.categories contains "languages" %}
                <li class="post-title-li"><a class="post-title" href="{{post.url | prepend:site.baseurl }}" > {{ post.title }}</a></li>
                {% endif %}
                {% endif %}
            {% endfor %}
            </ul>
        </div>
        
    </div>
</div>