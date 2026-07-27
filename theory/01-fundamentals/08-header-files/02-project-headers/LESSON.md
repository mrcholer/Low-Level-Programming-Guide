# Project Headers

Project headers are headers that you create for your own code.

## Purpose

- declare your functions and types
- share declarations between `.c` files
- keep the interface separate from the implementation

## How to write one

A header file typically contains declarations and include guards:

```c
#ifndef MYHEADER_H
# define MYHEADER_H

void my_function(void);

#endif
```

## How to use it

In your source file:

```c
#include "myheader.h"
```

This tells the compiler to look in the current directory or project include paths.

## Example workflow

1. write `myheader.h` with declarations.
2. write `my_function.c` with the function body.
3. write `main.c` that includes the header and calls the function.
4. compile both `.c` files and link them.
