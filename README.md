# Java Resources

Ready-to-run Java projects for students, packaged for **JuiceMind's free browser IDE**.

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
with `java -version` in the sandbox's **Shell** tool.

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
