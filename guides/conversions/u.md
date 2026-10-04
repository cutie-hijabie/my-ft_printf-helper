# %u

## What it's for

Printing an **unsigned** integer in decimal.

## Think about

- What's different about unsigned numbers compared to `%d`? What *disappears* from your
  problem — and what new problem is hiding behind it?
- What type do you ask the argument list for? What happens if you ask for the wrong one?
- Could this and `%d` share anything? What would they have to agree on?
- What's the largest value, and does the arithmetic in your digit loop stay inside the type?

## Go find out

- Pass a negative `int` to the real `printf` with `%u`. What comes out, and why? What does
  that tell you about how the same bits can mean different numbers?

## Man page

`man 3 printf` — the `u` conversion.

## Resources

- [Wikipedia: Signed number representations](https://en.wikipedia.org/wiki/Signed_number_representations)
