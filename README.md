
# Python Crash Course for Exam Preparation

## 1. Python Programming Basics

### Key Topics to Learn:
#### Variables and Data Types
- Integers, Floats, Strings, Booleans, Lists, Tuples, Sets, Dictionaries.

Example:
```python
x = 5  # Integer
y = 3.14  # Float
name = "John"  # String
is_active = True  # Boolean
numbers = [1, 2, 3, 4]  # List
```

#### Operators
- Arithmetic, Comparison, Logical, Assignment, and Membership Operators.

Example:
```python
# Arithmetic Operators
a = 10
b = 5
print(a + b)  # Addition
print(a > b)  # Comparison (True or False)

# Logical Operators
is_adult = True
has_license = False
print(is_adult and has_license)  # AND operator
```

#### Control Flow
- `if-elif-else`, `for`, `while` loops.

Example:
```python
# if-elif-else example
x = 10
if x < 5:
    print("Small")
elif x == 10:
    print("Exactly 10")
else:
    print("Big")

# for loop example
for i in range(5):
    print(i)  # Prints numbers 0 to 4
```

#### Functions and Recursion
- Functions for modular code. Recursion for problems like factorials, Fibonacci series.

Example:
```python
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

print(factorial(5))  # Output: 120
```

#### Error Handling
- Try-Except blocks for handling exceptions.

Example:
```python
try:
    x = 10 / 0  # Will raise ZeroDivisionError
except ZeroDivisionError:
    print("Cannot divide by zero")
```

## 2. Data Structures & Algorithms (DSA) in Python

### Key Topics to Learn:

#### Arrays
- Lists in Python are dynamic arrays.

Example:
```python
arr = [1, 2, 3, 4, 5]
arr.append(6)  # Adds 6 at the end
arr.remove(2)  # Removes 2 from the list
```

#### Stacks and Queues
- Implement using lists or collections.

Stack Example:
```python
stack = []
stack.append(10)  # Push
stack.append(20)
print(stack.pop())  # Pop (removes and returns top element)
```

#### Linked List
- Custom implementation of singly linked list.

Example:
```python
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

# Create nodes
head = Node(10)
second = Node(20)
head.next = second
```

#### Sorting Algorithms
- **Bubble Sort, Insertion Sort, Merge Sort, Quick Sort**.

Example (Bubble Sort):
```python
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
```

#### Time Complexity
- Learn **Big-O Notation** (e.g., O(n), O(n^2), O(log n)).

## 3. Aptitude & Logical Reasoning in Python

### Key Topics to Learn:

#### Number Series & Patterns
- Write a Python program to detect or generate number patterns.

Example:
```python
# Print Fibonacci Series up to 10 numbers
a, b = 0, 1
for _ in range(10):
    print(a, end=" ")
    a, b = b, a + b
```

#### Coding-Decoding Problems
- Practice string manipulation and shifting.

Example:
```python
def decode_string(s):
    return ''.join(chr(ord(c) + 3) for c in s)  # Caesar Cipher shift by 3
print(decode_string("abc"))  # Output: "def"
```

#### Logical Deductions
- If-else logic for decision-making.

Example:
```python
age = 20
if age >= 18:
    print("Adult")
else:
    print("Minor")
```

#### Blood Relations and Directions
- Basic algorithmic approach for solving relational problems.

## 4. SQL in Python (SQLite)

### Key SQL Commands in Python

#### Connecting to SQLite Database
- Use the `sqlite3` module in Python.

Example:
```python
import sqlite3

conn = sqlite3.connect('mydatabase.db')  # Connect to SQLite database
cursor = conn.cursor()
cursor.execute('''CREATE TABLE IF NOT EXISTS users (id INTEGER PRIMARY KEY, name TEXT)''')
```

#### CRUD Operations
- **Create, Read, Update, Delete** operations.

Example:
```python
# Insert data
cursor.execute("INSERT INTO users (name) VALUES ('Alice')")
conn.commit()

# Select data
cursor.execute("SELECT * FROM users")
print(cursor.fetchall())  # Display all rows

# Update data
cursor.execute("UPDATE users SET name = 'Bob' WHERE id = 1")
conn.commit()

# Delete data
cursor.execute("DELETE FROM users WHERE id = 1")
conn.commit()
```

#### Joins and Subqueries
- Example of an inner join:
```python
cursor.execute('''
    SELECT orders.id, users.name 
    FROM orders 
    JOIN users ON orders.user_id = users.id
''')
```

## 5. Final Strategy for Exam

- **Practice MCQs** (for DSA, SQL, Logical Reasoning).
- **Review Key Python Functions**:
    - **List, Set, Dictionary, Tuple** methods.
    - **String manipulation** (Slicing, Reversing, Joining, Replacing).
    - **File Handling** (Reading and Writing to files).
- **Time Management**:
    - Solve **easy questions first**.
    - Eliminate options you know are wrong, and **don't leave any question unanswered** (no negative marking).
- **For Python**:
    - **Use built-in functions** like `sum()`, `map()`, `filter()`, `sorted()` to save time.

## Final Python Code Example (for quick revision):

```python
# Factorial using recursion
def factorial(n):
    if n == 0:
        return 1
    return n * factorial(n - 1)

# Example of Bubble Sort
def bubble_sort(arr):
    n = len(arr)
    for i in range(n):
        for j in range(0, n-i-1):
            if arr[j] > arr[j+1]:
                arr[j], arr[j+1] = arr[j+1], arr[j]
    return arr

# Example usage:
print(factorial(5))  # Output: 120
print(bubble_sort([64, 25, 12, 22, 11]))  # Output: [11, 12, 22, 25, 64]
```
