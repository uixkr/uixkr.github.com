---
comments: true
date: 2012-06-13 16:28:21
layout: post
permalink: /archives/998
title: jQuery 팁1 - jQuery.when()
categories:
- jQuery
tags:
- jQuery
---

js애플리케이션 개발시에 다수의 api 들을 비동기로 호출하는 일이 빈번하다.  

이때  A라는 api에서 B라는 api데이터를 참조해야할때 'A api' callback에서 'B api' 를 호출 하기도 하는데 ..  

[jQuery.when()](http://api.jquery.com/jQuery.when/)은 이때 사용하면 좋은 메소드이다.




    
    function showData(data1, data2) {
        $('#debug').html( data1[0].max_id  +":"+ data2[0].max_id );
    }
    
    function method1() {
        return $.ajax("http://search.twitter.com/search.json", {
            data: {
                q: 'niceaji'
            },
            dataType: 'jsonp'
        });
    }
    
    function method2() {
        return $.ajax("http://search.twitter.com/search.json", {
            data: {
                q: 'niceaji'
            },
            dataType: 'jsonp'
        });
    }
    
    $.when(method1(), method2()).then(showData);​
    





직접 [작동예제](http://jsfiddle.net/niceaji/T7cw2/)를 보면 이해가 쉽다.



