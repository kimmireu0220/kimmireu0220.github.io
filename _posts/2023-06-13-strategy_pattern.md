---
layout: single
title: "디자인 패턴 - 전략 패턴"
categories: "design_patterns"
tag: ["strategy_pattern"]
author_profile: false
sidebar:
  nav: "counts"
---

## 개요

- 객체의 행위를 바꾸고 싶은 경우 '직접' 수정하지 않고 전략이라고 부르는'캡슐화한 알고리즘'을 컨텍스트 안에서 바꿔주면서 상호 교체가 가능하게 만드는 패턴
- 구체적인 객체가 아닌 추상화에 의존해야 한다는 DIP (의존성 역전 원칙)와 관련

## 사용 예시

1. passport: 인증 모듈 구현 라이브러리

- 아이디와 비밀번호 기반 인증 전략(LocalStrategy) / 페이스북, 네이버 등 다른 서비스 기반 인증 전략 (OAuth) 등 여러 가지 전략을 기반으로 인증할 수 있음
