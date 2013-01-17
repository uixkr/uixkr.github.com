---
comments: true
date: 2012-02-27 20:50:12
layout: post
permalink: /archives/608
title: jQuery 이해2 - $(document).ready()
categories:
- jQuery
tags:
- DomContentLoaded
- jQuery
---

[ready()](http://api.jquery.com/ready/) 메소드는 DOM이 모두 로드된후에 실행될 함수를 지정한다.





웹문서에서 자바스크립트의 개발은 DOM을 조작하는 경우가 많은데 이때 DOM이 로드가 되기전에 자바스크립트를 작성할경우 예상치 못한 버그나 에러를 발생할수 있다. 그래서 DOM 로드가 완료된후에 자바스크립트 코드를 작성하는 방식을 권장하고 이럴경우 차후에 마크업과 코드와의 분리도 수월할수 있다.





![uix.kr](https://img.skitch.com/20120227-es3dm9gt7xfkf3w5aa9bj5cis4.jpg)





위 그림은 uix.kr이 로딩될때 네크워크 콘솔을 확인한 모습이다. 파란색 라인이 DomContentLoaded 가 발생한 시점인데 1.30초쯤에 발생한것을 확인할수 있다. onload 이벤트는 이미지를 포함한 모든 문서의 로딩이 끝난후에 발생하게 된다.





jQuery에서 DomContentLoaded 이벤트핸들러의 작성은 아래코드 처럼 가능하다.




    
    $(document).ready(function() {
        //이곳에 실행될 함수를 작성한다
    
    });
    
    //축약형
    $(function() {
        //이곳에 실행될 함수를 작성한다
    
    });
    



