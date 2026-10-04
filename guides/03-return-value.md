# 03 — The return value

## What it's for

`printf` doesn't just print — it also **tells you how many characters it printed**.
That number is part of the spec, and evaluators will check it.

## Think about

- Everything you output must be counted. Where do you count — in one central place, or
  inside every handler? What are the trade-offs when you add a new conversion later?
- If a helper function prints a number, how does the *caller* learn how many characters
  that was?
- A number may print as a different count of characters depending on its value. Does your
  counting approach cope with that without special cases?
- What about a `%c` whose argument is the zero byte (`'\0'`)? Many functions treat zero as
  "end of text". Does your approach print it? Does it count it?
- What does `write` return, and can it fail? What should *your* function do (and return)
  if it does? What does the man page say printf itself returns on error?

## Go find out

- Read the RETURN VALUE section of `man 3 printf` carefully. What's the exact definition?
  Does it include the terminating zero of the format string?
- Compare: what does `printf` return for `"%s"` with an empty string? For an empty format?

## Man page

`man 3 printf` (RETURN VALUE) and `man 2 write` (RETURN VALUE).

## Resources

- [man7.org: write(2)](https://man7.org/linux/man-pages/man2/write.2.html)
