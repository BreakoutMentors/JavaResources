# Java Exercises

Short, self-contained practice problems — no zip, no upload, no images. Each one is a single
`Main.java` you paste straight into a fresh JuiceMind sandbox.

For the bigger graphical projects (Snake, Pacman, Tower Defense, and friends), see the
[main README](README.md) instead.

---

## How to use an exercise

**1. Go to [play.juicemind.com/dashboard/code-sandbox](https://play.juicemind.com/dashboard/code-sandbox)**
and sign in (a free account is fine).

**2. Click `+ Create New Sandbox`.**
   - Give it a name (for example, `Hailstone`)
   - Under **Choose Programming Language**, select **Java**
   - Click **🚀 Create Sandbox**

**3. Click inside `Main.java`, select everything (Ctrl-A / Cmd-A), and delete it.**

**4. Copy the code block for the exercise below and paste it in.**

**5. Press the blue ▶ Run button.**

Output appears in the console on the right. Exercises that ask you questions read your
answers from that same console — click into it and type.

> Every exercise is one file and the class is always called `Main`, because JuiceMind
> always runs `Main.java`. Don't rename the class.

---

## Contents

| # | Topic | Exercises |
|---|---|---|
| 1 | [Printing and User Input](#1-printing-and-user-input) | Introduction |
| 2 | [If / Else](#2-if--else) | Grade Checker · Number Guessing · Multiplication Game |
| 3 | [Loops and Functions](#3-loops-and-functions) | Loops Introduction · Hailstone Sequence · Factorial and Summation · Largest Square |
| 4 | [Randomness](#4-randomness) | Coin Flip and Dice Roll |
| 5 | [Lists and Arrays](#5-lists-and-arrays) | Basic Arrays · Silly Sentence Generator · ArrayLists |
| 6 | [Decomposition — Harder Problems](#6-decomposition--harder-problems) | Prime Factors · Same Hailstone · Memory Game |
| 7 | [Object-Oriented Design](#7-object-oriented-design) | Classroom |
| 8 | [Inheritance and Abstract Classes](#8-inheritance-and-abstract-classes) | Shapes · Graphics Objects |
| 9 | [Recursion](#9-recursion) | Intro to Recursion · Harder Problems |
| 10 | [Data Structures](#10-data-structures) | Linked List · Binary Tree |

---

## 1. Printing and User Input

### Introduction

Printing to the console, and reading typed answers back with a `Scanner`.

```java
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner s = new Scanner(System.in);
    System.out.print("What is your name? ");
    String name = s.nextLine();
    System.out.println("Hi " + name + "!");
    // Try int x = s.nextInt()
    // Now try asking for your age, school, and whatever other question you want, and printing it out afterwards!
  }
}
```

---

## 2. If / Else

### Grade Checker

<!-- CODE-PENDING: GradeChecker -->

### Number Guessing

<!-- CODE-PENDING: NumberGuessingGame -->

### Multiplication Game

<!-- CODE-PENDING: MultiplicationGame -->

---

## 3. Loops and Functions

### Loops Introduction

<!-- CODE-PENDING: Basic-Loops -->

### Hailstone Sequence

<!-- CODE-PENDING: Hailstone -->

### Factorial and Summation

<!-- CODE-PENDING: Factorial-and-Summation -->

### Largest Square

<!-- CODE-PENDING: Largest-Square -->

---

## 4. Randomness

### Coin Flip and Dice Roll

<!-- CODE-PENDING: Coins-and-Dice -->

---

## 5. Lists and Arrays

### Basic Arrays

<!-- CODE-PENDING: Arrays -->

### Silly Sentence Generator

<!-- CODE-PENDING: SillySentenceGenerator -->

### ArrayLists

<!-- CODE-PENDING: ArrayLists -->

---

## 6. Decomposition — Harder Problems

### Prime Factors

<!-- CODE-PENDING: Prime-Factors -->

### Same Hailstone

<!-- CODE-PENDING: SameHailstone -->

### Memory Game

<!-- CODE-PENDING: MemoryGame -->

---

## 7. Object-Oriented Design

### Classroom

<!-- CODE-PENDING: Classroom -->

---

## 8. Inheritance and Abstract Classes

### Shapes

<!-- CODE-PENDING: Shapes -->

### Graphics Objects

The starting point for the Space Invaders project. Uses the ACM graphics library, so this
one needs `acm.jar` in the sandbox — the easiest route is to upload
[SpaceInvaders-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/SpaceInvaders-Starter.zip)
from the main README, which already includes it.

<!-- CODE-PENDING: GraphicsObjects -->

---

## 9. Recursion

### Intro to Recursion

<!-- CODE-PENDING: Basic-Recursion -->

### Harder Problems

<!-- CODE-PENDING: Recursive-Sequences-harder-problems -->

---

## 10. Data Structures

### Linked List

<!-- CODE-PENDING: LinkedList -->

### Binary Tree

<!-- CODE-PENDING: BinaryTree -->

---

## Adding an exercise to this file

Keep each one to a single `Main.java` with no external files, so a student can paste and run
in under a minute. If an exercise needs images, level files, or `acm.jar`, it belongs in the
[main README](README.md) as a zip instead.
