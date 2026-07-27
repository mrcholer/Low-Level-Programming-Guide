# Header Files

Header files are a central part of C programming. They tell the compiler what exists before the code is compiled.

## Two kinds of headers

- System headers: provided by the operating system or language runtime, included with `<...>`.
- Project headers: written by you, included with `"..."`.

## System headers

System headers declare functions and macros provided by the system. Example:

```c
#include <unistd.h>
```

This header declares the `write()` function and other system call wrappers.

## Project headers

Project headers declare your own functions and types. Example:

```c
#include "myheader.h"
```

A project header usually includes include guards:

```c
#ifndef MYHEADER_H
# define MYHEADER_H

int my_function(int x);

#endif
```

## Why two parts?

- System headers are not stored in your project folder.
- Project headers are part of your source tree and are a contract between `.c` files.
- Understanding both makes it easier to read code from libraries and write your own reusable modules.
