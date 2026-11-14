---
title: Image Compression
showFooter: false
template: two-column
---

We now make the SVD decomposition and notice that the singular values are
```
S =
 [8.30104759e+02 3.47362929e+02 8.27548376e+00 4.12090313e+00
 2.52051507e+00 5.15628893e-01]
```

So relative to the first singular value, the last two are very small. This means that we can approximate the image using only the first four singular values and their corresponding singular vectors.

<!-- column -->
``` python runnable Image Matrix SVD
import numpy as np
import matplotlib.pyplot as plt

A = np.array([[201, 198, 21, 19, 22, 20],
              [199, 202, 18, 21, 19, 23],
              [203, 200, 22, 18, 20, 19],
              [198, 201, 19, 23, 21, 18],
              [202, 199, 201, 198, 203, 200],
              [200, 203, 199, 202, 198, 201]])

U_r, S_r, Vt_r = np.linalg.svd(A, full_matrices=False)
print("U =\n", U_r)
print("S =\n", S_r)
print("V^T =\n", Vt_r)
