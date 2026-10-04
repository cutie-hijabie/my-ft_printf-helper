# 02 — Parsing the format string

## What it's for

The format string is a tiny language: most characters mean "print me", but `%` means
"something special follows." Your function is an interpreter for that language.

## Think about

- What's the basic loop? What are you tracking as you move through the string?
- When you hit `%`, how do you know *which* conversion it is? What do you look at next?
- After handling a conversion, **where does the loop continue from**? Easy to get off by one.
- What if the string ends right after a `%`? What does the real printf do — and does the
  subject require you to care? (Test it, and read the man page's wording on undefined behavior.)
- What if `%` is followed by a character that isn't one of your conversions?
- How will you route to the right handler? Think about the options — a chain of
  conditions, a `switch`, a lookup table. What does each cost you in lines, given the Norm's
  25-line limit per function?
- Should the loop itself know how to print an integer? Or should it only know *who to ask*?

## Go find out

- How do functions in the standard library usually communicate "I printed N characters" back to
  a caller that's adding them up? (See [03 — Return value](03-return-value.md).)
- What are the pros and cons of writing one character at a time versus building up
  chunks? The subject doesn't force an answer — but evaluators may ask you to justify yours.

## Man page

`man 3 printf` — especially the description of how a format string is structured.

## Resources

- [Wikipedia: printf format string](https://en.wikipedia.org/wiki/Printf_format_string)
