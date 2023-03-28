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
You can restrict user input in Python to specific symbols using loops and conditional statements. Here's an example where we restrict the input to the symbols `@`, `#`, and `&`: <br>

```python
# This function checks if a given character is a valid symbol
def is_valid_symbol(char):
    valid_symbols = ['@', '#', '&']
    return char in valid_symbols

# This function gets the user input and checks if it contains only valid symbols
def get_restricted_input():
    while True:  # Keep looping until a valid input is received
        user_input = input("Enter a string with valid symbols (@, #, or &): ")
        # Output: Enter a string with valid symbols (@, #, or &):

        # Check if all characters in the user input are valid symbols
        all_valid_symbols = all(is_valid_symbol(char) for char in user_input)

        if all_valid_symbols:  # If all characters are valid symbols, return the input
            return user_input
        else:
            print("Invalid input! Please use only valid symbols: @, #, or &.")
            # Output: Invalid input! Please use only valid symbols: @, #, or &.
```

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

### Python List Index
In Python, a list is an ordered collection of items, and each item in a list has an index that indicates its position in the list. The first item in a list has an index of **0,** the second item has an index of **1**, and so on. You can access items in a list using their index by enclosing the index in square brackets after the name of the list. <br>
<br>
Python also supports **negative list indices**, which allow you to access items in a list counting from the end of the list instead of the beginning. The last item in a list has an index of **-1**, the second-to-last item has an index of **-2**, and so on. Negative indices can be useful in situations where you want to access the end of a list without knowing the length of the list. <br>

```python
numbers = [1, 2, 3, 4, 5]

# Access the first element of the list
first_number = numbers[0] 
print(first_number) # Output: 1 

# Access the second element of the list
second_number = numbers[1] 
print(second_number) # Output: 2 

# Access the last element of the list
last_number = numbers[-1] 
print(last_number) # Output: 5 

# Access the second-to-last element of the list
second_last_number = numbers[-2] 
print(second_last_number) # Output: 4 
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

You can also use Python basefunctionality to limit for example user input to a specific data type. Following we're using a `ValueError` excemption to ensure only integers are added to our list: <br>

```python
# Create an empty list to store integers
int_list = []

# Prompt the user to enter an integer, and add it to the list
while True:
    try:
        user_input = input("Enter an integer (or write \"done\" to finish): ")
        if user_input == 'done':
            break
        # Use the int() function to convert the user's input to an integer
        user_int = int(user_input)
        # Add the integer to the list
        int_list.append(user_int)
    except ValueError:
        # If the user enters something that can't be converted to an integer,
        # print an error message and continue to the next iteration of the loop
        print("Invalid input. Please enter an integer.")

# Print the list of integers entered by the user
print("List of integers:", int_list)

# Example In- / Output flow:                                                                                                                                              
# Output: Enter an integer (or write "done" to finish):                                                                                                                   
# Input: 7                                                                                                                                                                
# Output: Enter an integer (or write "done" to finish):                                                                                                                   
# Input: Wurst                                                                                                                                                            
# Output: Invalid input. Please enter an integer.                                                                                                                         
# Output: Enter an integer (or write "done" to finish): 
# Input: 9                                                                                                                                                                
# Output: Enter an integer (or write "done" to finish): 
# Input: done
# Output: List of integers: [7, 9] 
```

### List Functions
Python provides many built-in functions for manipulating lists, which makes it easy to work with them. For example, the `len()` function can be used to determine the length of a list, while the `append()` function can be used to add an element to the end of a list. The `insert()` function can be used to add an element at a specific position in the list, while the `remove()` function can be used to remove a specific element from the list. <br>
<br>
Other useful functions for working with lists include `sort()`, which can be used to sort the elements of a list in ascending or descending order, and `reverse()`, which can be used to reverse the order of the elements in a list. The `index()` function can be used to find the position of a specific element in the list, while the `count()` function can be used to count the number of times a specific element appears in the list. <br>

#### extend()
The `extend()` method is a built-in function in Python that allows you to add elements from one list to another list. It is used to concatenate multiple lists or add items from another iterable to an existing list. The `extend()` method modifies the original list and can be used to concatenate multiple lists, add items from another iterable, or even add characters from a string. <br>

```python
### Example 1: Extending a list with another list ###

# Define two lists to work with
list1 = [1, 2, 3]
list2 = [4, 5, 6]

# Use the extend method to add the contents of list2 to list1
list1.extend(list2)

# Print the updated list1
print(list1) # Output: [1, 2, 3, 4, 5, 6]


### Example 2: Extending a list with an iterable ###

# Define a list and a tuple to work with
list1 = [1, 2, 3]
tuple1 = (4, 5, 6)

# Use the extend method to add the contents of tuple1 to list1
list1.extend(tuple1)

# Print the updated list1
print(list1) # Output: [1, 2, 3, 4, 5, 6]
```

#### extend() vs. append()
In Python, both methods `extend()` and `append()` are used to add elements to a list, but they behave differently: <br>

* `append()` adds a single element to the end of a list.
* `extend()` adds elements from an iterable (such as a list, tuple, or string) to the end of a list.

```python
# Define a list to work with
my_list = [1, 2, 3]

# Append an element to the list
my_list.append(4)
print(my_list) # Output: [1, 2, 3, 4]

# Extend the list with another list
my_list.extend([5, 6, 7])
print(my_list) # Output: [1, 2, 3, 4, 5, 6, 7]
```

#### insert()
The `insert()` method is a built-in function in Python that allows you to add an element to a list **at a specific index**. It can be used to insert a new element at the beginning, middle, or end of a list, and can also be used to add multiple elements at specific indices. <br>

```python
creatures = ['Unicorn', 'Dragon', 'Phoenix']

