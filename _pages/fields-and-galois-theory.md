---
layout: single
title: "Fields and Galois Theory"
permalink: /fields-and-galois-theory/
author_profile: false
---

## Characteristic of a Field

Consider a map $\varphi: \mathbb{Z} \to F$ defined by $n \mapsto n \cdot 1_F$.

> **Note:** $n \cdot 1_F$ is an abuse of notation.
> $$n \cdot 1_F := \underbrace{(1_F + \dots + 1_F)}_{n \text{ times}}$$

### Claim: $\varphi$ is a ring homomorphism.

**Recall:** A ring homomorphism is a map $\varphi: R_1 \to R_2$ with the following properties:
* $\varphi(x)\varphi(y) = \varphi(xy)$
* $\varphi(x) + \varphi(y) = \varphi(x + y)$
* $\varphi(1_{a}) = 1_{b} where 1_a is the identity in R_1 and 1_b is the identity in R_2.$

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

### Recall:
**Definition:** The kernel of a homomorphism is the preimage of $0_F \in F$.

It is now natural to ask what the kernel of this homomorphism is.

### What if $\ker(\varphi)$ is trivial?
Note that if the kernel of a homomorphism is trivial, i.e., $\ker(\varphi) = \{0\}$ for $0 \in \mathbb{Z}$ in our case, then the homomorphism is injective. 

And, in our case, the homomorphism being injective also guarantees that all non-zero integers map to invertible elements of $F$.
i.e., let $n \in \mathbb{Z}$ and $n \neq 0$.
Then $\varphi(n) = n \cdot 1_F$ where $n \cdot 1_F$ is invertible $\Rightarrow (n \cdot 1_F)^{-1}$ exists in $F$.

We will take advantage of this last fact and extend this homomorphism to $\mathbb{Q}$.

Let us now define a new map $\phi: \mathbb{Q} \to F$:
$$\phi(m/n) = (m \cdot 1_F)(n \cdot 1_F)^{-1}$$

Notice that the validity of this is guaranteed to us by what we said earlier about invertible elements.

We can rewrite $\phi(m/n) = (m \cdot 1_F)(n \cdot 1_F)^{-1}$ as:
$$\phi(m/n) = \varphi(m)\varphi(n)^{-1}$$

---

### Claim: $\phi$ is also a ring homomorphism.

**Proof:** Note that proving well-definedness is important, but is left as an exercise.

### Verifying:
* **Addition:** Let $a/b, c/d \in \mathbb{Q}$
    $$
    \begin{aligned}
    \phi(a/b + c/d) &= \phi\left(\frac{ad + bc}{bd}\right) \\
    &= \varphi(ad + bc)\varphi(bd)^{-1} \\
    &= [\varphi(a)\varphi(d) + \varphi(b)\varphi(c)]\varphi((bd)^{-1}) \\
    &= [\varphi(a)\varphi(d) + \varphi(b)\varphi(c)]\varphi(d)^{-1}\varphi(b)^{-1} \\
    &= \varphi(a)\varphi(b)^{-1} + \varphi(c)\varphi(d)^{-1} \\
    &= \phi(a/b) + \phi(c/d)
    \end{aligned}
    $$

* **Multiplication:** Let $a/b, c/d \in \mathbb{Q}$
    $$
    \begin{aligned}
    \phi(a/b \cdot c/d) &= \phi\left(\frac{ac}{bd}\right) \\
    &= \varphi(ac)\varphi(bd)^{-1} \\
    &= \varphi(a)\varphi(c)\varphi(b)^{-1}\varphi(d)^{-1} \\
    &= \varphi(a)\varphi(b)^{-1}\varphi(c)\varphi(d)^{-1} \\
    &= \phi(a/b) \cdot \phi(c/d)
    \end{aligned}
    $$

* **Identity:**
    $$\phi(1) = \varphi(1)\varphi(1)^{-1} = 1_F \cdot 1_F^{-1} = 1_F$$

### Recall:
**Definition:** The kernel of a homomorphism is the preimage of $0_F \in F$.

It is now natural to ask what the kernel of this homomorphism is.

### What if $\ker(\varphi)$ is trivial?
Note that if the kernel of a homomorphism is trivial, i.e., $\ker(\varphi) = \{0\}$ for $0 \in \mathbb{Z}$ in our case, then the homomorphism is injective.

