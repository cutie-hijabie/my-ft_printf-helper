# 04 — Structuring your project

## What it's for

ft_printf is small enough to write in one messy file — and the Norm won't let you. This
guide is about splitting the work so each piece is small, named for what it does, and easy
to test on its own.

## Think about

- The Norm limits you to a small number of lines per function, a small number of functions
  per file, and a small number of parameters. Which jobs in ft_printf naturally become
  their own function? Which are *shared* between several conversions?
- Look at your list of conversions. Which ones are really "the same job with a different
  setting"? Which settings could be *parameters* instead of copy-pasted functions?
- What belongs in the header? What shouldn't?
- What does your library need to be called, and what Makefile rules does the subject
  require? Re-read that section — people lose points on Makefile details constantly.
- Is a Makefile that re-links or rebuilds everything every time `make` runs acceptable?
- The subject says something about libft. Read exactly what it says, and decide for yourself
  whether you actually need it for the mandatory part.

## Go find out

- How does a static library get built, and which tool does the subject require (or forbid)
  for packing the object files into one?
- What's a header guard and why does every `.h` need one?

## Resources

- [42 Norminette](https://github.com/42School/norminette)
- `man ar`
- [GNU Make manual](https://www.gnu.org/software/make/manual/make.html) — rules, prerequisites, phony targets.
