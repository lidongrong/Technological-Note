Kernel Density estimation in python:

```py
from sklearn.neighbors import KernelDensity

# must be (size * feature) shape
x=np.random.normal(0,1,(100,1))
kde=KernelDensity().fit(x)
# estimate log likelihood
kde.score_samples(x)
```
