# Prime Numbers Cheatsheet

Prime check rules:
- `n <= 1` -> not prime
- `n == 2` -> prime
- even numbers > 2 -> not prime
- test odd divisors up to `sqrt(n)`

Performance:
- skip even numbers after 2
- stop at the square root
- use `int limit = (int) sqrt((double)n);`
