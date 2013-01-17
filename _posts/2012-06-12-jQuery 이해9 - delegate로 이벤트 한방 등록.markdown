---
comments: true
date: 2012-06-12 15:55:06
layout: post
permalink: /archives/973
title: jQuery 이해9 - delegate로 이벤트 한방 등록
categories:
- jQuery
tags:
- jQuery
---

jQuery에는 이벤트등록을 할수 있는 흥미로운 방법이 존재한다.  

바로 [delegate()](http://api.jquery.com/delegate/)인데 1.7버전 이상부터는 [on()](http://api.jquery.com/on/)메소드를 권장하니 on()으로 살펴보자.  

소개되는 예제코드는 [예제페이지](http://api.jquery.com/on/)로 이동한후 개발자도구 콘솔을 열어서 실행하면 된다.





## delegate형태로 이벤트 등록




    
    $(document.body).on('click', 'div', function(event){
        console.log(event.target,   event.currentTarget);
    });
    





on()메소드의 두번째 인자가 div이다.  

해석해 보자면 **document.body에 click이벤트를 주고  document.body > div 만 감시**하겠다. 라는 의미
이런 delegate방식은 동적요소가 추가될경우 빛을 발한다!





## 동적요소 추가시 이벤트 등록




    
    $('#box').on('click', 'p', function(){
        $('#box').append("<p>나도 p태그, 클릭해보아요</p>");
    });
    





위의 코드로 새로 생기는 p태그에도 동일한 이벤트를 할당하게 된다.  

예제 [http://jsfiddle.net/niceaji/ea7v7/](http://jsfiddle.net/niceaji/ea7v7/)





delegate는 dom요소가 렌더링이 되기전에 이벤트 등록이 가능하고 이벤트 등록갯수를 줄이게 되어 결국 퍼포먼스 향상으로 이어질수 있다



