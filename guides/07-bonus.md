# 07 — Bonus (a map, not a walkthrough)

> The bonus is only evaluated if the mandatory part is **perfect**. Don't touch it until
> then, and re-read the subject's bonus section to see exactly what it asks for.

## What it's for

Real printf conversions can be modified: you can ask for a minimum width, left or right
alignment, padding with zeros, forcing a sign, adding a prefix, and so on. The bonus asks
you to support a set of these.

## Think about

- Where do these modifiers sit in the format string relative to the `%` and the
  conversion letter? What order can they come in?
- What **information** must you collect while parsing, before you know which conversion
  you're dealing with? Where will you store it so handlers can use it?
- Some modifiers only make sense for certain conversions. Some conflict with each other.
  Make a table on paper: modifier × conversion → what happens? (The man page tells you.)
- Your existing handlers just print a value. What new step now happens *around* that
  printing (before it? after it?), and how does it depend on the length of what's printed?
- How will you stay inside the Norm's limits when handlers now need much more state?

## Go find out

- Read the sections on **flag characters**, **field width**, and **precision** in
  `man 3 printf`. Find out precisely what each does for each conversion you support.
- Which combinations are explicitly "undefined" or ignored in the man page?

## Man page

`man 3 printf`

## Resources

- [Wikipedia: printf format string](https://en.wikipedia.org/wiki/Printf_format_string)
