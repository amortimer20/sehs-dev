---
container: "container"
layout: "../../../../layouts/PageLayout.astro"
title: "C# Fundamentals 1.1 Hello World"
---

[← Back](/courses/c-sharp-fundamentals/)

# Activity 1.1 Hello World!

---

## Introduction

Every programming course begins with a simple program known as _Hello World_. The programming construct you will learn in this lesson is known as **output**. Output is information that is given to the user. In order to output information to the use, we need to use something called `Console.WriteLine()`.

`Console.WriteLine()` is known as a _method_. Methods perform some action in programming. In this case, `Console.WriteLine()` outputs a message to the user via the console. The console is a simple terminal for running text based computer applications. Most of the introductory applications in these programming activities will be console based.

We will also learn how to write comments in C#. Comments serve two purposes, to document, or take notes, in your code, and to disable parts of your program for testing. We will be writing simple programs for the time being, but they will eventually grow in size and complexity. It's important to document parts of your code for yourself and your team, so your code can be easily understood and maintainable. We will start with one type of comment, the single line comment: `// comment`.

### Skills to Practice

- Writing and executing code
- Output messages with the `Console.WriteLine()` function
- Debugging potential errors in your code.
- Writing comments to document or disable code.

## Activity Instructions

### Setup

1. Create a new repl.
   1. Select _C#_ for the language.
   2. Name the Repl **1.1 Output**.
2. Click Create repl.

### Code

Your new workspace will contain a file with some starter code named _main.cs_ (or _Program.cs_ in Visual Studio). Erase the code on line 1, and follow along by typing the code you see below. No copy and pasting! You will never learn how to make programs if you don’t write your own code.

```cs
Console.WriteLine("Hello world!"); // Display the message 'Hello world!'
Console.WriteLine("This class is taught by Mr. Mortimer.");
Console.WriteLine("People say I look like Ethan from h3h3. Both are giant tools.");
Console.WriteLine("Here, have some soy: https://soylent.com/");
Console.WriteLine(); // What does this do?

Console.WriteLine("What is the answer to life, the universe, and everything?");
Console.WriteLine("42. The answer is 42.");
Console.WriteLine();

Console.WriteLine("Sally sells seashells by the seashore.");
Console.WriteLine("Sally is doing five to ten for tax evasion.");
Console.WriteLine();

Console.WriteLine("Sincerely,");
Console.WriteLine("INSERT YOUR NAME");

// These lines are disabled.
// Remove the comment symbols below (//) and run the program one more time.

// Console.WriteLine();
// Console.WriteLine("PS You're fired!");
```

### Debug

To execute your new program, click the run button at the top of your workspace. If everything was written correctly, you will see the various message output to the console. If not, you need to try and see where you made a mistake in your code. The process of testing your program is called _debugging_.

Compare your console output with the example below to see if they match.

```
Hello world!
This class is taught by Mr. Mortimer.
People say I look like Ethan from h3h3. Both are giant tools.
Here, have some soy: https://soylent.com/

What is the answer to life, the universe, and everything?
42. The answer is 42.

Sally sells seashells by the seashore.
Sally is doing five to ten for tax evasion.

Sincerely,
INSERT YOUR NAME

PS You're fired!!
```

## Tips, Tricks, and Reflection

- What happens when you write `Console.WriteLine()` without a message in the parentheses?
- You may have used a programming language where methods are referred to as functions. Technically, a method is a function, but it's defined in a different context. Don't worry about this for now. When we learn about object-oriented programming, we'll talk about this in more detail.
