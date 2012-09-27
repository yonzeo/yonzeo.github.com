---
layout: nil
---
<html>
<head>
<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
<title>demo</title>
<style>
*{padding:0;margin:0;}
fieldset,img,html,body,iframe{border:0;}
table{border-collapse:collapse;border-spacing:0;}
li{list-style:none;}
h1,h2,h3,h4,h5,h6{font-weight:bold;font-size:100%;}
em,strong{font-weight:bold;font-style:normal;}
body,textarea,select,input{font-family:Microsoft YaHei,\5FAE\8F6F\96C5\9ED1,tahoma,arial,simsun,\5B8B\4F53;font-size:12px;color:#444;}
a{text-decoration:none;color:#888;}
a:hover{text-decoration:none;color:#7594B3;}

.clear:after{clear:both;display:block;visibility:hidden;height:0;overflow:hidden;content:".";}
.clear{zoom:1;}

.arr,.arr span,.page a{background:url(/images/life/abg.png) no-repeat 999px 999px;}
.img{background:url(http://www.niumowang.org/demo/infinite/images/imgbg.png) no-repeat 999px 999px;}

.list li,.block{box-shadow:0 2px 3px -2px rgba(0,0,0,0.3);-webkit-box-shadow:0 2px 3px -2px rgba(0,0,0,0.3);-moz-box-shadow:0 2px 3px -2px rgba(0,0,0,0.3);-o-box-shadow:0 2px 3px -2px rgba(0,0,0,0.3);*border:1px solid #ededed;*border-width:0 1px 1px;*border-bottom-color:#e0e0e0;}
.list li:hover{box-shadow:0 2px 3px -2px rgba(0,0,0,0.6);-webkit-box-shadow:0 2px 3px -2px rgba(0,0,0,0.6);-moz-box-shadow:0 2px 3px -2px rgba(0,0,0,0.6);-o-box-shadow:0 2px 3px -2px rgba(0,0,0,0.6);}

.body{margin:0 0 0 218px;padding:30px 0 0;}

.list{overflow:hidden;zoom:1;}
.list ul{margin:-21px 0 0 -21px;padding:1px 2px 3px;position:relative;}
.list li,.link{float:left;width:230px;overflow:hidden;}
.list .post{width:230px;margin:21px 0 0 21px;float: left;}
.link{position:relative;display:block;background:#fff;cursor:pointer;}
.img{display:block;position:relative;width:100%;overflow:hidden;cursor:pointer;}
.img img{display:block;width:100%;}
.arr{position:absolute;top:0;left:0;width:100%;height:100%;background-position:999px 999px;}
.arr span{position:absolute;right:18px;bottom:0;width:16px;height:8px;overflow:hidden;background-position:0 0;cursor:pointer;}
.text{display:block;width:200px;overflow:hidden;margin:15px auto 10px;line-height:21px;color:#aaa;cursor:pointer;word-wrap:break-word;word-break:break-all;}
.text strong,.text em{display:block;font-weight:normal;}
.text em img{width:115%;}
.text strong{margin:0 0 4px;color:#606060;}
.link:hover .text strong{color:#333;}
.link:hover .text em{color:#999}
</style>
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
