# N-Queens and Puzzle Algorithms

The N-Queens problem asks: place `n` queens on an `n x n` chessboard so that none can attack another.

## Board representation

Use an array to store the column of the queen in each row:

```c
int board[10];
```

Each index is a row and the value is the column.

## Safety checks

A queen attacks another if they share:

- the same column
- the same diagonal

Check diagonals with row and column differences.

```c
int row_diff = row - prev;
if (prev_col == col - row_diff) return 0;
if (prev_col == col + row_diff) return 0;
```

## Backtracking

Try each column in the current row. If the position is safe, place the queen and move to the next row. If placement fails later, undo it and try the next column.

## Hard coding puzzles

Ten Queens is a harder version of the same problem with `n = 10`. The algorithm is the same; only the board is larger.

## Example structure

The low-level solution uses:

- plain arrays for board state
- loops for row and column choices
- recursion for backtracking
- boolean-like checks with integers

This problem is good practice for writing clear logic and controlling program flow in C.
