# AI程式設計（一） Fundamentals of AI Programming (I)

## 課程資訊 Course Information

- **課程名稱**: AI程式設計（一） Fundamentals of AI Programming (I)
- **課程代碼**: EG011 A
- **授課教師**: Prof. J.S. Shieh（謝建興）
- **教師信箱**: jsshieh@saturn.yzu.edu.tw
- **教師辦公室**: Room 1208, Tel: (03) 4638800 ext. 2250
- **助教**: 李彩康 (s1145006@mail.yzu.edu.tw)；禹佳杉 (s1120816@mail.yzu.edu.tw)
- **先修條件**: 無

## 課程目標 Course Goal

This course provides engineering freshmen with a comprehensive overview of computer science, positioning the computer as an essential tool for modern engineering design and computation. Students will develop proficiency in Python programming, a critical skill for building and deploying machine learning models.

The curriculum transitions from basic algorithmic logic to the fundamentals of Artificial Intelligence and Machine Learning, exploring how data-driven insights can solve real-world engineering challenges. Furthermore, students will be introduced to the emerging field of Quantum Computing. As quantum systems promise to solve complex problems with greater efficiency and lower energy consumption than classical hardware, students will gain hands-on experience with quantum programming to address foundational computational problems.

本課程旨在為工程系一年級學生提供電腦科學的全面概覽，將電腦定位為現代工程設計與運算中不可或缺的工具。學生將培養 Python 程式設計的熟練度，這是構建與部署機器學習模型的一項關鍵技能。課程內容將從基礎的演算法邏輯過渡到人工智慧（AI）與機器學習（ML）的核心原理，帶領學生探索如何利用數據驅動的洞察力來解決現實世界中的工程挑戰。此外，學生亦將接觸到量子運算（Quantum Computing）這一新興領域。

## 課程大綱 Course Overview

### Part I. Basic Python Programming

- Ch. 1 An Introduction to Computing and Problem Solving (wk 1)
- Ch. 2 Core Objects, Variables, Input and Output (wks 2~3)
- Ch. 3 Structures and Control Flow (wks 4~6) — Quiz 1 (50 min)
- Ch. 4 Functions (wk 7)
- Midterm Exam (wk 8)
- Ch. 5 Plotting (Matplotlib) (wk 9)

### Part II. Introduction to Machine Learning (Supervised)

- Ch. 6 Logistic Regression; how AI "labels" the world (Supervised) (wk 10)
- Ch. 7 Neural Networks: how "Deep Learning" mimics biological neurons (wk 11)

### Part III. Advanced Python Programming (Quantum Computing)

- Ch. 8 Introduction to Quantum Computing (wk 12)
- Ch. 9 Quantum Circuit Operations (wks 13-14) — Quiz 2 (50 min)
- Ch. 10 Quantum Machine Learning (wk 15)
- Final Exam (wk 16)
- Project Presentation & Demo at the Final Stage (I) (wk 17)
- Project Presentation & Demo at the Final Stage (II) (wk 18)

### 教科書 Textbooks

1. An Introduction to Programming Using Python, Global Edition (2016), by David I. Schneider, Pearson.
2. A practical guide to quantum machine learning and quantum optimisation: hands-on approach to modern quantum algorithms (2023), by Elias Fernandez-Combarro and Samuel González-Castillo, 1st Edition.

### 成績評量 Grading

- Homework: 20%
- Quiz: 20%
- Presentation & Demo: 20%
- Midterm Exam: 20%
- Final Exam: 20%

---

## Chapter 1: An Introduction to Computing and Problem Solving

### 1.1 An Introduction to Computing and Python

**How do we communicate with the computer?**
We use programming languages to communicate with computers.

**How do we get computers to perform complicated tasks?**
Tasks are broken down into a sequence of instructions.

**Why Python?**
Python is powerful, easy to download, write, and read.

**How did the language Python get its name?**
Python was named for the British comedy group Monty Python.

**What is IDLE?**
IDLE stands for Integrated DeveLopment Environment. It is the editor used to create Python programs.

