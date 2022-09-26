---
container: "container"
layout: "../../../../layouts/PageLayout.astro"
title: "JavaScript Fundamentals 2.3 Branching Statements"
---

[← Back](/courses/javascript-fundamentals/)

# Activity 2.3 Branching Statements

## Introduction

The last activity introduced us to the idea of controlling the flow of an application with _if statements_. The age checker app checked each if statement's condition resulted in true. There are many instances where you only want one selection to execute. i.e. One or the other.

We can _branch_ if statements with to other kinds of statements, `else if` and `else`.

- `else if` must follow and if statement, and will only check it's condition if the preceding if statement condition resulted in `false`. You can chain as many else if statements as you want, but they _must_ come after the initial if statement.
- `else` must be at the end of an if or else if statement. It does not require a condition, and will execute if any preceding if or else if statement coniditions result in `false`.

_Example:_

```js
var number = 100

if (number > 100) {
  console.log("number is higher than 100")
} 
else if (number == 100) {
  console.log("number is 100")
} 
else {
  console.log("number is less than 100")
}
```

### Skills to Practice

- Branching if statements with _else if_ and _else_
- Making a main menu

## Activity Instructions

### Setup

1. Create a new repl.
   1. Select _Node.js_ for the language.
   2. Name the Repl "_2.3 Branching_".
2. Click Create repl.

### Code

```javascript
var readline = require("readline-sync")

console.log("--- Not so Zodiac Calendar ---")

var month = readline.question("\nWhat month were you born? ")

console.log("You were born the month of the: ")

if (month == "January") {
    console.log("Beef and Cheese")
}
else if (month == "February") {
    console.log("Vegan Caserole")
}
else if (month == "March") {
    console.log("Buffalo Chicken Dip")
}
else if (month == "April") {
    console.log("Teriyaki Chicken")
}
else if (month == "May") {
    console.log("Deep Fried Hummus")
}
else if (month == "June") {
    console.log("Nachos and Gravy")
}
else if (month == "July") {
    console.log("Cottage Goat Cheese")
}
else if (month == "August") {
    console.log("Raw Soy")
}
else if (month == "September") {
    console.log("Fried Twinkie")
}
else if (month == "October") {
    console.log("Liver and Onions")
}
else if (month == "November") {
    console.log("Turkey Gizzard Tenders")
}
else if (month == "December") {
    console.log("Zucchini Muffin")
}
else {
    console.log("There's no such month as " + month + " you cottonheaded ninnymuggins.")
}


// Simple ATM Demo
console.log("\n--- ATM Demo ---\n")
var balance = parseFloat(readline.question("Set your initial balance: $"))

console.log("Crangis McBasketball ATM")
console.log("------------------------")
console.log("Select an option: ")
console.log("1) View Balance")
console.log("2) Deposit")
console.log("3) Withdraw")

// We're not doing math with the number, so it's okay to leave it as a string.
var option = readline.question("Enter your option (1,2,3): ")

if (option == "1") {
  console.log(`Your balance is $${balance}.`)
} 
else if (option == "2") {
  var deposit = readline.question("How much would you like to deposit? $")
  deposit = parseFloat(deposit)
  balance = balance + deposit
  console.log(`Thank you for your deposit of $${deposit}.`)
  console.log(`Your balance is now $${balance}.`)
} 
else if (option == "3") {
  var withdraw = readline.question("How much would you like to withdraw? $")
  withdraw = parseFloat(withdraw)
  balance = balance - withdraw
  console.log(`Thank you for your withdraw of $${withdraw}.`)
  console.log(`Your balance is now $${balance}.`)
} 
else {
  console.log("Invalid option. Exiting...")
}
```

### Debug

```
--- Not so Zodiac Calendar ---

What month were you born? May
You were born the month of the: 
Deep Fried Hummus

--- ATM Demo ---

Set your initial balance: $1200
Crangis McBasketball ATM
------------------------
Select an option:
1) View Balance
2) Deposit
3) Withdraw
Enter your option (1,2,3): 2
How much would you like to deposit? $75.95
Thank you for your deposit of $75.95.
Your balance is now $1275.95.
```

## Tips, Tricks, and Reflection

- Notice how many code blocks are used to create even a simple application. Be careful with the following formatting (You will thank me later):
  - Make sure all curly braces line up nicely.
  - Make sure code inside a code block is indented one tab.
- Each demo applicatio only has one `else if` statement. Remember, you can have as many `else if` statements as you need.
