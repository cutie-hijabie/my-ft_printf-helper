# 01 — Variadic functions

## What it's for

A variadic function accepts a variable number of arguments — that's the `...` in
printf's prototype. This is the one genuinely *new* C feature in ft_printf; everything
else is stuff you've done before in different clothing.

## Think about

- When a function takes `...`, what does the compiler know about the extra arguments?
  Their count? Their types? Neither?
- If the function itself can't know, **who tells it**? In printf's case, what plays that role?
- What would happen if the format says "an integer" but the caller passed a string?
  Why is this such a classic source of bugs and security vulnerabilities?
- You'll want to read arguments one at a time, in order. What does that imply about
  "going back" to an earlier argument?
- Your parsing code will probably be split across several functions. How will they all
  get access to the *same* argument list — and what has to be true so they don't skip or
  repeat an argument?

## Go find out

- `stdarg.h` provides **one type and a small handful of macros**. Find them in the man
  page and work out what role each plays and in what order they're used. The subject's
  allowed-functions list names four of them — match each to its job. Do you need all four?
- What happens to small types (like `char` or `short`) when they're passed through `...`?
  This has a direct consequence for what type you should ask for when reading a `%c`
  argument. (Search: *default argument promotions*.)
- What's the rule about passing the argument-list object to another function, and what
  state is it in afterwards? This is one of the most common "why is my output shifted by
  one argument?" bugs. (Search: *passing va_list to another function*.)

## Man page

`man 3 stdarg`

## Resources

- [cppreference: variadic arguments](https://en.cppreference.com/w/c/variadic)
- [cppreference: implicit conversions](https://en.cppreference.com/w/c/language/conversion) — the "default argument promotions" section.
- [Wikipedia: Variadic function](https://en.wikipedia.org/wiki/Variadic_function)
- [Beej's Guide to C](https://beej.us/guide/bgc/) — find the variadic functions chapter.
