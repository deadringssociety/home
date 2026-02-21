---
layout: single
title: "Fields and Galois Theory"
permalink: /fields-and-galois-theory/
author_profile: false
---

# Characteristic of a Field

Consider a map $\varphi: \mathbb{Z} \to F$ defined by $n \mapsto n \cdot 1_F$.

> **Note:** $n \cdot 1_F$ is an abuse of notation.
> $$n \cdot 1_F := \underbrace{(1_F + \dots + 1_F)}_{n \text{ times}}$$

### Claim: $\varphi$ is a ring homomorphism.

**Recall:** A ring homomorphism is a map $\varphi: R_1 \to R_2$ with the following properties:
* $\varphi(x)\varphi(y) = \varphi(xy)$
* $\varphi(x) + \varphi(y) = \varphi(x + y)$
* $\varphi(1_{R_1}) = 1_{R_2}$

Please take care to realize that the operations on opposite sides of the equality sign live in **different rings**, i.e., $R_1$ and $R_2$.

This is relevant to us because $(\mathbb{Z}, +, \cdot)$ is a ring. A Field is also a ring and so $\varphi$ can be said to be a map from one ring to another which allows us to ask if it is a ring homomorphism.

---

### Checking:

* **For $m, n \in \mathbb{Z}$:**
    $$
    \begin{aligned}
    \varphi(m+n) &= (m+n) \cdot 1_F \\
    &= \underbrace{(1_F + \dots + 1_F)}_{m+n \text{ times}} \\
    &= \underbrace{(1_F + \dots + 1_F)}_{m \text{ times}} + \underbrace{(1_F + \dots + 1_F)}_{n \text{ times}} \\
    &= \varphi(m) + \varphi(n)
    \end{aligned}
    $$

* **Multiplication:**
    $$
    \begin{aligned}
    \varphi(mn) &= (mn) \cdot 1_F \\
    &= (m \cdot 1_F)(n \cdot 1_F) \quad \text{(since } 1_F \cdot 1_F = 1_F) \\
    &= \varphi(m)\varphi(n)
    \end{aligned}
    $$

* **Identity:**
    $$\varphi(1) = 1 \cdot 1_F = 1_F$$

$\square$
