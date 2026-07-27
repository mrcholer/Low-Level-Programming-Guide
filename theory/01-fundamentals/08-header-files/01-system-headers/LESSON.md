# System Headers

System headers are provided by the operating system and standard library.

## What they do

A system header declares functions and symbols that are built into the platform. The compiler uses the header to check function calls, but the actual code is provided by the system libraries.

## Example headers

- `<unistd.h>` — declares `write()`, `read()`, and other low-level system calls.
- `<stdlib.h>` — declares `malloc()`, `free()`, and exit functions.
- `<stdio.h>` — declares `printf()`, `fopen()`, and other standard I/O functions.

## How to include

Use angle brackets for system headers:

```c
#include <unistd.h>
```

This tells the compiler to search the system include paths.

## Why this matters in low-level code

System headers allow your program to call operating system functions without knowing their implementation details.

You can use `write()` from `<unistd.h>` directly to send bytes to standard output.
