# Python Study Notes - Complete Guide
---
> *I hope it's easy to read and understand!*

**Credit**: [<span style="color: #007bffff;">Bro Code</span>](https://www.youtube.com/@BroCodez)
**Video Tutorial**: [<span style="color:#007bffff;">Python Tutorial for Beginners</span>](https://youtu.be/ix9cRaBkVe0)

---
## 1. Python Tutorial for Beginners 🐍
**Core Concepts:**
- Python is an interpreted, high-level programming language
- Known for readability and simplicity
- Uses indentation for code blocks (not braces)
- Case-sensitive language
- File extension: `.py`

**Key Points:**
- Install Python from python.org
- Use IDE/editor (VS Code, PyCharm, IDLE)
- Run programs: `python filename.py`
- Interactive mode: type `python` in terminal
- Comments: `#` for single line, `'''` or `"""` for multi-line

**Bullet Points to Remember:**
• Python emphasizes code readability and simplicity
• Indentation is mandatory and defines code structure
• Python is interpreted, not compiled
• Case sensitivity matters (Name ≠ name)

---
## 2. Variables ❎
**Definition:** Named storage locations for data

**Rules:**
- Start with letter or underscore
- Can contain letters, numbers, underscores
- Case-sensitive (age ≠ Age)
- No spaces or special characters
- Can't use Python keywords

**Examples:**
```python
name = "John"          # String
age = 25              # Integer
height = 5.9          # Float
is_student = True     # Boolean
```

**Best Practices:**
- Use descriptive names
- Use snake_case for variables
- Constants in UPPERCASE

**Bullet Points to Remember:**
• Variables are containers that store data values
• No need to declare variable type (dynamically typed)
• Variable names should be descriptive and meaningful
• Use snake_case convention for readability

---
## 3. Type Casting 💱
**Definition:** Converting one data type to another

**Common Conversions:**
```python
# String to Integer
age = int("25")

# Integer to String
age_str = str(25)

# String to Float
price = float("19.99")

# Integer to Float
decimal = float(10)

# Boolean conversions
bool(1)    # True
bool(0)    # False
bool("")   # False
bool("Hi") # True
```

**Important Notes:**
- Invalid conversions raise ValueError
- Loss of precision when converting float to int
- Empty strings/0/None convert to False

**Bullet Points to Remember:**
• Type casting allows conversion between data types
• int() truncates decimal part, doesn't round
• Always handle potential ValueError exceptions
• Empty values generally convert to False in boolean context

---
## 4. User Input ⌨️
**Basic Syntax:**
```python
name = input("Enter your name: ")  # Always returns string
age = int(input("Enter age: "))    # Convert to integer
```

**Key Points:**
- `input()` always returns a string
- Must convert for numerical operations
- Program pauses until user provides input
- Can include prompt message

**Bullet Points to Remember:**
• input() function always returns string type
• Convert input to appropriate type for calculations
• Always validate user input when possible
• Include clear prompts for better user experience

---
## 5. ⭐ Madlibs Game 📖
**Project Structure:**
```python
# Get user inputs
adjective1 = input("Enter an adjective: ")
noun = input("Enter a noun: ")
verb = input("Enter a verb: ")

# Create story
story = f"The {adjective1} {noun} likes to {verb}."
print(story)
```

**Learning Outcomes:**
- String concatenation/formatting
- User interaction
- Variable usage
- Creative output generation

**Bullet Points to Remember:**
• Collect multiple inputs before creating output
• Use f-strings for clean string formatting
• Make prompts specific and clear
• Test with different inputs for variety

---
## 6. Arithmetic & Math 📐
**Basic Operators:**
```python
+   # Addition
-   # Subtraction
*   # Multiplication
/   # Division (float result)
//  # Floor division
%   # Modulus (remainder)
**  # Exponentiation
```

**Math Module:**
```python
import math

math.sqrt(16)      # Square root
math.ceil(4.3)     # Round up
math.floor(4.7)    # Round down
math.pi            # Pi constant
math.pow(2, 3)     # Power
abs(-5)            # Absolute value (built-in)
round(3.7)         # Round (built-in)
```

**Order of Operations:** PEMDAS
1. Parentheses
2. Exponents
3. Multiplication/Division (left to right)
4. Addition/Subtraction (left to right)

**Bullet Points to Remember:**
• / always returns float, // returns integer division
• % operator gives remainder, useful for even/odd checks
• Import math module for advanced mathematical functions
• PEMDAS rules apply, use parentheses for clarity

---
## 7. If Statements 🤔
**Basic Structure:**
```python
if condition:
    # code block
elif another_condition:
    # code block
else:
    # code block
```

**Comparison Operators:**
```python
==  # Equal to
!=  # Not equal to
>   # Greater than
<   # Less than
>=  # Greater than or equal
<=  # Less than or equal
```

**Examples:**
```python
age = 18
if age >= 18:
    print("Adult")
elif age >= 13:
    print("Teenager")
else:
    print("Child")
```

**Bullet Points to Remember:**
• Use == for equality comparison, = for assignment
• elif allows multiple conditions to be checked
• else is optional and catches all remaining cases
• Indentation is crucial for code block definition

---
## 8. ⭐ Calculator Program 🧮
**Basic Implementation:**
```python
num1 = float(input("Enter first number: "))
operator = input("Enter operator (+, -, *, /): ")
num2 = float(input("Enter second number: "))

if operator == "+":
    result = num1 + num2
elif operator == "-":
    result = num1 - num2
elif operator == "*":
    result = num1 * num2
elif operator == "/":
    if num2 != 0:
        result = num1 / num2
    else:
        result = "Error: Division by zero"
else:
    result = "Invalid operator"

print(f"Result: {result}")
```

**Bullet Points to Remember:**
• Always check for division by zero
• Use float() for decimal number support
• Validate operator input before calculation
• Provide clear error messages for invalid inputs

---
## 9. ⭐ Weight Conversion Program 🏋️
**Implementation:**
```python
weight = float(input("Enter weight: "))
unit = input("Kilograms or Pounds? (K/P): ").upper()

if unit == "K":
    converted = weight * 2.205
    print(f"{weight} kg = {converted:.2f} lbs")
elif unit == "P":
    converted = weight / 2.205
    print(f"{weight} lbs = {converted:.2f} kg")
else:
    print("Invalid unit")
```

**Bullet Points to Remember:**
• Use .upper() to handle case variations in input
• Format output to 2 decimal places for readability
• Remember conversion factors (1 kg = 2.205 lbs)
• Handle invalid unit selections gracefully

---
## 10. ⭐ Temperature Conversion Program 🌡️
**Implementation:**
```python
temp = float(input("Enter temperature: "))
unit = input("Celsius or Fahrenheit? (C/F): ").upper()

if unit == "C":
    fahrenheit = (temp * 9/5) + 32
    print(f"{temp}°C = {fahrenheit:.1f}°F")
elif unit == "F":
    celsius = (temp - 32) * 5/9
    print(f"{temp}°F = {celsius:.1f}°C")
```

**Bullet Points to Remember:**
• Remember temperature conversion formulas
• F = (C × 9/5) + 32, C = (F - 32) × 5/9
• Use degree symbols for professional output
• Format to 1 decimal place for temperature precision

---
## 11. Logical Operators 🌦️
**Operators:**
- `and`: Both conditions must be True
- `or`: At least one condition must be True
- `not`: Inverts the boolean value

**Truth Tables:**
```python
# AND
True and True   # True
True and False  # False
False and False # False

# OR
True or False   # True
False or False  # False

# NOT
not True        # False
not False       # True
```

**Example:**
```python
age = 25
has_license = True

if age >= 18 and has_license:
    print("Can drive")
```

**Bullet Points to Remember:**
• 'and' requires all conditions to be True
• 'or' requires at least one condition to be True
• 'not' flips the boolean value
• Use parentheses to group complex logical expressions

## 12. Conditional Expressions ❓
**Ternary Operator:**
```python
# Syntax: value_if_true if condition else value_if_false
age = 20
status = "Adult" if age >= 18 else "Minor"

# Equivalent to:
if age >= 18:
    status = "Adult"
else:
    status = "Minor"
```

**Nested Conditional:**
```python
score = 85
grade = "A" if score >= 90 else "B" if score >= 80 else "C"
```

**Bullet Points to Remember:**
• Ternary operator is shorthand for simple if-else
• Keep ternary expressions simple for readability
• Nested ternaries can become hard to read
• Use regular if-else for complex logic

## 13. String Methods 〰️
**Common Methods:**
```python
text = "Hello World"

text.upper()          # "HELLO WORLD"
text.lower()          # "hello world"
text.capitalize()     # "Hello world"
text.title()          # "Hello World"
text.strip()          # Remove whitespace
text.replace("o", "0") # "Hell0 W0rld"
text.split()          # ["Hello", "World"]
text.find("World")    # 6 (index)
text.count("l")       # 3
text.startswith("He") # True
text.endswith("ld")   # True
text.isalpha()        # False (has space)
text.isdigit()        # False
len(text)             # 11 (built-in function)
```

**Bullet Points to Remember:**
• String methods don't modify original string (immutable)
• Use strip() to remove unwanted whitespace
• find() returns -1 if substring not found
• isdigit() and isalpha() useful for input validation

## 14. String Indexing ✂️
**Concepts:**
```python
text = "Python"
# Indices: 0  1  2  3  4  5
#          P  y  t  h  o  n
# Negative:-6 -5 -4 -3 -2 -1

# Accessing characters
first = text[0]       # 'P'
last = text[-1]       # 'n'

# Slicing [start:end:step]
text[0:3]    # "Pyt" (end exclusive)
text[2:]     # "thon"
text[:4]     # "Pyth"
text[::2]    # "Pto" (every 2nd char)
text[::-1]   # "nohtyP" (reverse)
```

**Bullet Points to Remember:**
• String indexing starts at 0
• Negative indices count from the end
• Slicing end index is exclusive
• [::-1] is common way to reverse strings

## 15. Format Specifiers 💬
**Methods:**
```python
name = "Alice"
age = 25
height = 5.7

# f-strings (Python 3.6+)
print(f"Name: {name}, Age: {age}")

# .format() method
print("Name: {}, Age: {}".format(name, age))

# % formatting (older)
print("Name: %s, Age: %d" % (name, age))

# Format specifiers
price = 19.99
print(f"Price: ${price:.2f}")      # 2 decimal places
print(f"Binary: {10:b}")            # Binary
print(f"Hex: {255:x}")              # Hexadecimal
print(f"Percentage: {0.25:.1%}")    # 25.0%
print(f"Padded: {5:03d}")           # 005
```

**Bullet Points to Remember:**
• f-strings are the modern, preferred method
• :.2f formats to 2 decimal places
• Format specifiers control number display
• f-strings are more readable and faster

## 16. While Loops ♾️
**Structure:**
```python
while condition:
    # code block
    # update condition

# Example
count = 0
while count < 5:
    print(count)
    count += 1

# Infinite loop with break
while True:
    user_input = input("Enter 'quit' to exit: ")
    if user_input == 'quit':
        break
```

**Control Statements:**
- `break`: Exit loop immediately
- `continue`: Skip to next iteration
- `else`: Executes if loop completes normally

**Bullet Points to Remember:**
• Always ensure the condition will eventually become False
• Use break to exit loops based on user input
• continue skips current iteration, doesn't exit loop
• Avoid infinite loops unless intentional

## 17. ⭐ Compound Interest Calculator 💵
**Implementation:**
```python
principal = float(input("Initial amount: $"))
rate = float(input("Interest rate (%): ")) / 100
time = int(input("Time period (years): "))
n = int(input("Compounds per year: "))

amount = principal * (1 + rate/n) ** (n * time)
interest = amount - principal

print(f"Final amount: ${amount:.2f}")
print(f"Interest earned: ${interest:.2f}")
```

**Bullet Points to Remember:**
• Formula: A = P(1 + r/n)^(nt)
• Convert percentage to decimal by dividing by 100
• Use ** for exponentiation
• Display results with 2 decimal places for currency

## 18. For Loops 🔁
**Syntax:**
```python
# Iterate over sequence
for item in sequence:
    # code block

# Range function
for i in range(5):        # 0 to 4
    print(i)

for i in range(1, 6):     # 1 to 5
    print(i)

for i in range(0, 10, 2): # 0, 2, 4, 6, 8
    print(i)

# Iterate over string
for char in "Python":
    print(char)

# Enumerate
fruits = ["apple", "banana", "orange"]
for index, fruit in enumerate(fruits):
    print(f"{index}: {fruit}")
```

**Bullet Points to Remember:**
• for loops iterate over sequences automatically
• range(stop) starts at 0, range(start, stop, step)
• enumerate() provides both index and value
• More pythonic than while loops for known iterations

## 19. ⭐ Countdown Timer Program ⌛
**Implementation:**
```python
import time

seconds = int(input("Enter time in seconds: "))

for remaining in range(seconds, 0, -1):
    mins, secs = divmod(remaining, 60)
    timer = f"{mins:02d}:{secs:02d}"
    print(timer, end="\r")
    time.sleep(1)

print("Time's up!")
```

**Bullet Points to Remember:**
• Use time.sleep(1) to pause for one second
• divmod() returns quotient and remainder
• end="\r" overwrites the same line
• :02d formats numbers with leading zeros

## 20. Nested Loops ➿
**Concept:**
```python
# Multiplication table
for i in range(1, 4):
    for j in range(1, 4):
        print(f"{i} x {j} = {i*j}")
    print()  # New line after each row

# Pattern printing
rows = 5
for i in range(rows):
    for j in range(i + 1):
        print("*", end="")
    print()
```

**Bullet Points to Remember:**
• Inner loop completes fully for each outer loop iteration
• Useful for 2D data structures and patterns
• Can impact performance with large datasets
• Break and continue affect the immediate containing loop

## 21. Lists, Sets, and Tuples 🍎
**Lists (Mutable, Ordered):**
```python
fruits = ["apple", "banana", "orange"]
fruits.append("grape")      # Add to end
fruits.insert(1, "mango")   # Insert at index
fruits.remove("banana")     # Remove by value
fruits.pop()               # Remove last item
fruits.pop(0)              # Remove at index
fruits.sort()              # Sort in place
fruits.reverse()           # Reverse in place
fruits.clear()             # Remove all items
```

**Tuples (Immutable, Ordered):**
```python
coordinates = (10, 20)
x, y = coordinates  # Unpacking
# coordinates[0] = 15  # Error! Immutable
```

**Sets (Mutable, Unordered, No Duplicates):**
```python
numbers = {1, 2, 3, 3}  # {1, 2, 3}
numbers.add(4)
numbers.remove(2)
numbers.discard(5)  # No error if not exists

# Set operations
set1 = {1, 2, 3}
set2 = {3, 4, 5}
set1.union(set2)        # {1, 2, 3, 4, 5}
set1.intersection(set2) # {3}
set1.difference(set2)   # {1, 2}
```

**Bullet Points to Remember:**
• Lists are ordered and mutable, use for sequences
• Tuples are ordered and immutable, use for fixed data
• Sets are unordered and unique, use for membership testing
• Choose the right data structure for your needs

## 22. ⭐ Shopping Cart Program 🛒
**Implementation:**
```python
cart = []
prices = []

while True:
    print("\n1. Add item")
    print("2. Remove item")
    print("3. View cart")
    print("4. Checkout")
    
    choice = input("Select option: ")
    
    if choice == "1":
        item = input("Enter item: ")
        price = float(input("Enter price: $"))
        cart.append(item)
        prices.append(price)
    elif choice == "2":
        item = input("Item to remove: ")
        if item in cart:
            index = cart.index(item)
            cart.pop(index)
            prices.pop(index)
    elif choice == "3":
        for i, item in enumerate(cart):
            print(f"{item}: ${prices[i]:.2f}")
    elif choice == "4":
        total = sum(prices)
        print(f"Total: ${total:.2f}")
        break

print("Thanks for shopping!")
```

**Bullet Points to Remember:**
• Use parallel lists to store related data
• Validate items exist before removing
• Use enumerate() to access both index and value
• sum() function calculates total of numeric list

## 23. 2D Collections ⬜
**2D Lists:**
```python
# Matrix
matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
]

# Accessing elements
matrix[0][0]  # 1
matrix[1][2]  # 6

# Iterating
for row in matrix:
    for element in row:
        print(element, end=" ")
    print()

# List comprehension for 2D
grid = [[0 for _ in range(3)] for _ in range(3)]
```

**Bullet Points to Remember:**
• Use [row][column] indexing for 2D lists
• Nested loops required for full traversal
• List comprehension can create 2D structures
• Useful for grids, matrices, and game boards

## 24. ⭐ Quiz Game 💯
**Implementation:**
```python
questions = [
    ["What is the capital of France?", "Paris"],
    ["What is 2 + 2?", "4"],
    ["What is the largest planet?", "Jupiter"]
]

score = 0

for i, (question, answer) in enumerate(questions):
    print(f"\nQuestion {i+1}: {question}")
    user_answer = input("Your answer: ")
    
    if user_answer.lower() == answer.lower():
        print("Correct!")
        score += 1
    else:
        print(f"Wrong! The answer is {answer}")

print(f"\nFinal score: {score}/{len(questions)}")
```

**Bullet Points to Remember:**
• Store questions and answers in structured format
• Use enumerate() for question numbering
• Make comparisons case-insensitive with .lower()
• Track score throughout the quiz

## 25. Dictionaries 📙
**Basic Operations:**
```python
# Creating dictionaries
student = {"name": "Alice", "age": 20, "grade": "A"}
student = dict(name="Alice", age=20, grade="A")

# Accessing values
print(student["name"])      # Alice
print(student.get("age"))   # 20
print(student.get("height", "Unknown"))  # Unknown (default)

# Modifying
student["age"] = 21         # Update
student["city"] = "NYC"     # Add new key

# Dictionary methods
student.keys()              # dict_keys(['name', 'age', 'grade'])
student.values()            # dict_values(['Alice', 21, 'A'])
student.items()             # key-value pairs

# Iteration
for key in student:
    print(f"{key}: {student[key]}")

for key, value in student.items():
    print(f"{key}: {value}")
```

**Bullet Points to Remember:**
• Dictionaries store key-value pairs
• Keys must be immutable (strings, numbers, tuples)
• Use .get() to avoid KeyError for missing keys
• items() returns key-value pairs for iteration

## 26. ⭐ Concession Stand Program 🍿
**Implementation:**
```python
menu = {
    "popcorn": 3.00,
    "chips": 2.00,
    "pretzel": 4.00,
    "soda": 2.50,
    "lemonade": 4.25
}

cart = []
total = 0

print("--- CONCESSION STAND ---")
for item, price in menu.items():
    print(f"{item}: ${price:.2f}")

while True:
    food = input("\nSelect an item (q to quit): ").lower()
    if food == "q":
        break
    elif food in menu:
        cart.append(food)
        total += menu[food]
        print(f"{food} added to cart")
    else:
        print("Invalid item")

print("\n--- YOUR ORDER ---")
for item in cart:
    print(f"- {item}: ${menu[item]:.2f}")
print(f"Total: ${total:.2f}")
```

**Bullet Points to Remember:**
• Use dictionaries for menu items and prices
• Validate user input against menu keys
• Keep running total as items are added
• Allow users to quit gracefully

## 27. Random Numbers 🎲
**Random Module:**
```python
import random

# Random integer
random.randint(1, 6)        # 1 to 6 inclusive
random.randrange(1, 11)     # 1 to 10 (11 exclusive)

# Random float
random.random()             # 0.0 to 1.0
random.uniform(1.5, 10.5)   # Between 1.5 and 10.5

# Random choice
colors = ["red", "blue", "green"]
random.choice(colors)

# Shuffle list
random.shuffle(colors)      # Modifies original list

# Multiple choices
random.choices(colors, k=3) # With replacement
random.sample(colors, 2)    # Without replacement
```

**Bullet Points to Remember:**
• Always import random module first
• randint() is inclusive on both ends
• randrange() excludes the stop value
• choice() picks one item, choices() picks multiple
• shuffle() modifies the original list

## 28. ⭐ Number Guessing Game 🔢
**Implementation:**
```python
import random

lowest = 1
highest = 100
secret = random.randint(lowest, highest)
guesses = 0
is_running = True

print(f"Number guessing game ({lowest} - {highest})")

while is_running:
    guess = input("Enter your guess: ")
    
    if guess.isdigit():
        guess = int(guess)
        guesses += 1
        
        if guess < lowest or guess > highest:
            print(f"Number must be between {lowest} and {highest}")
        elif guess < secret:
            print("Too low!")
        elif guess > secret:
            print("Too high!")
        else:
            print(f"Correct! The number was {secret}")
            print(f"Number of guesses: {guesses}")
            is_running = False
    else:
        print("Invalid input")
```

**Bullet Points to Remember:**
• Validate input using isdigit()
• Keep track of number of guesses
• Provide helpful feedback (too high/low)
• Check for out-of-range guesses

## 29. ⭐ Rock, Paper, Scissors Game 🗿
**Implementation:**
```python
import random

options = ("rock", "paper", "scissors")
playing = True

while playing:
    player = None
    computer = random.choice(options)
    
    while player not in options:
        player = input("Enter a choice (rock, paper, scissors): ").lower()
    
    print(f"Player: {player}")
    print(f"Computer: {computer}")
    
    if player == computer:
        print("It's a tie!")
    elif (player == "rock" and computer == "scissors") or \
         (player == "paper" and computer == "rock") or \
         (player == "scissors" and computer == "paper"):
        print("You win!")
    else:
        print("You lose!")
    
    if input("Play again? (y/n): ").lower() != "y":
        playing = False

print("Thanks for playing!")
```

**Bullet Points to Remember:**
• Store valid options in a tuple
• Use random.choice() for computer selection
• Check win conditions with logical operators
• Allow players to play multiple rounds

## 30. ⭐ Dice Roller Program ⚂
**Implementation:**
```python
import random

def roll_dice():
    dice_art = {
        1: ("┌─────────┐",
            "│         │",
            "│    ●    │",
            "│         │",
            "└─────────┘"),
        2: ("┌─────────┐",
            "│  ●      │",
            "│         │",
            "│      ●  │",
            "└─────────┘"),
        # ... (add more dice faces)
    }
    
    dice = []
    total = 0
    num_of_dice = int(input("How many dice?: "))
    
    for die in range(num_of_dice):
        dice.append(random.randint(1, 6))
    
    for line in range(5):
        for die in dice:
            print(dice_art[die][line], end=" ")
        print()
    
    total = sum(dice)
    print(f"Total: {total}")

while True:
    roll_dice()
    if input("Roll again? (y/n): ").lower() != "y":
        break
```

**Bullet Points to Remember:**
• Use ASCII art for visual dice representation
• Store dice values in a list
• Print dice art line by line for alignment
• Calculate and display total sum

## 31. Functions 📞
**Basic Syntax:**
```python
def function_name(parameters):
    """Optional docstring"""
    # function body
    return value  # optional

# Examples
def greet(name):
    return f"Hello, {name}!"

def add_numbers(a, b):
    return a + b

def print_info(name, age):
    print(f"Name: {name}, Age: {age}")

# Function call
result = add_numbers(5, 3)
print_info("Alice", 25)
```

**Bullet Points to Remember:**
• Use def keyword to define functions
• Parameters are variables that receive arguments
• return statement sends value back to caller
• Functions promote code reusability
• Use descriptive function names

## 32. Default Arguments 👍
**Syntax:**
```python
def greet(name, greeting="Hello"):
    return f"{greeting}, {name}!"

def calculate_area(length, width=None):
    if width is None:
        return length ** 2  # Square
    return length * width   # Rectangle

# Usage
print(greet("Alice"))           # Uses default greeting
print(greet("Bob", "Hi"))       # Custom greeting
print(calculate_area(5))        # Square: 25
print(calculate_area(4, 6))     # Rectangle: 24
```

**Bullet Points to Remember:**
• Default parameters must come after non-default ones
• Use None for mutable default arguments
• Allows function overloading-like behavior
• Makes functions more flexible

## 33. Keyword Arguments 🗝️
**Syntax:**
```python
def create_profile(name, age, city="Unknown", country="Unknown"):
    return f"{name}, {age} from {city}, {country}"

# Positional arguments
print(create_profile("Alice", 25, "NYC", "USA"))

# Keyword arguments
print(create_profile(name="Bob", age=30, country="Canada"))
print(create_profile("Charlie", age=35, city="London"))

# Mixed (positional first, then keyword)
print(create_profile("Diana", 28, country="Australia"))
```

**Bullet Points to Remember:**
• Keyword arguments can be in any order
• More readable and self-documenting
• Positional args must come before keyword args
• Useful for functions with many parameters

## 34. *args & **kwargs 📦
**Variable Arguments:**
```python
def sum_all(*args):
    """Accept any number of positional arguments"""
    return sum(args)

def print_info(**kwargs):
    """Accept any number of keyword arguments"""
    for key, value in kwargs.items():
        print(f"{key}: {value}")

def full_function(name, *args, **kwargs):
    print(f"Name: {name}")
    print(f"Args: {args}")
    print(f"Kwargs: {kwargs}")

# Usage
print(sum_all(1, 2, 3, 4, 5))  # 15
print_info(name="Alice", age=25, city="NYC")
full_function("Bob", 1, 2, 3, age=30, city="LA")
```

**Bullet Points to Remember:**
• *args collects extra positional arguments into tuple
• **kwargs collects extra keyword arguments into dict
• Order: positional, *args, keyword, **kwargs
• Useful for wrapper functions and APIs

## 35. Iterables 🔂
**Definition and Usage:**
```python
# Iterables: objects that can be looped over
numbers = [1, 2, 3, 4, 5]
text = "Python"
my_dict = {"a": 1, "b": 2}

# iter() and next()
iterator = iter(numbers)
print(next(iterator))  # 1
print(next(iterator))  # 2

# Custom iterable
class Countdown:
    def __init__(self, start):
        self.start = start
    
    def __iter__(self):
        return self
    
    def __next__(self):
        if self.start <= 0:
            raise StopIteration
        self.start -= 1
        return self.start + 1

# Usage
for num in Countdown(3):
    print(num)  # 3, 2, 1
```

**Bullet Points to Remember:**
• Iterables can be used in for loops
• iter() creates iterator from iterable
• next() gets next item from iterator
• StopIteration exception ends iteration
• Lists, strings, dicts are built-in iterables

## 36. Membership Operators 🔎
**Operators:**
```python
# 'in' operator
fruits = ["apple", "banana", "orange"]
print("apple" in fruits)        # True
print("grape" in fruits)        # False

# 'not in' operator
print("grape" not in fruits)    # True

# With strings
text = "Hello World"
print("World" in text)          # True
print("world" in text)          # False (case sensitive)

# With dictionaries (checks keys)
student = {"name": "Alice", "age": 20}
print("name" in student)        # True
print("grade" in student)       # False

# With ranges
print(5 in range(1, 10))        # True
print(15 in range(1, 10))       # False
```

**Bullet Points to Remember:**
• 'in' checks if item exists in sequence
• 'not in' is the opposite of 'in'
• Case-sensitive for strings
• For dicts, checks keys by default
• Works with any iterable object

## 37. List Comprehensions 📃
**Syntax:**
```python
# Basic syntax: [expression for item in iterable]
squares = [x**2 for x in range(1, 6)]  # [1, 4, 9, 16, 25]

# With condition: [expression for item in iterable if condition]
evens = [x for x in range(1, 11) if x % 2 == 0]  # [2, 4, 6, 8, 10]

# With string manipulation
words = ["hello", "world", "python"]
upper_words = [word.upper() for word in words]

# Nested comprehensions
matrix = [[j for j in range(3)] for i in range(3)]

# Dictionary comprehension
squares_dict = {x: x**2 for x in range(1, 6)}

# Set comprehension
unique_lengths = {len(word) for word in words}
```

**Bullet Points to Remember:**
• More concise than traditional loops
• Creates new list, doesn't modify original
• Can include conditions for filtering
• Works with dictionaries and sets too
• Don't overuse - readability matters

## 38. Match-Case Statements 📆
**Syntax (Python 3.10+):**
```python
def handle_response(status):
    match status:
        case 200:
            return "Success"
        case 404:
            return "Not Found"
        case 500:
            return "Server Error"
        case _:  # Default case
            return "Unknown Status"

# Pattern matching with values
def describe_animal(animal):
    match animal:
        case "dog" | "cat":
            return "Domestic pet"
        case "lion" | "tiger":
            return "Wild cat"
        case _:
            return "Unknown animal"

# With conditions
def categorize_number(x):
    match x:
        case n if n < 0:
            return "Negative"
        case 0:
            return "Zero"
        case n if n > 0:
            return "Positive"
```

**Bullet Points to Remember:**
• Python 3.10+ feature (alternative to if-elif)
• Use _ for default case (wildcard)
• Can match multiple values with |
• Supports pattern matching and guards
• More powerful than traditional switch statements

## 39. Modules 📨
**Creating and Using Modules:**
```python
# math_operations.py (custom module)
def add(a, b):
    return a + b

def multiply(a, b):
    return a * b

PI = 3.14159

# main.py
import math_operations
from math_operations import add, PI
import math_operations as math_ops

# Usage
result1 = math_operations.add(5, 3)
result2 = add(5, 3)  # Direct import
result3 = math_ops.multiply(4, 7)

# Built-in modules
import math, random, datetime
import os, sys
```

**Bullet Points to Remember:**
• Modules are .py files containing code
• import brings entire module
• from...import brings specific items
• Use 'as' for aliases
• Python has many built-in modules

## 40. Scope Resolution 🔬
**LEGB Rule:**
```python
x = "global"  # Global scope

def outer():
    x = "enclosing"  # Enclosing scope
    
    def inner():
        x = "local"  # Local scope
        print(f"Inner: {x}")
    
    inner()
    print(f"Outer: {x}")

outer()
print(f"Global: {x}")

# global and nonlocal keywords
count = 0

def increment():
    global count
    count += 1

def outer_func():
    x = 10
    
    def inner_func():
        nonlocal x
        x += 1
    
    inner_func()
    return x
```

**Bullet Points to Remember:**
• LEGB: Local → Enclosing → Global → Built-in
• Use 'global' to modify global variables
• Use 'nonlocal' to modify enclosing scope variables
• Variables are searched in LEGB order
• Avoid global variables when possible

## 41. if __name__ == '__main__': 📥
**Purpose and Usage:**
```python
# utilities.py
def helper_function():
    return "This is a helper function"

def main():
    print("Running utilities.py directly")
    print(helper_function())

if __name__ == "__main__":
    main()

# main_program.py
import utilities

# This will import utilities but won't run main()
result = utilities.helper_function()
print(result)
```

**Bullet Points to Remember:**
• Allows modules to be both imported and run directly
• Code under if __name__ == "__main__": only runs when script is executed directly
• Prevents code from running during imports
• Good practice for all Python modules
• Enables module testing

## 42. ⭐ Banking Program 💰
**Implementation:**
```python
def show_balance(balance):
    print(f"Your balance is ${balance:.2f}")

def deposit():
    amount = float(input("Enter amount to deposit: $"))
    if amount <= 0:
        print("Invalid amount")
        return 0
    return amount

def withdraw(balance):
    amount = float(input("Enter amount to withdraw: $"))
    if amount > balance:
        print("Insufficient funds")
        return 0
    elif amount <= 0:
        print("Invalid amount")
        return 0
    return amount

def main():
    balance = 0
    is_running = True
    
    while is_running:
        print("\n--- Banking Program ---")
        print("1. Show Balance")
        print("2. Deposit")
        print("3. Withdraw")
        print("4. Exit")
        
        choice = input("Enter choice: ")
        
        if choice == "1":
            show_balance(balance)
        elif choice == "2":
            balance += deposit()
        elif choice == "3":
            balance -= withdraw(balance)
        elif choice == "4":
            is_running = False
        else:
            print("Invalid choice")

if __name__ == "__main__":
    main()
```

**Bullet Points to Remember:**
• Separate functions for different operations
• Validate user input for amounts
• Check for sufficient funds before withdrawal
• Use main() function for program flow
• Keep running balance throughout session

## 43. ⭐ Slot Machine 🎰
**Implementation:**
```python
import random

def spin_row():
    symbols = ['🍒', '🍊', '🍋', '🔔', '⭐']
    return [random.choice(symbols) for _ in range(3)]

def print_row(row):
    print(" | ".join(row))

def get_payout(row, bet):
    if row[0] == row[1] == row[2]:
        if row[0] == '🍒':
            return bet * 3
        elif row[0] == '🍊':
            return bet * 4
        elif row[0] == '🍋':
            return bet * 5
        elif row[0] == '🔔':
            return bet * 10
        elif row[0] == '⭐':
            return bet * 20
    return 0

def main():
    balance = 100
    
    print("🎰 Welcome to Slot Machine! 🎰")
    
    while balance > 0:
        print(f"\nCurrent balance: ${balance}")
        
        bet = input("Place bet (or 'quit'): ")
        if bet.lower() == 'quit':
            break
            
        bet = int(bet)
        if bet > balance:
            print("Insufficient balance!")
            continue
        
        balance -= bet
        row = spin_row()
        print("Spinning...\n")
        print_row(row)
        
        payout = get_payout(row, bet)
        if payout > 0:
            print(f"You won ${payout}!")
        else:
            print("Sorry, you lost!")
        
        balance += payout
    
    print(f"Game over! Final balance: ${balance}")

if __name__ == "__main__":
    main()
```

**Bullet Points to Remember:**
• Use random.choice() for symbol selection
• Different symbols have different payout rates
• Check for three matching symbols
• Deduct bet before spinning
• Add payout to balance after winning

## 44. ⭐ Encryption Program 🔐
**Caesar Cipher Implementation:**
```python
def encrypt(text, shift):
    encrypted = ""
    for char in text:
        if char.isalpha():
            ascii_offset = 65 if char.isupper() else 97
            encrypted += chr((ord(char) - ascii_offset + shift) % 26 + ascii_offset)
        else:
            encrypted += char
    return encrypted

def decrypt(text, shift):
    return encrypt(text, -shift)

def main():
    print("--- Encryption Program ---")
    
    while True:
        choice = input("\n1. Encrypt\n2. Decrypt\n3. Quit\nChoice: ")
        
        if choice == "1":
            message = input("Enter message to encrypt: ")
            shift = int(input("Enter shift value: "))
            encrypted = encrypt(message, shift)
            print(f"Encrypted: {encrypted}")
            
        elif choice == "2":
            message = input("Enter message to decrypt: ")
            shift = int(input("Enter shift value: "))
            decrypted = decrypt(message, shift)
            print(f"Decrypted: {decrypted}")
            
        elif choice == "3":
            break
        else:
            print("Invalid choice")

if __name__ == "__main__":
    main()
```

**Bullet Points to Remember:**
• Caesar cipher shifts letters by fixed amount
• Use ord() to get ASCII value, chr() to convert back
• Handle uppercase and lowercase separately
• Non-alphabetic characters remain unchanged
• Decryption uses negative shift

## 45. ⭐ Hangman Game 🕺
**Implementation:**
```python
import random

def display_hangman(tries):
    stages = [
        """
           --------
           |      |
           |      O
           |     \\|/
           |      |
           |     / \\
           -
        """,
        """
           --------
           |      |
           |      O
           |     \\|/
           |      |
           |     / 
           -
        """
        # Add more stages...
    ]
    return stages[tries] if tries < len(stages) else ""

def main():
    words = ["python", "programming", "computer", "hangman"]
    word = random.choice(words).upper()
    word_completion = "_" * len(word)
    guessed = False
    guessed_letters = []
    tries = 6
    
    print("Let's play Hangman!")
    print(display_hangman(tries))
    print(word_completion)
    
    while not guessed and tries > 0:
        guess = input("Guess a letter: ").upper()
        
        if len(guess) == 1 and guess.isalpha():
            if guess in guessed_letters:
                print("Already guessed!")
            elif guess not in word:
                print(f"{guess} is not in the word")
                tries -= 1
                guessed_letters.append(guess)
            else:
                print(f"Good guess! {guess} is in the word")
                guessed_letters.append(guess)
                word_list = list(word_completion)
                indices = [i for i, letter in enumerate(word) if letter == guess]
                for index in indices:
                    word_list[index] = guess
                word_completion = "".join(word_list)
                
                if "_" not in word_completion:
                    guessed = True
        else:
            print("Invalid input")
        
        print(display_hangman(tries))
        print(word_completion)
    
    if guessed:
        print("Congratulations! You won!")
    else:
        print(f"Game over! The word was {word}")

if __name__ == "__main__":
    main()
```

**Bullet Points to Remember:**
• Track guessed letters to avoid duplicates
• Update word display when correct letter guessed
• Decrease tries only for wrong guesses
• Use ASCII art for visual feedback
• Check for win condition after each guess

## 46. Python Object-Oriented Programming 🚗
**Classes and Objects:**
```python
class Car:
    def __init__(self, make, model, year, color):
        self.make = make
        self.model = model
        self.year = year
        self.color = color
        self.odometer = 0
    
    def drive(self, distance):
        if distance >= 0:
            self.odometer += distance
        else:
            print("Distance cannot be negative")
    
    def get_info(self):
        return f"{self.year} {self.make} {self.model} ({self.color})"

# Creating objects
car1 = Car("Toyota", "Camry", 2022, "Blue")
car2 = Car("Honda", "Civic", 2021, "Red")

# Using methods
print(car1.get_info())
car1.drive(100)
print(f"Odometer: {car1.odometer}")
```

**Bullet Points to Remember:**
• Classes are blueprints for creating objects
• __init__ method initializes object attributes
• self refers to the current instance
• Methods are functions defined inside classes
• Objects are instances of classes

## 47. Class Variables 🎓
**Class vs Instance Variables:**
```python
class Student:
    school_name = "Python University"  # Class variable
    num_students = 0                   # Class variable
    
    def __init__(self, name, age):
        self.name = name               # Instance variable
        self.age = age                 # Instance variable
        Student.num_students += 1      # Access class variable
    
    @classmethod
    def get_school_name(cls):
        return cls.school_name
    
    @classmethod
    def get_num_students(cls):
        return cls.num_students

# Usage
student1 = Student("Alice", 20)
student2 = Student("Bob", 21)

print(Student.school_name)        # Class variable
print(student1.name)              # Instance variable
print(Student.get_num_students()) # 2
```

**Bullet Points to Remember:**
• Class variables are shared by all instances
• Instance variables are unique to each object
• Use ClassName.variable to access class variables
• @classmethod decorator for class methods
• cls parameter refers to the class itself

## 48. Inheritance 👨‍👦‍👦
**Parent and Child Classes:**
```python
class Animal:
    def __init__(self, name):
        self.name = name
        self.is_alive = True
    
    def eat(self):
        print(f"{self.name} is eating")
    
    def sleep(self):
        print(f"{self.name} is sleeping")

class Dog(Animal):  # Dog inherits from Animal
    def __init__(self, name, breed):
        super().__init__(name)  # Call parent constructor
        self.breed = breed
    
    def bark(self):
        print(f"{self.name} is barking")

class Cat(Animal):
    def __init__(self, name, indoor):
        super().__init__(name)
        self.indoor = indoor
    
    def meow(self):
        print(f"{self.name} is meowing")

# Usage
dog = Dog("Buddy", "Golden Retriever")
cat = Cat("Whiskers", True)

dog.eat()   # Inherited method
dog.bark()  # Child method
cat.sleep() # Inherited method
cat.meow()  # Child method
```

**Bullet Points to Remember:**
• Child classes inherit attributes and methods from parent
• Use super() to call parent class methods
• Child classes can override parent methods
• Child classes can add their own methods
• Promotes code reusability

## 49. Multiple Inheritance 🐟
**Inheriting from Multiple Classes:**
```python
class Animal:
    def __init__(self, name):
        self.name = name
    
    def eat(self):
        print(f"{self.name} is eating")

class Swimmer:
    def swim(self):
        print(f"{self.name} is swimming")

class Flyer:
    def fly(self):
        print(f"{self.name} is flying")

class Fish(Animal, Swimmer):
    def __init__(self, name):
        super().__init__(name)

class Bird(Animal, Flyer):
    def __init__(self, name):
        super().__init__(name)

class Duck(Animal, Swimmer, Flyer):
    def __init__(self, name):
        super().__init__(name)

# Usage
fish = Fish("Nemo")
bird = Bird("Tweety")
duck = Duck("Donald")

duck.eat()   # From Animal
duck.swim()  # From Swimmer
duck.fly()   # From Flyer
```

**Bullet Points to Remember:**
• A class can inherit from multiple parent classes
• Method Resolution Order (MRO) determines which method is called
• Use super() carefully with multiple inheritance
• Can lead to diamond problem - be cautious
• Consider composition over multiple inheritance

## 50. super() 🔴
**Using super() Function:**
```python
class Shape:
    def __init__(self, color, is_filled):
        self.color = color
        self.is_filled = is_filled
    
    def describe(self):
        print(f"It is {self.color} and {'filled' if self.is_filled else 'not filled'}")

class Circle(Shape):
    def __init__(self, color, is_filled, radius):
        super().__init__(color, is_filled)
        self.radius = radius
    
    def describe(self):
        super().describe()  # Call parent method
        print(f"It is a circle with area of {3.14159 * self.radius ** 2:.2f}cm²")

class Square(Shape):
    def __init__(self, color, is_filled, width):
        super().__init__(color, is_filled)
        self.width = width
    
    def describe(self):
        super().describe()
        print(f"It is a square with area of {self.width ** 2}cm²")

# Usage
circle = Circle("red", True, 5)
square = Square("blue", False, 4)

circle.describe()
square.describe()
```

**Bullet Points to Remember:**
• super() calls methods from parent class
• Useful for extending parent functionality
• Maintains inheritance chain properly
• Essential for proper constructor chaining
• Helps with method resolution in complex hierarchies

## 51. Polymorphism 🎭
**Same Interface, Different Implementation:**
```python
from abc import ABC, abstractmethod

class Shape(ABC):
    @abstractmethod
    def area(self):
        pass
    
    @abstractmethod
    def perimeter(self):
        pass

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    def area(self):
        return 3.14159 * self.radius ** 2
    
    def perimeter(self):
        return 2 * 3.14159 * self.radius

class Square(Shape):
    def __init__(self, side):
        self.side = side
    
    def area(self):
        return self.side ** 2
    
    def perimeter(self):
        return 4 * self.side

class Triangle(Shape):
    def __init__(self, a, b, c):
        self.a = a
        self.b = b
        self.c = c
    
    def area(self):
        s = (self.a + self.b + self.c) / 2
        return (s * (s - self.a) * (s - self.b) * (s - self.c)) ** 0.5
    
    def perimeter(self):
        return self.a + self.b + self.c

# Polymorphism in action
shapes = [Circle(5), Square(4), Triangle(3, 4, 5)]

for shape in shapes:
    print(f"Area: {shape.area():.2f}")
    print(f"Perimeter: {shape.perimeter():.2f}")
    print("-" * 20)
```

**Bullet Points to Remember:**
• Same method name, different implementations
• Abstract base classes define common interface
• Enables treating different objects uniformly
• @abstractmethod forces implementation in child classes
• Powerful for building flexible systems

## 52. Duck Typing 🦆
**"If it looks like a duck and quacks like a duck, it's a duck":**
```python
class Duck:
    def walk(self):
        print("Duck is walking")
    
    def talk(self):
        print("Duck says quack")

class Chicken:
    def walk(self):
        print("Chicken is walking")
    
    def talk(self):
        print("Chicken says cluck")

class Person:
    def walk(self):
        print("Person is walking")
    
    def talk(self):
        print("Person says hello")

def make_it_walk_and_talk(animal):
    # Duck typing - we don't check the type
    # We just call the methods
    animal.walk()
    animal.talk()

# Usage
duck = Duck()
chicken = Chicken()
person = Person()

make_it_walk_and_talk(duck)     # Works
make_it_walk_and_talk(chicken)  # Works
make_it_walk_and_talk(person)   # Works
```

**Bullet Points to Remember:**
• Python focuses on behavior, not type
• No need for explicit inheritance or interfaces
• If object has required methods, it works
• More flexible than static typing
• "Easier to ask for forgiveness than permission"

## 53. Static Methods ⚡
**Methods that don't need self or cls:**
```python
class MathUtils:
    @staticmethod
    def add(x, y):
        return x + y
    
    @staticmethod
    def multiply(x, y):
        return x * y
    
    @staticmethod
    def is_prime(n):
        if n < 2:
            return False
        for i in range(2, int(n ** 0.5) + 1):
            if n % i == 0:
                return False
        return True

class Employee:
    def __init__(self, name, position):
        self.name = name
        self.position = position
    
    @staticmethod
    def is_workday(day):
        return day.lower() not in ['saturday', 'sunday']

# Usage
print(MathUtils.add(5, 3))        # 8
print(MathUtils.is_prime(17))     # True

employee = Employee("Alice", "Developer")
print(Employee.is_workday("Monday"))  # True
print(employee.is_workday("Sunday"))  # False
```

**Bullet Points to Remember:**
• Static methods don't access self or cls
• Can be called on class or instance
• Use @staticmethod decorator
• Utility functions related to the class
• Don't need instance to be created

## 54. Class Methods 🏫
**Methods that work with the class itself:**
```python
class Pizza:
    def __init__(self, ingredients):
        self.ingredients = ingredients
    
    def __repr__(self):
        return f"Pizza({self.ingredients})"
    
    @classmethod
    def margherita(cls):
        return cls(['mozzarella', 'tomatoes', 'basil'])
    
    @classmethod
    def prosciutto(cls):
        return cls(['mozzarella', 'tomatoes', 'ham'])

class Person:
    population = 0
    
    def __init__(self, name, age):
        self.name = name
        self.age = age
        Person.population += 1
    
    @classmethod
    def get_population(cls):
        return cls.population
    
    @classmethod
    def from_string(cls, person_str):
        name, age = person_str.split('-')
        return cls(name, int(age))

# Usage
pizza1 = Pizza.margherita()  # Class method
pizza2 = Pizza.prosciutto()  # Class method

person1 = Person("Alice", 25)
person2 = Person.from_string("Bob-30")  # Alternative constructor

print(Person.get_population())  # 2
```

**Bullet Points to Remember:**
• Class methods receive cls as first parameter
• Use @classmethod decorator
• Can access class variables and methods
• Often used for alternative constructors
• Can be called on class or instance

## 55. Magic Methods 🌟
**Special Methods (Dunder Methods):**
```python
class Book:
    def __init__(self, title, author, pages):
        self.title = title
        self.author = author
        self.pages = pages
    
    def __str__(self):  # String representation for users
        return f"{self.title} by {self.author}"
    
    def __repr__(self):  # String representation for developers
        return f"Book('{self.title}', '{self.author}', {self.pages})"
    
    def __len__(self):  # len() function
        return self.pages
    
    def __eq__(self, other):  # == operator
        return self.title == other.title and self.author == other.author
    
    def __lt__(self, other):  # < operator
        return self.pages < other.pages
    
    def __add__(self, other):  # + operator
        return f"{self.title} & {other.title}"
    
    def __contains__(self, keyword):  # 'in' operator
        return keyword.lower() in self.title.lower()
    
    def __getitem__(self, key):  # [] operator
        if key == "title":
            return self.title
        elif key == "author":
            return self.author
        elif key == "pages":
            return self.pages

# Usage
book1 = Book("1984", "George Orwell", 328)
book2 = Book("Animal Farm", "George Orwell", 112)

print(str(book1))        # 1984 by George Orwell
print(repr(book1))       # Book('1984', 'George Orwell', 328)
print(len(book1))        # 328
print(book1 == book2)    # False
print(book1 > book2)     # True
print(book1 + book2)     # 1984 & Animal Farm
print("1984" in book1)   # True
print(book1["title"])    # 1984
```

**Bullet Points to Remember:**
• Magic methods start and end with double underscores
• Allow custom behavior for built-in operations
• __str__ for user-friendly string representation
• __repr__ for developer string representation
• Enable operator overloading

## 56. @property ⚙️
**Getter, Setter, and Deleter:**
```python
class Circle:
    def __init__(self, radius):
        self._radius = radius
    
    @property
    def radius(self):
        return self._radius
    
    @radius.setter
    def radius(self, value):
        if value > 0:
            self._radius = value
        else:
            raise ValueError("Radius must be positive")
    
    @property
    def area(self):
        return 3.14159 * self._radius ** 2
    
    @property
    def diameter(self):
        return self._radius * 2
    
    @diameter.setter
    def diameter(self, value):
        if value > 0:
            self._radius = value / 2
        else:
            raise ValueError("Diameter must be positive")

class Temperature:
    def __init__(self, celsius=0):
        self._celsius = celsius
    
    @property
    def celsius(self):
        return self._celsius
    
    @celsius.setter
    def celsius(self, value):
        if value < -273.15:
            raise ValueError("Temperature below absolute zero is not possible")
        self._celsius = value
    
    @property
    def fahrenheit(self):
        return (self._celsius * 9/5) + 32
    
    @fahrenheit.setter
    def fahrenheit(self, value):
        self.celsius = (value - 32) * 5/9

# Usage
circle = Circle(5)
print(circle.radius)     # 5
print(circle.area)       # 78.54
circle.diameter = 10     # Sets radius to 5
print(circle.radius)     # 5

temp = Temperature(25)
print(temp.celsius)      # 25
print(temp.fahrenheit)   # 77.0
temp.fahrenheit = 86
print(temp.celsius)      # 30.0
```

**Bullet Points to Remember:**
• @property makes methods accessible like attributes
• Provides getter, setter, and deleter functionality
• Enables data validation and computed properties
• Use underscore prefix for "private" attributes
• Maintains clean interface while adding logic

## 57. Decorators 🎊
**Functions that modify other functions:**
```python
def timing_decorator(func):
    import time
    def wrapper(*args, **kwargs):
        start = time.time()
        result = func(*args, **kwargs)
        end = time.time()
        print(f"{func.__name__} took {end - start:.4f} seconds")
        return result
    return wrapper

def debug_decorator(func):
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with args: {args}, kwargs: {kwargs}")
        result = func(*args, **kwargs)
        print(f"{func.__name__} returned: {result}")
        return result
    return wrapper

def cache_decorator(func):
    cache = {}
    def wrapper(*args):
        if args in cache:
            print(f"Cache hit for {args}")
            return cache[args]
        result = func(*args)
        cache[args] = result
        return result
    return wrapper

# Using decorators
@timing_decorator
@debug_decorator
def slow_function(n):
    import time
    time.sleep(1)
    return n * 2

@cache_decorator
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

# Usage
result = slow_function(5)  # Shows timing and debug info
print(fibonacci(10))       # Uses caching for efficiency
```

**Bullet Points to Remember:**
• Decorators modify function behavior without changing code
• Use @decorator_name syntax above function definition
• Common use cases: timing, logging, caching, authentication
• Can stack multiple decorators
• functools.wraps preserves original function metadata

## 58. Exception Handling 🚦
**Try, Except, Else, Finally:**
```python
# Basic exception handling
try:
    num = int(input("Enter a number: "))
    result = 10 / num
    print(f"Result: {result}")
except ValueError:
    print("Invalid input! Please enter a number.")
except ZeroDivisionError:
    print("Cannot divide by zero!")
except Exception as e:
    print(f"An unexpected error occurred: {e}")
else:
    print("No exceptions occurred!")
finally:
    print("This always executes")

# Custom exceptions
class CustomError(Exception):
    def __init__(self, message):
        self.message = message
        super().__init__(self.message)

def validate_age(age):
    if age < 0:
        raise CustomError("Age cannot be negative")
    elif age > 150:
        raise CustomError("Age seems unrealistic")
    return True

# Raising exceptions
try:
    age = int(input("Enter your age: "))
    validate_age(age)
    print(f"Age {age} is valid")
except CustomError as e:
    print(f"Validation error: {e}")
except ValueError:
    print("Please enter a valid number")
```

**Bullet Points to Remember:**
• Use try-except to handle potential errors gracefully
• Specific exceptions should be caught before general ones
• else block runs only if no exceptions occur
• finally block always executes (cleanup code)
• Create custom exceptions by inheriting from Exception

## 59. File Detection 🕵️‍♂️
**Checking if Files and Directories Exist:**
```python
import os

def check_file_or_directory(path):
    if os.path.exists(path):
        if os.path.isfile(path):
            print(f"'{path}' is a file")
            print(f"Size: {os.path.getsize(path)} bytes")
            print(f"Last modified: {os.path.getmtime(path)}")
        elif os.path.isdir(path):
            print(f"'{path}' is a directory")
            files = os.listdir(path)
            print(f"Contains {len(files)} items")
    else:
        print(f"'{path}' does not exist")

# File operations
import os.path

file_path = "example.txt"

# Check if file exists
if os.path.isfile(file_path):
    print("File exists")
else:
    print("File does not exist")

# Get file information
if os.path.exists(file_path):
    print(f"File size: {os.path.getsize(file_path)} bytes")
    print(f"Absolute path: {os.path.abspath(file_path)}")
    print(f"Directory: {os.path.dirname(file_path)}")
    print(f"Filename: {os.path.basename(file_path)}")

# Create directory if it doesn't exist
directory = "my_folder"
if not os.path.exists(directory):
    os.makedirs(directory)
    print(f"Created directory: {directory}")
```

**Bullet Points to Remember:**
• Use os.path.exists() to check if path exists
• os.path.isfile() checks specifically for files
• os.path.isdir() checks specifically for directories
• Always check existence before file operations
• os.makedirs() creates directories recursively

## 60. Writing Files ✍
**Creating and Writing to Files:**
```python
import json
import csv

# Basic file writing
def write_text_file():
    # Write mode (overwrites existing content)
    with open("example.txt", "w") as file:
        file.write("Hello, World!\n")
        file.write("This is line 2\n")
    
    # Append mode (adds to existing content)
    with open("example.txt", "a") as file:
        file.write("This line is appended\n")

# Writing JSON data
def write_json_file():
    data = {
        "name": "Alice",
        "age": 30,
        "city": "New York",
        "hobbies": ["reading", "swimming", "coding"]
    }
    
    with open("data.json", "w") as file:
        json.dump(data, file, indent=4)

# Writing CSV data
def write_csv_file():
    students = [
        ["Name", "Age", "Grade"],
        ["Alice", 20, "A"],
        ["Bob", 21, "B"],
        ["Charlie", 19, "A+"]
    ]
    
    with open("students.csv", "w", newline='') as file:
        writer = csv.writer(file)
        writer.writerows(students)

# Error handling with file writing
def safe_write_file(filename, content):
    try:
        with open(filename, "w") as file:
            file.write(content)
        print(f"Successfully wrote to {filename}")
    except PermissionError:
        print(f"Permission denied: Cannot write to {filename}")
    except Exception as e:
        print(f"Error writing file: {e}")

# Usage
write_text_file()
write_json_file()
write_csv_file()
safe_write_file("output.txt", "Sample content")
```

**Bullet Points to Remember:**
• Use 'with' statement for automatic file closing
• 'w' mode overwrites, 'a' mode appends
• Always handle file writing exceptions
• json.dump() for JSON files, csv.writer() for CSV files
• Use newline='' parameter when writing CSV files

## 61. Reading Files 🔍
**Reading Different File Types:**
```python
import json
import csv

# Basic file reading
def read_text_file(filename):
    try:
        with open(filename, "r") as file:
            # Read entire file
            content = file.read()
            print("Full content:")
            print(content)
            
        with open(filename, "r") as file:
            # Read line by line
            print("\nLine by line:")
            for line_num, line in enumerate(file, 1):
                print(f"Line {line_num}: {line.strip()}")
                
        with open(filename, "r") as file:
            # Read all lines into list
            lines = file.readlines()
            print(f"\nTotal lines: {len(lines)}")
            
    except FileNotFoundError:
        print(f"File '{filename}' not found")
    except Exception as e:
        print(f"Error reading file: {e}")

# Reading JSON files
def read_json_file(filename):
    try:
        with open(filename, "r") as file:
            data = json.load(file)
            print("JSON data:")
            for key, value in data.items():
                print(f"{key}: {value}")
    except FileNotFoundError:
        print(f"JSON file '{filename}' not found")
    except json.JSONDecodeError:
        print("Invalid JSON format")

# Reading CSV files
def read_csv_file(filename):
    try:
        with open(filename, "r") as file:
            reader = csv.reader(file)
            headers = next(reader)  # Get first row as headers
            print(f"Headers: {headers}")
            
            for row_num, row in enumerate(reader, 1):
                print(f"Row {row_num}: {dict(zip(headers, row))}")
                
    except FileNotFoundError:
        print(f"CSV file '{filename}' not found")
    except Exception as e:
        print(f"Error reading CSV: {e}")

# Reading file with encoding
def read_with_encoding(filename, encoding="utf-8"):
    try:
        with open(filename, "r", encoding=encoding) as file:
            content = file.read()
            return content
    except UnicodeDecodeError:
        print(f"Cannot decode file with {encoding} encoding")
    except FileNotFoundError:
        print(f"File '{filename}' not found")

# Usage
read_text_file("example.txt")
read_json_file("data.json")
read_csv_file("students.csv")
content = read_with_encoding("example.txt")
```

**Bullet Points to Remember:**
• Always use try-except when reading files
• read() gets entire file, readline() gets one line
• readlines() returns list of all lines
• Use appropriate encoding (utf-8 is common)
• json.load() for JSON, csv.reader() for CSV files

## 62. Dates & Times 📅
**Working with datetime Module:**
```python
import datetime
import time

# Current date and time
now = datetime.datetime.now()
print(f"Current datetime: {now}")
print(f"Current date: {now.date()}")
print(f"Current time: {now.time()}")

# Creating specific dates
birthday = datetime.date(1990, 5, 15)
meeting_time = datetime.time(14, 30, 0)  # 2:30 PM
appointment = datetime.datetime(2024, 12, 25, 10, 30)

# Formatting dates
print(f"Formatted date: {now.strftime('%Y-%m-%d %H:%M:%S')}")
print(f"Readable format: {now.strftime('%B %d, %Y at %I:%M %p')}")

# Date arithmetic
today = datetime.date.today()
one_week = datetime.timedelta(weeks=1)
next_week = today + one_week
last_month = today - datetime.timedelta(days=30)

print(f"Today: {today}")
print(f"Next week: {next_week}")
print(f"30 days ago: {last_month}")

# Age calculation
def calculate_age(birth_date):
    today = datetime.date.today()
    age = today - birth_date
    return age.days // 365

age = calculate_age(birthday)
print(f"Age: {age} years")

# Parsing date strings
date_string = "2024-03-15"
parsed_date = datetime.datetime.strptime(date_string, "%Y-%m-%d")
print(f"Parsed date: {parsed_date}")

# Time zones (requires pytz for full support)
utc_now = datetime.datetime.utcnow()
print(f"UTC time: {utc_now}")

# Measuring execution time
start_time = time.time()
time.sleep(1)  # Simulate work
end_time = time.time()
execution_time = end_time - start_time
print(f"Execution time: {execution_time:.2f} seconds")
```

**Bullet Points to Remember:**
• datetime.datetime.now() for current date and time
• Use strftime() to format dates as strings
• Use strptime() to parse strings into dates
• timedelta for date arithmetic
• time.time() for measuring execution time

## 63. ⭐ Alarm Clock ⏰
**Implementation:**
```python
import datetime
import time
import threading
import pygame  # For sound (install: pip install pygame)

class AlarmClock:
    def __init__(self):
        pygame.mixer.init()
        self.alarms = []
        self.running = True
    
    def add_alarm(self, alarm_time, message="Wake up!"):
        self.alarms.append({
            'time': alarm_time,
            'message': message,
            'active': True
        })
        print(f"Alarm set for {alarm_time.strftime('%H:%M:%S')}")
    
    def play_alarm_sound(self):
        # Create a simple beep sound or load a sound file
        try:
            # You can replace this with loading an actual sound file
            # pygame.mixer.music.load("alarm.mp3")
            # pygame.mixer.music.play()
            
            # Alternative: system beep
            import os
            os.system("echo '\a'")  # System beep
        except:
            print("BEEP! BEEP! BEEP!")  # Fallback
    
    def check_alarms(self):
        while self.running:
            current_time = datetime.datetime.now().time()
            
            for alarm in self.alarms:
                if alarm['active']:
                    alarm_time = alarm['time']
                    # Check if current time matches alarm time (within 1 second)
                    if (current_time.hour == alarm_time.hour and 
                        current_time.minute == alarm_time.minute and
                        current_time.second == alarm_time.second):
                        
                        print(f"\n🚨 ALARM! {alarm['message']} 🚨")
                        self.play_alarm_sound()
                        alarm['active'] = False  # Disable after triggering
            
            time.sleep(1)  # Check every second
    
    def start(self):
        # Start alarm checking in background thread
        alarm_thread = threading.Thread(target=self.check_alarms)
        alarm_thread.daemon = True
        alarm_thread.start()
        
        print("Alarm clock started! Press Ctrl+C to exit.")
        try:
            while True:
                command = input("\nCommands: 'add' to add alarm, 'list' to show alarms, 'quit' to exit: ").lower()
                
                if command == 'add':
                    time_str = input("Enter alarm time (HH:MM:SS): ")
                    try:
                        alarm_time = datetime.datetime.strptime(time_str, "%H:%M:%S").time()
                        message = input("Enter alarm message (optional): ") or "Wake up!"
                        self.add_alarm(alarm_time, message)
                    except ValueError:
                        print("Invalid time format. Use HH:MM:SS")
                
                elif command == 'list':
                    if self.alarms:
                        print("\nActive Alarms:")
                        for i, alarm in enumerate(self.alarms, 1):
                            status = "Active" if alarm['active'] else "Triggered"
                            print(f"{i}. {alarm['time'].strftime('%H:%M:%S')} - {alarm['message']} ({status})")
                    else:
                        print("No alarms set.")
                
                elif command == 'quit':
                    self.running = False
                    break
                
        except KeyboardInterrupt:
            self.running = False
            print("\nAlarm clock stopped.")

# Simple version without pygame
def simple_alarm_clock():
    print("Simple Alarm Clock")
    alarm_time = input("Set alarm time (HH:MM): ")
    
    try:
        hour, minute = map(int, alarm_time.split(':'))
        alarm_datetime = datetime.time(hour, minute)
        
        print(f"Alarm set for {alarm_datetime.strftime('%H:%M')}")
        print("Waiting for alarm time...")
        
        while True:
            current_time = datetime.datetime.now().time()
            if current_time.hour == hour and current_time.minute == minute:
                print("\n🚨 ALARM! Wake up! 🚨")
                for _ in range(5):
                    print("BEEP! ", end="", flush=True)
                    time.sleep(0.5)
                break
            time.sleep(30)  # Check every 30 seconds
            
    except ValueError:
        print("Invalid time format. Use HH:MM")
    except KeyboardInterrupt:
        print("\nAlarm cancelled.")

# Usage
if __name__ == "__main__":
    # Use simple version or full version
    choice = input("Use simple alarm (s) or full alarm clock (f)? ").lower()
    
    if choice == 's':
        simple_alarm_clock()
    else:
        alarm_clock = AlarmClock()
        alarm_clock.start()
```

**Bullet Points to Remember:**
• Use threading for background alarm checking
• Compare current time with alarm time
• Handle time parsing with strptime()
• Consider using sound libraries for audio alerts
• Implement graceful shutdown with keyboard interrupts

## 64. Multithreading 🧵
**Running Multiple Tasks Concurrently:**
```python
import threading
import time
import concurrent.futures

# Basic threading
def print_numbers():
    for i in range(1, 6):
        print(f"Number: {i}")
        time.sleep(1)

def print_letters():
    for letter in ['A', 'B', 'C', 'D', 'E']:
        print(f"Letter: {letter}")
        time.sleep(1)

# Running without threads (sequential)
def sequential_execution():
    print("Sequential execution:")
    start_time = time.time()
    print_numbers()
    print_letters()
    end_time = time.time()
    print(f"Total time: {end_time - start_time:.2f} seconds\n")

# Running with threads (concurrent)
def threaded_execution():
    print("Threaded execution:")
    start_time = time.time()
    
    # Create threads
    thread1 = threading.Thread(target=print_numbers)
    thread2 = threading.Thread(target=print_letters)
    
    # Start threads
    thread1.start()
    thread2.start()
    
    # Wait for threads to complete
    thread1.join()
    thread2.join()
    
    end_time = time.time()
    print(f"Total time: {end_time - start_time:.2f} seconds\n")

# Thread with parameters
def worker_function(name, work_time):
    print(f"Worker {name} started")
    time.sleep(work_time)
    print(f"Worker {name} finished")

def threaded_workers():
    threads = []
    
    # Create multiple worker threads
    workers = [("Alice", 2), ("Bob", 3), ("Charlie", 1)]
    
    for name, work_time in workers:
        thread = threading.Thread(target=worker_function, args=(name, work_time))
        threads.append(thread)
        thread.start()
    
    # Wait for all threads to complete
    for thread in threads:
        thread.join()
    
    print("All workers finished")

# Thread-safe operations with locks
balance = 0
balance_lock = threading.Lock()

def deposit(amount):
    global balance
    for _ in range(100000):
        with balance_lock:  # Thread-safe
            balance += amount

def withdraw(amount):
    global balance
    for _ in range(100000):
        with balance_lock:  # Thread-safe
            balance -= amount

def banking_simulation():
    global balance
    balance = 0
    
    # Create threads for deposits and withdrawals
    deposit_thread = threading.Thread(target=deposit, args=(1,))
    withdraw_thread = threading.Thread(target=withdraw, args=(1,))
    
    deposit_thread.start()
    withdraw_thread.start()
    
    deposit_thread.join()
    withdraw_thread.join()
    
    print(f"Final balance: {balance}")  # Should be 0 if thread-safe

# ThreadPoolExecutor for better thread management
def cpu_bound_task(n):
    """Simulate CPU-intensive task"""
    result = sum(i * i for i in range(n))
    return result

def thread_pool_example():
    numbers = [100000, 200000, 300000, 400000, 500000]
    
    # Sequential execution
    start_time = time.time()
    results = [cpu_bound_task(n) for n in numbers]
    sequential_time = time.time() - start_time
    
    # Threaded execution
    start_time = time.time()
    with concurrent.futures.ThreadPoolExecutor(max_workers=3) as executor:
        results = list(executor.map(cpu_bound_task, numbers))
    threaded_time = time.time() - start_time
    
    print(f"Sequential time: {sequential_time:.2f} seconds")
    print(f"Threaded time: {threaded_time:.2f} seconds")

# Producer-Consumer pattern
import queue

def producer(q, items):
    for item in items:
        print(f"Producing: {item}")
        q.put(item)
        time.sleep(0.5)
    q.put(None)  # Sentinel value to signal completion

def consumer(q):
    while True:
        item = q.get()
        if item is None:
            break
        print(f"Consuming: {item}")
        time.sleep(1)
        q.task_done()

def producer_consumer_example():
    q = queue.Queue()
    items = ['item1', 'item2', 'item3', 'item4', 'item5']
    
    producer_thread = threading.Thread(target=producer, args=(q, items))
    consumer_thread = threading.Thread(target=consumer, args=(q,))
    
    producer_thread.start()
    consumer_thread.start()
    
    producer_thread.join()
    consumer_thread.join()

# Usage examples
if __name__ == "__main__":
    sequential_execution()
    threaded_execution()
    threaded_workers()
    banking_simulation()
    thread_pool_example()
    producer_consumer_example()
```

**Bullet Points to Remember:**
• Use threading.Thread() to create threads
• Call start() to begin thread execution
• Use join() to wait for thread completion
• Use locks for thread-safe operations
• ThreadPoolExecutor for better thread management
• GIL (Global Interpreter Lock) limits true parallelism in Python

## 65. Request API Data ↩️
**Making HTTP Requests:**
```python
import requests
import json

# Basic GET request
def basic_get_request():
    try:
        response = requests.get("https://jsonplaceholder.typicode.com/users")
        
        # Check if request was successful
        if response.status_code == 200:
            data = response.json()  # Parse JSON response
            print(f"Retrieved {len(data)} users")
            
            # Display first user
            if data:
                user = data[0]
                print(f"First user: {user['name']} ({user['email']})")
        else:
            print(f"Request failed with status code: {response.status_code}")
            
    except requests.exceptions.RequestException as e:
        print(f"Request error: {e}")

# Weather API example
def get_weather_data(city):
    # Note: You'll need to get a free API key from OpenWeatherMap
    api_key = "your_api_key_here"
    base_url = "http://api.openweathermap.org/data/2.5/weather"
    
    params = {
        'q': city,
        'appid': api_key,
        'units': 'metric'  # For Celsius
    }
    
    try:
        response = requests.get(base_url, params=params)
        
        if response.status_code == 200:
            data = response.json()
            
            weather_info = {
                'city': data['name'],
                'country': data['sys']['country'],
                'temperature': data['main']['temp'],
                'description': data['weather'][0]['description'],
                'humidity': data['main']['humidity']
            }
            
            return weather_info
        else:
            print(f"Weather API error: {response.status_code}")
            return None
            
    except requests.exceptions.RequestException as e:
        print(f"Weather request error: {e}")
        return None

# POST request with data
def create_post():
    url = "https://jsonplaceholder.typicode.com/posts"
    
    post_data = {
        'title': 'My New Post',
        'body': 'This is the content of my post.',
        'userId': 1
    }
    
    try:
        response = requests.post(url, json=post_data)
        
        if response.status_code == 201:  # Created
            created_post = response.json()
            print(f"Created post with ID: {created_post['id']}")
            return created_post
        else:
            print(f"Failed to create post: {response.status_code}")
            
    except requests.exceptions.RequestException as e:
        print(f"POST request error: {e}")

# API with headers and authentication
def api_with_headers():
    url = "https://api.github.com/user"
    
    headers = {
        'User-Agent': 'Python App',
        'Accept': 'application/json',
        'Authorization': 'token your_github_token_here'  # Personal access token
    }
    
    try:
        response = requests.get(url, headers=headers)
        
        if response.status_code == 200:
            user_info = response.json()
            print(f"GitHub user: {user_info.get('login', 'Unknown')}")
        else:
            print(f"GitHub API error: {response.status_code}")
            
    except requests.exceptions.RequestException as e:
        print(f"GitHub API error: {e}")

# Error handling and timeouts
def robust_api_request(url, timeout=5):
    try:
        response = requests.get(url, timeout=timeout)
        response.raise_for_status()  # Raises exception for bad status codes
        
        return response.json()
        
    except requests.exceptions.Timeout:
        print(f"Request timed out after {timeout} seconds")
    except requests.exceptions.ConnectionError:
        print("Connection error occurred")
    except requests.exceptions.HTTPError as e:
        print(f"HTTP error: {e}")
    except requests.exceptions.RequestException as e:
        print(f"Request error: {e}")
    except json.JSONDecodeError:
        print("Invalid JSON response")
    
    return None

# Cryptocurrency price API
def get_crypto_prices():
    url = "https://api.coingecko.com/api/v3/simple/price"
    
    params = {
        'ids': 'bitcoin,ethereum,cardano',
        'vs_currencies': 'usd'
    }
    
    try:
        response = requests.get(url, params=params)
        
        if response.status_code == 200:
            prices = response.json()
            
            print("Cryptocurrency Prices (USD):")
            for crypto, data in prices.items():
                price = data['usd']
                print(f"{crypto.capitalize()}: ${price:,.2f}")
        else:
            print(f"Crypto API error: {response.status_code}")
            
    except requests.exceptions.RequestException as e:
        print(f"Crypto API error: {e}")

# Session for multiple requests
def use_session():
    session = requests.Session()
    
    # Set default headers for all requests in this session
    session.headers.update({'User-Agent': 'Python API Client'})
    
    try:
        # Multiple requests using the same session
        response1 = session.get("https://httpbin.org/headers")
        response2 = session.get("https://httpbin.org/ip")
        
        print("Headers response:", response1.json())
        print("IP response:", response2.json())
        
    except requests.exceptions.RequestException as e:
        print(f"Session error: {e}")
    finally:
        session.close()

# Usage
if __name__ == "__main__":
    print("=== Basic GET Request ===")
    basic_get_request()
    
    print("\n=== POST Request ===")
    create_post()
    
    print("\n=== Crypto Prices ===")
    get_crypto_prices()
    
    print("\n=== Session Example ===")
    use_session()
    
    # Uncomment if you have API keys:
    # weather = get_weather_data("London")
    # if weather:
    #     print(f"Weather in {weather['city']}: {weather['temperature']}°C, {weather['description']}")
```

**Bullet Points to Remember:**
• Install requests library: pip install requests
• Always check response.status_code before processing
• Use response.json() to parse JSON data
• Handle exceptions with try-except blocks
• Use params parameter for query parameters
• Set timeouts to avoid hanging requests

## 66. PyQt5 GUI Intro 🖥️
**Creating Desktop Applications:**
```python
import sys
from PyQt5.QtWidgets import QApplication, QWidget, QVBoxLayout, QHBoxLayout, QLabel, QPushButton, QMessageBox
from PyQt5.QtCore import Qt
from PyQt5.QtGui import QFont

class MainWindow(QWidget):
    def __init__(self):
        super().__init__()
        self.initUI()
    
    def initUI(self):
        # Set window properties
        self.setWindowTitle('My First PyQt5 App')
        self.setGeometry(100, 100, 400, 300)  # x, y, width, height
        
        # Create layout
        layout = QVBoxLayout()
        
        # Create widgets
        title_label = QLabel('Welcome to PyQt5!')
        title_label.setAlignment(Qt.AlignCenter)
        title_label.setFont(QFont('Arial', 16, QFont.Bold))
        
        description_label = QLabel('This is a simple PyQt5 application.')
        description_label.setAlignment(Qt.AlignCenter)
        
        # Create buttons
        button_layout = QHBoxLayout()
        
        hello_button = QPushButton('Say Hello')
        hello_button.clicked.connect(self.say_hello)
        
        quit_button = QPushButton('Quit')
        quit_button.clicked.connect(self.close_application)
        
        button_layout.addWidget(hello_button)
        button_layout.addWidget(quit_button)
        
        # Add widgets to layout
        layout.addWidget(title_label)
        layout.addWidget(description_label)
        layout.addLayout(button_layout)
        
        # Set layout
        self.setLayout(layout)
    
    def say_hello(self):
        QMessageBox.information(self, 'Hello', 'Hello from PyQt5!')
    
    def close_application(self):
        reply = QMessageBox.question(self, 'Quit', 'Are you sure you want to quit?',
                                   QMessageBox.Yes | QMessageBox.No, QMessageBox.No)
        if reply == QMessageBox.Yes:
            self.close()

# Simple window example
class SimpleWindow(QWidget):
    def __init__(self):
        super().__init__()
        
        # Window setup
        self.setWindowTitle('Simple Window')
        self.setGeometry(200, 200, 300, 200)
        
        # Create a label
        label = QLabel('Hello, PyQt5!', self)
        label.move(100, 80)  # Position the label
        
        # Show the window
        self.show()

# Counter application
class CounterApp(QWidget):
    def __init__(self):
        super().__init__()
        self.counter = 0
        self.initUI()
    
    def initUI(self):
        self.setWindowTitle('Counter App')
        self.setGeometry(150, 150, 250, 150)
        
        layout = QVBoxLayout()
        
        # Counter display
        self.counter_label = QLabel(f'Count: {self.counter}')
        self.counter_label.setAlignment(Qt.AlignCenter)
        self.counter_label.setFont(QFont('Arial', 14))
        
        # Buttons
        button_layout = QHBoxLayout()
        
        increment_btn = QPushButton('+')
        increment_btn.clicked.connect(self.increment)
        
        decrement_btn = QPushButton('-')
        decrement_btn.clicked.connect(self.decrement)
        
        reset_btn = QPushButton('Reset')
        reset_btn.clicked.connect(self.reset)
        
        button_layout.addWidget(decrement_btn)
        button_layout.addWidget(reset_btn)
        button_layout.addWidget(increment_btn)
        
        # Add to main layout
        layout.addWidget(self.counter_label)
        layout.addLayout(button_layout)
        
        self.setLayout(layout)
    
    def increment(self):
        self.counter += 1
        self.update_display()
    
    def decrement(self):
        self.counter -= 1
        self.update_display()
    
    def reset(self):
        self.counter = 0
        self.update_display()
    
    def update_display(self):
        self.counter_label.setText(f'Count: {self.counter}')

def main():
    app = QApplication(sys.argv)
    
    # Choose which window to show
    # window = SimpleWindow()
    # window = CounterApp()
    window = MainWindow()
    window.show()
    
    sys.exit(app.exec_())

if __name__ == '__main__':
    main()
```

**Bullet Points to Remember:**
• Install PyQt5: pip install PyQt5
• QApplication manages the GUI application
• QWidget is the base class for all GUI objects
• Use layouts for responsive design
• Connect signals to slots with .clicked.connect()
• Always call sys.exit(app.exec_()) to run the event loop

## 67. PyQt5 Labels 🏷️
**Working with Text and Labels:**
```python
import sys
from PyQt5.QtWidgets import QApplication, QWidget, QVBoxLayout, QHBoxLayout, QLabel, QPushButton
from PyQt5.QtCore import Qt, QTimer
from PyQt5.QtGui import QFont, QPixmap, QPalette, QColor
import datetime

class LabelDemo(QWidget):
    def __init__(self):
        super().__init__()
        self.initUI()
    
    def initUI(self):
        self.setWindowTitle('PyQt5 Labels Demo')
        self.setGeometry(100, 100, 500, 400)
        
        layout = QVBoxLayout()
        
        # Basic label
        basic_label = QLabel('This is a basic label')
        layout.addWidget(basic_label)
        
        # Styled label
        styled_label = QLabel('Styled Label')
        styled_label.setFont(QFont('Arial', 16, QFont.Bold))
        styled_label.setStyleSheet("color: blue; background-color: lightgray; padding: 10px;")
        layout.addWidget(styled_label)
        
        # Aligned labels
        left_label = QLabel('Left Aligned')
        left_label.setAlignment(Qt.AlignLeft)
        
        center_label = QLabel('Center Aligned')
        center_label.setAlignment(Qt.AlignCenter)
        
        right_label = QLabel('Right Aligned')
        right_label.setAlignment(Qt.AlignRight)
        
        layout.addWidget(left_label)
        layout.addWidget(center_label)
        layout.addWidget(right_label)
        
        # Multi-line label
        multiline_label = QLabel('This is a multi-line label.\nIt can contain multiple lines of text.\nEach line is separated by \\n')
        multiline_label.setWordWrap(True)  # Enable word wrapping
        layout.addWidget(multiline_label)
        
        # Dynamic label (updates with current time)
        self.time_label = QLabel()
        self.update_time()
        layout.addWidget(self.time_label)
        
        # Timer to update time label every second
        self.timer = QTimer()
        self.timer.timeout.connect(self.update_time)
        self.timer.start(1000)  # Update every 1000ms (1 second)
        
        # Rich text label (HTML)
        rich_label = QLabel('<b>Bold text</b>, <i>italic text</i>, and <u>underlined text</u>')
        rich_label.setTextFormat(Qt.RichText)
        layout.addWidget(rich_label)
        
        # URL label (clickable)
        url_label = QLabel('<a href="https://www.python.org">Visit Python.org</a>')
        url_label.setTextFormat(Qt.RichText)
        url_label.setOpenExternalLinks(True)
        layout.addWidget(url_label)
        
        # Interactive elements
        button_layout = QHBoxLayout()
        
        # Button to change label text
        self.changeable_label = QLabel('Click button to change this text')
        change_btn = QPushButton('Change Text')
        change_btn.clicked.connect(self.change_label_text)
        
        # Button to toggle label visibility
        self.toggle_label = QLabel('This label can be hidden/shown')
        toggle_btn = QPushButton('Toggle Visibility')
        toggle_btn.clicked.connect(self.toggle_label_visibility)
        
        button_layout.addWidget(change_btn)
        button_layout.addWidget(toggle_btn)
        
        layout.addWidget(self.changeable_label)
        layout.addWidget(self.toggle_label)
        layout.addLayout(button_layout)
        
        self.setLayout(layout)
    
    def update_time(self):
        current_time = datetime.datetime.now().strftime('%H:%M:%S')
        self.time_label.setText(f'Current Time: {current_time}')
    
    def change_label_text(self):
        import random
        texts = [
            'Text has been changed!',
            'Another random text',
            'PyQt5 is awesome!',
            'Labels are useful',
            'Click again for more'
        ]
        self.changeable_label.setText(random.choice(texts))
    
    def toggle_label_visibility(self):
        if self.toggle_label.isVisible():
            self.toggle_label.hide()
        else:
            self.toggle_label.show()

# Advanced label styling
class StyledLabels(QWidget):
    def __init__(self):
        super().__init__()
        self.initUI()
    
    def initUI(self):
        self.setWindowTitle('Styled Labels')
        self.setGeometry(200, 200, 400, 300)
        
        layout = QVBoxLayout()
        
        # Label with border
        border_label = QLabel('Label with Border')
        border_label.setStyleSheet("""
            QLabel {
                border: 2px solid black;
                padding: 5px;
                background-color: lightyellow;
            }
        """)
        
        # Label with gradient background
        gradient_label = QLabel('Gradient Background')
        gradient_label.setStyleSheet("""
            QLabel {
                background: qlineargradient(x1:0, y1:0, x2:1, y2:1,
                    stop:0 #ff7f7f, stop:1 #7f7fff);
                color: white;
                font-weight: bold;
                padding: 10px;
                border-radius: 5px;
            }
        """)
        
        # Label with shadow effect
        shadow_label = QLabel('Shadow Effect')
        shadow_label.setStyleSheet("""
            QLabel {
                color: #333;
                font-size: 18px;
                font-weight: bold;
                background-color: white;
                padding: 10px;
                border-radius: 5px;
            }
        """)
        
        layout.addWidget(border_label)
        layout.addWidget(gradient_label)
        layout.addWidget(shadow_label)
        
        self.setLayout(layout)

def main():
    app = QApplication(sys.argv)
    
    # Choose which demo to run
    window = LabelDemo()
    # window = StyledLabels()
    
    window.show()
    sys.exit(app.exec_())

if __name__ == '__main__':
    main()
```

**Bullet Points to Remember:**
• QLabel displays text or images
• Use setAlignment() for text positioning
• setWordWrap(True) enables automatic line breaks
• setStyleSheet() for custom CSS-like styling
• QTimer for updating labels dynamically
• Rich text format supports HTML tags

## 68. PyQt5 Images 📷
**Displaying and Working with Images:**
```python
import sys
import os
from PyQt5.QtWidgets import (QApplication, QWidget, QVBoxLayout, QHBoxLayout, 
                            QLabel, QPushButton, QFileDialog, QScrollArea)
from PyQt5.QtGui import QPixmap, QPainter, QPen
from PyQt5.QtCore import Qt

class ImageViewer(QWidget):
    def __init__(self):
        super().__init__()
        self.current_pixmap = None
        self.initUI()
    
    def initUI(self):
        self.setWindowTitle('PyQt5 Image Viewer')
        self.setGeometry(100, 100, 800, 600)
        
        # Main layout
        main_layout = QVBoxLayout()
        
        # Button layout
        button_layout = QHBoxLayout()
        
        load_btn = QPushButton('Load Image')
        load_btn.clicked.connect(self.load_image)
        
        clear_btn = QPushButton('Clear')
        clear_btn.clicked.connect(self.clear_image)
        
        rotate_btn = QPushButton('Rotate 90°')
        rotate_btn.clicked.connect(self.rotate_image)
        
        scale_up_btn = QPushButton('Scale Up')
        scale_up_btn.clicked.connect(self.scale_up)
        
        scale_down_btn = QPushButton('Scale Down')
        scale_down_btn.clicked.connect(self.scale_down)
        
        button_layout.addWidget(load_btn)
        button_layout.addWidget(clear_btn)
        button_layout.addWidget(rotate_btn)
        button_layout.addWidget(scale_up_btn)
        button_layout.addWidget(scale_down_btn)
        
        # Image display area with scroll
        self.scroll_area = QScrollArea()
        self.image_label = QLabel()
        self.image_label.setAlignment(Qt.AlignCenter)
        self.image_label.setStyleSheet("border: 1px solid black;")
        self.image_label.setMinimumSize(400, 300)
        
        self.scroll_area.setWidget(self.image_label)
        self.scroll_area.setWidgetResizable(True)
        
        # Info label
        self.info_label = QLabel('No image loaded')
        self.info_label.setAlignment(Qt.AlignCenter)
        
        # Add to main layout
        main_layout.addLayout(button_layout)
        main_layout.addWidget(self.scroll_area)
        main_layout.addWidget(self.info_label)
        
        self.setLayout(main_layout)
        
        # Load a default image if it exists
        self.load_default_image()
    
    def load_default_image(self):
        # Try to load a default image
        default_path = "sample_image.jpg"  # Change this to your image path
        if os.path.exists(default_path):
            self.load_image_from_path(default_path)
        else:
            # Create a simple colored rectangle as placeholder
            pixmap = QPixmap(300, 200)
            pixmap.fill(Qt.lightGray)
            
            # Draw some text on it
            painter = QPainter(pixmap)
            painter.setPen(QPen(Qt.black, 2))
            painter.drawText(pixmap.rect(), Qt.AlignCenter, "No Image\nClick 'Load Image' to browse")
            painter.end()
            
            self.current_pixmap = pixmap
            self.image_label.setPixmap(pixmap)
            self.info_label.setText("Placeholder image - Load an image to get started")
    
    def load_image(self):
        file_path, _ = QFileDialog.getOpenFileName(
            self, 
            'Open Image File', 
            '', 
            'Image Files (*.png *.jpg *.jpeg *.bmp *.gif *.tiff)'
        )
        
        if file_path:
            self.load_image_from_path(file_path)
    
    def load_image_from_path(self, file_path):
        pixmap = QPixmap(file_path)
        
        if not pixmap.isNull():
            self.current_pixmap = pixmap
            self.display_image()
            
            # Update info
            size = pixmap.size()
            file_name = os.path.basename(file_path)
            self.info_label.setText(f"Loaded: {file_name} ({size.width()}x{size.height()})")
        else:
            self.info_label.setText("Failed to load image")
    
    def display_image(self):
        if self.current_pixmap:
            # Scale image to fit in display area while maintaining aspect ratio
            scaled_pixmap = self.current_pixmap.scaled(
                self.scroll_area.size() * 0.9,
                Qt.KeepAspectRatio,
                Qt.SmoothTransformation
            )
            self.image_label.setPixmap(scaled_pixmap)
    
    def clear_image(self):
        self.current_pixmap = None
        self.image_label.clear()
        self.image_label.setText("No image loaded")
        self.info_label.setText("Image cleared")
    
    def rotate_image(self):
        if self.current_pixmap:
            # Create a transformation matrix for 90-degree rotation
            transform = self.current_pixmap.transformed(
                self.current_pixmap.transform().rotate(90)
            )
            self.current_pixmap = transform
            self.display_image()
            self.info_label.setText("Image rotated 90 degrees")
    
    def scale_up(self):
        if self.current_pixmap:
            size = self.current_pixmap.size()
            new_size = size * 1.2  # Scale up by 20%
            scaled_pixmap = self.current_pixmap.scaled(
                new_size,
                Qt.KeepAspectRatio,
                Qt.SmoothTransformation
            )
            self.current_pixmap = scaled_pixmap
            self.display_image()
            self.info_label.setText("Image scaled up")
    
    def scale_down(self):
        if self.current_pixmap:
            size = self.current_pixmap.size()
            new_size = size * 0.8  # Scale down by 20%
            scaled_pixmap = self.current_pixmap.scaled(
                new_size,
                Qt.KeepAspectRatio,
                Qt.SmoothTransformation
            )
            self.current_pixmap = scaled_pixmap
            self.display_image()
            self.info_label.setText("Image scaled down")

# Simple image display example
class SimpleImageDisplay(QWidget):
    def __init__(self):
        super().__init__()
        self.initUI()
    
    def initUI(self):
        self.setWindowTitle('Simple Image Display')
        self.setGeometry(200, 200, 400, 300)
        
        layout = QVBoxLayout()
        
        # Create QLabel for image
        self.image_label = QLabel()
        self.image_label.setAlignment(Qt.AlignCenter)
        self.image_label.setStyleSheet("border: 2px solid gray;")
        
        # Create a simple colored image programmatically
        pixmap = QPixmap(200, 150)
        pixmap.fill(Qt.blue)
        
        # Draw something on the image
        painter = QPainter(pixmap)
        painter.setPen(QPen(Qt.white, 3))
        painter.drawRect(20, 20, 160, 110)
        painter.drawText(60, 80, "PyQt5 Image")
        painter.end()
        
        self.image_label.setPixmap(pixmap)
        
        layout.addWidget(self.image_label)
        self.setLayout(layout)

def main():
    app = QApplication(sys.argv)
    
    # Choose which window to show
    window = ImageViewer()
    # window = SimpleImageDisplay()
    
    window.show()
    sys.exit(app.exec_())

if __name__ == '__main__':
    main()
```

**Bullet Points to Remember:**
• QPixmap for displaying images in PyQt5
• QFileDialog.getOpenFileName() for file selection
• Use QScrollArea for large images
• QPainter for drawing on images
• scaled() method for resizing images
• transformed() method for rotating images

## 69. PyQt5 Layout Managers 🧲
**Organizing Widgets with Layouts:**
```python
import sys
from PyQt5.QtWidgets import (QApplication, QWidget, QVBoxLayout, QHBoxLayout, 
                            QGridLayout, QFormLayout, QLabel, QPushButton, 
                            QLineEdit, QTextEdit, QTabWidget, QSplitter)
from PyQt5.QtCore import Qt

class LayoutDemo(QWidget):
    def __init__(self):
        super().__init__()
        self.initUI()
    
    def initUI(self):
        self.setWindowTitle('PyQt5 Layout Managers Demo')
        self.setGeometry(100, 100, 800, 600)
        
        # Create tab widget to show different layouts
        tab_widget = QTabWidget()
        
        # Add different layout examples as tabs
        tab_widget.addTab(self.create_vbox_demo(), "VBox Layout")
        tab_widget.addTab(self.create_hbox_demo(), "HBox Layout")
        tab_widget.addTab(self.create_grid_demo(), "Grid Layout")
        tab_widget.addTab(self.create_form_demo(), "Form Layout")
        tab_widget.addTab(self.create_nested_demo(), "Nested Layouts")
        
        # Main layout
        main_layout = QVBoxLayout()
        main_layout.addWidget(tab_widget)
        self.setLayout(main_layout)
    
    def create_vbox_demo(self):
        """Vertical Box Layout Demo"""
        widget = QWidget()
        layout = QVBoxLayout()
        
        layout.addWidget(QLabel("VBox Layout arranges widgets vertically"))
        layout.addWidget(QPushButton("Button 1"))
        layout.addWidget(QPushButton("Button 2"))
        layout.addWidget(QPushButton("Button 3"))
        layout.addWidget(QLineEdit("Text input"))
        
        # Add stretch to push widgets to top
        layout.addStretch()
        
        widget.setLayout(layout)
        return widget
    
    def create_hbox_demo(self):
        """Horizontal Box Layout Demo"""
        widget = QWidget()
        main_layout = QVBoxLayout()
        
        main_layout.addWidget(QLabel("HBox Layout arranges widgets horizontally"))
        
        # Horizontal layout with buttons
        hbox1 = QHBoxLayout()
        hbox1.addWidget(QPushButton("Left"))
        hbox1.addWidget(QPushButton("Center"))
        hbox1.addWidget(QPushButton("Right"))
        
        # Another horizontal layout with different spacing
        hbox2 = QHBoxLayout()
        hbox2.addWidget(QLabel("Name:"))
        hbox2.addWidget(QLineEdit())
        hbox2.addStretch()  # Push widgets to left
        hbox2.addWidget(QPushButton("Submit"))
        
        main_layout.addLayout(hbox1)
        main_layout.addLayout(hbox2)
        main_layout.addStretch()
        
        widget.setLayout(main_layout)
        return widget
    
    def create_grid_demo(self):
        """Grid Layout Demo"""
        widget = QWidget()
        layout = QGridLayout()
        
        layout.addWidget(QLabel("Grid Layout arranges widgets in rows and columns"), 0, 0, 1, 3)
        
        # Calculator-like layout
        buttons = [
            ('7', 1, 0), ('8', 1, 1), ('9', 1, 2),
            ('4', 2, 0), ('5', 2, 1), ('6', 2, 2),
            ('1', 3, 0), ('2', 3, 1), ('3', 3, 2),
            ('0', 4, 1), ('Clear', 4, 0), ('=', 4, 2)
        ]
        
        for text, row, col in buttons:
            button = QPushButton(text)
            layout.addWidget(button, row, col)
        
        # Add a widget that spans multiple columns
        display = QLineEdit("0")
        display.setReadOnly(True)
        layout.addWidget(display, 0, 3, 2, 1)  # row, col, rowspan, colspan
        
        widget.setLayout(layout)
        return widget
    
    def create_form_demo(self):
        """Form Layout Demo"""
        widget = QWidget()
        layout = QFormLayout()
        
        layout.addRow(QLabel("Form Layout creates forms with labels and inputs"))
        layout.addRow("Name:", QLineEdit())
        layout.addRow("Email:", QLineEdit())
        layout.addRow("Age:", QLineEdit())
        layout.addRow("Address:", QTextEdit())
        
        # Add buttons
        button_layout = QHBoxLayout()
        button_layout.addWidget(QPushButton("Submit"))
        button_layout.addWidget(QPushButton("Cancel"))
        
        layout.addRow(button_layout)
        
        widget.setLayout(layout)
        return widget
    
    def create_nested_demo(self):
        """Nested Layouts Demo"""
        widget = QWidget()
        main_layout = QVBoxLayout()
        
        main_layout.addWidget(QLabel("Nested Layouts combine different layout types"))
        
        # Top section with horizontal layout
        top_layout = QHBoxLayout()
        top_layout.addWidget(QLabel("Left Panel"))
        top_layout.addWidget(QLabel("Right Panel"))
        
        # Middle section with grid layout
        middle_widget = QWidget()
        middle_layout = QGridLayout()
        
        for i in range(2):
            for j in range(3):
                button = QPushButton(f"Button {i*3+j+1}")
                middle_layout.addWidget(button, i, j)
        
        middle_widget.setLayout(middle_layout)
        
        # Bottom section with form layout
        bottom_widget = QWidget()
        bottom_layout = QFormLayout()
        bottom_layout.addRow("Input 1:", QLineEdit())
        bottom_layout.addRow("Input 2:", QLineEdit())
        bottom_widget.setLayout(bottom_layout)
        
        # Add all sections to main layout
        main_layout.addLayout(top_layout)
        main_layout.addWidget(middle_widget)
        main_layout.addWidget(bottom_widget)
        
        widget.setLayout(main_layout)
        return widget

class SplitterDemo(QWidget):
    """Demonstration of QSplitter for resizable layouts"""
    def __init__(self):
        super().__init__()
        self.initUI()
    
    def initUI(self):
        self.setWindowTitle('QSplitter Demo')
        self.setGeometry(200, 200, 600, 400)
        
        # Main layout
        main_layout = QVBoxLayout()
        
        # Horizontal splitter
        h_splitter = QSplitter(Qt.Horizontal)
        
        # Left panel
        left_widget = QWidget()
        left_layout = QVBoxLayout()
        left_layout.addWidget(QLabel("Left Panel"))
        left_layout.addWidget(QPushButton("Button 1"))
        left_layout.addWidget(QPushButton("Button 2"))
        left_widget.setLayout(left_layout)
        
        # Right panel with vertical splitter
        v_splitter = QSplitter(Qt.Vertical)
        
        # Top right
        top_right = QWidget()
        top_layout = QVBoxLayout()
        top_layout.addWidget(QLabel("Top Right"))
        top_layout.addWidget(QTextEdit("This is a text area"))
        top_right.setLayout(top_layout)
        
        # Bottom right
        bottom_right = QWidget()
        bottom_layout = QVBoxLayout()
        bottom_layout.addWidget(QLabel("Bottom Right"))
        bottom_layout.addWidget(QTextEdit("Another text area"))
        bottom_right.setLayout(bottom_layout)
        
        v_splitter.addWidget(top_right)
        v_splitter.addWidget(bottom_right)
        
        # Add to horizontal splitter
        h_splitter.addWidget(left_widget)
        h_splitter.addWidget(v_splitter)
        
        # Set initial sizes
        h_splitter.setSizes([200, 400])
        
        main_layout.addWidget(h_splitter)
        self.setLayout(main_layout)

def main():
    app = QApplication(sys.argv)
    
    # Choose which demo to run
    window = LayoutDemo()
    # window = SplitterDemo()
    
    window.show()
    sys.exit(app.exec_())

if __name__ == '__main__':
    main()
```

**Bullet Points to Remember:**
• QVBoxLayout arranges widgets vertically
• QHBoxLayout arranges widgets horizontally  
• QGridLayout arranges widgets in rows and columns
• QFormLayout creates label-input pairs
• Use addStretch() to add flexible space
• QSplitter creates resizable panes
• Layouts can be nested for complex designs