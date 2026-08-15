# Java Resources

Ready-to-run Java projects for students, packaged for **JuiceMind's free browser IDE**.

> **Just looking for short practice problems?** The single-file exercises — printing, loops,
> recursion, data structures — live in **[EXERCISES.md](EXERCISES.md)**. Those are copy-and-paste,
> no zip needed. Everything below is the bigger graphical projects.

Nothing to install — no JDK, no Eclipse, no downloads beyond a single `.zip`. Works on
Chromebooks, school laptops, and tablets. Each project is a complete, working starting
point that students are meant to extend.

---

## How to use a project

**1. Download the project `.zip`** from the table below.

**2. Go to [play.juicemind.com/dashboard/code-sandbox](https://play.juicemind.com/dashboard/code-sandbox)**
and sign in (a free account is fine).

**3. Click `+ Create New Sandbox`.**
   - Give it a name (for example, `Tower Defense`)
   - Under **Choose Programming Language**, select **Java**
   - Click **🚀 Create Sandbox**

**4. Open the file explorer** — the folder icon in the top-left corner.

**5. Click the `⋮` button** next to the word **Files**, then choose **Upload zip**.

**6. Pick the `.zip` you downloaded**, then click **Override Project Files** when asked.
   (This replaces the "Hello world" starter, which is why you want a *fresh* sandbox.)

**7. Press the blue ▶ Run button.**

The game window appears in the display panel on the right. If it's cut off, collapse the
file explorer, or use the **Auto-resize / Fixed size** toggle in the bottom-right corner.

---

## Projects

| Project | Download | Try it live | What's in it |
|---|---|---|---|
| **Tower Defense** | [TowerDefense.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/TowerDefense.zip) | [Open sandbox](https://play.juicemind.com/sandbox/OQYed3EQ01DHKRXrBE3c) | Tile-based map loaded from a text file, animated enemy that walks the path, a tower that fires bullets. Uses the ACM graphics library. |
| **Tic Tac Toe** | [TicTacToe.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/TicTacToe.zip) | [Open sandbox](https://play.juicemind.com/sandbox/x3atUToiPU0XMvJU8ppw) | Play X against a computer opponent that blocks you and takes a win when it sees one. Plain Java Swing — no extra library. |
| **Space Invaders** — starter | [SpaceInvaders-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/SpaceInvaders-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/RCh6IeYAa8231sjDWhfX) | Your ship, one enemy, click to shoot. Deliberately unfinished: enemies fly off-screen, no rows, no enemy fire. Marked `IMPROVE THIS` in the code. Uses ACM. |
| **Space Invaders** — finished | [SpaceInvaders-Finished.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/SpaceInvaders-Finished.zip) | [Open sandbox](https://play.juicemind.com/sandbox/LMbmM1DIR3dKHNeMu1SK) | The completed game: rows of bouncing enemies, a mothership, bunkers, enemy fire, multiple bullet types, and Game Over. Uses ACM. |
| **Game of Life** — starter | [GameOfLife-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/GameOfLife-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/DBOpwYPkOUd8i0KFn6Hk) | Conway's Game of Life with the rules left out. Click cells to draw a starting pattern, then press Start. `doStep` and `countNeighbors` are marked `YOUR CODE HERE`. Plain Java Swing. |
| **Game of Life** — finished | [GameOfLife-Finished.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/GameOfLife-Finished.zip) | [Open sandbox](https://play.juicemind.com/sandbox/EnHOJBoUW8OFEO5TNghP) | The completed simulation: draw a pattern, press Start, and watch it evolve. Gliders travel. Neighbour counting wraps around the edges. Plain Java Swing. |
| **Snake** — starter | [Snake-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Snake-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/6ztBiLBqtMPMZ8nyaFxN) | Classic Snake with the movement left out. The board, apple and score all work; `moveSnakeCheckApple`, `checkBounds`, `checkOverlap` and `snakeToGrid` are marked `YOUR CODE HERE`. Plain Java Swing. |
| **Snake** — finished | [Snake-Finished.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Snake-Finished.zip) | [Open sandbox](https://play.juicemind.com/sandbox/xj1salIK3yBkS3CO1Lwk) | The completed game: steer with the arrow keys, eat apples to grow and score, and it's Game Over if you hit a wall or your own tail. Plain Java Swing. |
| **Sudoku Solver** — starter | [Sudoku-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Sudoku-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/vSgWw9FlTLBlX72G5hOc) | A constraint-solver skeleton. The puzzle loads from `boards/board1.txt` and every unsolved square draws the digits still possible for it. `isSolved()` and `onePass()` are marked *complete this*. Uses ACM. |
| **Pacman** — starter | [Pacman-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Pacman-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/gq14MS1Az0r5i7Wny5zx) | The maze, the dots and Pac-Man himself all draw correctly, but he can't move yet. `nextImage()`, `move()` and the turning logic are marked `TO DO`. No ghosts. Uses ACM. |
| **Pacman** — finished | [Pacman-Finished.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Pacman-Finished.zip) | [Open sandbox](https://play.juicemind.com/sandbox/vA4TbpjcnLjI9mD6Bo80) | The full game: click to start, arrow keys to steer, four ghosts (two wander, two hunt you), power pellets that turn them blue, and a dot counter. Uses ACM. |
| **War** | [War.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/War.zip) | [Open sandbox](https://play.juicemind.com/sandbox/tO9XTp9F4Ysz63jnPQeu) | The card game. Press **Flip Card** to play a round; a tie starts a war with three face-down cards each. Real card artwork, a shuffled `Deck`, and separate `Pile` and `Player` classes. Plain Java Swing. |
| **Graphics Programs** | [GraphicsPrograms.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/GraphicsPrograms.zip) | [Open sandbox](https://play.juicemind.com/sandbox/t4uX4eqvdomBpOCYQPEt) | Eleven small ACM drawing programs in one sandbox — seven finished examples (robot face, checkerboard, pyramid, recursive squares, bouncing ball, random art) and four with work left to do (Target, Row of Bricks, Random Art, Animation Pattern Matching). `Main.java` is a switchboard: uncomment the one you want. Includes a `Graphics commands.txt` cheat sheet. |
| **Breakout** — starter | [Breakout-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Breakout-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/yEGECZ2GRnD88bOmfg2H) | The classic brick-breaker, with every constant defined (paddle size, brick rows, ball radius) and `run()` empty. Build the bricks, the paddle, and the bouncing ball yourself. Uses ACM. |
| **Breakout** — finished | [Breakout-Finished.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Breakout-Finished.zip) | [Open sandbox](https://play.juicemind.com/sandbox/J3CTOFnBVXwkCPqN2Fjj) | The completed game: eight rows of coloured bricks, a mouse-controlled paddle, three lives, a score, and a bounce sound. Uses ACM. |
| **UFO Game** | [UfoGame.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/UfoGame.zip) | [Open sandbox](https://play.juicemind.com/sandbox/9gBGcdZ1ztmhKtfRD8Sg) | A small finished arcade game — shoot the UFO before it lands. A compact example of animation, mouse input and collision detection in about 150 lines. Uses ACM. |
| **Yahtzee** — starter | [Yahtzee-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Yahtzee-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/VSr3jHrMqSK9BXGwzdJr) | The dice game. It asks how many players and their names, then draws the full scorecard and five dice — `playGame()` is where you take over: roll, let the player re-roll, and score each category. Uses ACM plus `yahtzeelib.jar` for the board. |
| **Memory** | [Memory.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Memory.zip) | [Open sandbox](https://play.juicemind.com/sandbox/pt4OHx101zlG0QOUPe1x) | Pick a theme, then match 12 pairs on a 6x4 grid of face-down cards. A working game with room to grow: there's no score, no move counter, and nothing happens when you find the last pair. Uses ACM. |
| **Checkers** — starter | [Checkers-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Checkers-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/yI4kBlB2rbvZFZpYd28j) | The board draws itself and clicking a dark square highlights it in yellow — that's all. Moving pieces, taking turns and jumping are yours to write. Plain Java Swing, no extra library. |
| **Checkers** — finished | [Checkers-Finished.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Checkers-Finished.zip) | [Open sandbox](https://play.juicemind.com/sandbox/AOfUpnpcIHyuEv5sgarB) | Two-player checkers: click a piece then a square to move it, diagonal jumps capture, and a label tracks whose turn it is. No kings and no multi-jumps yet — good places to keep going. Plain Java Swing. |
| **Hangman** — starter | [Hangman-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/Hangman-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/8jrXbSnDPIefrBJoewW3) | The classic CS106A assignment, and the emptiest starter here — `run()`, `reset()`, `displayWord()` and `noteIncorrectGuess()` are all *You fill this in*. It runs to a blank console, which is correct. The scaffold measurements and a 100k-word lexicon are provided. Uses ACM. |
| **ImageShop** — starter | [ImageShop-Starter.zip](https://github.com/BreakoutMentors/JavaResources/raw/main/ImageShop-Starter.zip) | [Open sandbox](https://play.juicemind.com/sandbox/Dwq4Vkz3Dbk6jEjyo49P) | A working photo editor with every filter missing. The whole interface — load, save, and twelve buttons — is built; `ImageShopAlgorithms.java` has eight `// TODO` methods: rotate, flip, negative, green screen, blur, crop and equalize. Eleven sample images included. Uses ACM plus Stanford's `spl.jar`. |

> **Note on the "Try it live" links:** these open a JuiceMind sandbox that **anyone can edit.**
> **Do not make changes!** To get your own editable copy, follow the upload steps above.

---

## Things to know before you edit

**The main class must be called `Main`.** JuiceMind always runs `Main.java`, no matter what
else is in the project. Where a project's "real" main class has a different name, you'll find
a small `Main.java` that just launches it:

```java
public class Main {
    public static void main(String[] args) {
        new TowerDefense().start(args);
    }
}
```

Leave that file alone and edit the real class instead.

**`acm.jar` is already included** where a project needs it. This is Stanford's ACM graphics
library (`GraphicsProgram`, `GImage`, `GRect`, `GOval`, and friends). JuiceMind automatically
puts any `.jar` in the project folder on the classpath — no configuration required.

**Folders matter.** Some projects load images and level files by relative path, like
`src/resources/grass.png`. That's why these are distributed as zips: uploading files one at a
time can't recreate folders, and the project won't find its artwork.

**JuiceMind currently runs Java 17.** The ACM library is built on the old Applet API, which
was removed in Java 24 — so if JuiceMind upgrades that far in the future, ACM-based projects
will need replacing. Java-only projects are unaffected. You can check the version yourself
with `java -version` in the sandbox's **Shell** tool. Pacman and Breakout also use
`java.applet.AudioClip` for their sound effects, so they print deprecation warnings when they
compile — those are normal and the games run fine.

---

## Adding a new project to this repo

Package the zip so that it unpacks like this:

```
Main.java              <- launcher, or the real main class named Main
YourClass.java         <- all .java files at the TOP level
OtherClass.java
acm.jar                <- only if the project uses ACM
src/resources/...      <- keep any folders the code references by path
src/levels/...
```

Java files go at the top level because JuiceMind compiles and runs from the project root.
Don't include Eclipse's `bin/`, `.classpath`, `.project`, `.settings`, or `.DS_Store` —
they're just noise, and a stray duplicate `.java` under `bin/` will break the build with a
`duplicate class` error.

**If a demo sandbox gets edited.** The "Try it live" sandboxes are publicly editable, so
anyone can change what the next visitor sees. If one gets scribbled on, create a fresh
sandbox, upload that project's `.zip` again, and swap the link in the table above. The zips
in this repo are the source of truth — the sandboxes are only previews of them.
