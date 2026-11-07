---
title: Ordering of singular values
template: default
---


The singular values $\sigma_i = \sqrt{\lambda_i}$ are not ordered by the construction.



We may reorder them so that
$$
\sigma_1 \ge \sigma_2 \ge \dots \ge \sigma_r > 0,
$$
by permuting the corresponding singular vectors.



This reordering is done consistently:

1. columns of $V$ and $U$ are permuted accordingly
2. the diagonal entries of $\Sigma$ are rearranged



The zero singular values remain at the end, so
$$
\operatorname{span}(u_1,\dots,u_r)=\operatorname{im}(A), \quad
\operatorname{span}(u_{r+1},\dots,u_m)=\ker(A^T).
$$
and also we have
$$
\operatorname{span}(v_1,\dots,v_r)=\operatorname{im}(A^T), \quad
\operatorname{span}(v_{r+1},\dots,v_m)=\ker(A).
$$

