---
comments: true
date: 2012-02-27 22:17:27
layout: post
permalink: /archives/622
title: mongoDB 3 - mongod config  파일로 실행
categories:
- mongoDB
tags:
- mongoDB
- 터미널
---

## $PATH 설정





몽고db 데몬을 쉽게 올릴수 있게 어느 디렉토리든 mongod가 실행이 되게 설정해 보자 (mac같은 유닉스시스템 기준) 터미널에서 아래 명령을 실행한다




    
    > echo $PATH
    





위 명령으로 보이는 디렉토리 목록이 경로 지정 없이도 프로그램이 실행되는 디렉토리 모음이다. 이제 $PATH에  mongodb 설치경로를 지정해 보자.




    
    > vi ~/.profile
    





현재 계정의 .profile 파일을 vi 에디터로 열고 아래 내용을 한줄 추가한다




    
    export PATH=/Applications/mongodb/bin:$PATH
    





/Applications/mongodb/bin 이부분은 자기가 mongodb 를 둔 디렉토리 기준으로 작성하면 된다.  .profile 파일은 처음 터미널에 접속할경우 해석되는데 우린 이미 접속 하고 있기에  갱신 명령으로 바로 사용할수 있게 하자




    
    > source ~/.profile
    





이젠 바로 터미널에서 mongod 를 실행시켜 보면 path가 잡힌걸 확인가능 하다.





## config파일로 옵션 지정하기





mongod 를 올릴때 여러 옵션들을 config 파일을 지정하면 좀더 손쉽게 올릴수 있다.




    
    > mongod --config /Applications/mongodb/mongo.conf
    





mongo.conf 파일명과 위치는 원하는대로 하면 된다. 이제 mongo.conf 에 파일을 만들어보자




    
    port = 27017 # 몽고데몬이 돌아갈 포트
    fork = true # 데몬모드
    logpath = /tmp/mongodb.log  #로그파일 위치
    dbpath = /Applications/mongodb/data  # DB 파일의 path (기본 /data/db)
    





위 처럼 자신의 환경에 맞게 옵션을 설정하고 저장한다





자 이제 몽고db를 띄워보자!




    
    > mongod --config /Applications/mongodb/mongo.conf
    





## 도움글







  * [윈도우에서 환경변수 설정](http://judydba.tistory.com/tag/%EB%AA%BD%EA%B3%A0%EB%94%94%EB%B9%84%20%EC%84%A4%EC%B9%98)



