# Python Training :snake:

**Topics Covered In This Course:**

**Part I**
- [x] [Introduction](introduction.md)
- [x] [Data Types](variables.py)
- [x] [Strings and Concatenation](string_casting.py)
- [x] [Built-in Methods Examples](string_casting.py) 
- [x] [Importing built-in methods](math_functions.py) 
- [x] [More Built-in Functions with Python](https://docs.python.org/3/library/functions.html)
- [x] [Indexing And Slicing](slicing.md)
- [x] [List](lists.py)
- [x] [Dictionaries](dictionaries.py)
- [x] [Tuples](tuples.py)
- [x] [Functions](function.py)
- [x] [Variable-Length Arguments (*args, **kwargs)](kwargs.md)
- [x] [Object-Oriented Programming](OOP.md) :fire:
- [x] [Control Flow](control_flow.py)
- [x] [Sets](sets.py)
- [x] [Loops](loops.py)
- [x] [HTTP Requests and Python APIs](../Week4_Python/APIs)

For part II  [Click Here](/docs/Week4_Python)

## **Terminology**

**Abstraction**
- Abstraction focuses on hiding the internal implementations of a process or method from the user. In this way, the user knows what he is doing but not how the work is being done. 

---

**Control Flow**
- The order in which the program's code executes
- The control flow of a Python program is regulated by conditional statements, loops, and function calls

```python
# Control Flow Statements with If
required_age = 18
age = int(input("How old are you?"))

if age < 18:
    print("You are too young to watch this movie.\nThe required age to watch this movie is {}".format(str(required_age)))
else:
    print("Congratulations!\nYou are old enough to watch the movie! Enjoy!")
```
---

**Dictionary**
- An unordered collection of data values, used to store data values like a map
- Dictionary holds key:value pair
- Key value is provided in the dictionary to make it more optimised
- We use curly brackets {} to create a dictionary, separated by 'comma'
- Values in a dictionary can be of any data type and can be duplicated, whereas keys cannot be repeated and must be immutable
- Dictionaries are accessed via keys and not via their index position
- Can be nested
- Are mutable

```python
student_record = {
    "name": "Anais",
    "stream": "DevOps",
    "completed_lesson": 5,
    "completed_lesson_names": ["Business Skills", "SQL", "Python"]
}
```
`del student_record["stream"]`
or
`student_record.pop("stream")`

Outcome
```python
student_record = {
    "name": "Anais",
    "completed_lesson": 5,
    "completed_lesson_names": ["Business Skills", "SQL", "Python"]
}
```
---

**Collections**
- Containers used to store collections of data, e.g. list, dict, set, tuple
- They have different characteristics based on the declaration and the usage.
- Built-in Python module that implements specialised container datatypes.
- Developed to provide additional data structures to store collections of data. 
- Examples: 
    - OrderedDict
    - defaultdict
    - counter
    - namedtuple
    - deque

**OrderedDict**
```python
from collections import OrderedDict

roll_no = OrderedDict([
(11, 'Anais'),
(9, 'Severus'),
(17, 'Jonty'),
])

for key, value in roll_no.items():
print(key, value)
```

**Output:**
```python
(11, 'Anais')
(9, 'Severus'),
(17, 'Jony')
```
The output order is exactly the same as the order of insertion. 

---
**Dynamic vs Static**
- Python is dynamically typed meaning variable names (unless `NULL`) is bound only to an object
- Data type determined at run time, not in advance, so no need to specify type of variable.
- This makes python a strongly typed language (type checking happens at run time), python interpreter keeps track of all variables types. 
- In python, it is the program's responsibility to use built-in functions like `isinstance()` or `issubclass` to test variable types.

**Python (Dynamically Typed):**
```python
num = 5
```

**Java (Statically Typed):**
```java
int num;
num = 5;
```

**Python: strongly typed**
- In python, you cannot perform operations inappropriate to the type of object e.g adding numbers to strings
```python
'x' + 3
>>> # Returns error. Integer MUST be converted to string 
```

**Javascript: weakly typed**
- Compiler/interpreter sometimes changes the type of variable
```javascript
'x' + 3
>>> x3
```
Above program is problematic. Instead of raising exception, execution will continue but variables now have wrong and unexpected values.

---

**Encapsulation**
- Concept of encapsulation is to keep together the implementation (code) and the data it manipulates (variables). 
- In python, we can **restrict** access to methods and variables. This prevents data from being modified (encapsulation).
- In python, we denote private attributes using underscore `_` or dunder (double underscore) `__` as the prefix.

---
**Function**
- A block of organised, reusable code that is used to perform a single, related action
- DRY *Don't* *Repeat* *Yourself*
- You can pass data (parameters), into a function.

```python
def greet(name):
    name = input("What is your name? \n")
    return "Hello, " + name + " Good morning!"
```

---
**List**
- A data structure that is mutable, or changeable.
- Each element or value that is inside of a list is called an item.
- Lists are defined by having values between square brackets []

```python
cities = ["Paris", "Hong Kong", "Buenos Aires", "London,", "Tel Aviv", "Amsterdam"]
print(cities)
```

---
**Inheritance**
- Inheritance is a way of creating a new class for using details of an **existing** class without modifying it. The newly formed class is a derived class (or child class). Similarly, the existing class is a base class(or parent class).

---
**Loops**
- There are two types of loops, for and while 
- For loops can iterate over a sequence of numbers using the 'range' and 'xrange' functions
- While loops repeat as long as a certain boolean condition is met

```python
list_data = [1, 2, 3]

# Using for 
# Prints 1, 2, 3
for n in list_data:
    print(n)

# Using while
# Prints out the numbers 0, 1, 2, 3, 4
for x in range(5):
    print(x)
```

---
**Sets**
- An unordered collection data type that is iterable, mutable and has no duplicate elements
- They are very similar to lists but it has a highly optimised method for checking whether a specific element is contained in the set.
- This is based on a data structure known as a has table

```python
# Normal Set
# Prints b, c, a, d
normal_set = set(["a", "b", "c"])
normal_set.add("d")
print(normal_set)

# Frozen Set
# Prints f, e, g, cannot use 'add' attribute 
frozen_set = frozenset(["e", "f", "g"])
print(frozen_set)
```

---

**Polymorphism**
- Refers to the ability of an object taking many forms. 
- Python being an OOP supports Polymorphism through Method overriding and operator overloading. 
- Polymorphism can be achieved through inheritance - Method overriding
- Method overriding provides ability to change the implementation of a method in a child class which is already defined in one of its super class or parent class. 
- If there is a method in a super class the method having the same name number of arguments in a child class is said to be **overriding** the parent class method. 
- We can use the concept of polymorphism while creating class methods as Python allows different classes to have methods with the same name. 
- We can then later generalise calling these methods by disregarding the object we are working with. 

---
**Tuple**
- They are the same as lists but immutable meaning they cannot be changed
- Tuples use parenthesis ()

```python
dob = ("name", "dob", "passport number")
print(dob)
```
---

**Variable**
- Another name for placeholder
- A reserved memory location to store data values 
- Variables can be declared by any name 
```python
this_is_variable = 19
this_is_another_variable = "Hello World"
this_is_also_a_variable = (str(this_is_variable) + this_is_another_variable)
``` 

---
**List** vs **tuple** vs **set** vs **dictionary**

[List](lists.py) []
- mutable, stores duplicate values, elements accessed using indexes, ordered collection
- Methods = `.append()`, `.remove()`, `.insert()`, `.pop()`
- `.remove()` removes first matching value, `del list_name[index]` removes item at specific index. `.pop()` removes item at specific index and returns it.

[Tuple](tuples.py) ()
- Like a list but immutable, stores duplicate values, ordered collection, accessed using indexes.
- Methods = `.add()`, `.discard()`, `.count()`, `.del`

[Set](sets.py) ()
- Unordered, not indexed, does not store duplicate entries
- Methods = `.add()`, `.clear()`, `.update()`, `.remove()`

[Dictionary](dictionaries.py) {key:value}
- Key value pairs, mutable, unordered
- Methods = `.items()`, `.keys()`, `.values()`
- More useful than lists when mapping unique keys to values
- Dict elements accessed via keys NOT position of items so slicing cannot happen.
- `.pop("key")` method to remove entry in dictionary or `del`

---

> Common Python Interview Questions [HERE](https://www.guru99.com/python-interview-questions-answers.html)


