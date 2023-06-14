---
layout: single
title: "디자인 패턴 - 싱글톤 패턴"
categories: "design_patterns"
tag: ["strategy_pattern"]
author_profile: false
sidebar:
  nav: "counts"
---

## 개요

- 하나의 클래스에 오직 하나의 인스턴스만 가지는 패턴

## 사용 예시

1. mongoose: Node.js에서 MongoDB 데이터베이스 연결 시 사용
2. MySQL 데이터베이스 연결 시 사용

## 특징

- 미리 생성된 하나의 인스턴스를 기반으로 구현하는 패턴이므로 서로 독립적인 단위 테스트를 주로 하는 TDD 어려움
- 사용자가 사용하기 쉽고 실용적이지만 모듈 간의 결합을 강하게 만들 수 있음
- 의존성 주입자를 통해 메인 모듈이 간접적으로 하위 모듈에게 의존성을 주입하여 모듈 간의 결합을 느슨하게 만듦으로써 해결