# Insert an element at a specific index
creatures.insert(1, 'Griffin')
print(creatures) # Output: ['Unicorn', 'Griffin', 'Dragon', 'Phoenix']

# Insert multiple elements at specific indices
creatures.insert(0, 'Basilisk')
creatures.insert(3, 'Kraken')
print(creatures) # Output: ['Basilisk', 'Unicorn', 'Griffin', 'Kraken', 'Dragon', 'Phoenix']

# Insert elements at negative indices (counting from the end of the list)
creatures.insert(-1, 'Mermaid')
creatures.insert(-3, 'Siren')
print(creatures) # Output: ['Basilisk', 'Unicorn', 'Griffin', 'Kraken', 'Dragon', 'Siren', 'Phoenix', 'Mermaid']
```

#### remove()
The `remove()` function is a built-in function in Python that allows you to remove a specific item from a list. You can remove **by index** or **by value**. <br>

```python
wild_west_heroes = ['Billy the Kid', 'Jesse James', 'Wyatt Earp', 'Butch Cassidy']

# Example 1 – remove by value
# remove 'Billy the Kid' from the list
wild_west_heroes.remove('Billy the Kid')
print(wild_west_heroes) # Output: ['Jesse James', 'Wyatt Earp', 'Butch Cassidy']

# Example 2 – remove by index
# remove the first element from the list
wild_west_heroes.remove(wild_west_heroes[0])
print(wild_west_heroes) # Output: ['Wyatt Earp', 'Butch Cassidy'] 
```

#### clear()
The `clear()` method in Python is a built-in list function used to remove all items from a list. This method modifies the original list, making it an empty list. <br>

```python
my_list = [1, 2, 3, 4, 5]
print("Original List:", my_list)  # Output: Original List: [1, 2, 3, 4, 5]

# Using the clear() method to remove all elements from the list
my_list.clear()
print("List after clear():", my_list)  # Output: List after clear(): []
```

#### pop()
The `pop()` method is a built-in list function used to remove and return the last item from the list or the item at a specified index. If you provide an index as an argument, it will remove and return the item at that index. If no index is provided, it removes and returns the last item. <br>

```python
my_list = [1, 2, 3, 4, 5]

# Using pop() without an index, removing and returning the last item
removed_item = my_list.pop()
print("Removed item:", removed_item)  # Output: Removed item: 5
print("List after pop():", my_list)  # Output: List after pop(): [1, 2, 3, 4]

# Using pop() with an index, removing and returning the item at index 1
removed_item = my_list.pop(1)
print("Removed item at index 1:", removed_item)  # Output: Removed item at index 1: 2
print("List after pop(1):", my_list)  # Output: List after pop(1): [1, 3, 4]
```

#### index()
The `index()` method is a built-in list function that helps you find the index of the first occurrence of a specified value in a list. If the value is not present in the list, a ValueError will be raised. <br>

```python
fruits = ['apple', 'banana', 'orange', 'grape', 'mango']

# Finding the index of a value present in the list
fruit_to_find = 'orange'
try:
    index = fruits.index(fruit_to_find)
    print(f"{fruit_to_find} found at index:", index)  # Output: orange found at index: 2
except ValueError:
    print(f"{fruit_to_find} not found in the list.")

# Finding the index of a value not present in the list
fruit_to_find = 'kiwi'
try:
    index = fruits.index(fruit_to_find)
    print(f"{fruit_to_find} found at index:", index)
except ValueError:
    print(f"{fruit_to_find} not found in the list.")  # Output: kiwi not found in the list.
```

The `index()` function can also be used with optional `start` and `end` parameters, allowing you to search for the specified value within a specific range of indices in the list. The `start` parameter specifies the starting index to search from, and the `end` parameter specifies the ending index (exclusive). <br>

```python
job_titles = ['engineer', 'designer', 'developer', 'manager', 'developer', 'analyst']

# Finding the index of a value within a specific range
job_to_find = 'developer'
try:
    index = job_titles.index(job_to_find, 3, 6)  # Search between indices 3 (inclusive) and 6 (exclusive)
    print(f"{job_to_find} found at index:", index)  # Output: developer found at index: 4
except ValueError:
    print(f"{job_to_find} not found in the specified range.")

# When the value is not within the specified range
try:
    index = job_titles.index(job_to_find, 1, 3)  # Search between indices 1 (inclusive) and 3 (exclusive)
    print(f"{job_to_find} found at index:", index)
except ValueError:
    print(f"{job_to_find} not found in the specified range.")  # Output: developer not found in the specified range.
```

#### count()
The `count()` function is a built-in list method that returns the number of occurrences of a specified value in the list. <br>

```python
superheroes = ['Batman', 'Superman', 'Wonder Woman', 'Batman', 'Flash', 'Batman']

# Counting the occurrences of a value in the list
hero_to_count = 'Batman'
count = superheroes.count(hero_to_count)

print(f"{hero_to_count} appears {count} times in the list.")  # Output: Batman appears 3 times in the list.
```

#### sort()
The `sort()` method is a built-in list function that allows you to sort the elements of a list in ascending order by default. You can also sort the list in descending order by providing the optional reverse=True argument. The method sorts the list in-place, meaning it modifies the original list without creating a new one. <br>

```python
car_brands = ['Toyota', 'Honda', 'Ford', 'BMW', 'Audi']

# Sorting the list in ascending order (default behavior)
car_brands.sort()
print("Ascending order:", car_brands)  
# Output: Ascending order: ['Audi', 'BMW', 'Ford', 'Honda', 'Toyota']

