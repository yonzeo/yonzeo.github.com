---
layout: page
title: Life
---
<div class="lifefall">
    <ul id="lifecontent">
    {% for drip in site.categories.life.post %}
	{% if drip.type == 'article' %}
        	<li class="article post" >
                	<a href="{{ drip.url }}" class="link">
			    <span class="text">
				<strong>{{ drip.title }}</strong>
				<em>{{ drip.description }}</em>
			    </span>
			</a>
            	</li>
	{% else %}
		<li class="photo post">
			<a href="{{ drip.url }}" class="link">
			    <span class="img">
				<img src="/images/life/{{ drip.type.image }}">
				<span class="arr"><span></span></span>
				<span class="text">
				    <em>{{ drip.description  }}</em>
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
