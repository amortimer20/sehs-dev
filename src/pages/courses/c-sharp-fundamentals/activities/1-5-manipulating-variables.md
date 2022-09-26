---
container: "container"
layout: "../../../../layouts/PageLayout.astro"
title: C# Fundamentals 1.5 Manipulating Variables
---

[← Back](/courses/c-sharp-fundamentals/)

# Activity 1.5 Manipulating Variables

## Introduction

This activity will take you a little bit deeper into how variables can be used. While the programs below are merely simulations, they will demonstrate how variables can have their values changed. Here are a few things you need to understand:

- The last activity introduced the equal sign as the _assignment operator_ in programming. It is used to save, or assign a value to a variable. It is not used to check for equality as in Algebra.
- We can overwrite a variables current value using the assignment operator.

We will also start using a convention for naming variables with multiple words in the name. This is known as _camel case_. To use camel case naming for a variable name containing more than one word, capitalize any word _after_ the first word. Ex. **lastName**, **hitPoints**, **shoppingCart**.

### Skills to Practice

- Manipulate variable values using the assignment operator

## Activity Instructions

### Setup

1. Create a new repl.
   1. Select _C#_ for the language.
   2. Name the Repl "_1.5 Manipulating Variables_".
2. Click Create repl.

### Code

```cs
// Video game demo
Console.WriteLine("--- Battle Simulator ---");
int playerHealth = 100;
int enemyHealth = 100;
int enemyAttackDamage = 20;
int potions = 3;

Console.WriteLine($"Health: {playerHealth}");
Console.WriteLine($"Enemy health: {enemyHealth}");
Console.WriteLine();

Console.WriteLine("Round 1");
Console.WriteLine("Player attacks.");
// Subtract 15 from enemyHealth. Save new enemyHealth value.
enemyHealth = enemyHealth - 15;
Console.WriteLine($"You did 15 damage! Enemy health: {enemyHealth}");
// Subtract enemyAttackDamage from player health. Save new playerHealth value.
playerHealth = playerHealth - enemyAttackDamage;
Console.WriteLine($"Enemy did {enemyAttackDamage} damage! Player health: {playerHealth}");
Console.WriteLine();

Console.WriteLine("Using potion...");
playerHealth = playerHealth + 10;
potions--; // Whoa, what does -- do? Google C# ++
Console.WriteLine($"Player health: {playerHealth}. Potions left: {potions}");

Console.WriteLine("Buying one potion...");
potions++; // --, now ++?
Console.WriteLine($"Potions left: {potions}");
Console.WriteLine("Using the potion!!!");
potions--;


Console.WriteLine("\n\n"); // What does this do? Google search "\n C#"


// Bank account demo
Console.WriteLine("--- Banking Simulator ---");
string accountName = "Checking Account";
double accountBalance = 100.50;

Console.WriteLine($"{accountName} balance: {accountBalance}");
Console.WriteLine($"Depositing $99.01 to {accountName}");
accountBalance = accountBalance + 99.01;
Console.WriteLine($"{accountName} balance: {accountBalance}");
```

### Debug

```
--- Battle Simulator ---
Health: 100
Enemy health: 100

Round 1
Player attacks.
You did 15 damage! Enemy health: 85
Enemy did 20 damage! Player health: 80

Using potion...
Player health: 90. Potions left: 2
Buying one potion...
Potions left: 3
Using the potion!!!



--- Banking Simulator ---
Checking Account balance: 100.5
Depositing $99.01 to Checking Account
Checking Account balance: 199.51
```

## Tips, Tricks, and Reflection

- Remember that variables need to be spelled exactly the same every time.
- Make sure to use the right data type for your variables. When performing math, declare integers or doubles, not strings.
