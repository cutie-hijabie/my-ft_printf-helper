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

- What does the real printf do with `"%5%"` or `"% %"`? (Not required for mandatory — but
  good for understanding where bonus complexity comes from.)

## Man page

`man 3 printf` — the `%` conversion.

## Resources

- [Wikipedia: printf format string](https://en.wikipedia.org/wiki/Printf_format_string)
