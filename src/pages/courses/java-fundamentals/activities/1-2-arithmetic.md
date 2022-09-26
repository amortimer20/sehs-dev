---
container: "container"
layout: "../../../../layouts/PageLayout.astro"
title: "Java Fundamentals 1.2 Arithmetic"
---

[← Back](/courses/java-fundamentals/)

# Activity 1.2 # Activity 1.2 Arithmetic

## Introduction

Math is extremely important in computer science. Any useful program has to store and use numbers in some way. From video games, to online stores, to graphic design apps, math is necessary to creating the software we use every day. It is necessary to not only calculate math expressions, but also to display the results to the user. To practice these expressions, we'll be displaying the answer in the console using `System.out.println()`.

`System.out.println()` can display more than just plain text messages, it is also capable of outputting numbers and math expressions. In this activity, we will writing simple programs to demonstrate how math works in Java. There are multiple symbols used to write math expressions:

- \+ Addition operator
- \- Subtraction operator
- \* Multiplication operator
- / Division operator, calculates quotient
- % Modulus (mod) operator, calculates remainer

The symbols for division may throw you off, because they don't match the traditional arithmetic symbols we use in math class. We'll practice using them in depth, so you can see how useful it is to divide numbers in different ways.

### Skills to Practice

- Write math expressions
- Output numbers with `System.out.println()`
- Document code with single line comments
- Control math calculation with order of operations

## Activity Instructions

### Setup

1. Create a new repl.
   1. Select _Java_ for the language.
   2. Name the Repl **1.2 Math**.
2. Click Create repl.

### Code

```java
class Main {
  public static void main(String[] args) {
    // Addition
    System.out.println("I have two apples. I find another apple. How many apples do I have?");
    System.out.println(2 + 1);
    System.out.println();
    
    System.out.println("Bank balance: $1000. Depositing $500.96. Your new balance is:");
    System.out.println(1000 + 500.96);
    System.out.println();
    
    // Subtraction
    System.out.println("I'm hungry and I want to eat an apple. How many apples will I have left?");
    System.out.println(3 - 1);
    System.out.println();
    
    // Multiplication
    System.out.println("I'm 30 years old. In months, that's: "); // Replace 30 with your age
    System.out.println(30 * 12); // Replace 30 with your age
    System.out.println();
    
    // Division - Quotient and remainder
    
    // Quotients
    // Notice the difference between using integers and decimals
    System.out.println("We have eight slices of pizza between the three of us.");
    System.out.println("We each get this many slices:");
    System.out.println(8 / 2);
    System.out.println("If we cut up the other slice, we get:");
    System.out.println(8 / 3.0);
    System.out.println();
    
    System.out.println("I have to split this dollar between the six of us. We each get: ");
    System.out.println(100 / 6); // Will this divide evenly?
    System.out.println();
    
    // Remainder using the modulus operator
    System.out.println("After splitting up the dollar, how many cents are left over?");
    System.out.println(100 % 6);
    System.out.println();
    
    // Order of operations
    System.out.println("4 * 10 + 12 equals:");
    System.out.println(4 * 10 + 12);
    System.out.println("4 * (10 + 12); equals:");
    System.out.println(4 * (10 + 12));
  }
}
```

### Debug

```
I have two apples. I find another apple. How many apples do I have?
3

Bank balance: $1000. Depositing $500.96. Your new balance is:
1500.96

I'm hungry and I want to eat an apple. How many apples will I have left?
2

I'm 30 years old. In months, that's: 
360

We have eight slices of pizza between the three of us.
We each get this many slices:
4
If we cut up the other slice, we get:
2.6666666666666665

I have to split this dollar between the six of us. We each get: 
16

After splitting up the dollar, how many cents are left over?
4

4 * 10 + 12 equals:
52
4 * (10 + 12); equals:
88
```

## Tips, Tricks, and Reflection

- Notice that division with only integers returns an integer result. But if you include at least one decimal number, ex. 5.0 or 5.1, the result will contain a decimal answer.
- This program looks terrible. The math for each statement may correct, but it's hard to read. The division involving money returns a repeating decimal, every answer is on it's own line, and the monetary values don't have a dollar sign. These are called _formatting issues_, and we will learn how to make the output look better in future programs.
- When writing math expressions in code, you don't have to have a space in between the numbers and signs. It is valid to write **2+2**, but I recommend writing **2 + 2** with the spaces in between. We call this a _convention_, or a best practice.
- Math signs `+ - * / %` are known as _operators_, and numbers used with operators are known as _operands_. When we write math statements they are called _expressions_.
