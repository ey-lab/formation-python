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
NumPy's main object is the homogeneous multidimensional array. It is a table of elements (usually numbers), all of the same type, indexed by a tuple of positive integers. NumPy's array class is called ```ndarray```. In order to manipulate NumPy array structure we first have to import numpy package.
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

Wa can select an element from an array by calling the array with the index to pick starting from 0
```python
a[2] # return the 3rd element of the array
a[0] # return the 1st element of the array
```

## NumPy Array declaration
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

## NumPy Basic Operations
Declare 2 arrays
```python
a = np.ones((4,4))
b = np.diag([-2, 0.3, -4, 5])
```

All basic operations can be performed on NumPy arrays such as
 - **Arithmetical operations**
   ```python
   a + b # return sum
   b - a # return difference
   a * b # return pointwised multiplication
   b ** 2 # return the square
   3 * a
   ```
 - **Logical operations**
   ```python
   b == 0 # return a boolean array
   b > a # return a boolean array
   ```
 - **Matrix multiplication**
   ```python
   a.dot(b) # return matricial product
   ```
 - **Universal Functions**
   ```python
   np.exp(b) # return pointwised exponential
   np.sin(b) # return pointwised sinus
   ```
   
** Note that all these operations are *vectorial*. One particularity of these operations is that when they are called, the execution is performed by a low level computing language such as C, C++ or Fortran, consequence of what it makes these operations extremely time efficient **
