---
layout: page
title: Life
---
<style>
.list li:hover{box-shadow:0 2px 3px -2px rgba(0,0,0,0.6);-webkit-box-shadow:0 2px 3px -2px rgba(0,0,0,0.6);-moz-box-shadow:0 2px 3px -2px rgba(0,0,0,0.6);-o-box-shadow:0 2px 3px -2px rgba(0,0,0,0.6);}
.list{overflow:hidden;zoom:1;}
.list ul{margin:-21px 0 0 -21px;padding:1px 2px 3px;position:relative;}
.list li,.link{float:left;width:230px;overflow:hidden;}
.list .post{width:230px;margin:21px 0 0 21px;float: left;}
.link{position:relative;display:block;background:#fff;cursor:pointer;}
.img{display:block;position:relative;width:100%;height:170px;overflow:hidden;cursor:pointer;}
.img img{display:block;width:115%;}
.arr{position:absolute;top:0;left:0;width:100%;height:100%;background-position:999px 999px;}
.arr span{position:absolute;right:18px;bottom:0;width:16px;height:8px;overflow:hidden;background-position:0 0;cursor:pointer;}
.text{display:block;width:200px;overflow:hidden;margin:15px auto 10px;line-height:21px;color:#aaa;cursor:pointer;word-wrap:break-word;word-break:break-all;}
.text strong,.text em{display:block;font-weight:normal;}
.text em img{width:115%;}
.text strong{margin:0 0 4px;color:#606060;}
.link:hover .text strong{color:#333;}
.link:hover .text em{color:#999}
<style>
<div class="lifefall">
    <ul id="lifecontent">
    {% for drip in site.categories.life %}
	{% if drip.driptype == 'article' %}
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
				<img src="/images/life/{{ drip.image }}">
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

	YONZEO.includeScript('/js/jquery.masonry.min.js',function(){});
	$(document).ready(function(){
   	    $('#lifecontent').masonry({
    		itemSelector : '.post',
    		columnWidth : 251
  	    });
	});
</script>
