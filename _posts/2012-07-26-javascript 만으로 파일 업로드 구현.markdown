---
comments: true
date: 2012-07-26 13:01:54
layout: post
permalink: /archives/1126
title: javascript 만으로 파일 업로드 구현
tags:
- api
- html5
- 도움스킬
---

[이전에 봤던](http://uix.kr/archives/1076) imgur.com API 를 이용해서 javascript 만으로 직접 업로드를 구현해보자





![](https://img.skitch.com/20120726-mn56y46imerfakgd4xrin2pcsj.jpg)
[http://www.uix.kr/drag-uploader/](http://www.uix.kr/drag-uploader/)





[html5 file API](http://www.html5rocks.com/en/tutorials/dnd/basics/)를 이용해서 간단하게 가능한데 [소스](https://github.com/uixkr/drag-uploader/blob/gh-pages/index.html)를 보면 쉽게 이해 가능하다.







  1. 이미지를 브라우저에 드래그앤 드랍으로 떨구면


  2. file API로 이미지를 읽고 


  3. imgur.com에 base64방식으로 업로드 ~



