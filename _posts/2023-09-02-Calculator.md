---
toc: true
comments: true
layout: post
title: Calculator
description: Become one with your tools.  They could be more important than code, code, coding.
type: plans
courses: { compsci: {week: 3}, csp: {week: 0, categories: [4.A]}, csa: {week: 0} }
categories: [C1.4]
---
```python
# This function adds two numbers 
def add (x, y):
    return x + y

# This function subtracts two numbers
def subtract (x, y):
    return x - y

# This function multiplies two numbers 
def multiply (x, y):
    return x * y

# This function divides two numbers 
def divide (x, y):
    if y == 0:
        return "Cannot divide by zero"
    return x / y

print ("Select operation.")
print ("1.Add")
print ("2.Subtract")
print ("3.Multiply")
print ("4.Divide")

while True:
    # take input from the user 
    choice = input ("Enter choice (1/2/3/4): ")

    # check if choice is one of the four options
    if choice in ('1', '2', '3', '4'):
        try:
            num1 = float (input("Enter first number: "))
            num2 = float(input("Enter second number:"))
        except ValueError:
            print ("Invalid input. Please enter a number.")
            continue 

        if choice == '1':
            print (num1, "+", num2, "=", add (num1, num2))

        elif choice == '2':
            print (num1, "-", num2, "=", subtract (num1, num2))

        elif choice == '3':
            print(num1, "*", num2, "=", multiply (num1, num2))

        elif choice == '4':
            print (num1, "/", num2, "=", divide(num1, num2))

        # check if user wants another calculation 
        # berak the while loop if answer is no 
        next_calculation = input ("Let's do next calculation? (yes/no): ")
        if next_calculation == "no":
            break
        else: 
            print ("Invalid Input")
```

    Select operation.
    1.Add
    2.Subtract
    3.Multiply
    4.Divide


    Enter choice (1/2/3/4):  5
    Enter choice (1/2/3/4):  7
    Enter choice (1/2/3/4):  5
    Enter choice (1/2/3/4):  1
    Enter first number:  v


    Invalid input. Please enter a number.


    Enter choice (1/2/3/4):  6.8
    Enter choice (1/2/3/4):  1.2
    Enter choice (1/2/3/4):  1
    Enter first number:  1.34
    Enter second number: -0.00034


    1.34 + -0.00034 = 1.33966


    Let's do next calculation? (yes/no):  yes


    Invalid Input


    Enter choice (1/2/3/4):  4
    Enter first number:  0
    Enter second number: 345


    0.0 / 345.0 = 0.0


    Let's do next calculation? (yes/no):  yes


    Invalid Input


    Enter choice (1/2/3/4):  4
    Enter first number:  45
    Enter second number: 0


    45.0 / 0.0 = Cannot divide by zero


    Let's do next calculation? (yes/no):  no



```python

```
