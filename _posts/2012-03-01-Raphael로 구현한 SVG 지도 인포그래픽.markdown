---
comments: true
date: 2012-03-01 14:39:12
layout: post
permalink: /archives/661
title: Raphael로 구현한 SVG 지도 인포그래픽
categories:
- 기타
tags:
- html5
- raphael
- svg
- 기타
- 미디어다음
- 인포그래픽
---

이번에 [19대 총선 서비스](http://media.daum.net/2012g_election/)를 오픈하면서 역대 선거구별 당선현황을 지도 인포그래픽으로 구현해 보았다.





![지도 인포그래픽](https://img.skitch.com/20120301-rw4dswk65jajnktx4p1m2c592u.jpg)





지도는 [Raphael 자바스크립트 라이브러리](http://raphaeljs.com/)를 사용해서 그려졌는데  [SVG](http://ko.wikipedia.org/wiki/SVG)와 [VML](http://www.w3.org/TR/NOTE-VML) 중 브라우저에서 지원하는 방식으로 표현을 한다. 보통 지도에 인터랙티브 UI를 구현할때 플래시를 자주 사용하게 되는데  HTML5 이슈 등으로 이 방식을 선택했다.





주요 PC브라우저와 iOS는 커버했지만 아쉽게도 안드로이드에서는 SVG를 지원하지 않기에 보이지 않는다





## 지도 Path





지도 Path는 사내에서 사용중인 데이터를 그대로 SVG로 익스포트 하였기에 디자이너의 수작업은 필요치 않았다. 그 내려진 SVG를 다시 JSON형태로 변환하여 사용을 한다. 아래는 18대 서울지도(위 이미지)의 Path와 선거구포인트,명의 JSON이다





[http://s1.daumcdn.net/photo-media/static/2012g_election/path/109/map18-11.js](http://s1.daumcdn.net/photo-media/static/2012g_election/path/109/map18-11.js)





## Raphael 라이브러리





### path 그리기





Raphael 로 그리는건 간단하다. 위 JSON 에서 보이는 path 프로퍼티를 그대로 넣어주면 된다




    
    var paper = Raphael(0, 0, 500, 500);
    paper.path( path ).attr("fill", "#eee");
    





정당별 컬러값을 채우기 위해 [attr()](http://raphaeljs.com/reference.html#Element.attr) 메소드를 사용하여 폴리곤에 색상을 채우게 된다.





### 선거구명 표시





텍스트(선거구명)를 추가 할경우  [text()](http://raphaeljs.com/reference.html#Paper.text) 메소드를 사용하면 낮은버전 ie 에서 폰트가 제대로 표시가 안되기에 html에서 직접 올려서 표시했다.




    
    Raphael.fn.hangulText = function(x, t, text, style) {
        var wrap = daum.getParent(this.canvas);
        var div = daum.createElement('<div style="position:absolute;">' + text + "</div>");
        wrap.appendChild(div);
        daum.setLeft(div, x - (div.offsetWidth / 2));
        daum.setTop(div, y - (div.offsetHeight / 2));
        if (style) {
                daum.setStyle(div, style)
        }
        return this.set()
    };
    





## 정리





지도 인포그래픽은 어떻게 구현하든 조율이 많이 필요한 작업이다. 장점을 따져보자면







  * 액션스크립트 지식없이 자바스크립트로 가능


  * 플래시 없이 인터랙티브 지도  가능 (요새 악의축이 되어버린듯한;)


  * iOS 에서 지도 표시





물론 플래시 보다 단점도 존재한다







  * 폴리건에 mouseover 시에 지역명에 가면  mouseout 발생. 툴팁 유지하기가 힘들다


  * 디자이너가 직접 path와 포인트들을 다듬기엔 불편할수 있다


  * 플래시보다 피곤하다;(폰트, 마우스오버이슈 등)





## 관련글







  * [다음, 4월 총선특집 페이지 개설](http://media.daum.net/v/20120305095119693)



