---
comments: true
date: 2012-03-04 13:13:24
layout: post
permalink: /archives/713
title: mongoDB 5 - _id Field
categories:
- mongoDB
tags:
- mongoDB
---

우선 몽고쉘로 접속하여 아래와 같이 testdb 에서 comments에 하나의 row를 추가해서 find() 해보자





![몽고쉘예제](https://img.skitch.com/20120304-f4g1h9a2rttm7w3tsdk4iiugfq.jpg)





방금 추가한 desc필드외에 _id 필드가 보인다.





## _id필드는 Document의 고유한 key





위 쉘에서 한번 더 똑같은 Document를 넣어보자.




    
    db.comments.save({desc:'my comment!'})
    db.comments.find();
    





여기서 또다른 고유한 _id필드가 생성된것을 볼수 있다.





## _id필드 직접 넣어주기





Collections에 Document를 추가할때 _id필드를 생략하면 자동으로 유니크한 문자열로 생성이 되지만 직접 넣어줄수도 있다




    
    db.comments.save({_id:1,desc:"desc 1"})
    db.comments.save({_id:1,desc:"desc 2"}) // _id=1 인값이 update 된다
    





## 도움글





[mongoDB Object IDs](http://www.mongodb.org/display/DOCS/Object+IDs)



