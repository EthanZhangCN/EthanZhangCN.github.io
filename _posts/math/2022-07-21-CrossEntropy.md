---
layout: post
title: 交叉损失熵
subtitle: calculation
gh-repo: EthanZhangCN/Readings
gh-badge: [star, fork, follow]
tags: [Algorithm]
comments: true
---
##
#### 1) 信息量

$$I(x)=-log(P(x)),x\in X$$

$P(x)$:事件$x$发生的概率，一个事件发生的概率越大，不确定性越小，其携带的信息量就越小。

####2）熵
$$H(x) = -\overset{n} {\mathop{\sum} } \limits_{i=1}p(x_i)log(p(x_i))$$

代表系统中信息量的总和，反映一个系统的混乱程度。

####3）相对熵

$$D_{KL}(p||q) = \mathop{\sum}\limits_{i}p(x_i)log(\frac{p(x_i)}{q(x_i)})$$

$p(x_i)q(x_i)$事件$x$在$p q$两个系统中的概率。表示同一个随机变量的两个不同分布间的距离。
实际应用中假设$p(x)$为真实分布，$q(x)$为预测所得，就需要最小化KL

>$p(x)=q(x)$,则$D_{KL}(p||q)=0$

>$D_{KL}(p||q) \not= D_{KL}(q||p)$ ，相对熵距离不对称

>$D_{KL}(p||q)\geq0$

####4）交叉商
$$H(p,q)=\mathop{\sum}\limits_ip(x_i)log{\frac{1}{logq(x_i)}} = -\sum\limits_ip(x_i)logq(x_i)$$

$p(x)$是目标分布，p和q的交叉熵可以看作是使用分布q(x)表示目标分布p(x)的困难程度

将熵、相对熵以及交叉熵的公式放到一起

$$H(p)=-\sum\limits_ip(x_i)logp(x_i)$$

$$D_{KL}(p||q)=\sum_\limits{i}p(x_i)log{\frac{p(x_i)}{q(x_i)}}
=\sum_\limits{i}(p(x_i)logp(x_i)-p(x_i)logq(x_i))$$

$$H(p,q)=-\sum_\limits{i}p(x_i)logq(x_i)$$


在机器学习中，目标的分布p(x) 通常是训练数据的分布是固定，即是H(p) 是一个常量。这样两个分布的交叉熵H(p,q) 也就等价于最小化这两个分布的相对熵DKL(p∥q)。

设p(x) 是目标分布（训练数据的分布），我们的目标的就让训练得到的分布q(x)尽可能的接近p(x)，这时候就可以最小化DKL(p∥q)，等价于最小化交叉商




