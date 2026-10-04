# 04 — Structuring your project

## What it's for

ft_printf is small enough to write in one messy file — and the Norm won't let you. The
subject also says the key to a successful ft_printf is **well-structured and extensible
code**. This guide is about splitting the work so each piece is small, named for what it
does, and easy to test on its own.

## Think about

- The Norm limits you to a small number of lines per function, a small number of functions
  per file, and a small number of parameters. Which jobs in ft_printf naturally become
  their own function? Which are *shared* between several conversions?
- Look at your list of conversions. Which ones are really "the same job with a different
  setting"? Which settings could be *parameters* instead of copy-pasted functions?
- "Extensible" is the subject's own word. If someone asked you to add one more conversion
  tomorrow, how many places in your code would you have to touch? (The review may ask you to
  make a small change like this on the spot.)
- Which functions does the subject allow you to call? Which of them have you used so far,
  and why?
- **What must the submission contain?** Re-read the subject's table: the program name, the
  Makefile rules, where the library has to be created, and what the header must be called.
  People lose points on these details constantly.
- The Common Instructions add rules about the Makefile: which compiler, which flags, and
  something about *relinking*. Does `make` twice in a row do any work the second time?
- Libft is authorized for this project. Read what the Common Instructions say about **how**
  it must be included and built if you use it — and decide whether you actually need it.
- Which tool must you use to pack object files into a library, and which one does the subject
  forbid?
- What does your header need to contain, at minimum? What shouldn't be in it?

## Go find out

- How does a static library get built, and how do you link a test program against it?
- What's a header guard and why does every `.h` need one?
- What's a "phony" target in a Makefile and which of your rules should be one?

## Resources

- [42 Norminette](https://github.com/42School/norminette)
- `man ar`
- [GNU Make manual](https://www.gnu.org/software/make/manual/make.html) — rules, prerequisites, phony targets.
