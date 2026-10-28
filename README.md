# Marketing Engineer Skills

Five Claude Code skills from the talk "From Marketing Specialist to Marketing Engineer".

Each file is one skill: the method, the steps to build it, how it runs and the rules that keep it
useful. They are methods, not finished prompts. Write your own prompts from them, with your own
rules and your own numbers.

## Install

With the skills CLI:

```
npx skills add margaritkavibecodes/marketing-engineer-skills
```

It asks which skills and which agents to install them for. To install all five for Claude Code
without the questions:

```
npx skills add margaritkavibecodes/marketing-engineer-skills --skill '*' --agent claude-code -y
```

Or copy a folder from `skills/` into `~/.claude/skills/` by hand. Restart Claude Code. A skill
starts on its own when a task matches its description, or you can ask for it by name.

## The skills

- `taste-rules`: one rules file that makes the agent write and judge like you. **Start here.**
- `seo-geo-loop`: measure, make your site citable, a weekly radar and writer, and a check of what
  AI engines say about you.
- `ads-watchdog`: set up your ad channels, then a Monday report graded on your own goals and
  checked against your analytics.
- `brand-as-code`: the brand book as files, and every visual rendered from HTML templates.
- `product-launch-kit`: the order of things when a new product goes live.

## The idea behind all five

One repo per workflow. Rules, prompts and data live there. The agents push their work, you pull
it, and every change is visible. And when you correct the agent twice, write a rule.
