# Introduction to Python programming

## Syntax

Python was designed to be a highly readable language and aims to be simple and consistent in the design of its syntax.

PEP8 gives coding conventions for the Python code : [Style Guide for Python Code](https://www.python.org/dev/peps/pep-0008/). For example, it is recommended to respect a maximum line length of 79 characters.

#### Code structuration

- The statements are separated by semicolons : `;` or (and preferably) by line breaks
- Comments are preceded by the symbol `#`
- The blocks of instructions are delimited by their alignment on the same tabulation :
 - this particularity of the language compels to create well-structured codes
 - it is recommended to use spaces to achieve indentation

Example :

```python
# This is a comment
def foo(x):
    if x == 0:
        my_function1()
    else:
        my_function2(x)
        my_function2(x - 1)
```

#### Assigning values to variables

Python variables do not need explicit declaration to reserve memory space. The declaration happens automatically when you assign a value to a variable. The equal sign (=) is used to assign values to variables :

```python
>>> my_variable = 1
>>> print(my_variable)
1
```

You can also assign several variables in the same line : 

```python
>>> a, b, c = 1, 2, "john"
>>> print(a)
1
>>> print(c)
john
```

## Control structures

#### *If...else* statement

The syntax of the *if...else* statement is :

```python
if expression1:
   statement(s)
else:
   statement(s)
```

The elif statement allows you to check multiple expressions for TRUE and execute a block of code as soon as one of the conditions evaluates to TRUE :

```python
if expression1:
   statement(s)
elif expression2:
   statement(s)
elif expression3:
   statement(s)
else:
   statement(s)
```

#### Loops

The syntax for a *for* loop is the following :

```python
for iterating_var in sequence:
   statements(s)
```

A while loop statement in Python programming language repeatedly executes a target statement as long as a given condition is true :

```python
while expression:
   statement(s)
```

The loop can be stopped with one one these statements :

```python
break
```

It terminates the current loop and resumes execution at the next statement, just like the traditional break statement in C.

The most common use for break is when some external condition is triggered requiring a hasty exit from a loop. The break statement can be used in both while and for loops.

```python
continue
```

It returns the control to the beginning of the while loop.. The continue statement rejects all the remaining statements in the current iteration of the loop and moves the control back to the top of the loop.

The continue statement can be used in both while and for loops.


## Typing

Python has five standard data types : 

- Numbers
- String
- List
- Tuple
- Dictionary

#### Numbers

Number data types store numeric values. Python supports four different numerical types :

- int (signed integers)
- long (long integers, they can also be represented in octal and hexadecimal)
- float (floating point real values)
- complex (complex numbers)

#### String

Strings in Python are identified as a contiguous set of characters represented in the quotation marks. Python allows for either pairs of single or double quotes. Subsets of strings can be taken using the slice operator (`[ ]` and `[:]`) with indexes starting at 0 in the beginning of the string and working their way from -1 at the end.

The plus (+) sign is the string concatenation operator and the asterisk (*) is the repetition operator.

Example :

```python
str = 'Hello World!'
print(str)          # Prints complete string
print(str[0])       # Prints first character of the string
print(str[2:5])     # Prints characters starting from 3rd to 5th
print(str[2:])      # Prints string starting from 3rd character
print(str * 2)      # Prints string two times
print(str + "TEST") # Prints concatenated string
```

This will produce the following result :

```python
Hello World!
H
llo
llo World!
Hello World!Hello World!
Hello World!TEST
```

#### List

A list contains items separated by commas and enclosed within square brackets ([]). One particularity of Python is that all the items belonging to a list can be of different data type.

The values stored in a list can be accessed using the slice operator (`[ ]` and `[:]`) with indexes starting at 0 in the beginning of the list and working their way to end -1. The plus (+) sign is the list concatenation operator, and the asterisk (*) is the repetition operator.

Example :

```python
list = [ 'abcd', 786 , 2.23, 'john', 70.2 ]
tinylist = [123, 'john']

print(list)           # Prints complete list
print(list[0])        # Prints first element of the list
print(list[1:3])      # Prints elements starting from 2nd till 3rd 
print(list[2:])       # Prints elements starting from 3rd element
print(tinylist * 2)   # Prints list two times
print(list + tinylist) # Prints concatenated lists
```

This produce the following result :

```python
['abcd', 786, 2.23, 'john', 70.200000000000003]
abcd
[786, 2.23]
[2.23, 'john', 70.200000000000003]
[123, 'john', 123, 'john']
['abcd', 786, 2.23, 'john', 70.200000000000003, 123, 'john']
```

#### Tuple

A tuple is another sequence data type that is similar to the list. A tuple consists of a number of values separated by commas. Unlike lists, however, tuples are enclosed within parentheses.

The main differences between lists and tuples are: Lists are enclosed in brackets (`[ ]`) and their elements and size can be changed, while tuples are enclosed in parentheses (`( )`) and cannot be updated. Tuples can be thought of as **read-only** lists.

```python
tuple = ( 'abcd', 786 , 2.23, 'john', 70.2  )
tinytuple = (123, 'john')

print(tuple)             # Prints complete list
print(tuple[0])          # Prints first element of the list
print(tuple[1:3])        # Prints elements starting from 2nd till 3rd
print(tuple[2:])         # Prints elements starting from 3rd element
print(tinytuple * 2)     # Prints list two times
print(tuple + tinytuple) # Prints concatenated lists
```

This produce the following result :

```python
('abcd', 786, 2.23, 'john', 70.200000000000003)
abcd
(786, 2.23)
(2.23, 'john', 70.200000000000003)
(123, 'john', 123, 'john')
('abcd', 786, 2.23, 'john', 70.200000000000003, 123, 'john')
```

#### Dictionary

Python's dictionaries are kind of hash table type. They work like associative arrays or hashes found in Perl and consist of key-value pairs. A dictionary key can be almost any Python type, but are usually numbers or strings. Values, on the other hand, can be any arbitrary Python object.

Dictionaries are enclosed by curly braces (`{}`) and values can be assigned and accessed using square braces (`[]`).

```python
dict = {}
dict['one'] = "This is one"
dict[2]     = "This is two"

tinydict = {'name': 'john','code':6734, 'dept': 'sales'}

print(dict['one'])         # Prints value for 'one' key
print(dict[2])             # Prints value for 2 key
print(tinydict)            # Prints complete dictionary
print(tinydict.keys())     # Prints all the keys
print(tinydict.values())   # Prints all the values
```

This produce the following result :

```python
This is one
This is two
{'dept': 'sales', 'code': 6734, 'name': 'john'}
['dept', 'code', 'name']
['sales', 6734, 'john']
```

Dictionaries have no concept of order among elements. It is incorrect to say that the elements are "out of order"; they are simply unordered.

# Exercise 2.1 : Manipulate Python typing

Manipulate the different types of variables with the Python Notebook : [21-variables-typing](lessons/20-python-programming/notebooks/21-variables_typing.ipynb).


## Operations on lists

#### Specific functions

The list data type has some more methods. Here are all of the methods of list objects:

	list.append(x)

Add an item to the end of the list; equivalent to a[len(a):] = [x].

	list.extend(L)

Extend the list by appending all the items in the given list; equivalent to a[len(a):] = L.

	list.insert(i, x)

Insert an item at a given position. The first argument is the index of the element before which to insert, so a.insert(0, x) inserts at the front of the list, and a.insert(len(a), x) is equivalent to a.append(x).

	list.remove(x)

Remove the first item from the list whose value is x. It is an error if there is no such item.

	list.pop([i])

Remove the item at the given position in the list, and return it. If no index is specified, a.pop() removes and returns the last item in the list. (The square brackets around the i in the method signature denote that the parameter is optional, not that you should type square brackets at that position. You will see this notation frequently in the Python Library Reference.)

	list.index(x)

Return the index in the list of the first item whose value is x. It is an error if there is no such item.

	list.count(x)

Return the number of times x appears in the list.

	list.sort(cmp=None, key=None, reverse=False)

Sort the items of the list in place (the arguments can be used for sort customization, see sorted() for their explanation).

	list.reverse()

Reverse the elements of the list, in place.

Example :

```python
>>> a = [66.25, 333, 333, 1, 1234.5]
>>> print(a.count(333), a.count(66.25), a.count('x'))
2 1 0
>>> a.insert(2, -1)
>>> a.append(333)
>>> a
[66.25, 333, -1, 333, 1, 1234.5, 333]
>>> a.index(333)
1
>>> a.remove(333)
>>> a
[66.25, -1, 333, 1, 1234.5, 333]
>>> a.reverse()
>>> a
[333, 1234.5, 1, 333, -1, 66.25]
>>> a.sort()
>>> a
[-1, 1, 66.25, 333, 333, 1234.5]
>>> a.pop()
1234.5
>>> a
[-1, 1, 66.25, 333, 333]
```

#### List Comprehensions

List comprehensions provide a concise way to create lists. Common applications are to make new lists where each element is the result of some operations applied to each member of another sequence or iterable, or to create a subsequence of those elements that satisfy a certain condition.

For example, assume we want to create a list of squares, like:

```python
>>> squares = []
>>> for x in range(10):
...     squares.append(x**2)
...
>>> squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

We can obtain the same result with:

```python
squares = [x**2 for x in range(10)]
```

This is also equivalent to `squares = map(lambda x: x**2, range(10))`, but it’s more concise and readable.

This is also possible to add some conditions :

```python
>>> [(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]
[(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]
```

## Functional Programming Tools

There are three built-in functions that are very useful when used with lists: filter(), map(), and reduce().

	filter(function, sequence)

Returns a sequence consisting of those items from the sequence for which function(item) is true.

```python
>>> def f(x):
>>> 	return x % 3 == 0 or x % 5 == 0
...
>>> filter(f, range(2, 25))
[3, 5, 6, 9, 10, 12, 15, 18, 20, 21, 24]
```

	map(function, sequence)

Calls function(item) for each of the sequence’s items and returns a list of the return values.

```python
>>> def cube(x):
>>> 	return x*x*x
...
>>> map(cube, range(1, 11))
[1, 8, 27, 64, 125, 216, 343, 512, 729, 1000]
```

	reduce(function, sequence)

Returns a single value constructed by calling the binary function function on the first two items of the sequence, then on the result and the next item, and so on.

```python
>>> def add(x,y):
>>> 	return x+y
...
>>> reduce(add, range(1, 11))
55
```


## Python Modules

#### Import a library

You can use any Python source file as a module by executing an import statement in some other Python source file. The import has the following syntax :

```python
import module
```

You can also import specific attributes from a module into the current namespace with the following syntax :

```python
from module import function
```

This statement does not import the entire module `module` into the current namespace; it just introduces the item `function` from the module `module` into the global symbol table of the importing module.

It is also possible to import all names from a module into the current namespace by using the following import statement :

```python
from module import *
```

This provides an easy way to import all the items from a module into the current namespace; however, this statement should be used sparingly.

For further details about importing a library, [see explanations about the PYTHONPATH](http://sametmax.com/les-imports-en-python/).

#### Some classical packages

The most used scientific modules are :

	os / sys

The `os` and `sys` modules provide numerous tools to deal with filenames, paths, directories. The `os` module contains two sub-modules `os.sys` (same as `sys`) and `os.path` that are dedicated to the system and directories respectively.

	pandas

A module that implements tools and objects to easily and quickly manipulate complex data structures

	scipy / numpy

Framework for scientific computing (interpolation, integration, linear algebra, etc.)

	scikit-learn

Set of tools for data mining and data analysis

	matplotlib

Library for high-quality 2D scientific graphics

	statsmodels

Module allowing to carry out classic models of statistics


# Exercise 2.2 : Create your own functions

See an example of function in the Python Notebook : [22-define-functions](lessons/20-python-programming/notebooks/22-define-functions.ipynb) and create your own one.


# Exercise 2.3 : Create your own functions

See an example of a module import with the Python Notebook : [23-import-module](http://localhost:8888/notebooks/Desktop/formation-python/lessons/20-introduction-to-python-programming/notebooks/23-import-module.ipynb).
