Way to plot posterior in python:

```{py}
import arviz as az
```

Package arviz produces various APIs for Bayesian EDA.

Assume we have 2 parameters specified by a dictionary:

```py
dick={
'a':np.random.randn(100,1),
'b':np.random.randn(100,2,2)
}
```
Notice a is one dimensional and b is a 2x2 matrix.

More over, b has shape (100,2,2). If we have a posterior data with shape (n,d), then we shall expand its dim by:
```
b=np.expand_dims(b,0)
```
to turn it to shape(1,n,d)

Then we can:
```
dataset=az.convert_to_inference_data(dick)
az.plot_posterior(dataset,var_names='a')
```
and get the density plot.
