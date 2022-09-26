---
container: "container"
layout: "../../../../layouts/PageLayout.astro"
title: "JavaScript Fundamentals 2.5 Nested If Statements"
---

[← Back](/courses/javascript-fundamentals/)

# Activity 2.5 Nested If Statements

## Introduction

There are many instances where you need to further make decisions after executing an if statement. We can put an if statement inside of another if statement. This is called _nesting_.

```js
var someCondition = true
var someOtherCondition = true

if (someCondition) {
  if (someOtherCondition) {
    // code
  } 
  else {
    //code
  }
}
```

It's so important to keep your code nicely formatted. Here is a review of the tips from before:

- Always line up your curly braces for your code blocks. Most code editors show a line from the closing brace to the top of the if statement to show where a block starts and ends.
- Always indent one tab (2-4 spaces) for every code block. If you have a nested if statement, then the code in the nested code block should indented again.
- If else if, and else statements that belong together should not have space inbetween them. Butt them right up against eachother.
- Space your code based on sections. If you have seperate if statements, space them out with a blank line.

This program is called a choose your own adventure game. It's going to be the biggest program you make so far. Take your time, and test your code frequently. Don't try to write the whole program and then test it at the end, or else it could spell disaster when you try to debug. Write one section at a time, and then test it.

### Skills to Practice

- Nesting if statements
- Testing nested branching statements

## Activity Instructions

### Setup

1. Create a new repl.
   1. Select _Node.js_ for the language.
   2. Name the Repl "_2.5 Nested if statements_".
2. Click Create repl.

## Code

```javascript
var readline = require("readline-sync")

// Trigger an ending by setting on of the ending variables to true
var wolfpackEnding = false
var dragonEnding = false
var gold = 0
var twinkies = 0

console.log("Your car crashes into a tree during a thunderstorm in the woods.")
console.log("As the storm intensifies, you run into a nearby cave to seek shelter.")
console.log("Upon entering the cave, you see two diverging paths...\n")

// Append .toLowerCase() to any string, string variable, or function that returns a string.
// By making the value lowercase, it ensure the if statment executes whether they type "Left" or "left".
var choice = readline.question("Which path do you take? (left or right) -> ").toLowerCase()

console.log("\nRight before you leave, you see a delicious, unopened Hostess Twinkie.")
console.log("Do you eat the Twinkie for sustenance, or will you save it for later?")

var snackChoice = readline.question("(take or eat) -> ").toLowerCase()

if (snackChoice == "take") {
  twinkies = twinkies + 1
  console.log("You never know when a Twinkie will come in handy...\n")
}
else if (snackChoice == "eat") {
  console.log("It's going to be a long night, so you decide to eat it.\n")
} 
else {
  console.log("You leave the twinkie alone.\n")
}

// Left -> Wolves
// Right -> Dragon
if (choice == "left") {
  console.log("You decide to take the left path.")
  console.log("You stumble into a pack of wolves lying together.")
  console.log("The pack leader slowly approaches...\n")

  choice = readline.question("Do you pet the pack leader? (yes or no) -> ").toLowerCase()

  if (choice == "yes" && twinkies >= 1) {
    console.log("As you approach, the wolves smell a delicious snack cake..")
    console.log("In a fit of hungry rage, they rip you to shreds!\n")
  }
  else if (choice == "yes") {
    console.log("The pack leader respects and accepts you.")
    console.log("You are given a gold satchel by the pack leader.")
    console.log("You also cuddle with the wolf pack until the storm subsides...\n")

    gold = 5
    wolfpackEnding = true
  }
  else {
    console.log("The pack leader senses your fear.")
    console.log("The entire pack crowds around you and devours you...\n")
  }
} // End left path
else if (choice == "right") {
  console.log("You decide to take the right path.")
  console.log("\nLater down the trail, you stumble upon an overweight,")
  console.log("repulsive looking talking dragon named Mort the Pudgy.")

  console.log("The dragon speaks: 'Did you bring me snack cakes??'")

  choice = readline.question("Do you have a treat to give this foul creature? (yes, no) -> ")

  if (choice == "yes" && twinkies >= 1) {
    console.log("Me love Twinkie!!! Here take gold!")
    console.log("The dragon grants you the gold he was guarding.\n")

    var goldAmount = parseInt(readline.question("How much gold do you take? -> "))

    if (goldAmount > 0 && goldAmount <= 100) {
      console.log("Mortimer the Pudgy grants you his gold...\n")
      gold = goldAmount
    } 
    else if (goldAmount > 100) {
      console.log("'Greedy! No gold for you!'\n")
    } 
    else {
      // Easter Egg - Select negative amount
      console.log("Mortimer the pudgy respects your piety.")
      console.log("You are granted all of the gold!\n")
      gold = 100000
    }

    dragonEnding = true
  } 
  else if (choice == "yes") {
    // Say yes but you have no snack cakes
    console.log("'Fool!!!'")
    console.log("The dragon is angry that you would try to deceive him.")
    console.log("He smells that you have no Twinkie, and devours you instead...")
  } 
  else if (choice == "no") {
    console.log("'Fool!!!'")
    console.log("The dragon devours you whole.")
    console.log("He desired a delicious Hostess treat, but settles for you instead...\n")
  } 
  else {
    console.log("Your inability to answer his question upsets him.")
    console.log("The dragon smashes you with his tail...\n")
  }
} // End right path
else {
  console.log("You decide not to enter. You receive a thundershock and lie in the storm...\n")
}

// Ending
console.log("ENDING:")
if (wolfpackEnding) {
  // Same as wolfpackEnding == true
  console.log("By cuddling with the wolfpack, you weather out the storm.")
  console.log("Upon leaving the cave, they follow you, seeing you as the new pack leader.")
  console.log("You survived!!!")
} 
else if (dragonEnding) {
  // Same as dragonEnding == true
  console.log("By tempting Mortimer the Pudgy with a delicious Hostess snack cake, you avoid his wrath."
  )
  console.log("He flies you back home after the storm, but not after raiding the nearest Hostess factory.")
  console.log("You survived!!!")
} 
else {
  console.log("Game over!!!")
}

if (gold > 0) {
  console.log(`\nYou not only survived, but you found ${gold} gold! Good work!`)
}
```

### Debug

```
Your car crashes into a tree during a thunderstorm in the woods.
As the storm intensifies, you run into a nearby cave to seek shelter.
Upon entering the cave, you see two diverging paths...

Which path do you take? (left or right) -> left

Right before you leave, you see a delicious, unopened Hostess Twinkie.
Do you eat the Twinkie for sustenance, or will you save it for later?
(take or eat) -> eat
It's going to be a long night, so you decide to eat it.

You decide to take the left path.
You stumble into a pack of wolves lying together.
The pack leader slowly approaches...

Do you pet the pack leader? (yes or no) -> yes
The pack leader respects and accepts you.
You are given a gold satchel by the pack leader.
You also cuddle with the wolf pack until the storm subsides...

ENDING:
By cuddling with the wolfpack, you weather out the storm.
Upon leaving the cave, they follow you, seeing you as the new pack leader.
You survived!!!

You not only survived, but you found 5 gold! Good work!
```

## Tips, Tricks, and Reflection

- I cannot stress the importance of testing your application regularly. When you start nesting if statements, your app will potentially have many different paths of execution. It's important to make sure everything runs as you develop your application.