And, in our case, the homomorphism being injective also guarantees that all non-zero integers map to invertible elements of $F$.
i.e., let $n \in \mathbb{Z}$ and $n \neq 0$.
Then $\varphi(n) = n \cdot 1_F$ where $n \cdot 1_F$ is invertible $\Rightarrow (n \cdot 1_F)^{-1}$ exists in $F$.

We will take advantage of this last fact and extend this homomorphism to $\mathbb{Q}$.

Let us now define a new map $\phi: \mathbb{Q} \to F$:
$$\phi(m/n) = (m \cdot 1_F)(n \cdot 1_F)^{-1}$$

Notice that the validity of this is guaranteed to us by what we said earlier about invertible elements.

We can rewrite $\phi(m/n) = (m \cdot 1_F)(n \cdot 1_F)^{-1}$ as:
$$\phi(m/n) = \varphi(m)\varphi(n)^{-1}$$

---

### Claim: $\phi$ is also a ring homomorphism.

**Proof:** Note that proving well-definedness is important, but is left as an exercise.

### Verifying:
* **Addition:** Let $a/b, c/d \in \mathbb{Q}$
    $$
    \begin{aligned}
    \phi(a/b + c/d) &= \phi\left(\frac{ad + bc}{bd}\right) \\
    &= \varphi(ad + bc)\varphi(bd)^{-1} \\
    &= [\varphi(a)\varphi(d) + \varphi(b)\varphi(c)]\varphi((bd)^{-1}) \\
    &= [\varphi(a)\varphi(d) + \varphi(b)\varphi(c)]\varphi(d)^{-1}\varphi(b)^{-1} \\
    &= \varphi(a)\varphi(b)^{-1} + \varphi(c)\varphi(d)^{-1} \\
    &= \phi(a/b) + \phi(c/d)
    \end{aligned}
    $$

* **Multiplication:** Let $a/b, c/d \in \mathbb{Q}$
    $$
    \begin{aligned}
    \phi(a/b \cdot c/d) &= \phi\left(\frac{ac}{bd}\right) \\
    &= \varphi(ac)\varphi(bd)^{-1} \\
    &= \varphi(a)\varphi(c)\varphi(b)^{-1}\varphi(d)^{-1} \\
    &= \varphi(a)\varphi(b)^{-1}\varphi(c)\varphi(d)^{-1} \\
    &= \phi(a/b) \cdot \phi(c/d)
    \end{aligned}
    $$

* **Identity:**
    $$\phi(1) = \varphi(1)\varphi(1)^{-1} = 1_F \cdot 1_F^{-1} = 1_F$$

$\square$

---

Notice that this means that there is an injection between $\mathbb{Q}$ and $F$.
So we can say that there is an inclusion from $\mathbb{Q}$ to $F$.

### We can now make a statement:
Every such field $F$, for which the kernel of the homomorphism $\varphi$ is trivial, has a copy of $\mathbb{Q}$ in it.

More concretely, every such field has a subfield isomorphic to $\mathbb{Q}$.

### But, what if the kernel is not trivial?

Then, we claim that the minimum $n \in \mathbb{Z} \ni \varphi(n) = (n \cdot 1_F) = 0_F$ is a prime number.

In fact, this lowest integer $n$ is called the **characteristic of the Field $F$**.

So, in other words, we are claiming that if the kernel is not trivial, then the characteristic is a prime number.

---

**Proof:** Suppose for contradiction that the characteristic of $F$, denoted $\text{char}(F)$, is a composite number $m$.

$\therefore \exists m \in \mathbb{Z} \ni m = a \cdot b$ for $a, b \in \mathbb{Z} \ni m > a, m > b$ and $m \cdot 1_F = 0_F$.
$\Rightarrow (ab) \cdot 1_F = 0_F$
$\Rightarrow (a \cdot 1_F)(b \cdot 1_F) = 0_F$.

**Fact:** In a unique factorization domain, such as a Field, if two things multiply to give $0$, then one of them must be zero.

$\Rightarrow a \cdot 1_F = 0_F$ or $b \cdot 1_F = 0_F$.

Since $a < m$ and $b < m$, by definition of characteristic, either $a$ or $b$ should be the characteristic, not $m$.
$\rightarrow \leftarrow$ (Contradiction)

Moreover, we can say something similar to the statement we made in the trivial kernel case:

> Every field $F$ of characteristic $p$ has a subfield isomorphic to $\mathbb{F}_p$.
