# Square Root in Low-Level Code

The square root is useful for geometry, optimizations, and prime testing.

## Floating-point approach

Use `sqrt()` from `math.h`:

```c
#include <math.h>

double r = sqrt(16.0);
```

## Integer approximation

A low-level method computes the integer floor of the square root.

```c
int int_sqrt(int n) {
    int guess = 0;
    while ((guess + 1) * (guess + 1) <= n) {
        guess++;
    }
    return guess;
}
```

## Binary search method

Binary search is faster:

```c
int int_sqrt(int n) {
    int low = 0;
    int high = n;
    int result = 0;
    while (low <= high) {
        int mid = (low + high) / 2;
        if (mid * mid <= n) {
            result = mid;
            low = mid + 1;
        } else {
            high = mid - 1;
        }
    }
    return result;
}
```

## Why this matters

- used in prime checking up to `sqrt(n)`
- used in distance, area, and geometry calculations
- useful for performance when avoiding floating-point math
