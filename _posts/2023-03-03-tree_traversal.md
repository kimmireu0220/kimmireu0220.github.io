---
layout: single
title: "Tree Traversal Algorithm"
categories: "algorithm_theory"
tag: ["Tree"]
toc: true
author_profile: false
sidebar:
  nav: "docs"
---

## 예제 코드

```python
class Node:
    def __init__(self, parent, left, right):
        self.parent = parent
        self.left = left
        self.right = right

def pre_order(node):
    print(node.parent, end="")
    if node.left != "None":
        pre_order(tree[node.left])
    if node.right != "None":
        pre_order(tree[node.right])

def in_order(node):
    if node.left != "None":
        in_order(tree[node.left])
    print(node.parent, end="")
    if node.right != "None":
        in_order(tree[node.right])

def post_order(node):
    if node.left != "None":
        post_order(tree[node.left])
    if node.right != "None":
        post_order(tree[node.right])
    print(node.parent, end="")

n = int(input())
tree = {}

for i in range(n):
    parent, left, right = input().split()
    tree[parent] = Node(parent, left, right)
```