**What is an interpreted language?**
An interpreted language uses an interpreter, which translates high-level language one statement at a time into machine language and then runs it.

**What are the meanings of the terms "programmer" and "user"?**
- Programmer: a person who solves problems by writing programs on a computer
- User: any person who runs a program

**What is the meaning of the term "code"?**
Python statements that the programmer writes.

**Are there certain characteristics that all programs have in common?**
Yes: Input, Processing, Output.

**What are the meanings of the terms "hardware" and "software"?**
- Hardware: physical components of the computer
- Software: the programs

**How are problems solved with a program?**
By devising a step-by-step procedure to process given data and produce requested output.

**What is a zero-based numbering system?**
A numbering system where numbering begins with zero instead of one.

**Prerequisites to learning Python?**
Be familiar with how folders and files are managed.

### 1.2 Program Development Cycle

The problem solving process consists of:

1. **Analyze**: Define the problem.
2. **Design**: Plan the solution to the problem.
3. **Code**: Translate the algorithm into a programming language.
4. **Test and correct**: Locate and remove any errors in the program.
5. **Complete the documentation**: Organize all the material that describes the program.

### 1.3 Programming Tools

There are several programming tools:

**Algorithms**: A step-by-step procedure to solve a problem.

**Flowcharts**: Visual representation of an algorithm using symbols.

**Pseudocode**: Abbreviated plain English version of actual computer code. Symbols used in flowcharts are replaced by English-like statements. It allows the programmer to focus on the steps required to solve the problem.

**Hierarchy Charts**: Shows the overall program structure. Depicts organization of program, omits specific processing logic. Describes what each part, or module, of the program does. Each module can be subdivided into a succession of submodules.

#### Algorithm Example: Stamp Problem

Algorithm to determine number of stamps for a letter (Rule of thumb: 1 stamp for every 5 sheets of paper):
1. Request sheets of paper
2. Divide by 5
3. Round quotient up to next whole number
4. Reply with number of stamps

Python code:
```python
import math
a = float(input('Sheets number = '))
b = a / 5
r_b = math.ceil(b)
print('The number of stamps is ', r_b)
```

#### Decision Structure

A decision structure allows a program to choose between different actions based on a condition.

Example: Direction of Numbered NYC Streets
- Even-numbered streets run eastbound
- Odd-numbered streets run westbound

```python
s = float(input('Street number = '))
r = s % 2
if r != 0:
    print('Westbound')
else:
    print('Eastbound')
```

#### Repetition Structure (Loops)

A repetition (or looping) structure executes instructions many times. A test (or condition) is needed to tell when the loop should end. The condition is checked before each pass through the loop.

#### Class Average Algorithm

Problem: Calculate and report the average grade for a class.

- Input: Student grades
- Processing: Find the sum of the grades; count the number of students; calculate average grade = sum of grades / number of students
- Output: Average grade

```python
Grade1 = int(input('Enter score 1: '))
Grade2 = int(input('Enter score 2: '))
Grade3 = int(input('Enter score 3: '))
Grade4 = int(input('Enter score 4: '))
Grade5 = int(input('Enter score 5: '))
total = (Grade1 + Grade2 + Grade3 + Grade4 + Grade5)
Average = total / 5
print("The average grade is: ", Average)
```

---

## Chapter 2: Core Objects, Variables, Input, and Output

### 2.1 Numbers

#### Numeric Literals

Numbers are referred to as numeric literals. There are two types:
- **int** (integer): A whole number written without a decimal point. Example: `5`, `-3`, `100`
- **float**: A number written with a decimal point. Example: `3.14`, `-0.5`, `2.0`

#### Arithmetic Operators

Python supports these arithmetic operators:
- Addition: `+`
- Subtraction: `-`
- Multiplication: `*`
- Division: `/` (result is always a float)
- Exponentiation: `**`
- Integer division (quotient): `//`
- Modulus (remainder): `%`

The result of a division `/` is always a float. The result of other operations is a float if either of the numbers is a float; otherwise, it is an int.

#### The print Function

