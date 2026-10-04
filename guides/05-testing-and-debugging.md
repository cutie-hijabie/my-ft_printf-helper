# 05 — Testing and debugging

## What it's for

You have a perfect reference implementation sitting on your machine: the real `printf`.
The whole job of testing is to make *yours* behave identically — output **and** return value.

## Think about

- For every test, you should compare two things. What are they?
- What is the nastiest input for each conversion? (Zero, the biggest value, the smallest
  value, empty, missing, repeated…) Write those down per conversion *before* testing.
- What happens with many conversions in one call, in mixed order, back to back, with
  literal text in between?
- Does your test program call `printf` and `ft_printf` in a way that makes the two
  outputs easy to compare automatically — rather than eyeballing them?

## Go find out

- Why does output sometimes appear **out of order** when you mix `printf` and `write`
  (especially when output is redirected to a file)? Understand this before you decide your
  function is "buggy."
- What warnings does the compiler give you when you call the *real* printf with a wrong
  conversion? Those warnings are a free list of tricky cases.
- How can you redirect output to a file and compare two files from the terminal?
- Which compiler flags does the subject require? Which extra ones help you (look into
  sanitizers) while debugging?

## Resources

- `valgrind --leak-check=full ./your_test`
- [Valgrind quick start](https://valgrind.org/docs/manual/quick-start.html)
- `man diff`
