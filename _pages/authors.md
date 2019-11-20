---
title: "Authors"
layout: default
permalink: "/authors"
---
<br/>
<section class="mt-4 mb-5">    
    <div class="container-fluid">
        <div class="card-columns" style="margin-bottom: -90px !important;">
        </div>
        {% assign authors = site.data.authors| sort %}
        {% for author in authors %}
            {% assign pages_list = site.posts | where: "authors", author[0] | sort %}
    	    {% assign psize = pages_list | size %}
    	    {% if psize != 0 %}
    	        <section id="{{ author[0] | downcase }}" style="padding-top: 90px;"></section>	
                <h3 class="mt-4 display-4">
                    {{ author[1].name }}
					{% if author[1].twitter %}&nbsp;&nbsp;<a target="_blank" href="https://www.twitter.com/{{author[1].twitter}}"><i class="fa fa-twitter"></i></a>{% endif %}
					{% if author[1].linkedin %}&nbsp;&nbsp;<a target="_blank" href="https://www.linkedin.com/in/{{author[1].linkedin}}/"><i class="fa fa-linkedin"></i></a>{% endif %}
			                {% if author[1].linkedin_company %}&nbsp;&nbsp;<a target="_blank" href="https://www.linkedin.com/company/{{author[1].linkedin_company}}/"><i class="fa fa-linkedin"></i></a>{% endif %}
					{% if author[1].github %}&nbsp;&nbsp;<a target="_blank" href="https://github.com/{{author[1].github}}"><i class="fa fa-github"></i></a>{% endif %}
					{% if author[1].website %}&nbsp;&nbsp;<a target="_blank" href="{{author[1].website}}"><i class="fa fa-rss"></i></a>{% endif %}
	            </h3>
	            <hr>
                <div class="card-columns">
                    {% for post in pages_list %}
                        {% if post.title != null %}
                            {% if group == null or group == post.group %}
                                {% include card-post.html %}
                            {% endif %}
                        {% endif %}
                    {% endfor %}
                    {% assign pages_list = nil %}
                    {% assign group = nil %}
                </div>
            {% endif %}
        {% endfor %}
    </div>
</section>