# Sorting the list in descending order
car_brands.sort(reverse=True)
print("Descending order:", car_brands)  
# Output: Descending order: ['Toyota', 'Honda', 'Ford', 'BMW', 'Audi']
```

You can also use the key parameter to specify a custom function to determine the sort order. For example, you can sort a list of strings based on their length: <br>

```python
animals = ['elephant', 'cat', 'lion', 'giraffe', 'bear']

# Sorting the list based on the length of the strings
animals.sort(key=len)
print("Sorted by length:", animals)  
# Output: Sorted by length: ['cat', 'lion', 'bear', 'giraffe', 'elephant']
```

The `key` parameter for the `sort()` function accepts a custom function that you can define to determine the sort order based on specific attributes or calculations. The function should take a single argument and return a value that is used to sort the list. <br>

```python
# sorting a list of strings based on the last character

words = ['apple', 'banana', 'pear', 'grape', 'cherry']

# Define a function that takes a single string as input and returns its last character
def last_char(word):
    return word[-1]  # Access the last character in the string using negative indexing

# Use the custom function 'last_char' as the key function for the sort() method
words.sort(key=last_char)

print("Sorted by last character:", words)
# Output: Sorted by last character: ['banana', 'apple', 'grape', 'pear', 'cherry']
```

```python
# sorting a list of dictionaries based on a specific key

students = [
    {'name': 'Alice', 'age': 22},
    {'name': 'Bob', 'age': 25},
    {'name': 'Charlie', 'age': 20}
]

# Define a function that takes a single dictionary as input and returns the value associated with the 'age' key
def age_key(student):
    return student['age']  # Access the value associated with the 'age' key in the dictionary

# Use the custom function 'age_key' as the key function for the sort() method
students.sort(key=age_key)

print("Sorted by age:", students)
# Output: Sorted by age: [{'name': 'Charlie', 'age': 20}, {'name': 'Alice', 'age': 22}, {'name': 'Bob', 'age': 25}]
```

#### reverse()
The `reverse()` method is a built-in list function in Python that allows you to reverse the order of elements in a list. This method modifies the original list in-place, meaning it reverses the elements directly within the list without creating a new one. <br>

```python
instruments = ['guitar', 'piano', 'drums', 'violin', 'saxophone']

# Reversing the order of elements in the list using the reverse() method
instruments.reverse()

print("Reversed list:", instruments)
# Output: Reversed list: ['saxophone', 'violin', 'drums', 'piano', 'guitar']
```

#### copy()
The `copy()` method that allows you to create a shallow copy of a list. When you create a copy of a list using this method, the new list contains the same elements as the original list, but both lists are separate objects. Any changes made to the copy won't affect the original list, and vice versa. <br>

```python
book_genres = ['Mystery', 'Science Fiction', 'Romance', 'Fantasy', 'Biography']

# Create a copy of the original list using the copy() method
copied_genres = book_genres.copy()

print("Original list:", book_genres)
# Output: Original list: ['Mystery', 'Science Fiction', 'Romance', 'Fantasy', 'Biography']

print("Copied list:", copied_genres)
# Output: Copied list: ['Mystery', 'Science Fiction', 'Romance', 'Fantasy', 'Biography']

# Modify the copied list
copied_genres.append('Horror')

print("Modified copied list:", copied_genres)
# Output: Modified copied list: ['Mystery', 'Science Fiction', 'Romance', 'Fantasy', 'Biography', 'Horror']

print("Original list after modifying the copied list:", book_genres)
# Output: Original list: ['Mystery', 'Science Fiction', 'Romance', 'Fantasy', 'Biography']
```

## Tupels
A tuple is a built-in data type in Python, used for storing an ordered, immutable collection of elements. Tuples are similar to lists, but unlike lists, they cannot be modified after they are created. This means that elements within a tuple cannot be added, removed, or changed once the tuple is defined. Tuples are often used to store related pieces of data, such as coordinates or RGB color values. <br>
<br>
Tuples are created by placing a **comma-separated** sequence of elements inside parentheses `()`. <br>
There base functionalities are quite similar to lists. <br>

```python
animals = ('lion', 'tiger', 'elephant', 'giraffe', 'zebra')

first_animal = animals[0]
print("First animal:", first_animal)
# Output: First animal: lion

last_animal = animals[-1]
print("Last animal:", last_animal)
# Output: Last animal: zebra

first_three_animals = animals[:3]
print("First three animals:", first_three_animals)
# Output: First three animals: ('lion', 'tiger', 'elephant')
```

Although tuples are immutable, they can contain mutable elements, such as lists: <br>

```python
mixed_tuple = (1, 2, ['a', 'b'], 3)

# Modifying an element inside the mutable list within the tuple
mixed_tuple[2][1] = 'c'  

print("Modified mixed tuple:", mixed_tuple)
# Output: Modified mixed tuple: (1, 2, ['a', 'c'], 3)
```

But generally, if you're changing a value, adding a value, and removing a value, Python raises an exception (`TypeError` or `AttributeError`), indicating that the operation is not supported on tuples due to their immutability. <br>

```python
colors = ('red', 'green', 'blue')

# Attempting to change a value within the tuple
try:
    colors[1] = 'yellow'
except TypeError as e:
    print(f"Error while changing value: {e}")
# Output: Error while changing value: 'tuple' object does not support item assignment

# Attempting to add a value to the tuple
try:
    colors.append('orange')
except AttributeError as e:
    print(f"Error while adding value: {e}")
# Output: Error while adding value: 'tuple' object has no attribute 'append'

# Attempting to remove a value from the tuple
try:
    colors.remove('green')
