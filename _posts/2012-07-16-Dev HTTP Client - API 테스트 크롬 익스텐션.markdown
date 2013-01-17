---
comments: true
date: 2012-07-16 19:27:53
layout: post
permalink: /archives/1068
title: Dev HTTP Client - API 테스트 크롬 익스텐션
categories:
- 기타
tags:
- api
- 기타
- 크롬확장
---

[curl로 api 테스트하는 방법](http://uix.kr/archives/1059)을 살펴보았다  

GUI로 할수 있는 방법도 매우 많은데 그중에 크롬익스텐션으로 나온 [Dev HTTP Client ](https://chrome.google.com/webstore/detail/aejoelaoggembcahagimdiliamlcdmfm)를 소개한다.





![null](https://lh6.googleusercontent.com/8uPPttvzhJfqY17NDuhfLKZzFva8ZOFf5Rdrl9PVpoYcUGSVZYSVR1Kvpjb3VZHX--FdgdXZ_A=s640-h400-e365)





사용법은 간단하다. 크롬웹스토어에서 [다운로드](https://chrome.google.com/webstore/detail/aejoelaoggembcahagimdiliamlcdmfm) 받아 실행하고  

api url를 적고 post,get 처럼 http method를 선택후에  'send'버튼을 누르면 응답이 아래에 펼쳐지게 된다.  

**post 일경우엔  body부분에 파라미터 스트링을 적어주고 header에 Content-Type:application/x-www-form-urlencoded**를 빼먹지 말자.



