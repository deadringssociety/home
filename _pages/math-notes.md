---
layout: archive
title: "Fields and Galois Theory"
permalink: /fields-and-galois-theory/
author_profile: true
---
# Characteristic of a Field

**Consider a map** $\varphi: \mathbb{Z} \to F$ defined by:
$$n \mapsto n \cdot 1_F$$

where $n \cdot 1_F = (\underbrace{1_F + \cdots + 1_F}_{n \text{ times}})$

**Claim:** $\varphi$ is a ring homomorphism

**Proof:** Recall a ring homomorphism is a map $\varphi: R \to R_2$ with the following properties:
- $\varphi(x)\varphi(y) = \varphi(xy)$
- $\varphi(x) + \varphi(y) = \varphi(x+y)$
- $\varphi(1_R) = 1_{R_2}$

---

**Also:** Recall $(\mathbb{Z}, +, \cdot)$ is a ring

**Continuing with the proof:**

Checking $\varphi(n) = n \cdot 1_F$

⋆ $m,n \in \mathbb{Z}$, 
$$\varphi(m+n) = (m+n) \cdot 1_F$$
$$= m \cdot 1_F + n \cdot 1_F$$
$$= \varphi(m) + \varphi(n)$$

⋆ $\varphi(mn) = (mn) \cdot 1_F$
$$= (m \cdot 1_F)(n \cdot 1_F) \quad (\text{since } 1_F \cdot 1_F = 1_F)$$
$$= \varphi(m)\varphi(n)$$

⋆ $\varphi(1) = 1 \cdot 1_F = 1_F$

$\square$

[Box with text:] Every field $F$ of characteristic 0 has a copy of $\mathbb{Q}$

[Another note:] has a subfield isomorphic to $\mathbb{Q}$
