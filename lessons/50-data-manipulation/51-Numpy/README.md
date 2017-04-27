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
   
### Important Remark   
All these operations are said *vectorial*. One particularity of these kind of operations is that when they are called, the execution is performed by low level computing languages such as C, C++ or Fortran, consequence of what it makes these operations extremely time efficient. Keep it in mind, this is probably the feature that makes NumPy so popular.

## Indexing, Slicing and Iterating
In order to select elements from arrays it is possible to perform it in 2 ways (very similar to MatLab).
```python
temperatures = 35 * np.random.rand(50) - 10 # declare an array
```
 - Indexing
   ```python
   temperatures[0] # returns the first element of the array
   temperatures[:10] # returns an array consisting of 10 first elements of the initial array
   temperatures[5:10] # returns an array consisting of the elements from 5th to 9th of the initial array
   temperatures[-1] # returns the last element in the array 
   temperatures[-5:] # returns an array consisting the last 5 elements of the initial array
   ```
 - Slicing
   ```python
   temperatures[temperatures > 0] # returns an array consisting of the positive calues cf the initial array
   ```
## Data manipulation
NumPy allows to perform easily perform actions on data arrays such as
 - Sorting
   ```python
   np.sort(temperatures) # returns the sorted array
   np.argsort(temperatures) # returns the index of the sorted array
   ```
 - Aggregating
   ```python
   temperatures.max() # returns the maximum value
   temperatures.min() # returns the minimum value
   temperatures.mean() # returns the average
   temperatures.std() # returns the  standard deviation
   ```
   
