---
layout: single
title: "디자인 패턴 - MVVM 모듈 패턴"
categories: "computer_science"
tag: ["design_patterns"]
author_profile: false
sidebar:
  nav: "counts"
---

## 개요

- MVC 패턴에서 C에 해당하는 컨트롤러가 뷰모델(view model)로 바뀐 패턴

## 사용 예시

1. Vue.js(반응형이 특징인 프런트엔드 프레임워크): watch와 compound 등으로 쉽게 반응형적인 값 구축 가능

## 특징

- 뷰모델은 뷰를 더 추상화한 계층.
- MVC 패턴과 다르게 커맨드(여러 요소에 대한 처리를 하나의 액션으로 처리할 수 있는 기법)와 데이터 바인딩(화면에 보이는 데이터와 웹 브라우저의 메모리 데이터를 일치시키는 기법)을 가짐
- 뷰와 뷰모델 사이의 양방향 데이터 바인딩을 지원함
- UI를 별도의 코드 수정 없이 재사용 가능
- 단위 테스팅 쉬움
