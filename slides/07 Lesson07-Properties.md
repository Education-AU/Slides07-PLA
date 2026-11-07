---
title: Properties
template: default
---

#### Kernel

$\ker (A^TA)=\ker (A) \text{ and } \ker (AA^T)=\ker (A^T)$

Obviously

$x\in \ker (A) \Rightarrow x\in \ker (A^TA)$

conversely

$x\in \ker (A^TA)\Rightarrow 0=\langle A^TAx,x \rangle= \langle Ax,Ax \rangle \Rightarrow Ax=0 \Rightarrow x\in \ker (A)$

#### Rank

$\operatorname{rank} (A^TA)=\operatorname{rank} (A) \text{ and } \operatorname{rank} (AA^T)=\operatorname{rank} (A^T)$

From rank nullity theorem we have

$\dim (\ker (A^TA))+\operatorname{rank} (A^TA)=\dim (\mathbb{R}^n)=n$

and since the $\ker (A)=\ker (A^TA)$ and they act on the same
domain $\operatorname{rank} (A)=\operatorname{rank} (A^TA)$

$\dim (\ker (AA^T))+\operatorname{rank} (AA^T)=\dim (\mathbb{R}^m)=m$

and since the $\ker (A^T)=\ker (AA^T)$ and they act on the same
domain $\operatorname{rank} (A^T)=\operatorname{rank} (AA^T)$