except AttributeError as e:
    print(f"Error while removing value: {e}")
# Output: Error while removing value: 'tuple' object has no attribute 'remove'
```

## Functions
In Python, you can create custom functions using the `def` keyword. Functions are reusable pieces of code that can be called with a specific set of input values, known as arguments, and return a result. Creating custom functions helps improve code organization, modularity, and maintainability, as well as reducing redundancy. <br>
<br>
To define a function, you start with the `def` keyword, followed by the function name and a pair of parentheses containing any input parameters. After the parentheses, add a colon to mark the beginning of the function body. The function body should be indented to indicate the scope of the function. <br>

```python
# function that adds two numbers
def add_numbers(a, b):
    result = a + b
    return result

sum_result = add_numbers(3, 5)
print("Sum of 3 and 5:", sum_result)  # Output: Sum of 3 and 5: 8
```

Functions can also have default parameter values, which are used when no value is provided for a specific parameter during the function call. To define a default value for a parameter, use the assignment operator (`=`) followed by the default value within the function definition: <br>

```python
# function to create greeting, default is "Hello, $Name!"
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

welcome_message = greet("John")
print(welcome_message)  # Output: Hello, John!

custom_greeting = greet("Jane", "Good morning")
print(custom_greeting)  # Output: Good morning, Jane!
```

### return
The `return` keyword in Python is used within a function to indicate that the function should terminate and send back a specified value to the caller. The value can be a single object or multiple objects separated by commas. If no value is provided after the `return` keyword, the function returns `None` by default. <br>
<br>
In this example, the `square()` function calculates the square of the given number and returns the result using the `return` keyword: <br>

```python
def square(number):
    result = number ** 2
    return result

squared_value = square(4)
print("Squared value of 4:", squared_value)  # Output: Squared value of 4: 16
```

In this example, the `get_name_and_age()` function returns two values (name and age) using the `return` keyword. When multiple values are returned, they are packed into a tuple by default: <br>

```python
def get_name_and_age():
    name = "Alice"
    age = 30
    return name, age

person_name, person_age = get_name_and_age()
print("Name:", person_name)  # Output: Name: Alice
print("Age:", person_age)    # Output: Age: 30
```

In this example, the divide function checks if the divisor is zero. If it is, the function prints an error message and returns early using the return keyword without any value. In this case, the returned value is None by default: <br>

```python
def divide(a, b):
    if b == 0:
        print("Error: Division by zero")
        return
    result = a / b
    return result

output = divide(10, 0)
# Output: Error: Division by zero
print("Output:", output)  # Output: Output: None
```

The `return` keyword allows you to control the flow of your functions and define what values should be sent back to the caller. It helps make your code more modular and reusable, as well as allowing for better error handling and early termination when necessary. <br>

## IF, ELIF, ELSE 
**if**, **elif** and **else** statements are a fundamental control structure that allows your program to make decisions based on certain conditions. They enable your code to execute specific blocks of code depending on whether the given condition is `True` or `False`. This branching mechanism can lead to different outcomes in your program depending on the input or the state of your variables. <br>
<br>
Such statements are a fundamental concept of programming and appear in most programming languages. But there are a few specifics in Python to be considered: <br>
<br>
**Indentation**: In Python, indentation is used to define the scope of the if statements. Unlike some other languages that use braces, Python relies on consistent indentation to determine which code blocks belong to the if, elif, or else branches. This makes Python code generally more readable and consistent. The basic structure of an if statement in Python is: <br>

```python
if condition:
    # Code to execute if the condition is True
```

Those checks can be done on **Truthy** and **Falsy** values: <br>

```python
# Checking if a value is truthy (not empty, non-zero) or falsy (empty, zero)
if some_value:
    # Code to execute if the value is truthy
else:
    # Code to execute if the value is falsy
```

Or on **multiple conditions**: <br>

```python
# Checking if multiple conditions are met using 'and', 'or', and 'not'
if condition1 and condition2:
    # Code to execute if both conditions are True
elif condition1 or condition2:
    # Code to execute if either condition1 or condition2 is True
elif not condition1:
    # Code to execute if condition1 is False
```


**Inline if statement (ternary operator)**: Python supports a concise **inline if statement**, also known as a **ternary operator**. This allows you to write simple if-else statements in a single line:

```python
# Using an inline if statement with multiple conditions
# result = value_if_both_true if condition1 and condition2 else value_if_not_both_true

x = 5
y = 10

# Check if both x and y are positive, and assign "both positive" or "not both positive" accordingly
result = "both positive" if x > 0 and y > 0 else "not both positive"

print(result)  # Output: both positive
```

Following some examples with values. <br>
1) A simple if statement: <br>

```python
age = 18

if age >= 18:
    print("You are an adult.")
# Output: You are an adult.
```

2) An if-else statement: <br>

```python
temperature = 15

if temperature >= 20:
    print("It's warm outside.")
else:
    print("It's cold outside.")
# Output: It's cold outside.
```

3) An if-elif-else statement: <br>

```python
score = 85

if score >= 90:
    grade = 'A'
elif score >= 80:
    grade = 'B'
elif score >= 70:
    grade = 'C'
else:
    grade = 'D'

print("Your grade is:", grade)
# Output: Your grade is: B
```

### IF NOT
You can perform a **false check** by using the `not` keyword to reverse the truthiness of a condition. This can be helpful when you want to execute code when a condition is not met, or when the condition evaluates to `False`. <br>

```python
if not condition:
    # Code to execute if the condition is False
```

Here's an example with values: <br>

```python
temperature = 20

if not temperature > 25:
    print("The temperature is not greater than 25.")
