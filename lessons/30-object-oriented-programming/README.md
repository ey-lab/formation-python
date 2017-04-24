# Python object oriented

Python has been an object-oriented language since it existed. Because of this, creating and using classes and objects are quite easy.


## Creating Classes

The class statement creates a new class definition :

```python
class ClassName:
   'Optional class documentation string'
   class_instructions
```

- The class has a documentation string, which can be accessed via `ClassName.__doc__`

- The *class_instructions* consist of all the component statements defining class members, data attributes and functions

Here is an example of a simple Python class :

```python
class Employee:
   'Common base class for all employees'
   emp_count = 0

   def __init__(self, name, salary):
      self.name = name
      self.salary = salary
      Employee.emp_count += 1

   def display_count(self):
      print("Total Employee %d" % Employee.emp_count)

   def display_employee(self):
      print("Name : ", self.name,  ", Salary: ", self.salary)
```

- The variable `emp_count` is a class variable whose value is shared among all instances of a this class, this can be accessed as `Employee.emp_count` from inside the class or outside the class

- The first method `__init__()` is a special method, which is called class constructor or initialization method that Python calls when you create a new instance of this class

- You declare other class methods like normal functions with the exception that the first argument to each method is `self` (Python adds the `self` argument to the list for you, you do not need to include it when you call the methods)


## Creating Instance Objects

To create instances of a class, you call the class using class name and pass in whatever arguments its `__init__` method accepts :

```python
# This would create first object of Employee class
emp1 = Employee("EY Paris", 2000)
# This would create second object of Employee class
emp2 = Employee("EY Lyon", 500)
```

## Accessing Attributes

You access the object's attributes using the dot operator with object. Class variable would be accessed using class name as follows :

```python
emp1.display_employee()
emp2.display_employee()
print("Total Employee %d" % Employee.emp_count)
```

This produces the following result :

```python
Name :  EY Paris , Salary:  2000
Name :  EY Lyon , Salary:  500
Total Employee 2
```

You can add, remove, or modify attributes of classes and objects at any time :

```python
emp1.age = 7  # Add an 'age' attribute.
emp1.age = 8  # Modify 'age' attribute.
del emp1.age  # Delete 'age' attribute.
```

Instead of using the normal statements to access attributes, you can use some functions :

```python
hasattr(emp1, 'age')    # Returns true if 'age' attribute exists
getattr(emp1, 'age')    # Returns value of 'age' attribute
setattr(emp1, 'age', 8) # Set attribute 'age' at 8
delattr(emp1, 'age')    # Delete attribute 'age'
```

## Built-in class attributes

Every Python class keeps following built-in attributes and they can be accessed using dot operator like any other attribute :

-  `__dict__` : Dictionary containing the class's namespace.

- `__doc__` : Class documentation string or none, if undefined.

- `__name__` : Class name.

- `__module__` : Module name in which the class is defined. This attribute is "__main__" in interactive mode.

- `__bases__` : A possibly empty tuple containing the base classes, in the order of their occurrence in the base class list.


## To go further

#### Static and class methods

A function defined in a class is called a "method". Methods have access to all the data contained on the instance of the object; they can access and modify anything previously set on self. Because they use self, they require an instance of the class in order to be used. For this reason, they're often referred to as "instance methods". But there are other types of methods, which are a bit more esoteric : static and class methods.

These concepts are more advanced, so they won't be covered by this training but you can easily find a lot of tutorials on it, [here is an example](https://jeffknupp.com/blog/2014/06/18/improve-your-python-python-classes-and-object-oriented-programming/).

#### Inheritance

While Object-oriented Programming is useful as a modeling tool, it truly gains power when the concept of inheritance is introduced. Inheritance is the process by which a "child" class derives the data and behavior of a "parent" class.

This concept is also an advanced one. For more details, see for example [this tutorial](www.python-course.eu/python3_inheritance.php).

#### Decorators

In the context of design patterns, **decorators** dynamically alter the functionality of a function, method or class without having to directly use subclasses. This is ideal when you need to extend the functionality of functions that you don't want to modify. This is possible to implement the decorator pattern anywhere, but Python facilitates the implementation by providing much more expressive features and syntax for that.

To discover Python's function decorators in depth, see for example [this tutorial](http://thecodeship.com/patterns/guide-to-python-function-decorators/).


# Exercise 3.1 : Manipulate Python classes objects

Manipulate Python oriented objects with the Python Notebook : [31-oriented-object](/lessons/30-object-oriented-programming/notebooks/31-oriented-object.ipynb).
