# Java Exercises

Short practice problems — nothing to download, no files to upload. Every exercise is a single
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

That's the whole loop — one file, one paste, press play. Output appears in the console on the
right. Exercises that ask you questions read your typed answers from that same console, so
click into it and type.

> A few of the later exercises have more than one class — `Student` and `Classroom`, or
> `Shape` and `Rectangle` and `Square`. They all live in the one file, below `Main`. Java is
> fine with that, and it keeps these to a single copy and paste. Add your own new classes at
> the bottom of the same file.

> The first class is always called `Main`, because JuiceMind always runs `Main.java`.
> Don't rename it.

---

## Contents

| # | Topic | Exercises |
|---|---|---|
| 1 | [Printing and User Input](#1-printing-and-user-input) | Introduction |
| 2 | [If / Else](#2-if-else) | Grade Checker · Number Guessing · Multiplication Game |
| 3 | [Loops and Functions](#3-loops-and-functions) | Loops Introduction · Hailstone Sequence · Factorial and Summation · Largest Square |
| 4 | [Randomness](#4-randomness) | Coin Flip and Dice Roll |
| 5 | [Lists and Arrays](#5-lists-and-arrays) | Basic Arrays · Silly Sentence Generator · ArrayLists |
| 6 | [Decomposition — Harder Problems](#6-decomposition-harder-problems) | Prime Factors · Same Hailstone · Memory Game |
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

A working `if` for an A, and the rest of the letter grades left to you. The stretch goal is nesting a second `if / else if / else` inside the A branch for A+ / A / A-.

```java
import java.util.Scanner;

class Main {
  public static void main(String[] args) {
    Scanner s = new Scanner(System.in);
    int grade = s.nextInt(); // Gets the grade from the user input

    if (grade > 90) {
      // Print "A"
    }

    //Finish the rest of the grades - if > 80, print B, if > 70, print C, etc.
    //Can you do a nested if + if else + else statement within the A grade to making it print A+, A, A-?
  }
}
```

### Number Guessing

**This one already works** — play it first, then read the code. Four numbered challenges in the comments ask you to change the range, the number of tries, and the `if` structure.

```java
import java.util.Random;
import java.util.Scanner;

public class Main {

	//This is a working game! Play it to see what it does. Then take a look at the code.
	
	//Challenge #0: give the cowboy your name
	//Challenge #1: change the guessing game to between 1 and 199
	//Challenge #2: give 9 tries to guess it
  //Challenge #3: change it to use if + else if + else
	
	public static void main(String[] args) {
    Scanner s = new Scanner(System.in);  // Create a Scanner object

		System.out.println("Howdy, I'm Cowboy Dan! I have a secret number that is between 1 and 99.");
		System.out.println("I'll give you 6 tries to guess it!");
		System.out.println();
		
    Random r = new Random();

		int secret = r.nextInt(100);
		
		for(int i=0; i<6; i++){
			System.out.println("What is your guess? ");
      int guess = s.nextInt();
			
			if(guess < secret){
				System.out.println("Nope, higher");
			}
			if(guess > secret){
				System.out.println("Nope, lower");
			}
			if(guess == secret){
				System.out.println("You got it!");
				
				return; //so the game doesn't keep going
			}
			
		}
		
    System.out.println("You lose, better luck next time!");
		
	}
	
}
```

### Multiplication Game

The skeleton of a times-tables drill that doesn't work yet. Four numbered steps: welcome message, pick two random numbers, print the problem, read the answer.

```java
class Main {
  public static void main(String[] args) {

    //This game is not yet working!

    //0. Print a welcome message
    System.out.println("Hello world!");

    //1. Randomly pick the numbers to multiply
    //Hint: be sure to import the package and use new keyword
    int number1 = 1;
    int number2 = 1;
    int answer = number1 * number2; 

    int guess = 0;
    while(guess != answer){
      //2. Print the random math problem
      System.out.println("What is ...");
      
      //3. Ask the user to enter a number, set it to the guess variable
      //Hint: You may need to import something to get user input
      if(guess != answer){
        System.out.println("No, try again");
      }
    }
    
    
  }
}
```

---

## 3. Loops and Functions

### Loops Introduction

Two finished examples — the same countdown written as a `for` loop and as a `while` loop — then four methods to fill in: `numbersLessThanX`, `countdown`, `squares`, `powersOfTwo`.

```java
class Main {
  public Main() {
    numbersLessThan10();
    whileNumsLessThan10();
    // Call your other functions
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public void numbersLessThan10() {
    for(int i = 0; i < 10; i++) {
      System.out.println(i);
    }
  }

  public void whileNumsLessThan10() {
    // Does the same thing as the method above, but using a while loop instead of a for loop
    int i = 0;
    while (i < 10) {
      System.out.println(i);
      i++;
    }
  }

  public void numbersLessThanX(int x) {
    // Fill in this method to print all the numbers less than the parameter (placeholder variable) x
  }

  public void countdown(int x) {
    // Fill in this method to print all the numbers from x all the way to 0.
  }

  public void squares(int x) {
    // Fill in this method to print all the square numbers from 1 to x.
  }

  public void powersOfTwo(int x) {
    // Fill in this method to print all the powers of 2 from 1 to x.
    // Bonus: Try to count how many powers of two there were between 1 and x.
  }

  // Get creative! Make your own math printing problems to show on the screen. (Examples: cube numbers, multiples of 5, etc.)
}
```

### Hailstone Sequence

The 3n+1 sequence. Ask for a number; halve it when it's even, triple-plus-one when it's odd, and keep going until you reach 1. Bonus: count the steps.

> **Note:** the original had this class named `Hailstone` while the file was `Main.java`,
> which doesn't compile. Renamed to `Main` — that's what JuiceMind runs anyway.

```java
class Main {
	
	//ask the user for a number
	//until you reach zero, do the following:
		//if the number is even, divide by 2
		//if the number is odd, multiply by 3 and add 1
	
	//bonus: count how many steps it takes to get to zero
	
	public Main() {
		
		/* You fill this in */

	}

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }
	
}
```

### Factorial and Summation

Two methods to write, with the expected answers already in `main` so you can check yourself: `factorial(5)` → 120, `summation(5)` → 15.

```java
class Main {

  public Main() {
    System.out.println(factorial(5)); // Should print 120
    System.out.println(factorial(7)); // Should print 5040
    System.out.println(factorial(0)); // Should print 1

    System.out.println(summation(5)); // Should print 15
    System.out.println(summation(10)); // Should print 55
    System.out.println(summation(0)); // Should print 0

  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public int factorial(int x) {
    // Returns the factorial of a number. Hint: Use a for or while loop.
    // Example: For the number 5, answer would be 5 * 4 * 3 * 2 * 1 = 120.
    return 0;
  }

  public int summation(int x) {
    // Returns the summation of a number (or the triangular number).
    // Example: For the number 5, answer would be 5 + 4 + 3 + 2 + 1 = 15.
    return 0;
  }
}
```

### Largest Square

Return the largest perfect square less than or equal to x. `largestSquare(295)` should give 289.

```java
class Main {
  
  public Main() {
    System.out.println(largestSquare(10)); // Should print 9
    System.out.println(largestSquare(295)); // Should print 289
    System.out.println(largestSquare(36)); // Should print 36
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public int largestSquare(int x) {
    // Returns the largest square number that is under or equal to x.
    return 1; // Replace this return statement.
  }
}
```

---

## 4. Randomness

### Coin Flip and Dice Roll

Write `flipCoin()` and `rollDice()`, then flip 100 times and count the results. Bonus: track the six dice faces in an array.

```java
import java.util.Random;
class Main {

  public Main() {
    // Try to flip there coin 100 times and see how many heads and tails there are.
    // Do the same for the dice (keep track of how many 1 - 6). Bonus: Use an array to keep track of the numbers.
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public int flipCoin() {
    // Should return either 0 or 1, 0 = heads and 1 = tails; 
    Random r = new Random();
    return 1;
  }

  public int rollDice() {
    // Should return a number from 1 to 6
    Random r = new Random();
    return 1;
  }
}
```

---

## 5. Lists and Arrays

### Basic Arrays

Fixed-size arrays. One worked example, then three methods: build an array of numbers up to x, double every number in an array, and split a `String` into a `char[]`.

```java
class Main {

  public Main() {
    int[] intList = new int[5]; // Example of making an array. We HAVE to specify the size.
    intList[0] = 1;
    // Use a for loop to print out all the numbers in the array.
    // Try to change the other numbers in the array.
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public int[] numbersToX(int x){
    // Return an intarray with all the numbers to x
    return new int[1];
  }

  public int[] doubleNumbers(int[] l) {
    // Function that returns a new int array that doubles all the numbers in l.
    return new int[1];
  }

  public char[] separate(String s) {
    // Function that returns a char array of all the characters in String s.
    return new char[1];
  }
}
```

### Silly Sentence Generator

Pick a random word from an array, then build up to a whole sentence: *The &lt;adjective&gt; &lt;noun&gt; &lt;verb&gt; the &lt;adjective&gt; &lt;noun&gt;.* One line inside `randomWord` is marked `YOU FILL THIS IN`.

```java
import java.util.Random;
class Main {
  Random r = new Random();

  public Main() {
    String[] verbArray = {"runs", "jumps", "climbs"};

    //a simple sentence structure:
    //The <adjective> <noun> <verb> the <adjective> <noun>.
    //call the function and remember the result
    String verb = randomWord(verbArray);
    System.out.println(verb);
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  //this function is given a list of words and selects one at random
  private String randomWord(String[] wordArray){
    //get the length of the words list
    int numberOfWords = wordArray.length;
    //pick a random number up to the end of the list
    int randomIndex = r.nextInt(numberOfWords);
    //select the word at the number spot
    String selectedWord = "YOU FILL THIS IN";

    return selectedWord;
  }
}
```

### ArrayLists

The resizable cousin of the array. Three methods: a list of squares, a reversed copy, and merging two lists of names.

```java
import java.util.ArrayList;

class Main {
  public Main() {
    // Unlike arrays, we can actually change the size of arraylists;
    // Example:
    ArrayList<String> names = new ArrayList<>();
    names.add("Bob");
    names.add("Steve");
    names.add("Luke");
    System.out.println(names);
    // Look up java documentation for all the stuff you can do with java arraylists!
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public ArrayList<Integer> squares(int x) {
    // Function that returns all the square numbers in an array up to the number x.
    return null;
  }

  public ArrayList<Integer> reverse(ArrayList<Integer> l) {
    // Function that returns a new list with everything reversed.
    return null;
  }

  public ArrayList<String> addNames(ArrayList<String> oldNames, ArrayList<String> newNames) {
    // Function that returns the one list with the combination of two lists of names merged together.
    return null;
  }
}
```

---

## 6. Decomposition — Harder Problems

### Prime Factors

Four methods that build on each other — `is_prime`, `factors`, `primeFactors`, `biggestPrime`. The prime factors of 13195 are 5, 7, 13 and 29.

```java
import java.util.ArrayList;

//Example: The prime factors of 13195 are 5, 7, 13 and 29. So the biggest prime factor is 29.

class Main {
  public Main() {
    System.out.println("Hello world!");
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public boolean is_prime(int x) {
    /* Returns whether x is prime */
    return false;
  }

  public ArrayList<Integer> factors(int x) {
    /* Returns all the factors of x */
    return null;
  }

  public ArrayList<Integer> primeFactors(int x) {
    /* Returns all the prime factors of x */
    return null;
  }

  public int biggestPrime(int x) {
    /* Returns the biggest prime factor of x */
    return 0;
  }
}
```

### Same Hailstone

Do two numbers end up in the same hailstone sequence? Write `inHailSequence` first, then call it from `sameHailSequence`.

```java
class Main {
  // The hailstone sequence is a sequence in which a number will eventually get to 1. If the number is even, you divide it by 2 to get the next number in the sequence. If it is odd, you multiply it by 3 and add 1 to get the next number.
  
  public Main() {
    System.out.println(sameHailSequence(10, 4));
    // Should print true
    System.out.println(sameHailSequence(7, 32));
    // Should print false
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public boolean inHailSequence(int x, int y) {
    // This function should return whether the number y is inside the hailstone sequence of x.
    return false; // Replace this return with own code
  }

  public boolean sameHailSequence(int x, int y) {
    // This function should return whether the numbers x and y are in the same hailstone sequence.
    // Hint: think about how you might call inHailSequence multiple times
    return false;
  }
}
```

### Memory Game

**This one already runs** — digits flash on screen and a new one is added every couple of seconds. Your job is to read the player's guess back and stop when they get it wrong.

```java
import java.lang.Thread;
import java.util.ArrayList;
import java.util.Random;

class Main {

  /*
  The goal of this game is to memorize the digits that flash on the screen for 1-2 seconds. If you can correctly type the numbers back in, it will add a new digit to the pattern and repeat the process. See how far you can go!

Challenge: ask the user for an input, compare it to the list of random digits, keep going if they get it right or stop if they get it wrong.
  */

  Random r = new Random();
  ArrayList<Integer> numbers = new ArrayList<Integer>();

  public Main() throws InterruptedException{
    while(true){
      clearScreen();
      Thread.sleep(500);
      int newDigit = r.nextInt(9);
      numbers.add(newDigit);
      System.out.println(arrayToString(numbers));
      Thread.sleep(1500);
    }
  }

  public static void main(String[] args) {
    try{
      new Main(); //kicks off the program
    }catch(Exception e){
      System.out.println(e);
    }
  }

  private void clearScreen(){
    System.out.print("\033[H\033[2J");
    System.out.flush();
  }

  private String arrayToString(ArrayList<Integer> arraylist){
    String output = "";
    for(int i=0; i<arraylist.size(); i++){
      output += arraylist.get(i);
    }
    return output;
  }
}
```

---

## 7. Object-Oriented Design

### Classroom

`Student` and `Classroom` are skeletons — finish the constructors, the getters, and `toString()`, then make objects in `Main` and print them. All three classes are in the one file.

```java
import java.util.ArrayList;

class Main {
  public static void main(String[] args) {
    System.out.println("Hello world!");
    // Test out your classroom/student by making new variables.
  }
}

class Student {
  private int grade, age;
  private String name;
  //Add more instance variables as you see fit.

  public Student(String name, int grade, int age) {
    // Finish the constructor!
  }

  public String toString() {
    return "";  // Returns a string that represents the Student. This string will print out when we do System.out.println(student)
  }

  public int getGrade() {
    return 0; // Change to return the grade
  }

  public int getAge() {
    return 0; // Change to return the age
  }

  public void changeGrade(int x) {
    // Fill in!
  }

  // Add other methods as you see fit.
}

class Classroom {
  private String className;
  private ArrayList<Student> students;
  // Add more instance variables! (e.g. teacher name, time, etc.)

  public Classroom(ArrayList<Student> s, String name) {
    this.className = name;
    this.students = s;
  }

  public int getSize() {
    return 0; // How would we get the size of the class?
  }

  public void addStudent(){
    // How would we add a student to the class?
  }

  public String toString() {
    return ""; // Returns a string that represents the classroom. This string will print out when we do System.out.println(classroom)
  }

  // Make more methods!
  /* Example headers:
     public Student removeStudent()
     public void changeTeacher()
     public ArrayList<Student> getStudents()
     public void printStudents()
     
     public double getAverageGrade()

     etc..
  */

}
```

---

## 8. Inheritance and Abstract Classes

### Shapes

`Shape` is abstract, `Rectangle` extends it, and `Square` extends `Rectangle` (note how `super` reuses the parent constructor). Fill in `Rectangle`, then add `Triangle` and `Circle` at the bottom of the same file.

```java
class Main {
  public static void main(String[] args) {
    Rectangle r = new Rectangle(10, 30);
    // Add Triangle and Circle classes at the bottom of this file!
  }
}

abstract class Shape {
  abstract double getArea();
  abstract double getPerimeter();

  public boolean is2D() {
    return true;
  }
}

class Rectangle extends Shape {
  // Fill in instance variables
  
  public Rectangle (int width, int height) {
    // Implement instance variables, etc.
  }

  public double getArea(){
    return 0; // Replace this with a correct area function
  }

  public double getPerimeter(){
    return 0; // Replace this with a correct perimeter function
  }

  public double getDiagonal(){
    return 0; // Replace this with a correct diagonal function.
  }
}

class Square extends Rectangle {
  public Square(int side) {
    super(side, side); //super uses the constructor of the parent class.
  }
  
  //Add other methods as you see fit
}
```

### Graphics Objects

The starting point for the Space Invaders project, and a tour of how a game draws itself: an abstract `ScreenObject`, with `Oval` and `Image` both extending it, and a `Main` that runs a 40-frames-per-second game loop. The spaceship sprite is embedded in the file as Base64 text, so this pastes like everything else.

```java
import java.awt.*;
import java.awt.event.*;
import java.awt.image.BufferedImage;
import java.io.ByteArrayInputStream;
import java.io.File;
import java.io.IOException;
import java.util.ArrayList;
import java.util.Base64;
import javax.imageio.ImageIO;
import javax.swing.*;

class Main extends Canvas {

    private ArrayList<ScreenObject> objects;
    private Image player; 

    public Main() {

      //create game
      objects = new ArrayList<ScreenObject>();
      Oval o = new Oval(180, 100);
      objects.add(o);
      Image i = new Image(300, 0);
      objects.add(i);
      player = i;

      addMouseListener(new MouseListener(){
                    public void mouseClicked(MouseEvent e){
                        System.out.println("CLICKED: " + e.getX() + ", " + e.getY());
                    }
                    public void mouseEntered(MouseEvent arg0) {}
                    public void mouseExited(MouseEvent arg0) {}
                    public void mousePressed(MouseEvent arg0) {}
                    public void mouseReleased(MouseEvent arg0) {}
        });

      addKeyListener(new KeyListener(){
                    public void keyPressed(KeyEvent e){
                        System.out.println("PRESSED: " + e.getKeyCode());
                    }
                    public void keyReleased(KeyEvent e){}
                    public void keyTyped(KeyEvent e){}
        });

    addMouseMotionListener(new MouseMotionListener(){
                    public void mouseMoved(MouseEvent e){
                        System.out.println("MOVED: " + e.getX() + ", " + e.getY());
                    }
                    public void mouseDragged(MouseEvent e){}
      });
    
    }

    public static void main(String[] args) {
        JFrame f = new JFrame("Graphics");
        Main c = new Main();
        c.setSize(400, 400);
        f.add(c);
        f.pack();
        f.setVisible(true);

        c.gameLoop();
    }

    private void gameLoop(){
      //play game
      while(true){

        //move everything
        for(int i=0; i<objects.size(); i++){
          objects.get(i).move();
        }

        //decide any collisions

        //see if player hits any ovals
        for(int i=0; i<objects.size(); i++){
          ScreenObject obj = objects.get(i);
          if(obj instanceof Oval){
            boolean overlap = obj.getRectangle().intersects(player.getRectangle());
            if(overlap) System.out.println("HIT");
          }
        }

        repaint();

        try {
          //pause for 25 millisecs, can adjust if needed
          Thread.sleep(25);
        } catch(InterruptedException e) {
          //empty
        }
      }
    }

    public void paint(Graphics g) {

        //paint every object
        for(int i=0; i<objects.size(); i++){
          objects.get(i).paint(g);
        }
        
    }
}

abstract class ScreenObject {

    abstract Rectangle getRectangle();
    abstract void move();
    abstract void paint(Graphics g);
    
}

class Oval extends ScreenObject {

    private double x, y;

    public Oval(double x, double y){
      this.x = x;
      this.y = y;
    }

    public void move(){
      this.x += 1;
    }

    public Rectangle getRectangle(){
      //the oval is always 30x40
      return new Rectangle((int) x, (int) y, 30, 40);
    }

    public void paint(Graphics g) {
      //always 30x40 and green
      g.setColor(Color.GREEN);
      g.fillOval((int) x, (int) y, 30, 40);
    }
}

class Image extends ScreenObject {

    //The spaceship picture lives right here as text, so this whole exercise stays a single
    //copy and paste. Base64 is just a way of writing raw bytes using ordinary letters and
    //digits - decodeSprite() turns it back into a real PNG.
    private static final String SPACESHIP_PNG =
        "iVBORw0KGgoAAAANSUhEUgAAAEAAAABACAMAAACdt4HsAAAAM1BMVEVohqZbd51HXnw5S2QyQljm3oTerEPh" +
        "gUDmXjzDw8Ofn5+AgIBpaWlYWFg2NjYAAABQHBb2GnITAAAAEXRSTlP/////////////////////ACWtmWIA" +
        "AAHUSURBVHja7dfbkoMgDAZgDB6QyIb3f9pNALdYUVEudjpTu1dAPn7AtVb5xkt9gQ8ASK4GgH6ccz/UALgF" +
        "F/ccIOdwQXcmXAKSoAVYEM/XcAUgWsTHAAEnsJwA6DGA1lpsBWanmoAZnwKk0hJm1dNNgHJgXgGqBmihFUCc" +
        "eQ8CEFtrALLh3hHASX0EUmt9AlJKBC5XfR+E6gQ8lOcSQIF8+gBwgvol4AoogFAfAKxdQgYAJOE+QHqToKOb" +
        "gNYa8gRd190BQMuVJQAGOqgGQAcBXglCfQfVQBJiPQsQ6ysB0pAEWBOketBUBUg518tfuri8g2IEdRAAYoiU" +
        "IE4PpQiqGIB3PYSIt4CcQZhemq8BDtBDnFH3OPNDdcZex63k5vcIBUAGBkGTs+GpbJ0sKzVfATFArM+AVdhF" +
        "UKUdSPVeAP5qE8AnYXcQqnAEfar3QQgBdj3HQDy1NCoHgiB3A5wB6z2QZtkA751lYDtkC/wJx0Aa8ZpCBPv6" +
        "J971l4Gs/w3YDyjtQd7Nj2f+0PGAwjFuus04DMN0MqBwI23qh3GYpsEcDrh6xTHjOA3TaJ6+5hk/TmMb4AUw" +
        "z191jfHn81+/bPMuNALGtP5eaAWM/2/g+6vtE4BfNW7gFd6Et1wAAAAaYWxQaHic7cEBDQAAAMKg/qlvDwcU" +
        "AAAA8G6BYfDiMayM3QAAAABJRU5ErkJggg==";

    private double x, y;
    private BufferedImage i;

    //Use this one for the built-in spaceship
    public Image(double x, double y){
      this.x = x;
      this.y = y;
      this.i = decodeSprite();
    }

    private static BufferedImage decodeSprite(){
      try{
        byte[] bytes = Base64.getDecoder().decode(SPACESHIP_PNG);
        return ImageIO.read(new ByteArrayInputStream(bytes));
      } catch (IOException e){
        System.err.println("Could not decode the built-in sprite: " + e.getMessage());
        return null;
      }
    }

    //Use this one once you upload your own picture into the sandbox
    public Image(double x, double y, String filename){
      this.x = x;
      this.y = y;

      try{
        i = ImageIO.read(new File(filename));
      } catch (IOException e){
        System.err.println("Caught IOException: " +  e.getMessage());
      }
    }

    public void move(){
      this.y += 1;
    }

    public Rectangle getRectangle(){
      //this image is always 64x64
      return new Rectangle((int) x, (int) y, 64, 64);
    }

    public void paint(Graphics g) {

      g.drawImage(i, (int) x, (int) y, null);

    }
}
```

---

## 9. Recursion

### Intro to Recursion

Two finished recursive examples, including the helper-method pattern for `countUp`, then five to write recursively: factorial, summation, reverse a string, reverse a list, and power.

```java
import java.util.ArrayList;

class Main {

  public Main() {
    countdown(10);
    countUp(5);
    //Test all your other functions here.
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

// Basic recursive call function that counts down from x to 0.
  public void countdown(int x){
    if (x < 0) {
      return;
    }
    System.out.println(x);
    countdown(x - 1);
    // How could you write this function iteratively?
  }

// Some recursive functions might need a helper method - like this one - to keep track of another variable.
  public void countUp(int x) {
    countUpHelper(0, x);
  }

  public void countUpHelper(int current, int x) {
    if (current > x) {
      return;
    }
    System.out.println(current);
    countUpHelper(current + 1, x);
  }

  public int factorial(int x) {
    // Returns the factorial of x - do it RECURSIVELY!
    return 0;
  }

  public int summation(int x) {
    // Returns the summation of x - do it RECURSIVELY!
    return 0;
  }

  public String reverse(String s) {
    // Returns the reverse of a string
    return null;
  }

  public ArrayList<Integer> reverseList(ArrayList<Integer> x) {
    // Returns an arraylist in reverse.
    return null;
  }

  public int power(int x, int y) {
    // Returns x ^ y. Do it RECURSIVELY!
    return 0;
  }
}
```

### Harder Problems

Three harder ones: count how many times a digit appears in a number, the nth Fibonacci number, and printing the hailstone sequence recursively.

> **Note:** the worked example said `countDigits(10323, 3)` returns 3, but 10323 has only
> two 3s in it. Changed to 2 so students aren't chasing a wrong answer.

```java
class Main {

  public Main() {
    System.out.println("Hello world!");
  }

  public static void main(String[] args) {
    new Main(); //kicks off the program
  }

  public int countDigits(int number, int digit) {
    // Returns the amount of times digit appears inside number.
    // For example, countDigits(10323, 3) would return 2.
    return 0;
  }

  public int fibonacci(int x) {
    // Returns the x'th number of the fibonacci sequence
    // fibonacci(0) would return 0, fibonacci(1) = 1
    // fibonacci(2) = 1, fibonacci(6) = 8, etc.
    return 0;
  }

  public void hailstone(int x) {
    // Try to print out the hailstone sequence recursively!
  }
}
```

---

## 10. Data Structures

### Linked List

A generic `LinkedList<T>` with a private `Node` inner class, in the same file as `Main`. Every method is a stub — `getLength`, `addFirst`, `addLast`, `removeFirst`, `removeLast`, `get`, `toString`.

> **Note:** the original declared `addFirst()` twice (the second one's comment says
> *adds to the last node*), and the `Node` constructor took an `int` instead of a `T`.
> Both fixed, so the file compiles as-is.

```java
class Main {
  public static void main(String[] args) {
    // Test out your Linked List here!
  }
}

class LinkedList<T> { // T is the type of item, just like in ArrayList<String>
  
  private class Node {
    private T item;
    private Node next;

    private Node(T item, Node next) {
      this.item = item;
      this.next = next;
    }
    //Later on, you can change this even to save the previous node as well!
  }

  private Node firstNode;
  // What other instance variables would you want?

  public LinkedList() {
    firstNode = null;
  }

  public int getLength() {
    return 0; // Change this
  }

  public void addFirst(){
    // Adds to the first node
  }

  public void addLast(){
    // Adds to the last node
  }

  public T removeFirst(){
    // Removes and returns the first node
    return null;
  }

  public T removeLast(){
    // Removes and returns the last node
    return null;
  }

  public T get(int x) {
    // Gets an item at x index
    return null;
  }

  public String toString() {
    return null;
  }

  // What other methods would you want?

}
```

### Binary Tree

A generic `BinaryTree<T>`, same idea one step harder. `add` has to compare items and walk to the right spot; `remove` is the tricky one.

> **Note:** `getLargest()` was missing its `return`, and `contains()` returned `void`
> with no way to answer the question. Both fixed, so the file compiles as-is.

```java
class Main {
  public static void main(String[] args) {
    // Test out your Binary Tree here!
  }
}

class BinaryTree<T> { // T is the type of item, just like in ArrayList<String>
  
  private class Node {
    private T item;
    private Node left, right;

    private Node(T item, Node left, Node right) {
      this.item = item;
      this.left = left;
      this.right = right;
    }
    //Later on, you can change this even to save the previous node as well!
  }

  private Node root;
  // What other instance variables would you want?

  public BinaryTree() {
    this.root = null;
  }

  public int getSize() {
    return 0; // Change this
  }

  public void add(T item) {
    // Adds a node to the tree. Make sure you compare it to other nodes and put it in the right place!
    
  }

  public void remove(T item) {
    // Removes a node with item in it from the tree.
  }

  public boolean contains(T item) {
    // Checks if the tree contains the item.
    return false;
  }

  public T getSmallest() {
    // Returns the smallest item
    return null;
  }

  public T getLargest() {
    // Returns the largest item
    return null;
  }

  public String toString() {
    return null;
  }

  // Add other methods as necessary.

}
```

---

## Adding an exercise to this file

Keep each one to a single `Main.java` with no external files, so a student can paste and run
in under a minute. Extra classes are fine — put them below `Main` in the same block. If an
exercise genuinely needs images, level files, or `acm.jar`, it belongs in the
[main README](README.md) as a zip instead.
