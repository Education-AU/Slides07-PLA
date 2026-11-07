---
title: Proof SVD
template: default
---

For $\sigma_i = 0$, we cannot use the previous definition.

The eigenvectors corresponding to the eigenvalue $\lambda = 0$ span
$$
\ker(A^TA) = \ker(A).
$$


We extend the orthonormal set $\{u_1, u_2, \dots, u_r\}$ to an orthonormal basis of $\mathbb{R}^m$:
$$
\{u_1, u_2, \dots, u_r, u_{r+1}, \dots, u_m\}.
$$

Since $\operatorname{span}(u_1, \dots, u_r) = \operatorname{im}(A)$, the remaining vectors satisfy
$$
\operatorname{span}(u_{r+1}, \dots, u_m) = \operatorname{im}(A)^\perp = \ker(A^T).
$$


We now define the matrices:

$$
V = [v_1, v_2, \dots, v_n], \quad
U = [u_1, u_2, \dots, u_m],
$$
where $U$ and $V$ are orthogonal matrices.


Let $\Sigma \in \mathbb{R}^{m \times n}$ be the diagonal matrix defined by

$$
\Sigma_{ii} =
\begin{cases}
\sigma_i & i \le r, \\
0 & i > r.
\end{cases}
$$

