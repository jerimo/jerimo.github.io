---
layout: posts
title: "⛵ 여행 검색 및 예약 서비스 이용하기"
categories:
  - DBProject
last_modified_at: 2021-02-11
author_profile: true
tags:
  - Mysql
  - PHP
  - apache24
toc : true
toc_sticky : true
sidebar:
  title: Posts
  nav: "sidebar-contents"
---

## 🐣 코드를 다운받고 아래의 단계를 따라 서비스를 이용해 보자!

-----

- <a href="https://github.com/jerimo/2020.DatabaseProject.git">코드 다운</a><br>
![코드 다운](/assets/image/ts/code.png){: width="300" height="300"}<br>
<small>Download ZIP 클릭!</small>

### 🍀 사용방법

-----

0. ```apache24```가 설치되었고, 활성화 되어있음을 전제한다.
1. ```DB_data.dump``` 파일을 cmd창에서 실행시켜 데이터를 설치한다. 사용한 root 계정의 비밀번호는 ```0000```이다.
2. 이후 소스 코드중 ```dbconn.php``` 파일을 열어, ```db_user_id```와 ```db_pwd```를 필요시 변경한다.
3. ```apache24```의 ```htdocs 폴더```에 소스 코드를 설치한다.
4. 주소창에 ```localhost```를 입력해 실행시킨다.

### 🐱 서비스 소개

-----

- 로그인
  + 회원가입이 되어있지 않다면, 우선 회원가입을 진행한다.
  + 아이디는 중복될 수 없다.
<br>
- 검색 및 예약
  + 검색과 회원 여부와 관계가 없으며, 예약은 회원인 경우에만 가능하다.
  + 검색 내용은 나라 이름이나 특정한 테마, 관광 명소의 정확한 명칭으로만 특정한다.
  + 관광지의 이름으로 검색하는 경우 검색 결과는 하나의 나라만을 표시하게 된다.
  + 테마로 검색하는 경우는 해당하는 나라만을 표시한다.
  + 나라의 이름으로 검색하는 경우는 여러 개의 테마별로 해당 나라가 정렬된다.
  + 회원은 이름을 입력하고 동행인의 인원 원하는 날짜와 나라, 테마를 선택하여 예약을 할 수 있다.
<br>
- 예약 확인 및 변경
  + 예약 현황을 검색은 회원 아이디를 사용하여 동명이인의 경우 중복된 검색 내용이 나오지 않도록 한다.
  + 회원은 같은 날짜에 여행을 중복 예약할 수 없다.
  + 하나의 여행 상품에 대해 예약 가능한 최대 인원 수는 1,000명이다.