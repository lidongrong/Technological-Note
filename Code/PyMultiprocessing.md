Use starmap() to multiprocess your task:

```python
import multiprocessing as mp
from multiprocessing import Pool

if __name__ == '__main__':
  # specify number of cores
  pool=Pool(16)
  
  def func(m,n):
    return m,n,m*n

  m1=[1,2,3,4]
  m2=[5,6,7,8]
```

To apply func() on m1 and m2, we can call starmap() to perform multiprocessing:

```python
result=pool.starmap(func,[(m1[i],m2[i]) for i in range(0,4)])
```

where (m1[i],m2[i]) are parameters of each call and all prameters are packed in a list.

The returned object result is a Python list (should later be converted to array). Specifically, it is a 4x3 list in this case, where each roll stores the output 
returned from each call (i.e. each thread)
