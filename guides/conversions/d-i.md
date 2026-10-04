# %d and %i

## What it's for

Printing a **signed** integer in decimal. For printf, `%d` and `%i` behave identically.

## Think about

- Break the job into smaller jobs: handle the sign, then produce the digits. Which part is new?
- Digits appear from the **least** significant end when you divide, but must be printed
  from the **most** significant end. What strategies exist for fixing the order? (Think:
  store and reverse, count first, work from the other end, let the call stack do it…)
  Which fit comfortably within the Norm and don't need allocation?
- What's special about zero?
- What's special about the smallest representable `int`? Try negating it on paper using
  how two's complement works. What do you need to do differently?
- What's your count for a negative number — does the minus sign count?

## Go find out

- Why is negating the minimum value of a signed type a problem, and what are the common
  ways to avoid it? (Search: *two's complement INT_MIN negation overflow*.)
- `%d` and `%i` are identical in printf. Where in C do they differ? (Look at `scanf`.)

## Man page

`man 3 printf` — the `d` and `i` conversions.

## Resources

- [Wikipedia: Two's complement](https://en.wikipedia.org/wiki/Two%27s_complement)
- [cppreference: numeric limits](https://en.cppreference.com/w/c/types/limits)
