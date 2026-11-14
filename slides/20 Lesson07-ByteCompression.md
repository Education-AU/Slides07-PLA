---
title: Byte Compression
template: default
---

The original image matrix is $n\times m$, so it has $nm$ entries. Each entry is a factor $F$ of bytes, so the original
image takes up $Fnm$ bytes.

The compressed image matrix is $n\times k$ for $U_k$, $k\times 1$ for $S_k$, and $k\times m$ for $V_k^T$. So the
compressed image takes up $Fk(n + 1 + m)$ bytes

So the compression ratio may be defined as(or the reciprocal of the compression ratio, depending on how you define it):
$$
\frac{Fnm}{Fk(n + 1 + m)} = \frac{nm}{k(n + 1 + m)}
$$
So in the case of keeping only the first singular value, we have $k=1$, $n=6$, and $m=6$, so the compression ratio is
$$
\frac{6*6}{1*(6 + 1 + 6)} = \frac{36}{13} \approx 2.77
$$  
So approximately we have a compression ratio of 2.77, which means that the compressed image takes up about 36% of the
original image size.
