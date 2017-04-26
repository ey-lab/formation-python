# NumPy
NumPy is the fundamental package for scientific computing with Python. It is widely used due to the exhaustivity of the functionnalities it covers. Among other things, it contains
 - a powerful N-dimensional array object
 - useful linear algebra, Fourier transform, and random number capabilities
 - efficient multi-dimensional container of generic data

NumPy library uses many dependencies developped in primitive low level languages such as C,C++ or Fortran. This particularity significantly speeds up the exexcution of all NumPy functions. This feature has to be kept in mind at all time when programming with NumPy in order to benefit from the highest power/speed of NumPy.

## Install NumPy
### Mac / Linux
Pre-built binary package can be installed using pip.
```
pip install numpy
```

### Windows
For Windows users consider using a free Python distribution such as Anaconda.

## NumPy Basics
NumPy's main object is the homogeneous multidimensional array. It is a table of elements (usually numbers), all of the same type, indexed by a tuple of positive integers. NumPy's array classis called ```ndarray```. In order to manipulate NumPy array structure we first have to import numpy package.
```python
import numpy as np
```

One way to declare a ```ndarray``` is from a Python list using the command
```python
a = np.array([1, 2, 3])
```

We can inspect an array thanks to multiple methods such as
```python
a.ndim # return the number of dimensions in the array as an int
a.shape # return the shape of the array as a tuple
a.size # return the number of element in the array
```
## Numpy Array declaration
Multiple function are available to declare NumPy arrays such as
```python
array
zeros
zeros_like
ones
ones_like
empty
empty_like
arange
linspace
numpy.random.rand
numpy.random.randn
fromfunction
fromfile
```
