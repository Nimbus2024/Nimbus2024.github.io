---
title: 概率论笔记1
date: 2025-12-20T09:20:48+08:00
categories: [notes]
tags: [study]
description: 连续型随机变量的联合分布，与随机变量的函数的分布
slug: probability_theory_note
math: true
comments: true
draft: false
---
这个部分是概率论的关键基础，让我们可以借助运算从经典个体推广到广泛的分布情形。在我的视角中同样也是困扰了我很久的问题——课本安排实在是有点太错落了。今天刚好详细整理它。
首先，问题是从`随机变量的函数`（这显然也是个随机变量）的分布开始的。

最简单的是一元情形。对于$Y = g(X):R \rightarrow R$，如何确定$P(Y = y)$，或者$F(y) = P(Y \leq y)$？前者考虑的是离散型随机变量的情形。这大多数情况下都有直观的枚举，我们更关心非离散型的随机变量中，有特殊性质的`连续型随机变量`，也就是后者。

那么对于后者，显然我们有等价关系，$P(Y \leq y) = P(g(x) \leq y) = P(x\in A)$，其中 $A = \left\lbrace x \mid g(x) \le y \right\rbrace$

问题就变成，如何求关于每个$y$的$A(y)$？自然我们会考虑单调情形。不妨假设函数$g(X)$在定义域的若干个子区间上单调
