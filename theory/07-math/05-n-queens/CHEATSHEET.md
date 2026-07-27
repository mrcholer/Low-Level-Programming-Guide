# N-Queens Cheatsheet

Problem:
- place n queens on n x n board
- no queens in the same column or diagonal

Representation:
- `board[row] = col`
- row is current row
- col is chosen column

Backtracking steps:
1. try a column
2. check safety
3. place queen
4. move to next row
5. if stuck, backtrack
