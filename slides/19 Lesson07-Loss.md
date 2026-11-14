---
title: Loss in Image Compression
template: two-column
---

We saw that we could compress the image but can we define a measure of how much we lose of the image

One way is to measure the L2 norm of the difference between the original and compressed image matrices. This gives us a quantitative measure of the loss in image quality due to compression.

The L2 norm can often be interpreted as energy content.

So we can compute the energy loss as follows:
$$
EnergyLoss=\frac{\|A-A_k\|_F^2}{\|A\|_F^2}
$$
Which can be shown to be the same as
$$
EnergyLoss=1-\frac{\sum_{i=k}^{r} \sigma_i^2}{\sum_{i=1}^{r} \sigma_i^2}
$$
EnergyLoss=1-EnergyRetained

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
NumberOfKept=1
EnergyRetained=np.sum(S_r[:NumberOfKept]**2)/np.sum(S_r**2)
EnergyLoss=1-EnergyRetained
print("Energy Retained:", EnergyRetained)
print("Energy Loss:", EnergyLoss)
