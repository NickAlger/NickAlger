---
title: Hyperbolic cross power law sum
layout: page
permalink: hcross
---

<script>
MathJax = {
  tex: { inlineMath: [['$', '$'], ['\\(', '\\)']], displayMath: [['$$', '$$'], ['\\[', '\\]']] }
};
</script>
<script id="MathJax-script" async src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

---


**Proposition 1** (Bounding discrete sum by integrals).

Let $a \ge 0$, $R > 1$, let $n$ be a nonnegative integer, and define the discrete set

$$
\Xi := \{\xi \in \mathbb{Z}^n: 1 \le \xi, \text{ and } \prod_{i=1}^n \xi_i \le R\}
$$

the continuous sets

$$
\begin{aligned}
    \Upsilon_n :=& \{\mathbf{x} \in \mathbb{R}^n: 1 \le \mathbf{x}, \text{ and } \prod_{i=1}^n \mathbf{x}_i \le R\} \\
    \overline{\Upsilon}_n :=& \{\mathbf{x} \in \mathbb{R}^n: 0 \le \mathbf{x}, \text{ and } \prod_{i=1}^n \max(1, \mathbf{x}_i) < R\} 
\end{aligned}
$$

Here, vector inequalities are understood componentwise, e.g., $1 \le \mathbf{x}$ means $1 \le \mathbf{x}_i$ for $i=1,2,\dots,n$, where $\mathbf{x}_i$ denotes the $i$th component of the vector $\mathbf{x}$. These sets are illustrated for $n=2$ in the left and middle subfigures of Figure 1. Also define the integrals

$$
I_n := \int_{\Upsilon_n} \prod_{i=1}^n \mathbf{x}_i^{-a} d\mathbf{x} \qquad (1)
$$

$$
J_n := \int_{\overline{\Upsilon}_n} \prod_{i=1}^n \max(1, \mathbf{x}_i)^{-a} d\mathbf{x} \qquad (2)
$$

for $n>0$ and $I_0 = J_0 := 1$. Then

$$
I_n \le \sum_{\xi \in \Xi} \prod_{i=1}^n \xi_i^{-a} \le J_n. \qquad (3)
$$



**Proof.**
The case $n=0$ holds trivially, so assume that $n \ge 1$. Let $B_\xi := \bigtimes_{i=1}^n [\xi_i-1, \xi_i]$ denote the $1 \times \dots \times 1$ box in $\mathbb{R}^n$ with maximum corner $\xi$, and define 

$$
B := \bigcup_{\xi \in \Xi} B_\xi.
$$

Further, let $\text{ceil}(\cdot)$ denote the ceiling function. That is, $\text{ceil}(t)$ is the smallest integer greater than or equal to $t$. Since the function 
$\text{ceil}(x_l)^{-a}$
is piecewise constant and takes the value 
$\prod_{j=1}^n \xi_j^{-a}$ 
on the interior of $B_\xi$, it follows that

$$
\begin{aligned}
\sum_{\xi \in \Xi} \prod_{j=1}^n \xi_j^{-a} &= \sum_{\xi \in \Xi} \prod_{j=1}^n \xi_j^{-a} \int_{B_\xi} 1 d\mathbf{x} \\
&= \sum_{\xi \in \Xi} \int_{B_\xi} \prod_{j=1}^n \xi_j^{-a} d\mathbf{x} \\
&= \sum_{\xi \in \Xi} \int_{B_\xi} \text{ceil}(\mathbf{x}_i)^{-a} d\mathbf{x} \\
&= \int_{B}  \prod_{j=1}^n \text{ceil}(\mathbf{x}_i)^{-a} d\mathbf{x},
\end{aligned}
$$

Furthermore, from the definition of $\Xi$ it follows that

$$
B =\{\mathbf{x} \in \mathbb{R}^n: 0 \le \mathbf{x}, \text{ and } \prod_{i=1}^n\text{ceil}(\mathbf{x}_i) \le R \}.
$$

Using the fact that $\text{ceil}(t) \le t+1$ and the definition of $\Upsilon_n$, we have $\Upsilon_n \subset B+1$, where $B + 1 = \{B+1 : \mathbf{x} \in B\}$. Using the fact that $\max(1,t) \le \text{ceil}(t)$ and the definition of $\overline{\Upsilon}_n$, we have $B \subset \overline{\Upsilon}_n$. Together, this means

$$
\Upsilon_n - 1 \subset B \subset \overline{\Upsilon}_n.
$$

We derive the bound

$$
\begin{aligned}
\int_{B}  \prod_{j=1}^n \text{ceil}(\mathbf{x}_i)^{-a} d\mathbf{x} &\le \int_{B}  \prod_{j=1}^n \max(1, \mathbf{x}_i)^{-a} d\mathbf{x} \\
&\le \int_{\overline{\Upsilon}_n}  \prod_{j=1}^n \max(1, \mathbf{x}_i)^{-a} d\mathbf{x} 
= J_n.
\end{aligned}
$$

In the first inequality, we used the fact that $\text{ceil}(t) \ge \max(1,t)$, and hence $\text{ceil}(t)^{-a} \le \max(1,t)^{-a}$. In the second inequality, we used the fact that $B \subset \overline{\Upsilon}_n$, and the fact that the integrand is positive. This proves the upper bound in (eq:doublesided_disctete_to_continuous). 

We also derive the bound

$$
\begin{aligned}
\int_{B}  \prod_{j=1}^n \text{ceil}(\mathbf{x}_i)^{-a} d\mathbf{x} &\ge \int_{B}  \prod_{j=1}^n (\mathbf{x}_i + 1)^{-a} d \mathbf{x} \\
&= \int_{1 + B}  \prod_{j=1}^n \mathbf{y}_i^{-a} d \mathbf{y} \\
&\ge \int_{\Upsilon_n}  \prod_{j=1}^n \mathbf{x}_i^{-a} d \mathbf{x} 
= I_n.
\end{aligned}
$$

In the first line, we used the fact that $\text{ceil}(t) \le t+1$, and hence $\text{ceil}(t)^{-a} \ge (t+1)^{-a}$. In the second line, we performed the change of variables $\mathbf{y} = \mathbf{x} + 1$. In the third line, we used the fact that $\Upsilon_n - 1 \subset B$, and the fact that the integrand is positive. This proves the lower bound in (eq:doublesided_disctete_to_continuous) and completes the proof.

$\square$

---

----

The [Astroknot puzzle](http://puzzlesolver.com/puzzle.php?id=45) is one of the most difficult wire-and-string tanglement puzzles I’ve found. This page explains how to solve it, and in the process some general ideas about solving tanglement/topology-ladder puzzles. Here’s a picture of the puzzle; the goal is to remove the string.

![Astroknot whole puzzle](./astroknot/astroknot_all_pic.jpg)
