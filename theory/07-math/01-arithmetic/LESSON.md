# Arithmetic in Low-Level Programming

Basic arithmetic is the foundation of most low-level algorithms.

## Operators and meanings

- `+` addition: add two values.
- `-` subtraction: subtract one value from another.
- `*` multiplication: multiply values.
- `/` division: divide values.
- `%` modulus: remainder after division.

## How low-level code uses arithmetic

### Memory and size computation

When allocating memory, use multiplication to compute total bytes:

```c
int count = 5;
int bytes = count * sizeof(int);
```

### Array and pointer arithmetic

Indexing an array uses addition:

```c
int values[5];
int index = 2;
values[index + 1] = 10;
```

Pointer arithmetic also uses addition and subtraction:

```c
int *p = values;
p = p + 2; // move 2 integers forward
```

### Loop control

Use `+` and `-` to change loop counters:

```c
for (int i = 0; i < 10; i = i + 1) {
    // do work
}
```

### Integer division and modulus

Integer division drops the fractional part:

```c
int x = 7 / 2; // x is 3
int r = 7 % 2; // r is 1
```

Modulus is useful for cycles and parity checks:

```c
if (i % 2 == 0) {
    // even index
}
```

## Hidden details

- `a + b * c` multiplies before adding.
- Avoid overflow when values are large.
- Use unsigned arithmetic for bit patterns and sizes.
