# Bitwise Operators

Bitwise operators work on the individual bits inside integers. They are a key part of low-level programming because they let you manipulate flags and binary data efficiently.

Common bitwise operators in C:

- `&` bitwise AND: keeps bits that are 1 in both values.
- `|` bitwise OR: sets bits that are 1 in either value.
- `^` bitwise XOR: sets bits that are 1 in exactly one value.
- `~` bitwise NOT: flips every bit.
- `<<` left shift: moves bits left, multiplying by powers of two.
- `>>` right shift: moves bits right, dividing by powers of two.

## Why bitwise matters

- used for flags and mode settings
- used for packing multiple values into one integer
- used for fast arithmetic when working with powers of two
- used for low-level hardware control and binary protocols

## Examples

Set and clear individual flags in a value:

```c
const int FLAG_A = 1 << 0; // 0001
const int FLAG_B = 1 << 1; // 0010
int flags = 0;
flags |= FLAG_A; // set A
flags &= ~FLAG_B; // clear B
```

Compute a mask and test a bit:

```c
if (flags & FLAG_A) {
    // feature A is enabled
}
```

Shift operations:

```c
int value = 1 << 4; // 16
int half = value >> 1; // 8
```

## Low-level notes

- Use bitwise operators for compact state storage.
- `<<` and `>>` are faster than general multiplication or division by powers of two.
- Be careful with signed values when shifting right; use unsigned values for predictable behavior.
