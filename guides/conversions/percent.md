# %%

## What it's for

Printing a literal `%` — the way to write a percent sign when `%` normally means
"conversion starts here."

## Think about

- Does this conversion take an argument from the list? What would go wrong if your code
  fetched one anyway?
- Does your dispatcher treat it as a special case, or does it fit naturally with the others?
- What does it add to your count?
- What does the loop skip past after handling it?

## Go find out

- What does the real printf do with `"%5%"` or `"% %"`? (Not required by the subject — but
  a good way to see how much more the real printf does than you're asked to copy.)

## Man page

`man 3 printf` — the `%` conversion.

## Resources

- [Wikipedia: printf format string](https://en.wikipedia.org/wiki/Printf_format_string)
