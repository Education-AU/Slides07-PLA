---
title: Proof SVD
template: default
---
We compute

$$
AA^T u_i = A\left(\frac{1}{\sigma_i} A^T A v_i\right)
= A\left(\frac{\lambda_i}{\sigma_i} v_i\right)
= \frac{\lambda_i}{\sigma_i} A v_i
= \lambda_i u_i.
$$

Thus, $u_i$ are eigenvectors of the symmetric matrix $AA^T$.



Since $AA^T$ is symmetric, the vectors $u_i$ are orthogonal. Moreover, they are normalized:
$$
\langle u_i, u_i \rangle
= \frac{1}{\sigma_i^2} \langle A v_i, A v_i \rangle
= \frac{1}{\sigma_i^2} \langle v_i, A^T A v_i \rangle
= \frac{\lambda_i}{\sigma_i^2} \langle v_i, v_i \rangle
= 1.
$$

