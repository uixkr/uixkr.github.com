---
comments: true
date: 2012-09-08 10:02:50
layout: post
permalink: /archives/1150
title: jQuery - html문서 손쉽게 불러서 끼워넣기 .load()
categories:
- jQuery
tags:
- jQuery
---

a:[http://jsbin.com/orafim/1](http://jsbin.com/orafim/1)




    
    <script src="http://code.jquery.com/jquery-1.7.2.min.js"></script>
     <div id="result"></div>
    <script>
    $('#result').load("http://jsbin.com/alijey/3 #msg");
    </script>
    





b:[http://jsbin.com/alijey/3/](http://jsbin.com/alijey/3/)




    
     <h1>테스트</h1>
    <div id="msg">Hello World!!</div>
    





a문서의 #result에 b문서의 #msg부분을 불러서 넣는 간단한 예제



