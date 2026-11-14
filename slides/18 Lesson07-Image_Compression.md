---
title: Image Compression
showFooter: false
template: two-column
---

So we cut off the singular values and reconstruct the image using only the first four singular values and their
corresponding singular vectors. The reconstructed image is a good approximation of the original image, but with less
detail.

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
NumberOfKept=4
U_r_compressed = U_r[:, :NumberOfKept]
S_r_compressed = np.diag(S_r[:NumberOfKept])
Vt_r_compressed = Vt_r[:NumberOfKept, :]
A_compressed = U_r_compressed @ S_r_compressed @ Vt_r_compressed
rows, cols = np.indices(A_compressed.shape)
fig, ax = plt.subplots()
pixels = ax.scatter(cols.ravel(), rows.ravel(), c=A_compressed.ravel(),
                    cmap="gray", vmin=0, vmax=255, s=500)
ax.set(xlim=(-0.5, 5.5), ylim=(5.5, -0.5), aspect="equal",
       xticks=range(6), yticks=range(6),
       xlabel="Column", ylabel="Row", title="Compressed Image Matrix")
ax.set_facecolor("black")
fig.colorbar(pixels, ax=ax, label="Grayscale intensity")
plt.show()

