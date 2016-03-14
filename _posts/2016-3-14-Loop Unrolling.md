---
layout: post
title: Loop Unrolling
---

# Loop Unrolling (循环展开) #

## Refs ##

* http://www.cs.umd.edu/~meesh/cmsc411/website/proj01/proja/loop.html

## Problem Definition ##

**怎样最快的求出1,000,000个数的加法？**

一眼就知道直接$O(n)$就可以
```C
for (int i=0; i<=1000000; i ++) {
  sum += a[i];
}
```
这已经是复杂度的下限了，还可以怎么优化？

Loop Unrolling是一个很简单的编译器优化，相当直接却特别有效。当然，它也是我们理解更高级的优化的基础。

我们将回答两个问题 **WHY** 和 **HOW**:
- Why we need it?
- How does it work?

## Why we need it? ##

## How does it work? ##

## Examples ##
