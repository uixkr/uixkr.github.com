---
comments: true
date: 2012-03-18 20:40:57
layout: post
permalink: /archives/776
title: Canvas를 이용한 TreeMap 인포그래픽
categories:
- javascript
- 기타
tags:
- canvas
- javascript
- TreeMap
- 기타
- 미디어다음
- 인포그래픽
---

[예전에 프로토타이핑](http://blog.uix.kr/19)을 해보며 봐왔던 [JavaScript InfoVis Toolkit](http://thejit.org/)에 [TreeMap](http://thejit.org/static/v20/Jit/Examples/Treemap/example1.html) 라이브러리를 사용하여 이번 19대총선 웹서비스에 SNS맵 인포그래픽을 선보였다.





![SNS맵](https://img.skitch.com/20120316-mtayrqtyq71uts6pk51f69xqki.medium.jpg)





라이브러리에서 HTML5의 Canvas를 사용하여 표현하고 지원하지 않는 IE8이하에서는 [excanvas](http://excanvas.sourceforge.net/)를 사용하여 렌더링을 하게된다.  

보통 포털처럼 여러종류의 사용자를  커버해야하는 서비스등에선 HTML5의 최신기술들을 사용하기가 꺼려지는게 사실이다. 낮은 버전의 브라우저에 대한 하위호환성을 유지하기가 쉽지만은 않기 때문이다.  그리고 이런 부담들은 대부분 프론트엔드개발자들의 몫이 될수 밖에 없다.





## API





라이브러리의 사용은 쉽다. [예제코드](http://thejit.org/static/v20/Jit/Examples/Treemap/example1.code.html)에서 보이는 json형태로 데이터를 구성하고 호출해주면 끝이다. 백엔드에서 받게되는 API를 똑같이 맞추긴 보다 **프론트엔드에서 라이브러리에서 원하는 형태로 다시 맞춰주는게  일이 보다 수월**해 진다.





[SNS맵 백엔드 API 보기](http://media.daum.net/2012g_election/proxy/v1/sns_map?interval=&limit=50&asof=&candidate=potential)





## IE9 문제





IE9에서는 Canvas로 렌더링함에도 Area에서 mouseover가 발생하지 않고 Area안 텍스트에서만 mouseover가 발생하였다 그래서 아쉽지만  IE8 문서모드로 고정하는걸로 문제를 해결했다




    
    <meta http-equiv="X-UA-Compatible" content="IE=8">
    





## 다른 TreeMap





많은 웹서비스에서 TreeMap 인포그래픽을 사용중이다.







  * [http://www.yonhapnews.co.kr/medialabs/tm/ ](http://www.yonhapnews.co.kr/medialabs/tm/)


  * [http://newsmap.jp/](http://newsmap.jp/)


  * [구글 TreeMap ChartTool](http://code.google.com/apis/chart/interactive/docs/gallery/treemap.html)


  * [http://oursignal.com/](http://oursignal.com/)



