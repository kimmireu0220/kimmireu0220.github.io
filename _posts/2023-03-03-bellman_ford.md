---
layout: single
title: "Bellman-Ford Algorithm"
categories: "algorithm"
tag: ["bellman-ford"]
toc: true
author_profile: false
sidebar:
  nav: "docs"
---

## Code Example

```python
INF = int(1e9)

def bellman_ford():
    for i in range(n):
        for edge in edges:
            cur = edge[0]
            next_node = edge[1]
            cost = edge[2]
            if dist[cur] != INF and dist[next_node] > dist[cur] + cost:
                dist[next_node] = dist[cur] + cost
                if i == n - 1:
                    return True
    return False

n, m = map(int, input().split())
edges = []
dist = [INF] * (n + 1)

for i in range(m):
    a, b, cost = map(int, input().split())
    edges.append((a, b, cost))
```
