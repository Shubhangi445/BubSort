# LinearRegExample

import numpy as np
import matplotlib.pyplot as plt
import pandas as pd

X = np.random.randn(100)
y = 5 + 7 * X + np.random.randn(100)

plt.scatter(X,y)
plt.show()

X = np.c_[X,np.ones(100)]

theta = np.linalg.inv(X.T @ X) @ (X.T @ y)
#theta=(X^T.X^(-1))((X^T).y)
#T = transpose function in X and y
# @ represents dot product
#inv = inverse
#linalg = linear algebra
#hence proved linear reg for univariate
