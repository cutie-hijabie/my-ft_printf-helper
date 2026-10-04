# %x and %X

## What it's for

Printing an unsigned integer in **hexadecimal**: lowercase letters for `%x`, uppercase for `%X`.

## Think about

- You already turned a number into decimal digits. What is the *only* thing that changes
  when the base is 16 instead of 10?
- How would you get from "a digit's value" to "the character that represents it"? Can the
  answer be *data* instead of a long chain of conditions?
- `%x` and `%X` differ in one tiny way. Do you really need two separate functions?
- What's the output for zero?
- No `0x` prefix here. Compare with what the real printf does for `%p`.
- Could a single helper serve `%u`, `%x`, `%X` **and** `%p`? What would its inputs be?

## Go find out

- How do other bases (binary, octal, hex) relate to each other? Why do programmers like hex?
- What's the largest 32-bit unsigned value written in hex? Test yours against it.

## Man page

`man 3 printf` — the `x` and `X` conversions.

## Resources

- [Wikipedia: Hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal)
- [Wikipedia: Positional notation](https://en.wikipedia.org/wiki/Positional_notation)
