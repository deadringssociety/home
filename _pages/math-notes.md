---
layout: archive
title: "Mathematics Notes"
permalink: /math-notes/
author_profile: true
---

## Differential Geometry

### Manifolds

A smooth manifold $M$ of dimension $n$ is a topological space that locally resembles $\mathbb{R}^n$.

**Definition (Tangent Space):** The tangent space $T_p M$ at point $p \in M$ is defined as:

$$
T_p M = \left\{ \gamma'(0) : \gamma \text{ is a smooth curve with } \gamma(0) = p \right\}
$$

### Riemannian Metrics

A Riemannian metric $g$ assigns to each point $p \in M$ an inner product $g_p$ on $T_p M$. In local coordinates $(x^1, \ldots, x^n)$:

$$
g = \sum_{i,j} g_{ij} \, dx^i \otimes dx^j
$$

where $g_{ij} = g\left(\frac{\partial}{\partial x^i}, \frac{\partial}{\partial x^j}\right)$.

## Linear Algebra

The characteristic polynomial of a matrix $A \in \mathbb{R}^{n \times n}$ is:

$$
p_A(\lambda) = \det(A - \lambda I)
$$
