# Examples for System Headers

## Example 1: write() with <unistd.h>

```c
#include <unistd.h>

int main(void) {
    const char msg[] = "System headers example: write()\n";
    write(1, msg, sizeof(msg) - 1);
    return 0;
}
```

## Example 2: integer output with write()

```c
#include <unistd.h>

void print_num(int n) {
    char buf[16];
    int len = 0;
    if (n == 0) buf[len++] = '0';
    while (n > 0) {
        buf[len++] = '0' + (n % 10);
        n /= 10;
    }
    for (int i = 0; i < len / 2; i++) {
        char t = buf[i];
        buf[i] = buf[len - 1 - i];
        buf[len - 1 - i] = t;
    }
    buf[len++] = '\n';
    write(1, buf, len);
}

int main(void) {
    print_num(42);
    return 0;
}
```

## Example 3: helper function and newline

```c
#include <unistd.h>

void print_line(const char *s) {
    int len = 0;
    while (s[len]) len++;
    write(1, s, len);
    write(1, "\n", 1);
}

int main(void) {
    print_line("System header example");
    return 0;
}
```
