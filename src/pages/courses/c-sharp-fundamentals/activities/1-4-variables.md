---
container: "container"
layout: "../../../../layouts/PageLayout.astro"
title: C# Fundamentals 1.4 Variables
---

[← Back](/courses/c-sharp-fundamentals/)

# Activity 1.4 Variables

## Introduction

_Variables_ allow us to save data during our program execution. For example, in an RPG video game, your character has attributes such as health, magic, stamina, etc. These are values that need to be tracked throughout the game. Variables allow us to store this data and use it throughout the program.

In C#, creating a variable is known as _declaring a variable_. When we want a variable to 'store' some value, this is known as _variable assignment_. We use the equal sign **`=`** to assign a value to a variable. We can both declare and assign a value in one line, which is known as _initialization_. We will start by using three data types: `string`, `int`, and `double`.

When declaring a variable, the data type must be specified. Once the data type is declared, the variable can only ever store data of that type. This is known as **static typing**.


```cs
// Declare a string variable.
string name;

// Assign a value to name.
// No need to use the string keyword after the variable has been declared.
name = "Anthony";

// Initialize an integer and a double variable.
int age = 5;
double weight = 500.55;

name = 10; // BAD! name is a string. This will cause an error.
```

### Skills to Practice

- Declaring and assigning values to variables
- Use variables in formatted strings

## Activity Instructions

### Setup

1. Create a new repl.
   1. Select _C#_ for the language.
   2. Name the Repl "_1.4 Variables_".
2. Click Create repl.

### Code

```cs
// String variables
string name = "Anthony"; // Replace the name with your name;
string food = "Steak"; // Replace the food with your favorite food;
string item = "peppers";

Console.WriteLine($"Hello, my name is {name}");
Console.WriteLine($"{name} likes the stinkiest of {food}.");
Console.WriteLine($"{name} likes {food} so much, he/she eats it out of the garbage!");
Console.WriteLine();

Console.WriteLine($"Peter Piper picked a peck of pickled {item}");
Console.WriteLine($"A peck of pickled {item} Peter Piper picked");
Console.WriteLine();

// Numbers
int age = 30; // Replace the number with your age

Console.WriteLine($"You will reach age 100 in {100 - age} years!");
Console.WriteLine();

double balance = 35.25;
double withdraw = 0; // Replace the 0 with larger number
double leftover = balance - withdraw;

Console.WriteLine($"You have a balance of ${balance} in your bank account.");

Console.WriteLine($"If you withdraw ${withdraw}, you will have ${leftover}.");
Console.WriteLine();

int health = 100;
double damage = 55.5;

Console.WriteLine($"You've taken {damage} damage. You have {health - damage} health left.");
```

### Debug

```
Hello, my name is Anthony
Anthony likes the stinkiest of Steak.
Anthony likes Steak so much, he/she eats it out of the garbage!

Peter Piper picked a peck of pickled peppers
A peck of pickled peppers Peter Piper picked

You will reach age 100 in 70 years!

You have a balance of $35.25 in your bank account.
If you withdraw $0, you will have $35.25.

You've taken 55.5 damage. You have 44.5 health left.
```

## Tips, Tricks, and Reflection

- Variable names must begin with a letter or underscore.
- Variables **cannot** contain spaces in their name!
- Notice how I use underscores when making variables that have multiple words in the name. This is known as snake case, and it's the convention for writing variable names with multiple words. I recommend this style of variable naming when you want to use multiple words for the variable name.
- C# 3.0 brought support to a new keyword `var` for declaring variables. This is known as _type inference_, and we will check out how
it works shortly.
- Technically speaking, variables just reference data stored in memory, but as a beginner, it's okay to think of a variable as a storage unit. People may cry about this, but just ignore them and give them a wedgie.