The `print()` function is used to display numbers on the monitor. If `n` is a number, `print(n)` displays the number `n`. The print function can display the result of evaluated expressions. A single print function can display several values.

#### Variables

In mathematics problems, quantities are referred to by names. The names given to values are called variables.

**Assignment statements**: The expression on the right side is evaluated first, then that value is assigned to the variable on the left side.

```python
speed = 60
time = 3
distance = speed * time
print(distance)  # Output: 180
```

**Variable naming rules in Python**:
- Must begin with a letter or underscore `_`
- Can only consist of letters, numbers, and underscores
- Should use descriptive variable names
- Convention: begin with lowercase, use capital letters for additional words (camelCase). Example: `rateOfChange`
- Names are case-sensitive (`myVar` and `myvar` are different)
- Cannot use Python's 33 reserved words (keywords) as variable names (see Appendix B)

#### Built-in Functions for Numbers

**abs(x)**: Returns the absolute value of `x`.
```python
abs(-5)    # Returns 5
abs(3)     # Returns 3
```

**int(x)**: Converts `x` to an integer by truncating (dropping) the decimal part.
```python
int(3.7)   # Returns 3
int(-2.3)  # Returns -2
```

**round(x)**: Rounds `x` to the nearest integer. When the decimal part is exactly 0.5, Python rounds to the nearest even number.
```python
round(3.7)    # Returns 4
round(3.2)    # Returns 3
round(2.5)    # Returns 2  (rounds to even)
round(3.5)    # Returns 4  (rounds to even)
```

**round(x, n)**: Rounds `x` to `n` decimal places.
```python
round(3.14159, 2)  # Returns 3.14
```

#### Augmented Assignments

Python provides shorthand operators for common assignment patterns:

| Standard | Augmented | Meaning |
|----------|-----------|---------|
| `var = var + 1` | `var += 1` | Add and assign |
| `var = var - 1` | `var -= 1` | Subtract and assign |
| `var = var * 2` | `var *= 2` | Multiply and assign |
| `var = var / 2` | `var /= 2` | Divide and assign |
| `var = var % 3` | `var %= 3` | Modulus and assign |
| `var = var // 3` | `var //= 3` | Integer divide and assign |

Remember: The expression on the right side of the assignment statement is evaluated before the assignment is made.

#### Integer Division and Modulus Operators

- Integer division `//` returns the quotient (whole number part)
- Modulus `%` returns the remainder

```python
# Convert 41 inches to feet and inches
totalInches = 41
feet = totalInches // 12    # 3
inches = totalInches % 12   # 5
print(feet, "feet,", inches, "inches")
# Output: 3 feet, 5 inches
```

#### Order of Precedence

Operations are evaluated in this order:
1. Terms inside parentheses (inner to outer)
2. Exponentiation `**`
3. Multiplication `*`, Division `/`, Integer Division `//`, Modulus `%`
4. Addition `+`, Subtraction `-`

Parentheses can be used to clarify or change the order of evaluation.

#### Types of Errors

**Syntax Errors**: Grammatical and punctuation errors in the code. Detected before the program runs.
- Example: Missing closing parenthesis, misspelled keywords

**Runtime Errors (Exceptions)**: Errors discovered while the program is running. Python terminates execution and displays an error message.
- Example: Division by zero, using an undefined variable

**Logic Errors**: Occurs when a program does not perform the way it was intended. The syntax is correct, but the logic is wrong. These are the most difficult type of error to locate.
```python
# Logic error example:
average = firstNum + secondNum / 2      # Wrong!
average = (firstNum + secondNum) / 2    # Correct!
```

#### Numeric Objects in Memory

When you assign a value to a variable, Python creates an object in memory to store that value. The variable name is a reference (pointer) to that object.

#### Exercises for Section 2.1

Exercises 49-54: Find the value of the function where a = 6 and b = 4.

