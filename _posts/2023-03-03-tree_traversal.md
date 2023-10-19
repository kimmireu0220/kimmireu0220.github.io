---
layout: single
title: "트리 순회 알고리즘"
categories: "algorithm_theory"
tag: ["Tree"]
author_profile: false
sidebar:
  nav: "counts"
---

## 예제 코드

```python
def pre_order(p):
    if p == ".":
        return
    print(p, end="")
    pre_order(l[p])
    pre_order(r[p])


def in_order(p):
    if p == ".":
        return
    in_order(l[p])
    print(p, end="")
    in_order(r[p])


def post_order(p):
    if p == ".":
        return
    post_order(l[p])
    post_order(r[p])
    print(p, end="")


n = int(input())
l, r = {}, {}

for _ in range(n):
    p, lc, rc = input().split()
    l[p] = lc
    r[p] = rc

root = "A"
pre_order(root)
print()
in_order(root)
print()
post_order(root)
print()
```
