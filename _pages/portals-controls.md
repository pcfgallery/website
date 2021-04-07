---
title: "Controls made for Power Apps Portals"
layout: default
permalink: "/portals-controls"
---
<br/>
<section class="mt-4 mb-5">    
<div class="container-fluid">

    <div class="card-columns">        
        {% for post in site.posts %}
			{% if post.portals_support == true %}
				{% include card-post.html %}
			{% endif %}
        {% endfor %}            
    </div>
	
</div>
    
</section>