49. `int(-a / 2)` → `int(-6/2)` = `int(-3.0)` = `-3`
50. `round(a / b)` → `round(6/4)` = `round(1.5)` = `2`
51. `abs(a - 5)` → `abs(6-5)` = `abs(1)` = `1`
52. `abs(4 - a)` → `abs(4-6)` = `abs(-2)` = `2`
53. `round(a + 0.5)` → `round(6.5)` = `6`
54. `int(b * 0.5)` → `int(4*0.5)` = `int(2.0)` = `2`

Exercises 55-60: Rewrite the statements using augmented assignment operators.

55. `cost = cost + 5` → `cost += 5`
56. `sum = sum * 2` → `sum *= 2`
57. `cost = cost / 6` → `cost /= 6`
58. `sum = sum - 7` → `sum -= 7`
59. `sum = sum % 2` → `sum %= 2`
60. `cost = cost // 3` → `cost //= 3`

#### Practice Problems (Section 2.1)

**Practice: No. 62, 64, 66, 68, and 70**
**Homework: No. 72, 73, 76, 77, and 78**

**61. Calculate Profit** — The following steps calculate a company's profit:
(a) Create the variable `revenue` and assign it the value 98,456.
(b) Create the variable `costs` and assign it the value 45,000.
(c) Create the variable `profit` and assign it the difference between `revenue` and `costs`.
(d) Display the value of `profit`.

```python
revenue = 98456
costs = 45000
profit = revenue - costs
print(profit)
```

**62. Stock Purchase** — The following steps calculate the amount of a stock purchase:
(a) Create the variable `costPerShare` and assign it the value 25.625.
(b) Create the variable `numberOfShares` and assign it the value 400.
(c) Create the variable `amount` and assign it the product of `costPerShare` and `numberOfShares`.
(d) Display the value of `amount`.

```python
costPerShare = 25.625
numberOfShares = 400
amount = costPerShare * numberOfShares
print(amount)
```

**63. Discounted Price** — The following steps calculate the price of an item after a 30% reduction:
(a) Create variable `price` = 19.95
(b) Create variable `discountPercent` = 30
(c) Create variable `markdown` = (discountPercent / 100) * price
(d) Decrease `price` by `markdown`
(e) Display `price` (rounded to two decimal places)

```python
price = 19.95
discountPercent = 30
markdown = (discountPercent / 100) * price
price -= markdown
print(round(price, 2))
```

**64. Break-Even Point** — Calculate the number of units to break even:
(a) `fixedCosts` = 5000
(b) `pricePerUnit` = 8
(c) `costPerUnit` = 6
(d) `breakEvenPoint` = fixedCosts / (pricePerUnit - costPerUnit)
(e) Display `breakEvenPoint`

```python
fixedCosts = 5000
pricePerUnit = 8
costPerUnit = 6
breakEvenPoint = fixedCosts / (pricePerUnit - costPerUnit)
print(breakEvenPoint)
```

**65. Savings Account** — Calculate balance after three years at 5% interest compounded annually:

```python
balance = 100
balance *= 1.05  # Year 1
balance *= 1.05  # Year 2
balance *= 1.05  # Year 3
print(round(balance, 2))
```

**66. Savings Account** — Calculate balance at end of three years when $100 is deposited at beginning of each year at 5% interest:

```python
balance = 100
balance *= 1.05       # Year 1 interest
balance += 100        # Deposit at start of Year 2
balance *= 1.05       # Year 2 interest
balance += 100        # Deposit at start of Year 3
balance *= 1.05       # Year 3 interest
print(round(balance, 2))
```

**67. Savings Account** — Calculate balance after 10 years at 5% interest compounded annually:

```python
balance = 100
balance = balance * (1.05 ** 10)
print(round(balance, 2))
```

**68. Profit from Stock** — Calculate percentage profit from selling a stock:

```python
purchasePrice = 10
sellingPrice = 15
percentProfit = 100 * (sellingPrice - purchasePrice) / purchasePrice
print(percentProfit)
```

**69. Corn Production** — How many tons of corn on a 30-acre farm (18 tons per acre)?

```python
acreage = 30
tonsPerAcre = 18
totalTons = acreage * tonsPerAcre
print(totalTons)
```

