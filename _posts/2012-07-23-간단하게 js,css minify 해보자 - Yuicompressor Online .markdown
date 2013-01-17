---
comments: true
date: 2012-07-23 18:31:17
layout: post
permalink: /archives/1101
title: '간단하게 js,css minify 해보자 - Yuicompressor Online '
categories:
- 서비스
tags:
- 서비스
- 클라우드
---

js,css 를 실제 서비스에 배포할때는 압축(minify)를 하게 된다.  

미디어다음 js - [http://s1.daumcdn.net/photo-media/static/media/3.3.2.3/dist/news.commons.min.js](http://s1.daumcdn.net/photo-media/static/media/3.3.2.3/dist/news.commons.min.js)  

minify 하게되면 지역변수가 짧아지고 공백과 주석이 제거되어 성능향상(용량)과 소스보안에도 도움이 될수 있다.





이때 주로 [Yuicompressor](http://developer.yahoo.com/yui/compressor/) 가 사용되어지는데 매번 그 환경을 구성하기가 번거롭다.  

그래서 간단하게 **js파일을 업로드하면 압축된 js소스를 뱉어주는 서비스**를 만들어 보았다.





![](https://img.skitch.com/20120720-e7tdhkgaxha9bypxycsb7agk48.jpg)  

[http://yuionline.herokuapp.com/](http://yuionline.herokuapp.com/)







  * [heroku](http://www.heroku.com/)에 올려보았다. 나중에 정리예정


  * 참고 - [heroku nodejs](https://devcenter.heroku.com/articles/nodejs), [H14 에러](https://devcenter.heroku.com/articles/error-codes#h14__no_web_processes_running)


  * 이미 비슷한 [서비스](http://refresh-sf.com/yui/)도 존재



