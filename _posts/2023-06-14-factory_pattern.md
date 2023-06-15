---
layout: single
title: "디자인 패턴 - 팩토리 패턴"
categories: "design_patterns"
tag: ["factory_pattern"]
author_profile: false
sidebar:
  nav: "counts"
---

## 개요

- 객체 생성 부분을 떼어내 추상화한 패턴
- 상속 관계에 있는 두 클래스에서 상위 클래스가 뼈대를 결정하고 하위 클래스에서 구체적인 내용르 결정하는 패턴

## 사용 예시

## 특징

- 상위 클래스와 하위 클래스의 분리로 인해 느슨한 결합을 가짐
- 상위 클래스엥서는 인스턴스 생성 방식에 대해 알 필요가 없으므로 더 많은 유연성을 가짐
- 별도의 객체 생성 로직이 존재하기 때문에 코드 유지 보수성 증가
