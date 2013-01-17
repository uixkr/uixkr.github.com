---
comments: true
date: 2012-02-28 18:23:14
layout: post
permalink: /archives/642
title: jQuery 이해3 - Selectors 메소드들
categories:
- jQuery
tags:
- jQuery
- selector
---

웹개발에서 대부분의 자바스크립트의 작업이 [DOM](http://ko.wikipedia.org/wiki/%EB%AC%B8%EC%84%9C_%EA%B0%9D%EC%B2%B4_%EB%AA%A8%EB%8D%B8)을 조작하는 일로 이루어진다.





문서의 특정 태그엘리먼트에 접근하여 이벤트를 주거나 class명을 변경, 내용을 채워넣는(innerHTML)일등을 하기위해선 그 특정 태그엘리먼트를 쉽게 찾을수 있어야 하는데 이때 사용 되어지는게 [Selector](http://api.jquery.com/category/selectors/) 이다. jQuery에서 사용되는 [Sizzle CSS Selector Engine](http://sizzlejs.com/)은 현재 가장 빠른 속도를 자랑하기도 한다.





## 자주 사용하는 기본 셀렉터





### 태그 셀렉터




    
    $('div'); //모든 div 태그엘리먼트를 가지고 온다
    





### id  셀렉터




    
    $('#daum'); // id="daum" 엘리먼트를 가지고 온다
    





### class 셀렉터




    
    $('.bar'); // class="bar" 엘리먼트를 가지고 온다
    





### Multiple 셀렉터




    
    $('div','span','img'); //div ,span, img 엘리먼트 모두를 가지고 온다
    





중복 사용과 해당 엘리먼트 내부에서만 검색도 가능하다




    
    $('div.bar'); //div 태그엘리먼트중에 bar 클래스명을 사용하는 엘리먼트
    $('img' , '#content'); // id="content" 안에 img 태그 엘리먼트만 가져온다
    





이 외에 많은,유용한 셀렉터들이 존재하는데 꼭 하단에 '도움글'들을 참고하여 학습하도록 하자





## 도움글







  * [jQuery Selector API](http://api.jquery.com/category/selectors/)


  * [CSS3 Selectors](http://www.w3.org/TR/css3-selectors/)



