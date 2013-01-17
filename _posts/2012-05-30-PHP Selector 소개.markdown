---
comments: true
date: 2012-05-30 09:54:21
layout: post
permalink: /archives/907
title: PHP Selector 소개
tags:
- php
- 도움스킬
---

[PHP Selector](https://github.com/visionmedia/php-selector) 풍기는 이름에서도 대충 어떤일을 하는 라이브러인지 짐작이 가능할것 같다.





PHP로 html문서를 파싱할때 CSS Selector문법으로 쉽게 요소를 가져올수 있게 도와준다. (PHP DOM parser / queries with CSS selectors)





자주쓰던 php용 라이브러리 [PHP Simple HTML DOM Parser](http://simplehtmldom.sourceforge.net/) 보다 더 심플하다.




    
    include "selector.inc";
    $dom = new SelectorDOM($html);
    $links = $dom->select('a');
    $list_links = $dom->select('ul li a');
    





한글이 있을경우 깨질때는 html 스트링 맨처음에 아래 코드를 넣어주면 해결된다;




    
    <meta http-equiv="content-type" content="text/html; charset=utf-8">
    





[타임라인](http://uix.kr/archives/893) 프로토타이핑 할때 [사용한 소스](https://github.com/niceaji7/niceaji7.github.com/blob/master/ex/issue-timeline-parse.php)를 참고.



