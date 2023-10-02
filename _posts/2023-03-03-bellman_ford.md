---
layout: single
title: "벨만-포드 알고리즘"
categories: "algorithm_theory"
tag: ["Bellman-Ford"]
author_profile: false
sidebar:
  nav: "counts"
---

## 예제 코드

```python
import sys

input = sys.stdin.readline

INF = int(1e9)
n, m = map(int, input().split())
edges = []
distance = [INF] * (n + 1)

for _ in range(m):
    a, b, c = map(int, input().split())
    edges.append((a, b, c))

def bf(start):
    distance[start] = 0
    for i in range(n):
        for j in range(m):
            cur_node = edges[j][0]
            next_node = edges[j][1]
            edge_cost = edges[j][2]
            if (
                distance[cur_node] != INF
                and distance[next_node] > distance[cur_node] + edge_cost
            ):
                distance[next_node] = distance[cur_node] + edge_cost
                if i == n - 1:
                    return True
    return False


negative_cycle = bf(1)

if negative_cycle:
    print("-1")
else:
    for i in range(2, n + 1):
        if distance[i] == INF:
            print("-1")
        else:
            print(distance[i])
```
