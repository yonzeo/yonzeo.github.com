---
layout: nil
---
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<title>demo</title>
<link href="http://www.niumowang.org/demo/infinite/style.css" rel="stylesheet" type="text/css"/>
<script type="text/javascript" src="/js/jquery-1.7.1.min.js"></script>
<style type="text/css">
/* 背景色和背景图 */
body{background-color:#fff;background-image:url(http://www.niumowang.org/demo/infinite/images/bg.png);background-repeat:repeat;}
/* 侧栏：文字色和分割线颜色 */
.b1{border-color:#96999D;}
.c1,.c1 a{color:#96999D;}
/* 侧栏：文字色hover色 */
a.c1:hover,.c1 a:hover{color:#000;}
/* 侧栏：博客名称色和hover色 */
.c2,a.c2:hover{color:#444;}
</style>
</head>
<body>
<!-- 内容 -->
<div class="body">
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
</div>
    <script type="text/javascript">
        var YONZEO = {};
        YONZEO.includeScript = function(file,callback){
            var _doc = document.getElementsByTagName('head')[0];
            var js = document.createElement('script');
            js.setAttribute('type', 'text/javascript');
            js.setAttribute('src', file);
            _doc.appendChild(js);

            if (!/*@cc_on!@*/0) { //if not IE
                //Firefox2、Firefox3、Safari3.1+、Opera9.6+ support js.onload
                js.onload = function () {
                    callback();
                }
            } else {
                //IE6、IE7 support js.onreadystatechange
                js.onreadystatechange = function () {
                    if (js.readyState == 'loaded' || js.readyState == 'complete') {
                        callback();
                    }
                }
            }
            return false;
        }

	YONZEO.includeScript('/js/jquery.masonry.min.js',function(){});
	$(document).ready(function(){
   	    $('#lifecontent').masonry({
    		itemSelector : '.post',
    		columnWidth : 251
  	    });
	});
</script>
</body>
</html>
