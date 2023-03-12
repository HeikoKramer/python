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
