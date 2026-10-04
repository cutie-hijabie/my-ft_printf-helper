# 06 — Common pitfalls (as questions)

Each of these is a place where lots of people lose points. They're phrased as questions on
purpose — find the answer by testing against the real `printf`.

**Numbers**

- What happens when you negate the smallest possible `int`? Why is that a problem, and what
  could you do about it?
- Digits come out of a division loop in one order, but you need to print them in the
  opposite order. What are your options?
- What does your function print for zero? Is that a special case or does it fall out
  naturally?
- If you read an argument as the wrong signedness, what does a negative number turn into
  with `%u` or `%x`? Try it with the real printf.

**Strings and characters**

- What does your system's `printf` do with `%s` when given a null pointer? Is that
  behavior *required* by the C standard, or just what this particular library does?
- What does `%c` do with a zero value, and does your return value agree?
- What's the length of an empty string, and does your code handle it without special cases?

**Pointers**

- What type could hold *any* pointer value without losing bits? Is `int` big enough?
- What does the real `printf` print for a null pointer with `%p`? Does it print the same
  on every operating system? (If you work on both Linux and macOS, try both.)

**Plumbing**

- After a handler runs, does your loop move past the right number of characters of the format?
- Are you accidentally consuming an argument for `%%`? (It shouldn't need one.)
- Does every code path return a sensible count, including the error ones?
- Did you introduce a memory allocation for number-to-text? Is every one freed on every path?
