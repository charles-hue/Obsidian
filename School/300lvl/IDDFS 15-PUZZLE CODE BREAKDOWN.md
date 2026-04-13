 
## 1. Printing the Board (`print_board`)

**What it does:** Draws the 4×4 grid on screen.

**Why:** You need to see the puzzle before solving and after each move. It's the visual feedback that lets you follow along with the computer's thinking.

---

## 2. Checking Solvability (`is_solvable`)

**What it does:** Runs a quick math test to tell if the scrambled puzzle can actually be solved.

### What's an *inversion*?

Imagine you take all the numbered tiles and lay them in a single line, **ignoring the blank space**. Now read from left to right. An inversion happens whenever a **larger number comes *before* a smaller number**.

Think of it like a line of people arranged by height. If a tall person stands in front of a shorter person, that's one "inversion" of the proper short‑to‑tall order.

#### Example (using a smaller 3×2 puzzle):
```
Tiles in reading order:  2  →  1  →  3

Pairs to check:
  (2, 1)  →  2 > 1?  Yes → Inversion!  (count = 1)
  (2, 3)  →  2 > 3?  No
  (1, 3)  →  1 > 3?  No

Total inversions = 1
```

If the tiles were `[3, 1, 2]`:
- (3,1) → inversion
- (3,2) → inversion
- (1,2) → no inversion  
Total = 2.

### What's the "row of the blank"?

We number rows starting from the **bottom** with 0:

```
Row from top    Row from bottom
   ┌──┬──┬──┬──┐   ┌──┬──┬──┬──┐
 3 │  │  │  │  │  0 │  │  │  │  │   ← Bottom row
   ├──┼──┼──┼──┤   ├──┼──┼──┼──┤
 2 │  │  │  │  │  1 │  │  │  │  │
   ├──┼──┼──┼──┤   ├──┼──┼──┼──┤
 1 │  │  │  │  │  2 │  │  │  │  │
   ├──┼──┼──┼──┤   ├──┼──┼──┼──┤
 0 │  │  │  │  │  3 │  │  │  │  │   ← Top row
   └──┴──┴──┴──┘   └──┴──┴──┴──┘
```

The code finds the blank's row from the top, then converts it: `blank_row_from_bottom = 3 - row_from_top`. For example, if the blank is in the **second row from the top** (row index 2), its bottom‑row index is `3 - 2 = 1`.

### The Magic Formula
```
(inversions + blank_row_from_bottom) is EVEN  →  solvable
(inversions + blank_row_from_bottom) is ODD   →  impossible
```

**Why this works:** Every legal slide changes both the inversion count and the blank's row in a coordinated way. Their sum's even/odd nature never changes. The solved puzzle has 0 inversions and the blank in the bottom row (row 0 from bottom) → sum = 0 (even). So if your starting sum is odd, you'll **never** reach the goal. It's like a built‑in safety lock.

---

## 3. Generating Moves (`get_successors`)

**What it does:** Looks at the empty spot (0) and figures out which neighbouring tiles can slide into it.

### Only Four Directions — No Diagonals!

The blank can move **up, down, left, or right**. Diagonal jumps are not allowed (you can't slide a corner tile directly into the hole).

#### Visual of Valid Moves from the Middle
```
    ┌────┬────┬────┬────┐
    │    │    │ ↑  │    │   ← UP
    ├────┼────┼────┼────┤
    │    │ ←  │ 0  │ →  │   ← LEFT / RIGHT
    ├────┼────┼────┼────┤
    │    │    │ ↓  │    │   ← DOWN
    ├────┼────┼────┼────┤
    │    │    │    │    │
    └────┴────┴────┴────┘
```

Diagonal squares (✗) are off‑limits:
```
    ┌────┬────┬────┬────┐
    │ ✗  │    │ ✗  │    │
    ├────┼────┼────┼────┤
    │    │ 0  │    │    │
    ├────┼────┼────┼────┤
    │ ✗  │    │ ✗  │    │
    ├────┼────┼────┼────┤
    │    │    │    │    │
    └────┴────┴────┴────┘
```

### The "Stay Inside the Grid" Check

When the blank is on an edge or corner, some directions point outside the 4×4 board. The code checks `0 <= r < 4 and 0 <= c < 4` to prevent trying to slide a tile from outside the puzzle.

#### Example: Blank in Top‑Left Corner
```
    ┌────┬────┬────┬────┐
    │ 0  │ →  │    │    │   ← RIGHT is valid
    ├────┼────┼────┼────┤
    │ ↓  │    │    │    │   ← DOWN is valid
    ├────┼────┼────┼────┤
    │    │    │    │    │
    ├────┼────┼────┼────┤
    │    │    │    │    │
    └────┴────┴────┴────┘

    UP   → row -1 = -1  (invalid)
    LEFT → col -1 = -1  (invalid)
    DOWN → row +1 = 1   (valid)
    RIGHT→ col +1 = 1   (valid)
```

For each valid direction, the function creates a new board where the blank and the chosen tile have swapped places. It returns all those new boards so the solver can explore them next.

---

## 4. Depth‑Limited Search (`dls`)

**What it does:** This is the **explorer**. It tries one move, then another, then another… but it stops after a set number of moves (the "limit").

**Why:** Imagine telling someone, "Find the exit in this maze, but you're only allowed **10 steps**. If you don't find it by step 10, come back and tell me you hit the limit."  
This stops the computer from wandering off forever. It also keeps a tiny sticky note of where it has been **on this current try** so it doesn't slide the same tile back and forth endlessly.

---

## 5. Iterative Deepening Loop (`iddfs`)

**What it does:** It tells the explorer (from step 4):  
"Okay, try with a limit of **1 move**. Didn't work? Now try with **2 moves**. Still no? Try **3 moves**…"

**Why:**
- **Memory:** The explorer only needs to remember the one path it's on right now—no giant map of the whole puzzle.
- **Shortest Path:** Because we check all 1‑move solutions first, then all 2‑move solutions, the **first time we find the goal, it's the shortest possible route**. We never settle for a long, rambling solution.

This is the core strategy of the whole project. It's like a manager giving the explorer a strict budget and slowly raising it until the job is done.

---

## 6. Replaying the Solution (`replay_solution`)

**What it does:** Once the computer finds the list of moves ("Up, Left, Down…"), this part shows you the puzzle **after each move** one by one.

**Why:** Trust but verify. You watch the solution unfold to be sure it actually solves the puzzle and isn't just claiming victory.

---

## 7. Main Program (`if __name__ == "__main__":`)

**What it does:** This is the **conductor**. It:
- Sets up the starting scrambled puzzle.
- Runs the solvability check.
- Launches the "Try 1 step, try 2 steps…" process.
- Shows you the final results.

**Why:** It ties all the separate tools together into one smooth, click‑and‑run operation.

---

### The Big‑Picture Analogy

Think of finding a specific room in a massive hotel:

- **BFS:** You'd station a person in every single hallway on every floor at once. You'd find the room fast, but you'd need a huge staff. *(Too much memory)*
- **DFS:** You'd send one person down the stairs to the basement and let them keep walking until they hit a wall. They might get lost for hours. *(Not efficient/short)*
- **IDDFS (This Code):** You give the person a walkie‑talkie and say, *"Go 10 feet. Stop. Come back. Now go 20 feet. Stop. Come back."* They repeat the first 10 feet over and over, but it's the only way to search a huge building with just one person and a small notepad. And when they finally find the room, you know they took the **most direct route possible** from the front door.

That's exactly what your code is doing.