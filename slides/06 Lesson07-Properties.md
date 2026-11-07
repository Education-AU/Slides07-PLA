---
title: Properties
template: default

---

1. **Symmetry**<br>
   The matrices $A^TA$ and $AA^T$ are symmetric:
   $$
   \langle A^TAx, x \rangle_{\mathbb{R}^n} = \langle Ax, Ax \rangle_{\mathbb{R}^m} = \langle x, A^TAx \rangle_{\mathbb{R}^n}
   $$

$$
\langle AA^Tx, x \rangle_{\mathbb{R}^m} = \langle A^Tx, A^Tx \rangle_{\mathbb{R}^n} = \langle x, AA^Tx \rangle_{\mathbb{R}^m}
$$

2. **Positive semidefinite**<br>
   $$
   \langle A^TAx, x \rangle_{\mathbb{R}^n} = \langle Ax, Ax \rangle_{\mathbb{R}^m} \ge 0
   $$

   $$
   \langle AA^Tx, x \rangle_{\mathbb{R}^m} = \langle A^Tx, A^Tx \rangle_{\mathbb{R}^n} \ge 0
   $$

3. **Eigenvalues are non-negative**<br>
   Let $\lambda$ be an eigenvalue of $S = A^TA$ with eigenvector $x \neq 0$. Then
   $$
   \langle Sx, x \rangle_{\mathbb{R}^n} = \langle \lambda x, x \rangle_{\mathbb{R}^n} = \lambda \|x\|^2
   $$
   implying
   $$
   \lambda = \frac{\langle Sx, x \rangle_{\mathbb{R}^n}}{\|x\|^2} \ge 0.
   $$

    