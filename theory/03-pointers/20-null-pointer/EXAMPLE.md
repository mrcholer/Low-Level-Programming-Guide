# Examples for Null Pointer

## Example 1: simple write() output

```c
#include <unistd.h>

int main(void) {
    const char msg[] = "Hello from Null Pointer\n";
    write(1, msg, sizeof(msg) - 1);
    return 0;
}
```

## Example 2: helper functions and write()

```c
#include <unistd.h>

void print_str(const char *s) {
    int len = 0;
    while (s[len]) len++;
    write(1, s, len);
}

void print_line(const char *s) {
    print_str(s);
    write(1, "\n", 1);
}

int main(void) {
    print_line("Example 2 for Null Pointer");
    print_line("This uses helper functions and write().");
    return 0;
}
```

## Example 3: loop and number output

```c
#include <unistd.h>

void print_num(int n) {
    char buf[16];
    int len = 0;
    if (n == 0) {
        buf[len++] = '0';
    } else {
        int temp = n;
        char rev[16];
        int rev_len = 0;
        while (temp > 0) {
            rev[rev_len++] = '0' + (temp % 10);
            temp /= 10;
        }
        while (rev_len > 0) {
            buf[len++] = rev[--rev_len];
        }
    }
    buf[len++] = '\n';
    write(1, buf, len);
}

int main(void) {
    for (int i = 1; i <= 3; i++) {
        print_num(i);
    }
    return 0;
}
```

