---
comments: true
date: 2012-06-14 10:08:03
layout: post
permalink: /archives/1007
title: jQuery 팁2 - ajax로 폼값 쉽게 넘기기 serialize()
categories:
- jQuery
tags:
- jQuery
---

[serialize()](http://api.jquery.com/serialize/)는 form요소들의 값을 한번에 url parameter형식으로 변환  

ajax형태의 submit등에서 유용





html 코드




    
    <div id="debug"></div>
    <form id="wform">
        id : <input type="text" name="id" value="aji" > <br>
    
        sex :<input type="radio" name="sex" value="m" checked >
        <input type="radio" name="sex" value="f" > <br>
    
        <button type="submit">전송</button>
    </form>
    





​
js 코드




    
    $('#wform').submit(function(evemt){
    
        $('#debug').html( $('#wform').serialize() );
    
        //ajax 구현
    
    
        event.preventDefault();
    });
    





​
[동작예제](http://jsfiddle.net/niceaji/zFhQB/)를 참고



