# %p

## What it's for

Printing the **address** held by a pointer, in hexadecimal, in a recognizable format.

## Think about

- A pointer isn't an integer — but it is a number in memory. How can you treat its
  bits as a number you can convert to text?
- How big is a pointer on your machine? Is it the same size as an `int`? What does that
  imply for the type you choose?
- Look at what the real `printf` outputs for a normal pointer. What appears *before* the digits?
- Which of your other conversions does this resemble? Can you reuse something you already
  wrote — and what would you need to add?
- What about the null pointer? Test it on your machine and think about whether the
  behavior is the same everywhere.

## Go find out

- Which standard unsigned integer type exists specifically to hold a pointer's value
  without losing bits? (Look at the integer types in `<stdint.h>`.)
- How does the null-pointer output differ between Linux and macOS? Which one will your
  evaluator's machine use?

## Man page

`man 3 printf` — the `p` conversion.

## Resources

- [cppreference: fixed-width integer types](https://en.cppreference.com/w/c/types/integer)
- [Wikipedia: Hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal)
