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

<b>Proposition 1<\b>(Bounding discrete sum by integrals)
<i>
<!---\label{prop:discrete_to_continuous_hypercross}-->
    Let $a \ge 0$, $\hcrossradius > 1$, let $n$ be a nonnegative integer, and define the discrete set
    \begin{equation*}
        \Xi := \{\xi \in \mathbb{Z}^n: 1 \le \xi, \text{ and } \prod_{i=1}^n \xi_i \le R\}
    \end{equation*}
    the continuous sets
    \begin{align*}
        \Upsilon_n :=& \{\vb{x} \in \mathbb{R}^n: 1 \le \vb{x}, \text{ and } \prod_{i=1}^n \vb{x}_i \le R\} \\
        \overline{\Upsilon}_n :=& \{\vb{x} \in \mathbb{R}^n: 0 \le \vb{x}, \text{ and } \prod_{i=1}^n \max(1, \vb{x}_i) < R\} 
    \end{align*}
    Here, vector inequalities are understood componentwise, e.g., $1 \le \vb{x}$ means $1 \le \vb{x}_i$ for $i=1,2,\dots,k$, where $\vb{x}_i$ denotes the $i$th component of the vector $\vb{x}$. These sets are illustrated for $n=2$ in the left and middle subfigures of Figure \ref{fig:hcross_In_Jn_binomial}. Also define the integrals
    \begin{align}
        I_n :=& \int_{\Upsilon_n} \prod_{i=1}^n \vb{x}_i^{-a} d\vb{x}, \label{eq:Ik_defn}\\
        J_n :=& \int_{\overline{\Upsilon}_n} \prod_{i=1}^n \max(1, \vb{x}_i)^{-a} d\vb{x}. (\#eq:Jk_defn)
    \end{align}
    for $n>1$ and $I_0 = J_0 := 1$.
    Then
    \begin{equation}
     (\#eq:doublesided_disctete_to_continuous)
        I_n \le \sum_{\xi \in \Xi} \prod_{i=1}^n \xi_i^{-a} \le J_n.
    \end{equation}
<\i>


----

The [Astroknot puzzle](http://puzzlesolver.com/puzzle.php?id=45) is one of the most difficult wire-and-string tanglement puzzles I’ve found. This page explains how to solve it, and in the process some general ideas about solving tanglement/topology-ladder puzzles. Here’s a picture of the puzzle; the goal is to remove the string.

![Astroknot whole puzzle](./astroknot/astroknot_all_pic.jpg)
