---
name: ads-watchdog
description: "Set up ad channels and a weekly read-only agent that grades every ad account against your own goals file, cross-checks the platforms against your analytics, and posts a short scorecard and to-do list to your team chat. Use when setting up Google, YouTube, Meta, AI-chat or Bing campaigns, building an ads report routine, or explaining ad numbers to non-marketers."
---

# Ads watchdog

Platforms grade their own homework. A video platform counts any tap inside its own app as a
click. A new ad channel reports conversions your analytics never sees. So nothing goes into a
report until it is checked against what happened on your own site.

## How to build it: four steps

1. **Research first.** No campaign before you know how each account should be set up. Write a
   step-by-step setup guide per channel and follow it.
2. **A weekly report.** One scheduled agent reads every ad account and posts to your team chat
   every Monday. Your first version will have too much text. Cut it to a scorecard and a to-do
   list, and grade on your own goals, not the platforms' scores.
3. **Make every click count.** Track every real action on the site (booked a call, sent the form,
   used the free tool) through your tag manager, only after cookie consent. Give ads their own
   landing page with one question.
4. **Check the numbers.** Cross-check every platform against your analytics. Where they disagree
   a lot, believe your site.

## Setting up the channels

For each channel, write down what you set up and with what: an MCP or connector, the platform's
own screen, or a browser agent. Some changes only work in the platform's screen, so do those by
hand. Keep a list of which.

- **Search:** its own account per product, so one product's conversions don't train another's
  bidding. Intent keywords, negatives from week one.
- **Video:** a campaign built around your best explainer video.
- **Social:** manual placements, budgets per ad set, every "automatic" option off. The people you
  pay to bring in become your retargeting pool, so relevance beats cheap reach.
- **AI chat ads and smaller engines:** two weeks, judged only on real actions.
- **Creatives:** design by hand in a design tool. Mockups can come from a connector.

## One repo

```
routines/    the Monday report prompt
goals.md     your goals, one row per metric, with the reason. The team edits this.
accounts.md  every live account and campaign
scripts/     direct API pulls for platforms with no connector
```

## The ground rule

The platform's ratings and recommendations are not findings. Before writing one, ask: which row
in `goals.md` does this number break? If none, it isn't a finding.

## How the report runs

1. Same two date ranges for every platform: the week that just ended and the week before.
2. Pull read-only. Never call anything that creates, changes or pauses. Save raw responses.
3. Cross-check with analytics, filtered by exact campaign name.
4. Grade each goal row: on goal, missed, too new to grade, no data. A failed pull is never zero.
5. Read last week's report and mark each recommendation done or still open.
6. Post: results first, then a few recommendations that each name the object, the number and the
   exact change. Details go in a thread, one reply per account.

Write it in plain words. Put the meaning in brackets on first use: "click rate (clicks per 100
people who saw the ad)".

## Set your own numbers

Every threshold in `goals.md` is yours to choose: how big a gap between platform and analytics is
worth flagging, how much worse than last week counts as a warning, how long a message may be.
Write the reason next to each one. Changing a number there changes next Monday's report.
