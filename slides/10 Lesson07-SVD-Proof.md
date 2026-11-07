---
title: Proof SVD
template: default
---




The number of nonzero singular values is equal to $\operatorname{rank}(A)$.

Since $\ker(A^TA)$ corresponds to the eigenvalue $0$, and $A^TA$ has $n$ eigenvalues in total, the number of nonzero eigenvalues is
$$
\operatorname{rank}(A^TA).
$$

which is inferred by the rank–nullity theorem,
$$
\dim(\ker(A^TA)) + \operatorname{rank}(A^TA) = n,
$$
We have the property from before 

$$
\operatorname{rank}(A^TA) = \operatorname{rank}(A) = r.
$$

Thus, there are $r$ nonzero singular values.


Moreover, since $u_i = \frac{1}{\sigma_i} A v_i \in \operatorname{im}(A)$ and the $r$ vectors $u_i$ are orthonormal, we have
$$
\operatorname{span}(u_1, \dots, u_r) = \operatorname{im}(A).
$$

