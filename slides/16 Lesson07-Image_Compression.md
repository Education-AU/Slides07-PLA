---
title: Image Compression
template: two-column
---

One application of SVD is image compression. The idea is to represent an image as a matrix and then use SVD to
approximate the matrix with a lower rank approximation.

Recall that the SVD of a matrix $A$ is given by $A = U \Sigma V^T$, where $U$ and $V$ are orthogonal matrices
and $\Sigma$ is a diagonal matrix containing the ordered singular values.

Consider a $6 \times 6$ grayscale image: $0$ is black and $255$ is white. Pixels near $200$ form a bright
letter **L** against a dark background near $20$, with small variations in intensity:
<!-- column -->
``` python runnable Image Matrix
import numpy as np
import matplotlib.pyplot as plt

A = np.array([[201, 198, 21, 19, 22, 20],
              [199, 202, 18, 21, 19, 23],
              [203, 200, 22, 18, 20, 19],
              [198, 201, 19, 23, 21, 18],
              [202, 199, 201, 198, 203, 200],
              [200, 203, 199, 202, 198, 201]])
rows, cols = np.indices(A.shape)
fig, ax = plt.subplots()
pixels = ax.scatter(cols.ravel(), rows.ravel(), c=A.ravel(),
                    cmap="gray", vmin=0, vmax=255, s=500)
ax.set(xlim=(-0.5, 5.5), ylim=(5.5, -0.5), aspect="equal",
       xticks=range(6), yticks=range(6),
       xlabel="Column", ylabel="Row", title="Image Matrix")
ax.set_facecolor("black")
fig.colorbar(pixels, ax=ax, label="Grayscale intensity")
plt.show()

```
