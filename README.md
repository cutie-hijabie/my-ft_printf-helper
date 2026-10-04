# ft_printf Helper Guides

*A study companion for 42 newcomers working on the ft_printf project — not a solution repo.*

This repo exists to help Core students **think through** ft_printf on their own, without
handing over code or answers. It's organized around the official subject and gives you:

- a plain-words explanation of **what each piece is for**
- things to **think about** before you start coding
- a few **"go find out"** questions — details I deliberately left out so you have to look
  them up yourself (that's where the learning sticks)
- the **man page(s)** you should read
- **resources** to help you understand the underlying concept

There is **no code** here. No finished algorithms, no prototypes spelled out. Reading the
man pages and the subject PDF is part of the exercise.

> If you want to compare against a finished implementation *after* you've written your
> own, see [my-ft_printf](https://github.com/cutie-hijabie/my-ft_printf) — but try first.

## Why this exists

At 42, the point of ft_printf isn't to produce a `libftprintf.a` — it's to understand:

- how a function can accept a **variable number of arguments**
- how to **parse** a string and react to what's in it
- how numbers are **represented** (signed vs unsigned, different bases) and turned into text
- how pointers look as values
- how to **split a bigger problem** into small, single-purpose pieces
- how real library functions behave in the corners, not just the happy path

Copy-pasting an answer (from AI or anywhere else) skips all of that. You'll feel it in
your defense, and you'll feel it harder in exams with no AI and no internet.

## How to use this repo

1. Read the subject PDF first. Keep it open next to you the whole time.
2. Start with [00 — Big picture](guides/00-big-picture.md), then work through the guides in order.
3. For each conversion, open its page in `guides/conversions/`.
4. Read the man pages linked. Actually read them.
5. Answer the "Think about" questions *before* touching your editor — on paper is fine.
6. Write it. Get it wrong. Debug it. That's the project.
7. Compare your output to the real `printf` constantly, not just at the end.
8. Before you submit, read [07 — README and defense](guides/07-readme-and-defense.md).

> Based on subject **version 1.1**, which has **no bonus part**. If your subject version
> differs, the subject always wins over this repo.

## Guides

| # | Guide | What it covers |
|---|-------|----------------|
| 00 | [Big picture](guides/00-big-picture.md) | What printf actually does, and a sensible order to build in |
| 01 | [Variadic functions](guides/01-variadic-functions.md) | How `...` works and what it can't tell you |
| 02 | [Parsing the format string](guides/02-parsing-the-format-string.md) | Walking the string and deciding what each character means |
| 03 | [The return value](guides/03-return-value.md) | Counting what you print |
| 04 | [Structuring your project](guides/04-structuring-your-project.md) | Files, helpers, Norm, Makefile |
| 05 | [Testing and debugging](guides/05-testing-and-debugging.md) | How to catch your own bugs |
| 06 | [Common pitfalls](guides/06-common-pitfalls.md) | Questions that catch most people out |
| 07 | [README and defense](guides/07-readme-and-defense.md) | The README the subject requires, and what to expect in the review |

Per-conversion guides live in [`guides/conversions/`](guides/conversions/README.md):
`%c` · `%s` · `%p` · `%d` / `%i` · `%u` · `%x` / `%X` · `%%`

## General resources (not specific to one guide)

- [Beej's Guide to C Programming](https://beej.us/guide/bgc/) — one of the best free C intros. Look for the chapter on variadic functions.
- `man 3 printf` — your spec. The conversion and return-value sections are the important ones.
- `man 3 stdarg` — everything about variable argument lists.
- `man 2 write` — the only output function you're allowed to build on. Read its return value section.
- [cppreference: variadic arguments](https://en.cppreference.com/w/c/variadic)
- [42 Norminette](https://github.com/42School/norminette) — know the Norm before you write a line.
- `valgrind --leak-check=full ./your_test` — find leaks before your evaluator does.

## A note on AI

Per the subject's own AI Instructions chapter: you're expected to *reason first*, and not
ask AI for direct answers. This repo was built to give explanations and pointers to
official documentation only — never generated code, never filled-in logic. If you use AI
yourself while learning, the healthiest use is asking it to explain a concept you already
tried to understand from the man page — not asking it to write or fix your function.