**70. Projectile Motion** — How high will a ball be after 3 seconds? (initial velocity = 50 ft/s, initial height = 5 ft)
Height = -16t² + v₀t + h₀

```python
t = 3
v0 = 50
h0 = 5
height = -16 * t**2 + v0 * t + h0
print(height)
```

**71. Distance Covered** — Car left airport at 5 o'clock, arrived home at 9 o'clock, speed 81.34 km/h:

```python
speed = 81.34
time = 9 - 5  # 4 hours
distance = speed * time
print(distance)
```

**72. Gas Mileage** — Calculate miles per gallon:

```python
odometer1 = 23352
odometer2 = 23695
gallons = 14
distance = odometer2 - odometer1
mpg = distance / gallons
print(mpg)
```

**73. Power Usage** — Average monthly consumption 750 million watts, population ~5 million:

```python
monthlyWatts = 750_000_000
daysPerMonth = 30
population = 5_000_000
dailyWattsPerPerson = monthlyWatts / daysPerMonth / population
print(dailyWattsPerPerson)
```

**74. Square Deck** — Building permit for 432-square-foot deck, find side length:

```python
import math
area = 432
side = math.sqrt(area)
print(side)
```

**75. Banks** — $1000 at 8.7% interest for 2 years:

```python
balance = 1000
balance *= (1 + 0.087) ** 2
print(round(balance, 2))
```

**76. Population Increase** — Village population was 845, grew by 6.5%:

```python
population = 845
growthRate = 6.5 / 100
newPopulation = population * (1 + growthRate)
print(round(newPopulation))
```

**77. Bacterial Growth** — Surface initially 2.19×10¹⁴ cells, later 4.68×10¹⁴ cells:

```python
initial = 2.19e14
final = 4.68e14
percentGrowth = (final - initial) / initial * 100
print(round(percentGrowth))
```

**78. Calories** — Estimate calories in one cubic mile of chocolate ice cream (5280 feet in a mile, 48600 calories per cubic foot):

```python
feetPerMile = 5280
cubicFeetPerCubicMile = feetPerMile ** 3
caloriesPerCubicFoot = 48600
totalCalories = cubicFeetPerCubicMile * caloriesPerCubicFoot
print(totalCalories)
```

#### Solutions to Practice Problems 2.1

1. Modulus operations are performed before subtractions. If the intent is for the subtraction to be performed first, the expression should be written `(7 - 4) % 3`.

2. The first assignment statement assigns the value of `var2` to `var1`, whereas the second assignment statement assigns `var1`'s value to `var2`.

3. Tracing through the code:

| Statement | a | b | c |
|-----------|---|---|---|
| `a = 5` | 5 | — | — |
| `b = 4` | 5 | 4 | — |
| `c = a * b` | 5 | 4 | 20 |
| `a = c // a` | 4 | 4 | 20 |
| `print((a - b)*c)` | 4 | 4 | 20 |
| `b = b * b * b` | 4 | 64 | 20 |

Output of `print((a - b)*c)`: `(4 - 4) * 20 = 0`

4. Four ways to increase the value of `var` by 5%:
```python
var = var + (.05 * var)
var = 1.05 * var
var += .05 * var
var *= 1.05
```

---

### 2.2 Strings

#### String Literals

A string is a sequence of characters treated as a single item. Strings are written surrounded by either single quotes (`'`) or double quotes (`"`). The opening and closing quotation marks must be the same type.

```python
"Hello, World!"
'Python is fun'
```

#### String Variables

Variables can be assigned string values. They are created the first time they appear in an assignment statement. When used as an argument of a print statement, the quotation marks are not included in the display.

```python
name = "Python"
print(name)  # Output: Python
```

#### Indices and Slices

Each character in a string has a position (index), starting from 0.

For the string `"spam & eggs"`:
```
Index:  0  1  2  3  4  5  6  7  8  9  10
Char:   s  p  a  m     &     e  g  g  s
```

**Slicing**: If `str1` is a string, `str1[m:n]` returns the substring from position `m` to position `n-1`.

