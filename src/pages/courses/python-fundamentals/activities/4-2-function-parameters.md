---
container: "container"
layout: "../../../../layouts/PageLayout.astro"
title: Python Fundamentals 4.2 Function Parameters
---

[← Back](/courses/python-fundamentals/)

# Activity 4.2 Function Parameters

## Introduction

We can give functions dynamic behavior by passing information when calling them. When we give information to a function, we call this _passing arguments_. Argument values are assigned to special variables called _parameters_. Parameter variables store the argument values passed to them. This allows us to use the arguments inside of a function.

**argument** - Information/data passed to a function
**parameter** - A variable that receives an argument

### Skills to Practice

- Defining functions with parameters
- Invoking user defined functions with arguments

## Activity Instructions

### Setup

1. Create a new repl.
   1. Select _Python_ for the language.
   2. Name the Repl "_4.2 Function Parameters_".
2. Click Create repl.

### Code

```python
def counter(number):
  current_number = 1

  print(f"Counting from {current_number} to {number}.")

  while current_number <= number:
    print(current_number)
    current_number += 1

def specialGreeting(name):
  print(f"Hey there, {name}!")

def specialScolding(name):
  print(f"Shame on you, {name}!")

def bottlesSong(beverage, numberOfBottles):
  while numberOfBottles > 0:
    print(f"{numberOfBottles} bottles of {beverage} on the wall,")
    print(f"{numberOfBottles} bottles of {beverage}!")
    print("You take one down, pass it around.")

    numberOfBottles -= 1

    print(f"{numberOfBottles} bottles of {beverage} on the wall!")


# Test out each def by invoking them.
counter(10) # Replace the 10 argument with a different number
specialGreeting("") # Pass your name as an argument
specialScolding("") # Pass your name as an argument
bottlesSong("Pepsi Max", 3) # Replace the arguments with your own values
```

### Debug

```
Counting from 1 to 10.
1
2
3
4
5
6
7
8
9
10
Hey there, Anthony!
Shame on you, Anthony!
3 bottles of Pepsi Max on the wall,
3 bottles of Pepsi Max!
You take one down, pass it around.
2 bottles of Pepsi Max on the wall!
2 bottles of Pepsi Max on the wall,
2 bottles of Pepsi Max!
You take one down, pass it around.
1 bottles of Pepsi Max on the wall!
1 bottles of Pepsi Max on the wall,
1 bottles of Pepsi Max!
You take one down, pass it around.
0 bottles of Pepsi Max on the wall!
```

## Tips, Tricks, and Reflection

- Try adding some validations to your functions. For example, if the argument passed to the bottlesSong function is less than 1, refuse to sing the song. For the greeting functions, output an error message if the parameter variables are undefined.
