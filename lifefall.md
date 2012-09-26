---
layout: page
title: Life
---
<div class="lifefall">
    <ul id="lifecontent">
    {% for life in site.categories.life %}
	{% if life.type == 'article' %}
        	<li class="article post" >
                	<a href="{{ life.url }}" class="link">
			    <span class="text">
				<strong>{{ life.title }}</strong>
				<em>{{ life.description }}</em>
			    </span>
			</a>
            	</li>
	{% else %}
		<li class="photo post">
			<a href="{{ life.url }}" class="link">
			    <span class="img">
				<img src="/images/life/{{ life.type.image }}">
				<span class="arr"><span></span></span>
				<span class="text">
				    <em>{{ life.description  }}</em>
				</span>
			    </span>
			</a>
		</li>    
	{% endif %}
    {% endfor %}
    </ul>
</div>
<script type="text/javascript">

	YONZEO.includeScript('/js/jquery.masonry.min..js',function(){});
	$(document).ready(function(){
   	    $('#lifecontent').masonry({
    		itemSelector : '.post',
    		columnWidth : 251
  	    });
	});
</script>
