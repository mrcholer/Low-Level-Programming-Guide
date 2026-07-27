# Bitwise Cheatsheet

Operators:
- `&`: AND
- `|`: OR
- `^`: XOR
- `~`: NOT
- `<<`: left shift
- `>>`: right shift

Common patterns:
- `flags |= MASK` set bits
- `flags &= ~MASK` clear bits
- `if (value & MASK)` check bits
- `value << n` multiply by 2^n
- `value >> n` divide by 2^n

Examples:
- `1 << 0` = 1
- `1 << 3` = 8
- `0b1010 & 0b1100` = 0b1000