# Output: The temperature is not greater than 25.
```

## Comparison Operators
Comparison operators enable the evaluation of relationships between values in programming. They are vital for controlling the flow of a program through conditional statements, allowing for dynamic and adaptable code. <br>
<br>
In Python, comparison operators are straightforward and easy to read, closely resembling their mathematical counterparts. <br>

```python
# Equal to (==)
if 5 == 5:
    print("5 is equal to 5")  # Output: 5 is equal to 5

# Not equal to (!=)
if 4 != 5:
    print("4 is not equal to 5")  # Output: 4 is not equal to 5

# Less than (<)
if 3 < 4:
    print("3 is less than 4")  # Output: 3 is less than 4

# Greater than (>)
if 6 > 5:
    print("6 is greater than 5")  # Output: 6 is greater than 5

# Less than or equal to (<=)
if 4 <= 4:
    print("4 is less than or equal to 4")  # Output: 4 is less than or equal to 4

# Greater than or equal to (>=)
if 7 >= 6:
    print("7 is greater than or equal to 6")  # Output: 7 is greater than or equal to 6
```

Chaining comparisons in Python allows you to check multiple conditions in a single expression, making the code shorter and more readable. <br>

```python
# Example 1
x = 5
if 3 < x < 7:
    print("x is between 3 and 7")  # Output: x is between 3 and 7

# Example 2
y = 10
if 8 <= y <= 12:
    print("y is between 8 and 12")  # Output: y is between 8 and 12

# Example 3
a, b, c = 3, 5, 9
if a < b < c:
    print("a is less than b, and b is less than c")  # Output: a is less than b, and b is less than c

# Example 4
num = 4
if 0 < num < 5 and num % 2 == 0:
    print("num is an even number between 1 and 4")  # Output: num is an even number between 1 and 4
```

## Dictionaries
Python dictionaries are a built-in data structure that allows you to store and manage **key-value pairs**. Dictionaries are mutable, unordered, and do not allow duplicate keys. They are commonly used for tasks like data organization, counting occurrences, and configuration settings. Dictionaries can be created using curly braces `{}` with keys and values separated by colons, or by using the `dict()` constructor. <br>

```python
# Creating a dictionary using curly braces
superheroes = {
    "Iron Man": "Tony stark",
    "Captain America": "Steve Rogers",
    "Black Widow": "Natasha Romanoff",
}

# Creating a dictionary using the dict() constructor
western_movies = dict([
    ("The Good, the Bad and the Ugly", 1966),
    ("Once Upon a Time in the West", 1968),
    ("Unforgiven", 1992),
])
```

Accessing a value using a key: <br>

```python
print(superheroes["Iron Man"])  # Output: Tony stark
```

Updating an existing key-value pair: <br>

```python
superheroes["Iron Man"] = "Tony Stark"
```

Adding a new key-value pair: <br>

```python
superheroes["Hulk"] = "Bruce Banner"
```

Checking if a key exists in the dictionary: <br>

```python
print("Batman" in superheroes)  # Output: False
```

The default output for a non-existing key if `False`. By using the `get()` method, you can specify a default output. Here a more advanced example: <br>

```python
# Get user input
user_input = input("Enter a superhero name: ")
# Output: Enter a superhero name: 

# Use the get() method to retrieve the value for the user-input key or return "Unknown superhero" if the key doesn't exist
secret_identity = superheroes.get(user_input, "Unknown superhero")

if secret_identity == "Unknown superhero":
    print(f"{user_input} is an unknown superhero.")
# Input: Batman
# Output: Batman is an unknown superhero.
else:
    print(f"The secret identity of {user_input} is: {secret_identity}")
# Input: Iron Man
# Output: The secret identity of Iron Man is: Tony Stark
```

Removing a key-value pair using the `del` keyword <br>

```python
del western_movies["The Good, the Bad and the Ugly"]
```

Iterating through keys and values in a dictionary: <br>

```python
for key, value in superheroes.items():
    print(key, ":", value)
    # Iron Man : Tony Stark (Updated)
    # Captain America : Steve Rogers
    # Black Widow : Natasha Romanoff
    # Hulk : Bruce Banner
```

To search for a value instead of a key, you have to loop through the entire dictionary: <br>

```python
# Get user input
user_input = input("Enter a secret identity: ")
# Output: Enter a secret identity: Tony Stark

# Search for the value in the dictionary and print the corresponding key
found = False
for superhero, secret_identity in superheroes.items():
    if secret_identity == user_input:
        print(f"{user_input} is the secret identity of {superhero}.")
        found = True
        break
# Input: Tony Stark
# Tony Stark is the secret identity of Iron Man

if not found:
    print(f"{user_input} is not the secret identity of any known superhero.")
# Input: Bruce Wayne
# Output: Bruce Wayne is not the secret identity of any known superhero.
```

Merging two dictionaries: <br>

```python
industries = {"Apple": "Technology", "Ford": "Automotive"}
more_industries = {"Pfizer": "Pharmaceutical", "Sony": "Electronics"}
industries.update(more_industries)
print(industries)
# Output: {'Apple': 'Technology', 'Ford': 'Automotive', 'Pfizer': 'Pharmaceutical', 'Sony': 'Electronics'}
```

## While Loops
While loops are a control flow structure in Python that allow you to repeatedly execute a block of code as long as a given condition is true. The loop will continue iterating until the condition becomes false. <br>

```python
count = 1

# Repeat the loop as long as count is less than or equal to 5
while count <= 5:
    print("Current count:", count)
    count += 1

