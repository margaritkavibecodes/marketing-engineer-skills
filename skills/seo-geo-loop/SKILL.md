---
name: seo-geo-loop
description: "Build and run a weekly SEO and GEO loop for a new site: measure, make the site citable by AI answer engines, a weekly radar agent that picks ONE article, a writer agent that drafts it, a human gate, and a cross-check of what the AI engines actually say. Use for search measurement, llms.txt, schema, Wikidata, picking the next article, or checking AI citations."
---

# SEO + GEO loop

SEO is Google finding you. GEO is AI answers quoting you. On a brand-new site, nobody knows your
name, Google has a few of your pages, and no AI answer cites you. And when AI has no good source,
it makes one up. The first good source wins.

Read `RULES.md` (see `taste-rules`) before writing anything.

## How to build it: four steps

1. **Measure.** Keyword volumes, including AI search volume if your tools have it. Then where you
   stand: how many of your pages Google knows, your position for the head term, which sites the
   AI answers cite. If most of your pages aren't indexed, this week's job is indexing.
2. **Make it citable.** Every claim links to its primary source. FAQ markup that matches the
   visible FAQ. An `llms.txt` (see below). A first batch of articles, each owning one real query.
3. **Automate.** A weekly radar agent, then a writer agent. Expect things to break: some sources
   block cloud bots, so save them from a machine you control and push the copies to the repo.
4. **Step back.** Once you approve most drafts as they are, let the writer start on its own and
   ping you when a draft is ready. You review and publish. The human gate never goes away.

## What's llms.txt?

A plain text file at the root of your website, written for AI tools: what you are, what you are
not, your key pages, the facts you want quoted. The "what you are not" part matters. It is how you
correct features an AI engine invented for you.

## One repo for the whole loop

```
routines/    the radar prompt and the writer prompt
RULES.md     house rules and rules of evidence
snapshots/   text copies of sources that block bots, refreshed daily
probes/      the questions you ask the AI engines
drafts/      what the writer produces, one branch per article
```

The agents push their work to the repo. You pull it. Rules, prompts and data stay in one place,
and you can see every change.

## The radar (weekly)

A scheduled agent that posts ONE message to your team chat and stops. It covers:

- what changed in your topic this week, from primary sources only, each with a date and link
- where you stand on a short fixed keyword list, and who the AI answers cite
- the questions and error messages people search, in their exact wording
- ONE recommended article and why now, plus one alternative so the backlog stays visible
- existing articles that this week's changes made wrong

## The writer

Starts from the radar's pick. Drafts, checks every fact against a primary source during the run,
lints, and opens a pull request. It never publishes.

Rules of evidence: a fact goes in only if it was read in this run in a primary source. Memory and
search snippets are not sources. A fact that fails the check is cut.

Shape that AI engines can lift: the H1 is the question people type, a bold one-line answer under
it and under every H2, an FAQ in the searchers' own phrasing, sources at the end.

## Cross-check: ask the AIs

Every few weeks, ask ChatGPT, Google AI Mode and Perplexity the same handful of questions about
your topic and your name. Record whether you are cited, who is, and any claim about you that is
not on your site. A wrong claim is a content gap. Fix what AI reads: llms.txt, a "what is <you>"
page, an entity in Wikidata, the same name everywhere, video with chapters.

Then watch the AI report in your search console for impressions inside AI answers.

## Publish checklist

- cover from your brand template, never stock
- sources block, one primary source per line
- article and FAQ schema, internal links only to pages that exist
- in the sitemap, indexing requested, IndexNow pinged if you use it
- older articles on the topic now link to the new one
