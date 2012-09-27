---
layout: page
---
<ul id="lxf-box">
    <li>
	<a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
	<h3></h3>
    </li>
    <li>
        <a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
        <h3></h3>
    </li>
    <li>
        <a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
        <h3></h3>
    </li>
    <li>
        <a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
        <h3></h3>
    </li>
    <li>
        <a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
        <h3></h3>
    </li>
<li>
        <a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
        <h3></h3>
    </li>
<li>
        <a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
        <h3></h3>
    </li>
<li>
        <a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
        <h3></h3>
    </li>
<li>
        <a href="#"><img src="http://www.liuxiaofan.com/demo/waterfall/OLqypfV.jpg"></a>
        <h3></h3>
    </li>
</ul>
<style type="text/css">
    body,ul,li,h3 { margin: 0px; padding: 0px; list-style: none; font-family:Microsoft YaHei,\5FAE\8F6F\96C5\9ED1,tahoma,arial,simsun,\5B8B\4F53;font-size:12px;color:#444;}
    #lxf-box { position: relative; }
    #lxf-box li { position: absolute; background: #fff; border: solid 1px #ccc; text-align: center; padding: 10px; left: 0px; top: 0px;}
    h3 { padding-top: 8px;}
    img { width: 200px; height: auto; display: block; border: 0}
    li { -webkit-transition: all .7s ease-out .1s; -moz-transition: all .7s ease-out; -o-transition: all .7s ease-out .1s; transition: all .7s ease-out .1s }
</style>
<script><!--
var margin = 10;
var li = $('li');
var li_W = li[0].offsetWidth + margin;
function liuxiaofan(){
    var h = [];
    var n = document.documentElement.offsetWidth / li_W | 0;
    for(var i = 0; i < li.length; i++ ){
	li_H = li[i].offsetHeight;
        if( i < n ) {
            h[i] = li_H;
            li.eq(i).css("top",0);
            li.eq(i).css("left",i * li_W);
        }else{
            min_H = Math.min.apply(null, h);
            minKey = getarraykey(h, min_H);
            h[minKey] += li_H + margin;
            li.eq(i).css("top", min_H + margin);
            li.eq(i).css("left", minKey * li_W);
        }
        $("h3").eq(i).text("num"+i+"height"+li_H);
    }
}

function getarraykey(s, v){
    for(k in s){
        if(s[k] == v){
            return k;
        }
    }
}
window.onload = function(){liuxiaofan();};
window.onresize = function(){liuxiaofan();}; -->
</script>
