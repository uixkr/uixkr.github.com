---
comments: true
date: 2012-02-29 17:15:57
layout: post
permalink: /archives/655
title: jQuery 이해5 - Attributes 메소드들
categories:
- jQuery
tags:
- jQuery
---

이번 시간에는 엘리먼트의 [Attribute 관련된 메소드](http://api.jquery.com/category/attributes/)들을 살펴보자





소개하는 메소드들은 [예제페이지](/ex/jquery/ex.html)로 이동한후 개발자도구 콘솔을 열어서 입력하면서 테스트 해보면 된다. 자 하나씩 따라해보자





## .addClass()





엘리먼트에 css클래스명을 추가할때 사용한다.




    
    $('#box').addClass('red');
    
    //모든 div엘리먼트에 border 클래스 추가
    $('div').addClass('border');
    





## .removeClass()





엘리먼트에 css클래스명을 제거 한다




    
    $('#box').removeClass('red');
    $('div').removeClass('border');
    





## .hasClass()





클래스명의 존재여부를 true,false 로 리턴한다




    
    if($('#box').hasClass('red')){
        $('#box').removeClass('red'); 
    }
    





## .toggleClass()





인자로 주어지는 클래스명이 toggle 된다





## .attr()





엘리먼트에 있는 어트리뷰트를 읽거나 세팅할때 사용된다.




    
    $('#box').attr('data','i am box');
    $('#box').attr('data'); //i am box 출력
    





## .removeAttr()





엘리먼트에 있는 어트리뷰트 제거




    
    $('#box').removeAttr('data'); 
    





## .html()





엘리먼트의 내용을 html형태로 가지고 오던가 세팅한다




    
    $('#box').html(); // id=box
    $('#box').html('hello box');  
    





## .prop()





엘리먼트의 프로퍼티에 직접 접근하여 값을 가져오거나 세팅한다




    
    $("input[type='checkbox']").attr("checked") // checked
    $("input[type='checkbox']").prop("checked") // true
    $("input").prop("disabled", true) // 폼요소를 사용하지 못하게 세팅
    $("input").prop({"disabled": false}) //인자를 object 형태로도 전달 가능
    





## .removeProp()





프로퍼티를 제거한다





## .val()





value어트리뷰트가 있는 엘리먼트에서 value값을 가져온다




    
    $('input[type=text]').val()
    





엘리먼트의 어트리뷰트와 프로퍼티의 차이점을 이해 해보고, 자주 사용하게 되는 메소드들이니 [API페이지](http://api.jquery.com/category/attributes/)에서 더 많은 예제를 보고 완벽히 학습하도록 하자!



