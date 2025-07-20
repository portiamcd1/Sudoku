# Sudoku

<img width="800" height="361" alt="sudoku" src="https://github.com/user-attachments/assets/fad49175-32ac-46cb-8c53-9e36a5c8bd52" />

## Instructions

For this assignment, I had to write an agent that can solve sudoku puzzle with difficulties ranging from very easy to hard.

To solve the puzzle, the objective was to fill the empty cells of the 9x9 grid as shown in the picture above such that the numbers 1 to 9 appear exactly once in each row, column, and 3x3 block of the grid.

Some puzzles were unsolveable and in that instance the output had to return a 9x9 grid containing only -1 in each cell.

## Solution

- Arc Consistency 3 (AC-3) algorithm
- Backtracking search
- Minimum Remaining Values (MRV) heuristic

This Sudoku solver uses a combination of the AC-3 (Arc Consistency 3) algorithm and backtracking search, enhanced by the Minimum Remaining Values (MRV) heuristic, to solve standard 9x9 Sudoku puzzles. The solver first constructs domains for each empty cell, representing the possible valid values based on current constraints from the row, column, and 3×3 box. AC-3 is then applied to enforce local consistency by removing invalid values from these domains. If the puzzle is not yet fully solved, the backtracking algorithm recursively attempts assignments for the most constrained cells (using MRV), maintaining consistency by reapplying AC-3 after each choice. If a contradiction arises, the algorithm backtracks to explore other options. This approach allows the solver to efficiently handle puzzles of easy to medium difficulty, ensuring that solutions respect all Sudoku rules.
