---
title: Proof SVD
template: default
---

For each basis vector $v_i$, we have
$$
Av_i =
\begin{cases}
\sigma_i u_i & i \le r, \\
0 & i > r.
\end{cases}
$$


Thus, the action of $A$ on the basis $\{v_i\}$ can be written as
$$
AV = U \Sigma.
$$

Multiplying on the right by $V^T$, we obtain
$$
A = U \Sigma V^T.
$$


For $i > r$, we also have $u_i \in \ker(A^T)$.
