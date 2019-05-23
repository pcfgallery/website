---
title: "Categories"
layout: default
permalink: "/categories"
---
<br/>
<section class="mt-4 mb-5">    
<div class="container-fluid">
    <div class="card-columns" style="margin-bottom: -90px !important;">
	{% assign sorted_cats = site.categories | sort %}
    {% for category in sorted_cats %}
	</div>     
	<section id="{{ category[0] | downcase }}" style="padding-top: 90px;"></section>
    <h3 class="mt-4 display-4"><small class="text-muted">#</small> {{ category[0] }}</h3><hr>
    
    <div class="card-columns">

        {% assign pages_list = category[1] | sort %}
        {% for post in pages_list %}
          {% if post.title != null %}
              {% if group == null or group == post.group %}
                {% include card-post.html %}
              {% endif %}
          {% endif %}
        {% endfor %}
        {% assign pages_list = nil %}
        {% assign group = nil %}

    {% endfor %}
    </div>
</div>
    
</section>
