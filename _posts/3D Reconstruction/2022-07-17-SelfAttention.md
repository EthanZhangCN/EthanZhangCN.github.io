---
layout: post
title: 注意力机制
subtitle: calculation
gh-repo: EthanZhangCN/Readings
gh-badge: [star, fork, follow]
tags: [Algorithm]
comments: true
---
##



#### 1) 注意力机制

$$ Attention(Q,K,V) =softmax(\frac{QK^T}{\sqrt{d_k}})V    ----（1）$$

输入序列 Qurey, Q由 n 个长度为 $d_k$ 的向量组成  ,大小为 [n , d_k]， $K大小为[m, d_k]$, $V大小为[m, d_v]$，输出大小为$[n,d_v]$

$$softmax( \frac{Q_{[n,d_k]}  K^T_{[d_k,m]} }{\sqrt{d_k}}  )V_{[m,d_v]} =Attention_{ [n,d_v]}$$

#### 2）自注意力机制
$Q=K=V$

$$softmax( \frac{Q_{[n,d_k]}  K^T_{[d_k,n]} }{\sqrt{d_k}}  )V_{[n,d_k]} =Attention_{ [n,d_k]}$$
