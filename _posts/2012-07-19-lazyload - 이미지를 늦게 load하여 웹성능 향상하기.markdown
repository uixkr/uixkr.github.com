---
comments: true
date: 2012-07-19 15:35:19
layout: post
permalink: /archives/1088
title: lazyload - 이미지를 늦게 load하여 웹성능 향상하기
categories:
- javascript
tags:
- javascript
- lazyload
- widget
- 도움스킬
---

요즘의 웹페이지에는 많은 이미지를 포함하게 된다.  

웹페이지 첫 로딩시에는 사용자의 브라우저 영역안의 이미지만 로드를 하고 스크롤될때 해당 영역의 이미지를 로드하면 성능이 좋아질수 있는데 이러한 방법을 lazyloading이라 한다.





실제 실무에서 사용하는 방법은 여러가지가 있을수 있는데 그중에 [lazyload](https://github.com/fasterize/lazyload)라는 간단한 js모듈을 소개 한다.




    
    <img
        data-src="real/image/src.jpg"
        src=data:image/gif;base64,R0lGODlhAQABAAAAACH5BAEKAAEALAAAAAABAAEAAAICTAEAOw==
        onload=lzld(this) onerror=lzld(this) />
    





[lazyload js](https://raw.github.com/fasterize/lazyload/master/lazyload.min.js)을 head에서 부르고 위처럼 img 태그를 구성하면 끝이다.  

실제 테스트는 [이곳](http://uix.kr/widget/lazyload.html)에서 해보자 ( 브라우저 창 높이를 작게 해서 보자 )





![](https://img.skitch.com/20120719-k2qnmyqigyr3f6i4daiwr9cdwm.jpg)





위의 그림을 보듯이  하단에서 불려지는 이미지는 아직 로딩전이고 스크롤을 내리면 로딩되는것을 확인할수 있다.



