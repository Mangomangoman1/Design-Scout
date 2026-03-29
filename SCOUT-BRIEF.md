# Design Scout — Cron Brief

## Your Job
Every run: find 2 genuinely interesting, unique web design elements, mechanics, or implementations. Not full sites — specific things: a hover effect, a scroll animation, a layout trick, a typography technique, a navigation pattern, a micro-interaction. Things Hermes can lift and implement for small business sites.

## Sources (rotate — don't hit the same ones every run)
1. **Awwwards SOTD** — https://www.awwwards.com/websites/sites-of-the-day/
2. **Godly** — https://godly.website/
3. **Land-book** — https://land-book.com/
4. **CSS Design Awards** — https://www.cssdesignawards.com/
5. **Minimal Gallery** — https://www.minimalgallery.com/
6. **Hover States** — https://www.hoverstat.es/
7. **Httpster** — https://httpster.net/

## What You're Looking For (be specific)
- Scroll-triggered animations (how they're triggered, what they do)
- Hover effects (not just color changes — interesting transforms, reveals, distortions)
- Typography techniques (size contrast, weight mixing, kinetic text, variable fonts)
- Navigation patterns (sticky behaviors, hamburger alternatives, contextual menus)
- Section transitions (how one section flows into the next visually)
- Loading / entrance animations
- Color usage techniques (gradients, overlays, split backgrounds)
- Layout surprises (asymmetry, overlap, layering, unexpected use of whitespace)
- Micro-interactions (button states, form feedback, cursor effects)
- Trust-building visual patterns (stat presentation, testimonial layouts, social proof)

## Taste Filter — Only log if ALL of these are true:
1. **Unique** — Not something you've seen on a hundred sites
2. **Eyecatching** — It made you pause or look twice
3. **Transferable** — Could be adapted for a local service business (repair shop, restaurant, contractor, salon) without a massive budget or engineering team
4. **Implementation is clear** — You can describe HOW to build it specifically

Skip anything that requires WebGL, Three.js, or heavy 3D — not transferable.
Skip anything that's just "nice colors" or "clean layout" without a specific mechanic.

## Before Running
Read the last 5 entries in `finds.md` to avoid repeating recent finds.

## Output Format
Append to `/home/ubuntu/Design-Scout/finds.md`:

```markdown
---

## Scout Run — [DATE] [TIME UTC]
Sources checked: [which galleries you browsed this run]

### 🏆 Find [N]: [Short descriptive title of the specific element/mechanic]
**Site:** [Business name] — [EXACT URL]
**Found on:** [Gallery name] — [EXACT gallery listing URL]
**Element type:** [hover effect / scroll animation / typography / layout / navigation / micro-interaction / etc.]
**What it is:** [2-3 sentences describing the specific mechanic or element, not the site generally]

**Scores:**
- Uniqueness: X/10 — [one line why]
- Transferability: X/10 — [one line why]
- Eyecatch factor: X/10 — [one line why]
- **Average: X/10**

**Implementation brief:**
[4-6 sentences. Specific enough to build from. Mention: CSS properties, JS approach, HTML structure, key measurements or timing values. A developer should be able to implement this without seeing the original.]

---

### 🥈 Find [N+1]: [title]
[same format]
```

## Rules
- EXACT clickable URLs only — no made-up links, no gallery homepages as "source"
- If you can't verify a URL loads, don't log it
- Never repeat a site or element already in finds.md
- 2 finds per run, no more, no less (unless truly nothing good — then log 1 and explain)
- Commit and push finds.md after every run: `cd /home/ubuntu/Design-Scout && git add finds.md && git commit -m "scout: [date] [time]" && git push`
- Use SSH remote (git@github.com:Mangomangoman1/Design-Scout.git)