# Output:
# Current count: 1
# Current count: 2
# Current count: 3
# Current count: 4
# Current count: 5
```
 
The `+=` operator is a shorthand for `count = count + 1`. It adds the value on the right side of the operator (in this case, 1) to the variable on the left side (here, count) and assigns the result back to the variable. This allows you to increment the value of count more concisely. <br>
<br>
Examples for commonly used while loop conditions: <br>

```python
# Loop until a specific value is reached
while variable < specific_value:

# Loop until a specific value is not equal to the variable
while variable != specific_value:

# Loop until a list is empty (i.e., has no elements)
while len(some_list) > 0:

# Loop until a condition involving multiple variables is met
while variable1 < specific_value1 and variable2 < specific_value2:

# Loop until a boolean flag is set to False
while boolean_flag:

# Loop with a complex condition using multiple operators
while (condition1 and condition2) or (condition3 and not condition4):
```

Here an example how to loop through an external file, until it is fully processed: <br>

```python
with open("file.txt", "r") as file:
    # Read the first line from the file
    line = file.readline()

    # Loop until the end of the file is reached
    while line:
        # Process the line (e.g., print it)
        print(line.strip())

        # Read the next line from the file
        line = file.readline()
```

## For Loops
For loops are used to iterate over a sequence (such as a list, tuple, string, or other iterable objects). Instead of using a counter variable as in many other programming languages, Python's for loop iterates directly over the items in the sequence. <br>

```python
# Iterating over a list of numbers
numbers = [1, 2, 3, 4, 5]
for num in numbers:
    print(num)
# Output:
# 1
# 2
# 3
# 4
# 5

# Iterating over a string
text = "Python"
for char in text:
    print(char)
# Output:
# P
# y
# t
# h
# o
# n

# Iterating over a tuple
fruits = ('apple', 'banana', 'cherry')
for fruit in fruits:
    print(fruit)
# Output:
# apple
# banana
# cherry

# Using the range() function to create a sequence of numbers
for i in range(3):
    print(i)
# Output:
# 0
# 1
# 2
```

You can use the `key` keyword, to loop through dictionary keys: <br>

```python
# Loop through a dictionary (keys)
person = {'name': 'Heiko', 'age': 30, 'city': 'Berlin'}
for key in person:
    print(key)
    # Each iteration gets the next key in the dictionary (e.g., 'name', 'age', 'city')
```

Or loop through a `key`, `value` pair: <br>

```python
# Loop through a dictionary (key-value pairs)
for key, value in person.items():
    print(key, value)
    # Each iteration gets the next key-value pair in the dictionary
```

Looping through sets works as looping through lists in general: <br>

```python
# Loop through a set
unique_numbers = {1, 2, 3, 4, 5}
for number in unique_numbers:
    print(number)
    # Each iteration gets the next value in the set (1, 2, 3, …)
```

## Try Except
In Python, `try … except` blocks are used for error handling. When you anticipate that a certain part of your code might raise an exception (runtime error), you can use the try except block to catch and handle the exception gracefully. This prevents your program from crashing and allows you to provide alternative actions or display informative messages to the user. <br>

```python
# Example 1: Basic try-except block
try:
    result = 10 / 0
except ZeroDivisionError:
    print("Oops! Division by zero is not allowed.")
# Output: Oops! Division by zero is not allowed.

# Example 2: Catching multiple exceptions
try:
    num = int("string")
    result = 10 / num
except ZeroDivisionError:
    print("Oops! Division by zero is not allowed.")
except ValueError:
    print("Oops! Invalid input. Please enter a number.")
# Output: Oops! Invalid input. Please enter a number.

# Example 3: Using a generic except block
try:
    num = int("string")
    result = 10 / num
except Exception as e:
    print(f"An error occurred: {e}")
# Output: An error occurred: invalid literal for int() with base 10: 'string'
```

Here some examples for the most common error types: <br>

```python
# SyntaxError: Raised when there's a syntax error in the code
try:
    eval('1 ++ 2')
except SyntaxError as se:
    print("SyntaxError:", se)
    # Output: SyntaxError: invalid syntax

# ZeroDivisionError: Raised when attempting to divide by zero
try:
    result = 10 / 0
except ZeroDivisionError as zde:
    print("ZeroDivisionError:", zde)
    # Output: ZeroDivisionError: division by zero

# FileNotFoundError: Raised when trying to open a non-existent file
try:
    with open("non_existent_file.txt") as file:
        content = file.read()
except FileNotFoundError as fnfe:
    print("FileNotFoundError:", fnfe)
    # Output: FileNotFoundError: [Errno 2] No such file or directory: 'non_existent_file.txt'

# ValueError: Raised when a function receives an argument of the correct type but an inappropriate value
try:
    int("string")
except ValueError as ve:
    print("ValueError:", ve)
    # Output: ValueError: invalid literal for int() with base 10: 'string'

# TypeError: Raised when an operation is performed on an object of an inappropriate type
try:
    "1" + 2
except TypeError as te:
    print("TypeError:", te)
    # Output: TypeError: can only concatenate str (not "int") to str

# IndexError: Raised when attempting to access an
try:
    my_list = [1, 2, 3]
    my_list[4]
except IndexError as ie:
    print("IndexError:", ie)
    # Output: IndexError: list index out of range 
```

To execute specific lines of code even if an exception was thrown, use `finally`: <br>   

```python
# Using 'finally' with try-except
try:
    num = int("string")
    result = 10 / num
except ValueError:
    print("Oops! Invalid input. Please enter a number.")
finally:
    print("This block will always be executed, regardless of an exception.")