```python
"spam & eggs"[2:7]   # Returns "am & "
```

**The `find` and `rfind` methods**:
- `str.find(substring)` returns the index of the first occurrence from the left
- `str.rfind(substring)` returns the index of the first occurrence from the right

#### Negative Indices

Python allows strings to be indexed from the right using negative numbers.

For the string `"spam & eggs"`:
```
Negative Index: -11 -10 -9 -8 -7 -6 -5 -4 -3 -2 -1
Char:             s    p   a   m      &      e   g   g   s
```

```python
str1 = "spam & eggs"
str1[-1]      # 's' (last character)
str1[-4:]     # 'eggs' (last 4 characters)
```

#### Default Bounds for Slices

```python
str1 = "spam & eggs"
str1[:4]      # 'spam'   (from beginning to index 3)
str1[7:]      # 'eggs'   (from index 7 to end)
str1[:]       # 'spam & eggs' (entire string)
```

#### String Concatenation

Two strings can be combined using the `+` operator:

```python
"Hello" + " " + "World"   # "Hello World"
firstName = "John"
lastName = "Doe"
fullName = firstName + " " + lastName   # "John Doe"
```

#### String Repetition

The asterisk `*` operator repeats a string:

```python
"Ha" * 3    # "HaHaHa"
"-" * 20    # "--------------------"
```

#### String Functions and Methods

Common string operations (given `str1 = "Python"`):

| Operation | Result | Description |
|-----------|--------|-------------|
| `len(str1)` | `6` | Length of string |
| `str1.upper()` | `"PYTHON"` | Convert to uppercase |
| `str1.lower()` | `"python"` | Convert to lowercase |
| `str1.count("o")` | `1` | Count occurrences |
| `str1.find("th")` | `2` | Find position of substring |
| `str1.startswith("Py")` | `True` | Check if starts with |
| `str1.endswith("on")` | `True` | Check if ends with |
| `str1.replace("P","J")` | `"Jython"` | Replace characters |
| `str1.strip()` | Removes leading/trailing whitespace |
| `str1.split()` | Splits string into a list |

#### Chained Methods

Methods can be combined (chained) in a single line, executed from left to right:

```python
"Hello World".upper().replace("O", "0")   # "HELL0 W0RLD"
```

#### The input Function

The `input()` function prompts the user to enter data. The user types a response and presses ENTER. The entry is assigned to the variable on the left. The `input()` function always returns a string.

```python
name = input("Enter your name: ")
print("Hello, " + name)
```

#### Converting Between Types

- `int(x)`: Converts string `x` to an integer
- `float(x)`: Converts string `x` to a float
- `str(x)`: Converts number `x` to a string
- `eval(x)`: Evaluates string `x` as a Python expression

```python
age = int(input("Enter your age: "))
price = float(input("Enter the price: "))
result = str(42)      # "42"
```

#### Internal Documentation (Comments)

Comments help other people understand your program and help you understand it later. In Python, comments start with `#`.

```python
# This program calculates the area of a rectangle
length = 10     # Length in meters
width = 5       # Width in meters
area = length * width   # Calculate area
print("Area:", area)    # Display result
```

#### Line Continuation

Long statements can be split across multiple lines using a backslash `\` or by enclosing code in parentheses (preferred style):

```python
# Using backslash
quotation = "Well written code is its own" + \
            " best documentation."

# Using parentheses (preferred)
quotation = ("Well written code is its own"
             " best documentation.")
```

#### Indexing and Slicing Out of Bounds

Python does NOT allow out-of-bounds indexing for individual characters:
```python
str1 = "Python"
# str1[7]   → IndexError!
# str1[-7]  → IndexError!
```

But it DOES allow out-of-bounds indices for slices:
```python
str1 = "Python"
str1[3:100]   # "hon" (no error)
str1[-100:3]  # "Pyt" (no error)
```

#### Practice and Homework for Section 2.2

**Practice: No. 94, 98, 100, 101, and 102**
**Homework: No. 104, 105, 106, 108, and 112**
