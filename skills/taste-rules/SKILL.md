---
name: taste-rules
description: "Make the agent write, design and judge like you, using one rules file that every other task reads first. Use when starting a new marketing repo, when copy sounds generic, when you correct the agent on the same thing a second time, or before writing any copy, ad, article, post or visual."
---

# Taste rules

The tools are the easy part. Taste is the hard part. An agent has averages, not taste, so you
write your taste down and make it read that file before every piece of work.

Start here. Every other skill in this set reads this file first.

## How to build it

1. **Collect your corrections.** For one week, every time you fix the agent's output, write the
   fix down in one line. Don't organise it yet.
2. **Sort them into the file.** Use the sections below. Most of your lines will land in "banned"
   and "claims we can't make".
3. **Add the why.** Each rule gets one sentence on why it exists. This matters more than the rule.
4. **Point everything at it.** Every prompt starts with: "Read RULES.md first. It wins over this
   prompt."

## The file

`RULES.md` in the root of your repo. Short enough to be read every single time.

1. **Who we sell to.** One paragraph: their job, what they already know, what they distrust.
2. **How we sound.** A few lines, plus two or three real sentences you wrote and liked. Real
   examples beat adjectives.
3. **Banned words and phrases.** What makes you sound like everyone else in your category.
4. **Claims we can't make.** Anything a buyer can't check. Numbers not cleared for public use.
5. **Sources.** Where facts may come from, and what happens when one can't be verified.
6. **Visual checks.** What every image passes before it ships.
7. **Rulings log.** Dated, one line each.

## The habit: twice means a rule

When you correct the same thing twice, it becomes a written rule. Not the third time.

Write each one as: the rule as an instruction, the why in one sentence, and how to apply it if
that isn't obvious. An agent that knows why handles the case the rule didn't foresee.

When a rule turns out wrong, change it and log the date. Never keep two rules that disagree.

## Rules worth starting with

- No em dashes. Use a comma, a colon or a full stop.
- No rhythm triads and no "not X, but Y" as a habit.
- No puffery: seamless, robust, powerful, cutting-edge, unlock, elevate.
- Never invent a quote, a number or a URL. If it can't be verified, cut it. Don't soften it.
- Never sell on a claim the buyer can't check. Describe the mechanism instead.
- "Cringe" is valid feedback. The agent's job is to work out why, then write the rule.

## Lint what a machine can check

End every writing task with a lint step and fix every hit before delivering: em dashes, your
banned words list, links that point nowhere. A grep never forgets a rule.

## Reviewing a draft

Go section by section through `RULES.md`, quote each line that breaks a rule, give the rewrite.
Then read it once more as the reader from section 1: would they trust it?
