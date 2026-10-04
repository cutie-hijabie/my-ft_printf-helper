# 00 — Big picture

## What it's for

`printf` is a function you've used since your first program, but always as a black box.
ft_printf asks you to open the box. Strip away the details and it does three jobs:

1. **Walk** through the format string from start to end.
2. For each character, **decide**: is this plain text to output as-is, or the start of a
   conversion that needs an argument?
3. For a conversion, **fetch** the next argument, **turn it into text**, **output** it,
   and keep a running **count** of everything written.

Everything else in the project is just those three jobs, repeated for different types.

## Think about

- What's the *simplest possible* version of this function — one that handles zero
  conversions? What does it already need to return?
- What changes in your design when the first conversion is added? Then the second? Which
  parts stay identical and which parts multiply?
- Where does the *knowledge about each conversion* live — inside the loop, or somewhere else?
- What does the subject say you do **not** need to replicate from the real printf (look for
  the word "buffer")?

## A sensible order to build in

You don't have to follow this, but it keeps you from drowning:

1. Plain text only, with the correct return value.
2. `%c` and `%%` — no number logic yet, just the plumbing for fetching arguments.
3. `%s`.
4. `%d` / `%i` — your first real conversion logic.
5. `%u`.
6. `%x` / `%X` — now think about bases in general.
7. `%p` — a twist on what you just built.
8. Only then: Makefile polish, Norm, edge cases, leak checks.

## Go find out

- What does `man 3 printf` call the part of the format that comes after `%`? Learn the
  vocabulary (conversion specifier, flags, etc.) — it makes searching much easier later.

## Man page

`man 3 printf` — read the whole "Conversion specifiers" overview, not only the ones you implement.

## Resources

- [Wikipedia: printf](https://en.wikipedia.org/wiki/Printf) — history and the format string "mini-language" at a glance.
