---
layout: post
title: Loop Unrolling
---

# Loop Unrolling (循环展开) #

## Refs ##

* [Tutorial 1](http://www.cs.umd.edu/~meesh/cmsc411/website/proj01/proja/loop.html)
* [Tutorial 2](http://www.keil.com/support/man/docs/armcc/armcc_chr1359124222660.htm)

## Problem Definition ##

**怎样最快的求出1,000,000个数的加法？**

一眼就知道直接O(n)就可以

```C
for (int i=0; i<=1000000; i ++) {
  sum += a[i];
}
```

这已经是复杂度的下限了，还可以怎么优化？

**Loop Unrolling**是一个很简单的编译器优化，相当直接却特别有效。当然，它也是我们理解更高级的优化的基础。

我们将回答两个问题 **WHY** 和 **HOW**:
- **Why we need it?**
- **How does it work?**

## Why we need it? ##

### Reason I ###
: from [Tutorial 2](http://www.keil.com/support/man/docs/armcc/armcc_chr1359124222660.htm)


#block_container
{
    text-align:center;
}
#bloc1, #bloc2
{
    display:inline;
}

<div id="block_container">
    <div id="bloc1"><version rgtjf Copyright &copy; All Rights Reserved.></div>  
    <div id="bloc2"><version rgtjf Copyright &copy; All Rights Reserved.></div>
</div>

我们用汇编来描述这段代码，假设R1寄存器存着数组a的基地址， R2里存着sum， R3从1,000,000开始。

```
Loop: LW R4, 0(R1);     //element of a
ADD R3, R3, R4
ADDI R1, R1, #4
```

## How does it work? ##

## Examples ##
