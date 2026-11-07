---
title: Proof SVD
template: default
---

Let $S = A^TA$. Since $S$ is symmetric and positive semidefinite, it can be diagonalized with nonnegative eigenvalues:
$$
A^TA = V \Lambda V^T,
$$
where $V$ is an orthogonal matrix whose columns are orthonormal eigenvectors $v_i$ of $A^TA$, and
$$
\Lambda = \operatorname{diag}(\lambda_1, \lambda_2, \dots, \lambda_n), \quad \lambda_i \ge 0.
$$


For $\lambda_i > 0$, we define the singular values of $A$ by
$$
\sigma_i = \sqrt{\lambda_i}.
$$


For $\sigma_i > 0$, define vectors
$$
u_i = \frac{1}{\sigma_i} A v_i, \quad A v_i = \sigma_i u_i.
$$