# Output:
# Oops! Invalid input. Please enter a number.
# This block will always be executed, regardless of an exception.
```

## Reading Files
In Python, reading files is a common and essential task when working with data or text-based input. Python offers several built-in functions and methods that simplify the process of reading, parsing, and extracting information from files.

### open() & close()
One of the most frequently used functions for file handling is the `open()` function. It provides a way to open a file, read its contents, and perform various operations like **reading**, **writing**, or **appending** data. The `open()` function returns a file object, which can be used to read or manipulate the file's content. <br>
<br>
The `close()` method is used to close an opened file and release the resources associated with it. Closing a file ensures that any changes made to it are saved and prevents potential data loss or file corruption. <br>
<br>
**file.txt**:

```
Cinderella - Cinderella
Ariel - The Little Mermaid
Belle - Beauty and the Beast
```

```python
# Reading a file
file = open("file.txt", "r")
print(file.read())
# Output:  
# Cinderella - Cinderella
# Ariel - The Little Mermaid
# Belle - Beauty and the Beast
file.close()

# Reading a file line by line
file = open("file.txt", "r")
print(file.txt.readline())
# Output: Cinderella - Cinderella
print(file.txt.readline())
# Output: Ariel - The Little Mermaid
file.close()

# Writing to a file
file = open("file.txt", "w")
file.write("Jasmin - Aladdin")
file.close()
# Reading same file
file = open("file.txt", "r")
print(file.read())
# Output: Jasmin - Aladdin
# File has been overwritten with entered content.

# Appending to a file
file = open("file.txt", "a")
file.write("\nElsa - Frozen")
file.close()
# Reading same file
file = open("file.txt", "r")
print(file.read())
# Output: 
# Jasmin - Aladdin
# Elsa - Frozen

# Writing multiple lines to a file using the writelines() method
lines_to_write = ["Moana - Moana\n", "Rapunzel - Tangled\n", "Pocahontas - Pocahontas\n"]
file = open("file.txt", "w")
file.writelines(lines_to_write)
file.close()
# Reading same file
file = open("file.txt", "r")
print(file.read())
# Output:  
# Moana - Moana
# Rapunzel - Tangled
# Pocahontas - Pocahontas

# NOTE: write() and writelines() can both used with a file opened in "a" mode, to append instead of overwriting.
```

### with statement
The `with` statement in Python is used for convenient and efficient handling of resources, such as file operations. When working with the `open()` function, it is recommended to use the with statement because it automatically manages the opening and closing of files. This ensures that the file is properly closed after the block of code is executed, even if an exception occurs during the operation. By using the `with` statement, you can avoid potential issues like resource leaks, data loss, or file corruption. <br>
<br>
**file.txt**

```
Moana - Moana
Rapunzel - Tangled
Pocahontas - Pocahontas
```

```python
# Reading a file in 'r' mode
with open("file.txt", "r") as file:
    content = file.read()
    print(content)
# Output:
# Moana - Moana
# Rapunzel - Tangled
# Pocahontas - Pocahontas

# Writing to a file in 'w' mode
with open("file.txt", "w") as file:
    file.write("Elsa - Frozen")
# After executing this code, the content of file.txt will be:
# Elsa - Frozen

# Appending to a file in 'a' mode
with open("file.txt", "a") as file:
    file.write("\nAnna - Frozen")
# After executing this code, the content of file.txt will be:
# Elsa - Frozen
# Anna - Frozen

# Reading and writing to a file in 'r+' mode
with open("file.txt", "r+") as file:
    content = file.read()
    print(content)
    # Output:
    # Elsa - Frozen
    # Anna - Frozen
    file.write("\nMerida - Brave")
# After executing this code, the content of file.txt will be:
# Elsa - Frozen
# Anna - Frozen
# Merida - Brave
```

You can as well read multiple files using the `with` statement: <br>
<br>
**file1.txt**:

```
Elsa - Frozen
Anna - Frozen
```

**file2.txt**:

```
Merida - Brave
Tiana - The Princess and the Frog
```

```python
# Reading multiple files at once using the 'with' statement
with open("file1.txt", "r") as file1, open("file2.txt", "r") as file2:
    content1 = file1.read()
    content2 = file2.read()

print(content1)
# Output:
# Elsa - Frozen
# Anna - Frozen

