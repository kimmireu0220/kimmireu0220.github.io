---
layout: single
title: "2차원 배열 회전"
categories: "algorithm_theory"
tag: ["Rotate"]
author_profile: false
sidebar:
  nav: "counts"
---

## 예제 코드

```python
def rotate(board, degree):
    if degree == 90:
        return list(map(list, zip(*board[::-1])))
    elif degree == 180:
        return rotate(rotate(1, board), 90)
    elif degree == 270:
        return list(map(list, zip(*board)))[::-1]
    else:
        return board
```
