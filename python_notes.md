# Python Notes

## Variables and Data Types
Python has a simple and intuitive syntax for defining variables and assigning values to them. The data type of a variable is automatically inferred based on the value assigned to it. However, you can also explicitly specify the data type of a variable using type casting. <br>
<br>
Link: [Official documentation on Python data types](https://docs.python.org/3/library/datatypes.html) <br>
<br>
**NOTE:** Best practice in Python is to name variables all **lower case**, with **underscores** between words. <br>
So `my_string` instead of `myString` or `is_valid` instead of `isValid`. <br>

```python
# integer variable
x = 10
print(x)  # output: 10

# float variable
y = 3.14
print(y)  # output: 3.14

# string variables
name = 'Alice'
print(name)  # output: Alice
last_name = "Little"
print(last_name) # output: Little
# NOTE: single & double quotes accepted

# boolean variable
is_valid = True
print(is_valid)  # output: True
is_valid = False
print(is_valid)  # output: False
# NOTE: booleans have to start with a capital letter

# list variable
numbers = [1, 2, 3, 4]
print(numbers)  # output: [1, 2, 3, 4]
```

## Strings in Python
### String declaration
String declaration in Python is done by enclosing a sequence of characters within quotes. Python supports both single quotes ('...') and double quotes ("...") to declare strings. <br>

```python
my_string = "Hello, World!"

print(my_string) # Output: Hello, World!
```

### String concatenation
String concatenation is the process of combining two or more strings into a single string. In Python, we can use the '+' operator to concatenate two or more strings. <br>

```python
string1 = "Hello"
string2 = "World"

concatenated_string = string1 + " " + string2

print(concatenated_string) # Output: Hello World
```

### Escape characters 
Escape characters are special characters that are used to represent characters that are difficult or impossible to type into a string. If we want to include a quotation mark within a string, we need to use an escape character (\\) before the quotation mark. The most commonly used escape characters in Python are: <br>

* \\n - newline
* \\t - tab
* \\' - single quote
* \\" - double quote

```python
print("Hello\nWorld") 
# Output: 
# Hello
# World

print("He said, \"Hello World!\"") # Output: He said, "Hello World!"

print("C:\\Users\\John\\Documents") # Output: C:\Users\John\Documents

print("Name:\tJohn") # Output: Name:    John

print('He said, "I\'m busy."') # Output: He said, "I'm busy."
```

### String functions
Python provides a wide range of string manipulation functions that can be used to modify and analyze strings. These functions make it easy to perform common string operations such as finding substrings, replacing text, and converting case. String functions in Python are essential to many programming tasks, from data cleaning and formatting to web scraping and natural language processing. <br>
<br>
Link: [The official documentation for string functions in Python](https://docs.python.org/3/library/stdtypes.html#string-methods) on the Python Software Foundation's website. <br>

```python
my_string = "Hello, World!"

# len(): Returns the length of a string
print(len(my_string)) # Output: 13

# str.lower(): Returns a string in all lowercase letters
print(my_string.lower()) # Output: hello, world!

# str.upper(): Returns a string in all uppercase letters
print(my_string.upper()) # Output: HELLO, WORLD!

# str.capitalize(): Returns a string with the first letter capitalized
print(my_string.capitalize()) # Output: Hello, world!

# str.title(): Returns a string with the first letter of each word capitalized
print(my_string.title()) # Output: Hello, World!

# str.replace(): Returns a string with all occurrences of a substring replaced with another substring
print(my_string.replace("Hello", "Hi")) # Output: Hi, World!

# str.split(): Splits a string into a list of substrings, separated by a specified delimiter
print(my_string.split(",")) # Output: ['Hello', ' World!']

# str.startswith(): Checks if a string starts with a specified substring and returns a boolean value
print(my_string.startswith("Hello")) # Output: True

# str.upper(): Is used to convert the string to uppercase, 
# str.isupper(): Checks if all the characters in the string are uppercase.
print(my_string.upper().isupper()) # Output: True

# str.[i]: Accessing the character in the string using the appropriate index
print(my_string[0]) # Output: "H"

# str.index(): Find the index of the first occurrence of the letter or substring given as the parameter.
print(my_string.index("o"))  # Output: 4
print(my_string.index("or")) # Output: 8

# str.endswith(): Checks if a string ends with a specified substring and returns a boolean value
print(my_string.endswith("World!")) # Output: True

# str.join(): Concatenates a list of strings into a single string, separated by a specified delimiter
my_list = ["Hello", "World"]
print(", ".join(my_list)) # Output: Hello, World

# str.strip(): Returns a string with leading and trailing whitespace removed
my_string = "  hello, world!  "
print(my_string.strip()) # Output: hello, world!
```

## Numbers in Python
Python is a popular programming language that is widely used for working with numbers and performing mathematical operations. Python provides a wide range of built-in functions and libraries for working with numbers, making it easy to perform simple or complex mathematical computations. <br>

### Types of Numbers
In Python, there are different types of numbers that you can work with. The most common types of numbers are integers, floating-point numbers, and complex numbers. <br>
Here's an overview of these different number data types with examples: <br>

```python
# Integers
x = 10
y = -5
z = 0
print(type(x))  # Output: <class 'int'>
print(type(y))  # Output: <class 'int'>
print(type(z))  # Output: <class 'int'>

# Floating-point numbers
a = 3.14
b = -2.5
c = 0.0
print(type(a))  # Output: <class 'float'>
print(type(b))  # Output: <class 'float'>
print(type(c))  # Output: <class 'float'>

# Complex numbers
m = 2 + 3j
n = 4 - 2j
o = 0 + 1j
print(type(m))  # Output: <class 'complex'>
print(type(n))  # Output: <class 'complex'>
print(type(o))  # Output: <class 'complex'>
```

### Math Operators
Let's look at some examples of basic math operations. In the following code block, we will perform addition, subtraction, multiplication, division, and modulus operations on two numbers: <br>

```python
# Addition
x = 10
y = 5
result = x + y
print("The result of addition is:", result)
# Output: The result of addition is: 15

# Subtraction
x = 10
y = 5
result = x - y
print("The result of subtraction is:", result)
# Output: The result of subtraction is: 5 

# Multiplication
x = 10
y = 5
result = x * y
print("The result of multiplication is:", result)
# Output: The result of multiplication is: 50 

# Division
x = 10
y = 5
result = x / y
print("The result of division is:", result)
# Output: The result of division is: 2.0 

# Modulus
x = 10
y = 5
result = x % y
print("The result of modulus is:", result)
# Output: The result of modulus is: 0 
```

### Order of Math Operations
In Python, the order of math operations is determined by the rules of operator precedence. It's important to be aware of these rules when performing complex calculations, as they can affect the outcome of the calculation. Here are some examples of how to determine the order of math operations in Python: <br>

```python
# Example 1
result = 10 + 5 * 2
print(result)  # Output: 20

# Example 2
result = (10 + 5) * 2
print(result)  # Output: 30

# Example 3
result = 10 / 2 * 3
print(result)  # Output: 15.0

# Example 4
result = 10 / (2 * 3)
print(result)  # Output: 1.6666666666666667
```

### The Modulus Operator
The modulus operator **%** returns the remainder of a division operation. It can be used to perform various calculations, such as determining if a number is even or odd, or if it's divisible by another number. <br>

```python
# Example 1 - Checking if a number is even or odd
num1 = 10
if num1 % 2 == 0:
    print(f"{num1} is even")
else:
    print(f"{num1} is odd")
# Output: 10 is even 

num2 = 5
if num2 % 2 == 0:
    print(f"{num2} is even")
else:
    print(f"{num2} is odd")
# Output: 5 is odd 

# Example 2 - Checking if a number is divisible by another number
num3 = 15
if num3 % 5 == 0:
    print(f"{num3} is divisible by 5")
else:
    print(f"{num3} is not divisible by 5")
# Output: 15 is divisible by 5 

num4 = 7
if num4 % 3 == 0:
    print(f"{num4} is divisible by 3")
else:
    print(f"{num4} is not divisible by 3")
# Output: 7 is not divisible by 3 
```

### Numbers & Strings
Combining numbers with strings is a common task in Python programming. It allows you to create dynamic messages, labels, and data summaries that include both text and numeric values. Python provides several ways to combine numbers and strings and to transform both data types vice versa. Following some common examples. <br>

```python
# Numbers in strings
string_with_numbers = "I have 5 apples and 3 bananas"
numbers_list = [int(s) for s in string_with_numbers.split() if s.isdigit()]
print(numbers_list)  # Output: [5, 3]
# split(): This splits the string into a list of words, using whitespace as the delimiter: ["I", "have", "5", "apples", "and", "3", "bananas"].
# if s.isdigit(): This condition checks whether each element of the list is a digit or not. If it is, the element is included in the list comprehension.
# int(s): This converts each element that is a digit (i.e., a string containing only numbers) to an integer using the int() function.

# Transform numbers to strings
num = 42
string_num = str(num)
print(type(string_num))  # Output: <class 'str'>

# Transform string number values to numbers
string_num = "123"
num = int(string_num)
print(type(num))  # Output: <class 'int'>

# Number variable in string
age = 25
print("I am " + str(age) + " years old.")  # Output: "I am 25 years old."

# Another example
price = 12.99
quantity = 3
total = price * quantity
print("The total cost is $" + str(total))  # Output: "The total cost is $38.97"

# Using f-strings
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")  # Output: "My name is Alice and I am 25 years old."
# The f before the opening quotation mark indicates that the string is an f-string, and any expressions inside curly braces {} will be evaluated and inserted into the string.

# Using string formatting
name = "Bob"
age = 35
print("My name is {} and I am {} years old.".format(name, age))  # Output: "My name is Bob and I am 35 years old."
# The curly braces {} are used as placeholders for the values, and the values are passed to the str.format() method as arguments.

# Using % formatting
name = "Charlie"
age = 45
print("My name is %s and I am %d years old." % (name, age))  # Output: "My name is Charlie and I am 45 years old."
# We're using % formatting to embed the values of the name and age variables into the string. 
# %s is a placeholder for a string. %d is a placeholder for an integer. 
```

### Number Functions
Python provides a wide range of built-in functions that allow you to perform various operations on numbers. In the following code block you can see examples of some of the most common number functions in Python (excluding **math** module). <br>

```python
# Absolute value
print(abs(-10))  # Output: 10
# abs(x) returns the absolute value of x.

# Power
print(pow(2, 3))  # Output: 8
# pow(x, y) returns x raised to the power of y.

# Maximum 
print(max(1, 5, 3, 2))  # Output: 5
# max(iterable) returns the largest item in the iterable.

# Minimum
print(min(-3, -1, -5))  # Output: -5
# min(iterable) returns the smallest item in the iterable.

# Rounding
print(round(3.14159, 2))  # Output: 3.14
# round(number, ndigits) rounds number to ndigits decimal places.
```

### **math** Module
In Python, math is a built-in module that provides various mathematical functions and constants. When you `import math`, you are essentially telling Python to load this module so that you can access the functions and constants it provides. <br>
<br>
The import statement in Python is used to import a module into your program's namespace, which makes the names (i.e., functions, variables, classes) defined in the module accessible in your code. In this case, we use `import math` to import the **math module**, which provides mathematical functions like `sin`, `cos`, `exp`, and `log`, as well as constants like `pi` and `e`. <br>

It's worth noting that you can import only specific functions or constants from a module by using the from statement. For example, you could write `from math import pi, sin` to import only the `pi` and `sin` functions from the math module. You could also import every component of the module with `from math import *`. In the following code block, we import the entire math module because we use several of its functions and constants. <br>

```python
import math

# Round a number up to the nearest integer
ceil_value = math.ceil(3.2)
print(ceil_value)  # Output: 4

# Round a number down to the nearest integer
floor_value = math.floor(3.9)
print(floor_value)  # Output: 3

# Calculate the exponential of a number
exp_value = math.exp(2)
print(exp_value)  # Output: 7.3890560989306495

# Calculate the natural logarithm of a number
log_value = math.log(10)
print(log_value)  # Output: 2.302585092994046

# Calculate the square root of a number
sqrt_value = math.sqrt(16)
print(sqrt_value)  # Output: 4.0

# Convert radians to degrees
deg_value = math.degrees(math.pi/2)
print(deg_value)  # Output: 90.0

# Convert degrees to radians
rad_value = math.radians(90)
print(rad_value)  # Output: 1.5707963267948966

# Compute the trigonometric sine of an angle in radians
sin_value = math.sin(math.pi/2)
print(sin_value)  # Output: 1.0

# Compute the trigonometric cosine of an angle in radians
cos_value = math.cos(math.pi/2)
print(cos_value)  # Output: 6.123233995736766e-17

# Compute the trigonometric tangent of an angle in radians
tan_value = math.tan(math.pi/4)
print(tan_value)  # Output: 0.9999999999999999
```

## User Input
To accept input from a user during the execution of the program is relatively easy in Python, as the language provides a built-in function called `input()`. The text withing the function's brackets is called **prompt** `input("The user will see this text"` – this text is displayed to the user when she is asked for the input. By default Python will convert any Input into a string. To restrict the input to a specific type, such as an integer or a floats, you've to specifically declare this as shown in example 2 and 3 below. <br>
<br>
Example 1: Accepting a string input from the user and printing it <br>

```python
# Prompt the user to enter their name
name = input("Please enter your name: ")
# Output: Please enter your name:
# Input: Susi

# Print the name entered by the user
print("Hello, " + name + "!")
# Output: Hello, Susi!
```

Example 2: Accepting an integer input from the user and performing a calculation <br>

```python
# Prompt the user to enter their age
age = int(input("Please enter your age: "))
# Output: Please enter your age: 
# Input: 41

# Calculate the number of days the user has lived
days_lived = age * 365

# Print the result
print("You have lived for approximately " + str(days_lived) + " days.")
# Output: You have lived for approximately 14965 days. 
```

Example 3: Accepting a float input from the user and performing a calculation <br>

```python
# Prompt the user to enter a temperature in Celsius
celsius = float(input("Please enter the temperature in Celsius: "))
# Output: Please enter the temperature in Celsius: 
# Input: 25.5

# Convert the temperature to Fahrenheit
fahrenheit = (celsius * 9 / 5) + 32

# Print the result
print("The temperature in Fahrenheit is: " + str(fahrenheit) + " degrees.")
# Output: The temperature in Fahrenheit is: 77.9 degrees.
```

**NOTE:** The system will produce an error if you accept only a specific data type but an other input has been made: <br>
For example *float* is expected, but *string* was entered: `ValueError: could not convert string to float: 'Susi'` <br>

## Lists in Python
Lists are enclosed in square brackets and allow you to store, access and manipulate collections of data in a single variable. Lists can hold different data types, such as integers, floats, strings, and even other lists. You can access, modify, add, and remove items from a list using a variety of built-in methods and indexing techniques. Python's list index starts with `[0]`. <br>

```python
# Creating a list of integers
numbers = [1, 2, 3, 4, 5]
print(numbers) # Output: [1, 2, 3, 4, 5]

# Creating a list of strings
fruits = ['apple', 'banana', 'orange']
print(fruits) # Output: ['apple', 'banana', 'orange']

# Creating a list of mixed data types
mixed = [1, 'hello', 3.14, True]
print(mixed) # Output: [1, 'hello', 3.14, True]

# Accessing items in a list using indexing
print(fruits[0]) # Output: 'apple'
print(numbers[-1]) # Output: 5

# Slicing a list to get a subset of items
print(fruits[1:3]) # Output: ['banana', 'orange']

# Changing an item in a list
fruits[0] = 'pear'
print(fruits) # Output: ['pear', 'banana', 'orange']

# Adding an item to the end of a list
fruits.append('grape')
print(fruits) # Output: ['pear', 'banana', 'orange', 'grape']

# Removing an item from a list
fruits.remove('banana')
print(fruits) # Output: ['pear', 'orange', 'grape']
```

Here two examples that are combining lists with user input: <br> 

```python
# Adding an item to a list from user input
numbers = [1, 2, 3]
new_number = int(input("Enter a new number: ")) # Input: 7
numbers.append(new_number)
print(numbers) # Output: [1, 2, 3, 7]

# Searching for an item in a list
fruits = ['apple', 'banana', 'orange']
search_item = input("Enter a fruit to search for: ") # Input: Apple
if search_item in fruits:
    print("Found", search_item) # Output: Found Apple  
else:
    print(search_item, "not found")
```

### List of Lists
A list of lists, also known as a **2D list**, is a list where each item in the list is itself a list. This is useful when you want to represent a grid or a table of data. <br>
<br>
In the following example, we create a list of lists called `grid`. Each item in `grid` is itself a list of three integers. We then demonstrate how to access and modify items in the grid, add new rows and columns to the grid, and remove rows from the grid: <br>

```python
# Creating a list of lists
grid = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Accessing an item in a list of lists
print(grid[0][0]) # Output: 1
print(grid[1][2]) # Output: 6

# Changing an item in a list of lists
grid[1][1] = 'X'
print(grid) # Output: [[1, 2, 3], [4, 'X', 6], [7, 8, 9]]

# Adding a row to a list of lists
new_row = [10, 11, 12]
grid.append(new_row)
print(grid) # Output: [[1, 2, 3], [4, 'X', 6], [7, 8, 9], [10, 11, 12]]

# Adding an item to an existing row in a list of lists
grid[2].append(10)
print(grid) # Output: [[1, 2, 3], [4, 'X', 6], [7, 8, 9, 10], [10, 11, 12]]

# Removing a row from a list of lists
del grid[0]
print(grid) # Output: [[4, 'X', 6], [7, 8, 9, 10], [10, 11, 12]]
```

### Lists of specific Data Types
In Python, you can create lists that are limited to specific data types using the `typing` module. <br>
<br>
The `typing` module is a part of the Python standard library that provides support for type hints and annotations in Python code. It contains a set of classes and functions that can be used to define types, including built-in types, custom types, and generic types. These types can be used to annotate function arguments and return values, as well as variable assignments. <br>
<br>
**List:** <br>
The `List` class is a generic type that represents a list of values of a specific type. For example, `List[int]` would represent a list of integers. It is commonly used in function annotations to indicate that a function expects a list of a certain type as an argument, or returns a list of a certain type. <br>
<br>
**Tuple:** <br>
The `Tuple` class is another generic type that represents a fixed-length sequence of values of specific types. For example, `Tuple[int, str]` would represent a tuple containing an integer followed by a string. It is commonly used in function annotations to indicate that a function returns multiple values of specific types, or accepts multiple arguments of specific types. <br>
<br>
**Dict:** <br>
The `Dict` class is a generic type that represents a dictionary with keys and values of specific types. For example, `Dict[str, int]` would represent a dictionary with string keys and integer values. It is commonly used in function annotations to indicate that a function expects a dictionary with keys and values of specific types as an argument, or returns a dictionary with keys and values of specific types. <br>
<br>
In the following example, we import the `List`, `Tuple`, and `Dict` classes from the `typing` module: <br>

```python
from typing import List,Tuple,Dict

# Create a list of integers
int_list: List[int] = [1, 2, 3, 4, 5]

# Create a list of strings
str_list: List[str] = ["apple", "banana", "cherry"]

# Create a list of tuples, where each tuple contains an integer and a string
tuple_list: List[Tuple[int, str]] = [(1, "apple"), (2, "banana"), (3, "cherry")]

# Create a list of dictionaries, where each dictionary has a string key and an integer value
dict_list: List[Dict[str, int]] = [{"apple": 1, "banana": 2, "cherry": 3}, {"orange": 4, "pear": 5}]

# Print the contents of the lists
print(int_list)    # Output: [1, 2, 3, 4, 5]
print(str_list)    # Output: ["apple", "banana", "cherry"]
print(tuple_list)  # Output: [(1, "apple"), (2, "banana"), (3, "cherry")]
print(dict_list)   # Output: [{"apple": 1, "banana": 2, "cherry": 3}, {"orange": 4, "pear": 5}]
```
