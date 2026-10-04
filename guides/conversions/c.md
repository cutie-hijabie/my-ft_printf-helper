# %c

## What it's for

Printing a single character.

## Think about

- This is the simplest conversion — which makes it the right one to use to get your
  argument-fetching right before anything else.
- The argument arrives through `...`. Does it arrive as the type you'd expect?
- How many characters does this always output? So what does it add to your count?
- What if the character is the zero byte? How does that differ from every string-based
  approach you've used so far?

## Go find out

- What type should you request from the argument list when the caller passed a `char`?
  Why? (Search: *default argument promotions*.)

## Man page

`man 3 printf` — the `c` conversion; `man 2 write`.

## Resources

- [cppreference: implicit conversions](https://en.cppreference.com/w/c/language/conversion)
