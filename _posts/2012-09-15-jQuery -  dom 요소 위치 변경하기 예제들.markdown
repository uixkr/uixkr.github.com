---
comments: true
date: 2012-09-15 00:12:02
layout: post
permalink: /archives/1194
title: jQuery -  dom 요소 위치 변경하기 예제들
categories:
- jQuery
tags:
- jQuery
- manipulation
---



    <div id="menu">
      <p class="about">이곳은?</p>
      <p class="jquery">jQuery 맛보기</p>
      <p class="nodejs">node.js 맛보기</p>
      <p class="mongodb">mongo DB 맛보기</p>
    </div>





위와 같은 메뉴에서 `jquery`와 `mongodb`의 위치를 jQuery를 이용해서 바꿔보자.  

아래 실행되는 코드는 [이곳](http://jsbin.com/enuviq/11)에서 테스트 가능하다.





### 코드 1




    
    $('.jquery').clone().appendTo( $('#menu') );    
    $('.mongodb').replaceAll( $('.jquery').eq(0) );
    







  1. `.jquery`를 하나 더 만들어서 `#menu` 제일 하단에 넣는다


  2. `.mongodb`로 첫번째 `.jquery`를 대체





### 코드 2




    
    $('.jquery').replaceWith( $('.mongodb') ).appendTo( $('#menu') );
    







  1. `.jquery`를 `.mongodb` 로 대체하고 바로  `#menu` 하단에 넣는다





### 코드 3




    
    $('.mongodb').after( $('.jquery') );
    $('.about').after( $('.mongodb') );
    







  1. `.mongodb`뒤에 `.jquery` 두고


  2. `.about` 뒤에 `.mongodb`





### 코드 4




    
    $('.mongodb').after( $('.jquery') ).insertAfter( $('.about') );
    







  1. `.mongodb`뒤에 `.jquery` 두고, 바로 `.about` 뒤에 두기





  * replaceAll(), replaceWith()


  * after(), insertAfter()


  * append(), appendTo() 





누가 selector이고 target인지만 잘 구별 할수 있으면 될듯.. 머리 아픔



