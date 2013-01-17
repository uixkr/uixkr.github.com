---
comments: true
date: 2012-02-14 22:53:09
layout: post
permalink: /service/bgfinder
title: background-image 쉽게 찾기 – BG Finder
categories:
- 서비스
---

디자이너가 백그라운드 이미지명을 쉽게 찾지 못하는걸 보고 간단하게 만들어본 북마클릿입니다.
찾고자 하는 bg가 있는 웹페이지에서 북마클릿을 실행하고 원하는곳에 클릭하면 bg이미지 명이 나옵니다(상위 엘리먼트의 bg까지~)

북마클릿 등록 : <a href='javascript:s=document.createElement("script");s.setAttribute("type","text/javascript");s.setAttribute("charset","utf-8");s.setAttribute("src","https://raw.github.com/uixkr/bg-finder/master/bg-finder.js");document.getElementsByTagName("head").item(0).appendChild(s);void(0)'>BG Finder</a>

![](http://cfile3.uf.tistory.com/image/181D091B49DAD9FB5CB9A0)

iframe 일경우 bg이미지명을 가져올수 없기에 새창으로 iframe url을 띄울수 있도록 했습니다

![](http://cfile22.uf.tistory.com/image/111C881B49DAD9FBAFC636)

만들어놓고 보니 파이어버그등으로 bg를 찾아보는것보다 편하네요 ^^
