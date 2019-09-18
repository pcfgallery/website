---
title: "Controls made for Canvas Apps"
layout: default
permalink: "/canvas-controls"
---
<br/>
<section class="mt-4 mb-5">    
<div class="container-fluid">

    <div class="card-columns">        
        {% for post in site.posts %}
			{% if post.canvas_support == true %}
				{% include card-post.html %}
			{% endif %}
        {% endfor %}            
    </div>
	
	
</div>
    
</section>
