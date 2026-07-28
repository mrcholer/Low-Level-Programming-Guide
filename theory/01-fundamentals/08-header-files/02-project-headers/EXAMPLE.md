# Examples for Project Headers

## Example 1: header declaration with write()

```c
#include <unistd.h>

int main(void) {
    const char msg[] = "Project header example using write()\n";
    write(1, msg, sizeof(msg) - 1);
    return 0;
}
```

## Example 2: helper function in a project module

```c
#include <unistd.h>

void print_message(void) {
    const char msg[] = "Header-based helper\n";
    write(1, msg, sizeof(msg) - 1);
}

int main(void) {
    print_message();
    return 0;
}
```

## Example 3: declaration and use in one file

```c
#include <unistd.h>

void print_hello(void);

int main(void) {
    print_hello();
    return 0;
}

void print_hello(void) {
    const char msg[] = "Hello from project header example\n";
    write(1, msg, sizeof(msg) - 1);
}
```
