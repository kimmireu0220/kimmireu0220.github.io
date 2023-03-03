---
layout: single
title: "Bellman-Ford Algorithm"
---

- Code Example

```python
INF = int(1e9)

def bellman_ford():
    for i in range(n):
        for edge in edges:
            cur = edges[j][0]
            next_node = edges[j][1]
            cost = edges[j][2]
            if dist[cur] != INF and dist[next_node] > dist[cur] + cost:
                dist[next_node] = dist[cur] + cost

                if i == n - 1:
                    return True
    return False

n, m = map(int, input().split())
edges = []
dist = [INF] * (n + 1)

for i in range(m):
    s, e, t = map(int, input().split())
    edges.append((s, e, t))
```
