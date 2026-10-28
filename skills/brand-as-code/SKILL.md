---
name: brand-as-code
description: "Keep the brand book as files in a repo and render every visual from HTML templates with headless Chrome, in every size. Use when setting up a brand book, making covers, social images, posters, banners or speaker cards, or when visuals have started to drift between tools."
---

# Brand as code

Visuals drift when the brand lives in five tools. Put the brand in a repo as files. Every visual
is an HTML template that reads from it. Because the brand is files, the agent reads it before it
makes anything.

## How to build it: four steps

1. **Start from what you have.** The colours you already use, your logo files, your old covers.
   Never redraw a logo or sample colours from a screenshot.
2. **Who you are.** Your story and how you sound, wherever it already lives: a knowledge base, a
   workspace, a doc. If your agent can read it through a connector, point it there.
3. **Write it down.** One long prompt about what your brand is, then round after round of
   corrections until it reads right. Every correction you make twice goes into the book.
4. **Brand book as files.** In the repo, next to the templates that use it.

## The repo

```
brand/
  tokens.css   colours, type and spacing as CSS variables
  BRAND.md     the rules in words: logo, colour use, type scale, how we write
  logo/        the real SVG files
templates/     one HTML file per format family
render.sh      HTML in, PNG out
```

## Write rules, not mood

`BRAND.md` answers the questions a template must decide: which ground and ink colours, ONE accent
per piece and where it may appear, one headline face with its weight and tracking, which logo
lockups exist and in which colours, how co-branded pieces work.

## Templates

- CSS variables from `tokens.css`, a fixed canvas, text passed in as parameters, so one file
  renders every event.
- Position in proportions, not fixed pixels, so the layout survives other sizes.
- Vertical and horizontal formats need different layouts. Write two layouts, not six.

## Sizes

Square 1080 × 1080, portrait 1080 × 1350, story 1080 × 1920 (keep text out of the top and bottom
edges), landscape 1920 × 1080, link preview 1200 × 628.

## Render

Headless Chrome, a screenshot at 2x, with a short wait so web fonts load. Without the wait you get
the fallback font, and it looks almost right. For print, render to PDF instead.

## The human part

The agent doesn't design for you. You bring the taste, it brings the versions. Expect several
rounds on anything that matters, and say what's wrong in plain words.

## Check before you send

- Look at every render at about 200 px wide. That is how it will be seen in a feed.
- Check the logo on dark grounds. An SVG made for white pages may vanish on black.
- Real photos over generated ones.
