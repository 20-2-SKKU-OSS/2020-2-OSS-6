---
layout: post
title: 크롤링 카테고리 추가 
subtitle: by 원종원
date: 2020-12-10 18:00:00 +0900
category: Process
---

## 1. 크롤링 카테고리 추가 
기존 크롤링은 '정치,'경제','시회','생활문화','IT과학','세계','오피니언'카테고리만 크롤링이 가능
![issue15](../assets/img/news_home.png)


따라서 '연합뉴스속보'카테고리도 크롤링이 가능하도록 수정
![issue15](../assets/img/category_issue.png)

articlecrawler.py에 코드 수정 

![issue15](../assets/img/code_edit.png)

이때 '연합뉴스속보'카테고리 html 형식에 맞추어 기존 카테고리와 동일한 방식으로 크롤링하도록 코드 수정

![issue15](../assets/img/html.png)

## 2. 크롤링 실행

정상적으로 실행되는 것을 확인할 수 있음
![issue15](../assets/img/operation_test.png)

크롤링 결과
![issue15](../assets/img/result.png)

## 3. commit 작성 및 readme 수정

코드 수정중 nomultiproc 브랜치에서 크롤링 카테고리와 진행상황을 볼수 있도록 코드가 수정된것을 확인하고 main 브랜치가 아닌 nomultiproc브랜치에 바로 commit하였

![issue15](../assets/img/commit1.png)

![issue15](../assets/img/readme.png)

![issue15](../assets/img/commit2.png)




