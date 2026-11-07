---
title: SVD Decomposition
template: theorem
theoremTitle: SVD theorem in coordinates
---

<!-- theorem -->
For a matrix $A \in \mathbb{R}^{m \times n}$ representing a linear map $L: V \to W$, where $\dim (V)=n$
and $\dim (W)=m$, we can decompose
$$
A = U \Sigma V^T
$$

This expresses $A$ as a composition of a rotation, a scaling, and another rotation.

1. $U \in \mathbb{R}^{m \times m}$ is orthogonal
2. $V \in \mathbb{R}^{n \times n}$ is orthogonal
3. $\Sigma \in \mathbb{R}^{m \times n}$ is a rectangular diagonal matrix
4. its first $r$ diagonal entries satisfy $\sigma_1 \ge \sigma_2 \ge \dots \ge \sigma_r > 0$,
   where $r = \mathrm{rank} (A)$

<!-- /theorem -->