# 07 — README and defense

## What it's for

Version 1.1 of the subject requires a proper `README.md` and tells you what to expect at
the review. Both are graded, so don't leave them to the last five minutes.

## The README

Re-read the "Readme Requirements" chapter of the subject. In plain words, it asks for:

- A specific **first line**, written in italics, that credits the author(s). The subject gives
  the exact wording — copy it from there.
- A **Description** section: what the project is and what it's for.
- An **Instructions** section: how to compile it and use the library.
- A **Resources** section: classic references (docs, articles, tutorials) **and** an honest
  description of how AI was used — which tasks, which parts of the project.
- A **detailed explanation and justification of the chosen algorithm and data structure.**
- It should be readable by someone who has never heard of the project (peers, staff,
  recruiters). English is recommended; your campus's main language is also allowed.

### Think about

- What is your *algorithm* here, in plain words? How does your function move through the
  format string, and how does it decide what to do at each point?
- What is your *data structure*, if any? Even if the answer is "I didn't need one," can you
  justify that? What would you have stored, and why did you decide against it?
- Why did you organize your files and functions the way you did? What would have been worse?
- Is your AI-usage paragraph truthful and specific? "I used AI to understand what variadic
  functions are" is very different from "AI wrote my conversion handlers."

## The defense

- You'll be compared against the real `printf`: expect tests on every conversion, odd
  values, and many conversions combined in one call.
- You may be asked to make a **small modification** during the review: a minor behavior
  change, rewriting a few lines, or an easy-to-add feature. This checks that *you*
  understand your own code. If someone asked you to support one more conversion, or change how
  one existing one prints, could you do it in a few minutes?
- You may use your own tests or your peer's. Prepare a diverse set.
- Once you pass, the subject lets you add `ft_printf` to your Libft so you can use it in later
  projects. Think about what that means for how your code is organized.

## Go find out

- Pick any three functions in your code and ask yourself: "Why does this exist? What breaks
  if I delete it?"
- Explain your solution out loud to someone else. Where do you stumble? That's the part to
  study again.

## Resources

- [GitHub: About READMEs](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-readmes)
