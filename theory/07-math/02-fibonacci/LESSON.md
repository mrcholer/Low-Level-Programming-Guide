# Fibonacci Sequence

The Fibonacci sequence is a simple numeric pattern that appears in math and programming.

## Definition

- `F(0) = 0`
- `F(1) = 1`
- `F(n) = F(n-1) + F(n-2)`

Sequence: `0, 1, 1, 2, 3, 5, 8, 13, ...`

## Iterative implementation

Low-level code prefers loops because recursion uses stack space.

```c
int fib(int n) {
    if (n <= 1) return n;
    int a = 0;
    int b = 1;
    for (int i = 2; i <= n; i++) {
        int next = a + b;
        a = b;
        b = next;
    }
    return b;
}
```

## Recursive implementation

Recursion is easier to write but slower:

```c
int fib(int n) {
    if (n <= 1) return n;
    return fib(n-1) + fib(n-2);
}
```

## Memoization

A better recursive version stores results in an array to avoid repeated work.

## Low-level notes

- Use `int` for small values, but larger `n` may overflow.
- Iteration is usually more efficient than plain recursion.
- This sequence is a good example for loops, arrays, and function calls.
