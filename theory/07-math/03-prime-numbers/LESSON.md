# Prime Numbers

Prime numbers are integers greater than 1 with no divisors besides 1 and themselves.

## Simple test

- if `n <= 1`, it is not prime
- if `n == 2`, it is prime
- if `n % 2 == 0`, it is not prime

## Improved test

Only test odd divisors from 3 up to `sqrt(n)`.

```c
#include <math.h>

int is_prime(int n) {
    if (n <= 1) return 0;
    if (n == 2) return 1;
    if (n % 2 == 0) return 0;
    int limit = (int)sqrt((double)n);
    for (int i = 3; i <= limit; i += 2) {
        if (n % i == 0) return 0;
    }
    return 1;
}
```

## Why this matters

- prime checking uses division and modulus.
- efficient loops are critical for larger values.
- this is a good exercise in integer math and conditionals.

## Low-level note

- `%` can be slower than basic arithmetic, so reduce the number of checks.
- `sqrt()` uses floating-point math; cast carefully.
- For larger ranges, use a sieve instead of repeated checks.