print(content2)
# Output:
# Merida - Brave
# Tiana - The Princess and the Frog
```

## Modules
In Python, a module is a file containing Python definitions and statements that can be imported into other Python scripts. Modules allow developers to group related code and reuse it across different projects. By using modules, you can organize your code better, improve maintainability, and avoid code duplication. Python has a vast library of built-in modules, as well as a large number of third-party modules available. <br> 

### built-in modules
Here's an overview of some of the most commonly used built-in modules and their purposes: <br>

* `os`: Provides a way to interact with the operating system, such as file and directory management, environment variables, and process control.
* `sys`: Enables access to some variables and functions related to the Python interpreter and its environment, such as command-line arguments and exit status.
* `math`: Offers mathematical functions and constants, such as trigonometric functions, logarithms, and the value of pi.
* `random`: Includes functions for generating random numbers and performing random operations, like shuffling a list or selecting a random element.
* `datetime`: Supports working with dates and times, including arithmetic operations, formatting, and parsing.
* `json`: Enables the encoding and decoding of JSON data, which is commonly used for data exchange between a server and a client.
* `re`: Provides regular expression support for advanced text manipulation and pattern matching.
* `collections`: Offers additional data structures and tools for working with collections, such as namedtuple, deque, Counter, and OrderedDict.
* `itertools`: Contains a set of tools for working with iterable objects, such as iterators and generators, which help create efficient looping constructs.
* `urllib`: A package that contains multiple modules for working with URLs, such as opening, reading, parsing, and constructing URLs.
* `socket`: Enables low-level networking functionality, such as creating and managing sockets for various networking protocols like TCP and UDP.
* `threading`: Supports the creation and management of threads, which can be used for concurrent execution of multiple tasks within a single process.
* `subprocess`: Provides a way to create and interact with additional processes, allowing you to run external programs, connect to their input/output/error pipes, and obtain their return codes.
* `csv`: Offers functionality for reading and writing CSV (Comma Separated Values) files, a common format for data exchange between applications.
* `sqlite3`: Includes an interface for working with SQLite databases, a lightweight disk-based database that doesn't require a separate server process.

A list of internal modules can be found here: [Python Module Index](https://docs.python.org/3/py-modindex.html)

### 3rd-party modules
Here's a list of some popular third-party Python modules and a brief description of their functionalities: <br>

* `requests`: Simplifies the process of making HTTP requests and handling responses, making it easier to interact with web services and APIs.
* `numpy`: Provides support for numerical computing with Python, including efficient array operations and complex mathematical functions.
* `pandas`: A powerful data manipulation library that offers data structures like DataFrame and Series for handling and analyzing large datasets.
* `matplotlib`: A widely-used plotting library for creating static, interactive, and animated visualizations in Python.
* `scipy`: A scientific computing library built on top of NumPy that provides additional functionality, such as optimization, signal processing, and statistical functions.
* `scikit-learn`: A machine learning library offering a wide range of algorithms for classification, regression, clustering, and dimensionality reduction.
* `tensorflow`: An open-source machine learning library developed by Google for creating, training, and deploying neural networks and other machine learning models.
* `keras`: A high-level neural networks API, running on top of TensorFlow, Microsoft Cognitive Toolkit, Theano, or PlaidML, designed for fast experimentation with deep learning.
* `flask`: A lightweight web application framework that allows you to build web applications and APIs quickly and easily.
* `django`: A high-level web framework that encourages rapid development and clean, pragmatic design, enabling you to build robust web applications quickly.
* `beautifulsoup4`: A library for web scraping purposes, making it easy to parse HTML and XML documents and extract useful information.
* `sqlalchemy`: A SQL toolkit and Object-Relational Mapping (ORM) library for Python, providing a full suite of well-known enterprise-level persistence patterns.
* `pillow`: An easy-to-use library for opening, manipulating, and saving image files in various formats, which is a fork of the Python Imaging Library (PIL).
* `pytorch`: An open-source machine learning library based on the Torch library, primarily developed by Facebook's AI Research lab, for deep learning and tensor computation.
* `fastapi`: A modern, fast, web framework for building APIs with Python based on standard Python type hints, providing high performance and easy-to-learn syntax.
* `pytest`: A powerful and mature testing framework for Python that simplifies the process of writing and running tests, offering advanced features and plugin support.
* `selenium`: A browser automation library, often used for web testing, that allows you to control a browser programmatically and interact with web pages.
* `celery`: A distributed task queue library that enables you to distribute the execution of tasks across multiple worker processes or even multiple machines.

The **Python Package Index (PyPI)** is the primary source for 3rd-party modules. PyPI is a repository of software packages developed and shared by the Python community. You can browse, search, and install packages from PyPI using package management tools like `pip`. Here's the [link to PyPI](https://pypi.org/). <br>

### add modules into your script
**Built-in modules** are **pre-installed** in the Python installation directory, and they are available for use in any Python script without needing to install or import them separately. To add a built-in module to your Python script, you simply need to import it at the beginning of your code using the import statement. <br>
<br>
In the following example, we import the math module and use one of its methods to perform a calculation: <br>

```python
# Import the build-in math module
import math

# Calculate the square root of 25 using the sqrt() function
result = math.sqrt(25)

print("The square root of 25 is:", result)
# Output: The square root of 25 is: 5.0
```

On the other hand, third-party modules are not included in the standard Python installation, and they need to be installed separately. The most popular way to install third-party modules is by using the Python Package Index (PyPI) and `pip`, the package installer for Python.

Make sure to use `pip` for the version of Python you're using. To install a third-party module using `pip`, you can use the following command in your terminal or command prompt: <br>

```sh
pip install requests
```

With that command we have installed the `requests` module, which allows us to send HTTP requests to URLs and receive responses. Now we can import and use the module like any other build-in module or locally stored Python file: <br>

```python
# Import the third-party requests module
import requests

# Make a GET request to a URL 
response = requests.get('https://jsonplaceholder.typicode.com/todos/1')

print(response.content)
# Output:
# b'{\n  "userId": 1,\n  "id": 1,\n  "title": "delectus aut autem",\n  "completed": false\n}'
```

When you install a Python module using `pip`, it is installed in the **site-packages directory** of your Python installation. The location of this directory may vary depending on your operating system and Python version. To find the site-packages directory for your Python installation, you can use the following command in your terminal or command prompt: <br>

```sh
python -m site --user-site
```

This will print the path to the site-packages directory, which should contain all the modules you've installed using `pip`. <br>
<br>
To remove a Python module that you've installed using `pip`, you can use the **uninstall command** with the module's name. For example, to uninstall the `requests` module, you can use the following command: <br>

```sh
pip uninstall requests
```

Besides `pip`, there are other methods to download and import modules. One such method is using Anaconda, a popular Python distribution that includes many scientific computing packages. Anaconda provides its own package manager called `conda`, which you can use to install and manage packages. <br>
<br>
Another method is to download and install the module manually from the official website or repository and then add the module path to your PYTHONPATH environment variable. This method is not recommended for beginners, as it can be error-prone and time-consuming. <br>
