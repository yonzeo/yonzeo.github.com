---
layout: nil
---
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<title>demo</title>
<link href="http://www.niumowang.org/demo/infinite/style.css" rel="stylesheet" type="text/css"/>
<script type="text/javascript" src="/js/jquery-1.7.1.min.js"> </script>
<script type="text/javascript" src="/js/jquery.masonry.min.js"> </script>
<script type="text/javascript">
        $(document).ready(function(){
            $('#lifecontent').masonry({
                itemSelector : '.post',
                columnWidth : 251
            });
        });
</script>
</head>
<body>
<!-- 内容 -->
<div class="body clear">
	<div class="list">

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
				<span class="arr"><span> </span> </span>
			    </span>
			    <span class="text">
                                <em>{{ drip.description  }}</em>
                            </span>
			</a>
		</li>    
	{% endif %}
    {% endfor %}
    </ul>
</div>
</div>
</body>
</html>
