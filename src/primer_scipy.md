---
jupyter:
  jupytext:
    formats: ipynb,md
    text_representation:
      extension: .md
      format_name: markdown
      format_version: '1.3'
      jupytext_version: 1.17.3
  kernelspec:
    display_name: Python 3
    language: python
    name: python3
---

Scientific Computations: Scipy
===============

In the numpy primer, we saw how we can use the numpy module to represend data as
true multidimensional arrays that we can operate on efficiently and in a way
that mirrors how we do science and engineering math.

What about more complex operations though? How do we find the root of a function? What about integrating a system of equations?

Fear not. We have the scipy module. Now, Numpy *does* include methods to perform some of the topics we approach here, but not all and not with as much flexibility or efficiency.

## Function optimization and root-finding
One of the age-old questions of engineering and science is **How do we find the zero of a function, i.e. how do we find the value of x_0 such that the function F(x) satisfies F(x_0)=0?** Another related question is **For which value x_{min} is F(x) a minimum, i.e. F(x_{min}) < F(x) for all other values of x?** (This question can be turned to a maximum and it's the same question.)

Let's look at some random function to test our algorithms. We'll use the following function

F(x) = e^x - 3.

That function has a zero F(x) = 0 for e^x = 3 or x = ln(3).

We can define and test our function with the following code. We can even check that our zero is indeed in the correct place.

```python
import numpy as np
import scipy.optimize as opt

def fnc(x):
    return np.exp(x)-3

x0 = np.log(3)
print(fnc(x0))
```

## Function integration

### Quadrature

### Integrating a system of equations
