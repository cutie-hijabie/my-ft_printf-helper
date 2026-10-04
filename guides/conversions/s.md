# %s

## What it's for

Printing a null-terminated string.

## Think about

- How do you know where a string ends? Do you need a helper from your Libft for that — and
  are you allowed to use it? (Check the subject.)
- Output one character at a time, or all at once? What does each approach cost?
- What's the count if the string is empty?
- What if the caller passes a pointer that points to nothing? Run the real `printf` with
  that and see what it does. Then decide how yours should behave.

## Go find out

- Is the behavior you observed for a null string *guaranteed* by the C standard, or is it a
  choice made by the library you're testing against? What does that mean for how you should
  handle it?

## Man page

`man 3 printf` — the `s` conversion.

## Resources

- [cppreference: printf](https://en.cppreference.com/w/c/io/fprintf)
