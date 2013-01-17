---
comments: true
date: 2012-05-25 19:01:15
layout: post
permalink: /archives/886
title: jQuery cdn서비스 이용시 안전한 방법
categories:
- javascript
- jQuery
tags:
- cdn
- javascript
- jQuery
---

jQuery를 문서에 삽입할경우 [cdn서비스](https://www.google.co.kr/search?rlz=1C1CHFA_enKR484KR484&sugexp=chrome,mod=11&sourceid=chrome&ie=UTF-8&q=jquery+cdn)를 이용하면 편리하다.  

이때 만약 cdn서비스가 죽는다면 내 웹사이트는 어떻게 보장하지? 라는 물음이 들때 사용할수 있는 방법




    
    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.7.2/jquery.min.js"></script>
    <script>window.jQuery || document.write('<script src="/js/jquery-1.7.2.min.js"><\/script>')</script>
    



