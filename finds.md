# Design Scout — Finds Log 🔭

*Curated web design inspiration for Hailey Device Repair*
*Scored on: Uniqueness (1-10) | Transferability (1-10) | Personal Taste (1-10)*

---

## Scout Run — 2026-03-28 10:58 UTC
Sources checked: [Godly](https://godly.website/), [Land-book](https://land-book.com/), [CSS Design Awards](https://www.cssdesignawards.com/)

### 🏆 Find 1: Sequential Phrase-Building Hero Headline
**Site:** Samara — [https://www.samara.com](https://www.samara.com)
**Found on:** Godly — [https://godly.website/website/samara-973](https://godly.website/website/samara-973)
**What it is:** The hero headline animates phrase by phrase — "Backyard is the | super simple, | smartly customizable, | all-new ADU | from Samara." Each chunk appears on its own line with a staggered fade-in, forcing the reader to read at the site's pace rather than skim. It functions like a cinematic text reveal, but fully in HTML/CSS.

**Scores:**
- Uniqueness: 8/10 — Not technically new, but the execution is precise and intentional. Most sites use word-by-word; this uses meaningful phrase chunks that each land as a beat.
- Transferability: 9/10 — Extremely portable. A repair shop headline could read: "We fix your phone | same day | no appointment needed | in Hailey, Idaho." Zero budget required — pure CSS animation + span wrapping.
- Personal taste: 9/10 — It made me slow down and actually read the headline instead of scrolling past. That's rare and valuable.
- **Average: 8.7/10**

**Implementation brief:**
Wrap each phrase chunk in a `<span>` with `display: block` or `display: inline-block`. Apply a `@keyframes fadeInUp` animation (translate Y from ~16px to 0, opacity 0→1, ~400ms ease-out). Stagger each span using `animation-delay` increments of ~150-200ms. Use `animation-fill-mode: both` so spans stay invisible before their delay fires. The overall container can be a standard `<h1>` with `line-height: 1.2`. For added polish, pair with a subtle font weight shift — lighter for descriptors, heavier for the key value phrase. No JavaScript needed; pure CSS with prefers-reduced-motion fallback that just shows all text instantly.

---

### 🥈 Find 2: Mid-Page Founder Letter as Trust Anchor
**Site:** Acctual — [https://www.acctual.com](https://www.acctual.com)
**Found on:** Land-book — [https://land-book.com/websites/92938-console](https://land-book.com/) (browsed listing; Acctual from Godly #998)
**What it is:** Halfway down the page, between feature sections, there's a plain "Dear business owner," letter — written in first person by the founder, acknowledging real pain ("running a small business isn't for the faint of heart"), and ending with "Love you, pay me." It's styled like a typewritten letter with attribution photo and name. It completely breaks the marketing pattern of the page, which makes it land hard.

**Scores:**
- Uniqueness: 8/10 — Personal letters on landing pages exist, but embedding one mid-page as a context break rather than a testimonial is a smart structural move I haven't seen done this cleanly.
- Transferability: 10/10 — Sam *is* a small business owner in a small town. A version of this for Hailey Device Repair basically writes itself: "Dear fellow Hailey resident, when your phone screen cracks, the last thing you need is..." Requires zero design budget — just a text block with the right typography.
- Personal taste: 9/10 — It's the moment on that page where you feel like you're talking to a human. Everything else is polished SaaS; this is a gut punch of authenticity.
- **Average: 9/10**

**Implementation brief:**
Create a full-width section with a max-width container (~600px) centered. Use a slightly warm off-white background (`#faf9f6` or similar) with subtle border or drop shadow to separate it from surrounding sections. Set the body text in a serif or typewriter-style font (Georgia, or a Google Font like "DM Serif Display" for the opening, switching to a clean sans for the body). Open with "Dear [customer type]," in slightly larger type. Keep the letter to 100-150 words — real, specific, emotionally honest. End with a signature line using `font-style: italic`. Include a small photo or avatar, name, and title below. Place this section after the second or third feature block, not at the top — it works as a trust reset before the final CTA.

---

### 🥉 Find 3: "Superpower" Feature Sectioning with Labeled Scroll Anchors
**Site:** Lóvi — [https://lovi.care](https://lovi.care)
**Found on:** Godly — [https://godly.website/website/lovi-994](https://godly.website/website/lovi-994)
**What it is:** Each major feature section opens with a small inline label "✦ Superpower #1", "✦ Superpower #2", etc. — displayed in a muted small-caps or label style before the section headline. It gamifies the scroll, makes features feel like capabilities rather than bullet points, and gives the page a rhythm that makes it feel longer without feeling bloated. The ✦ glyph adds personality without requiring any image assets.

**Scores:**
- Uniqueness: 7/10 — Numbered sections aren't new, but the "Superpower" framing + decorative glyph label is a step above the standard "Feature 01 / 02 / 03" treatment. Feels more human.
- Transferability: 8/10 — Directly usable. A repair shop's superpowers: "✦ Superpower #1: Same-day screen repairs. ✦ Superpower #2: Honest, upfront pricing. ✦ Superpower #3: Text us — no hold music." The framing reframes commoditized services as something special.
- Personal taste: 8/10 — The ✦ glyph detail is the kind of thing that makes a site feel like someone cared. It costs nothing and signals intentionality.
- **Average: 7.7/10**

**Implementation brief:**
Add a `<p class="section-label">` element above each `<h2>` section headline. Style it with `font-size: 0.75rem`, `letter-spacing: 0.12em`, `text-transform: uppercase`, and a muted brand color (a desaturated version of your primary). Use the Unicode ✦ character (U+2726) or similar decorative glyph as a prefix — no icon library needed. Increment the label text manually or via a CSS counter: `counter-increment: superpower; content: "✦ Superpower #" counter(superpower)`. The section itself doesn't need to change — just adding this label above the H2 restructures the visual hierarchy and gives the page a consistent cadence. Works especially well when sections have alternating background colors to further segment them.

---

## Scout Run — 2026-03-28 12:57 UTC
Sources checked: [Land-book](https://land-book.com/design/landing-page), [Godly](https://godly.website/) (new listings), [Awwwards](https://www.awwwards.com/websites/sites-of-the-day/)

### 🏆 Find 4: Audience-Specific Hero Swap (Rotating Sport/Service Targeting)
**Site:** Veo Sports Cameras — [https://www.veo.com](https://www.veo.com)
**Found on:** Land-book — [https://land-book.com/websites/92676-veo-sports-cameras-record-stream-and-analyse](https://land-book.com/websites/92676-veo-sports-cameras-record-stream-and-analyse)
**What it is:** The hero headline cycles through audience-specific versions of the same offer: "Record, analyse, and livestream every basketball match / every lacrosse match / every rugby match." The sport name swaps out on a timer (or scroll trigger) while everything else stays anchored. The feeling is that the site is talking specifically to *you* — even though it's the same sentence for everyone.

**Scores:**
- Uniqueness: 7/10 — Text-swap heroes exist, but most cycle through buzzwords or generic claims. Veo's version swaps a concrete, specific noun (the sport) rather than abstract adjectives. That specificity is what makes it feel targeted rather than gimmicky.
- Transferability: 9/10 — Near-perfect for a repair shop. "We fix cracked iPhone screens / broken charging ports / dead Samsung batteries / water-damaged iPads." Each swap represents a real customer coming in with a real problem. Zero budget, just a JS interval and a CSS transition.
- Personal taste: 8/10 — It's one of those ideas that's so obvious in hindsight it's annoying. Why isn't every service business doing this?
- **Average: 8/10**

**Implementation brief:**
Create an array of service-specific strings (e.g., `["cracked iPhone screens", "broken charging ports", "water-damaged iPads", "dead laptop batteries"]`). Wrap the swappable word in a `<span id="swap-target">` inside the H1. Use a JS `setInterval` every ~2500ms to fade out the current text (`opacity: 0`, `transition: opacity 200ms`), swap the `textContent`, then fade back in. Alternatively use CSS `animation: swap-cycle Xs infinite` with `@keyframes` defining multiple `content:` states if using a pseudo-element. Keep the surrounding text constant and short — the swap should be the only moving part. Add `prefers-reduced-motion` fallback that just shows all options as a static list instead of cycling.

---

### 🥈 Find 5: Outcome Stats as Editorial Interrupt Cards
**Site:** Superpower — [https://superpower.com](https://superpower.com)
**Found on:** Godly — [https://godly.website/website/superpower-1015](https://godly.website/website/superpower-1015)
**What it is:** Between feature sections, Superpower drops standalone cards with a single bold outcome statistic: "63% of members find early risk factors for diabetes" / "44% of members find elevated heart disease risk" / "70% of members slow their speed of ageing." Each is a full-width dark card, large type, one sentence. They read like editorial fact-drops from a magazine — not marketing, not testimonials, just data presented with confidence.

**Scores:**
- Uniqueness: 8/10 — Using outcome stats as layout elements (not buried in a grid or under a heading) is genuinely fresh. Most sites hide their best proof in a "results" section nobody reaches. Surfacing it mid-scroll as a dark interrupt breaks the visual pattern and makes the number unavoidable.
- Transferability: 9/10 — A repair shop has real data: "95% of repairs done same day." "We've fixed 500+ phones in Hailey since 2023." "Most repairs take under an hour." These are boring in a bullet list but powerful as a full-width interrupt card in 60pt font on a dark background.
- Personal taste: 9/10 — This is exactly the kind of thing I'd steal immediately. It uses design to give credibility the visual weight it deserves instead of burying it.
- **Average: 8.7/10**

**Implementation brief:**
Create a `<section class="stat-interrupt">` with `background: #111` (or your darkest brand color), `padding: 80px 24px`, `text-align: center`. The stat number goes in a `<p class="stat-number">` at ~72px or larger, bold, white. The supporting sentence goes in a `<p class="stat-context">` at ~18px, lighter weight, `color: rgba(255,255,255,0.7)`. No icons, no images — just text on dark. Repeat 2-3 times throughout the page at natural transition points (after a features section, before testimonials). The contrast switch from light page body to dark interrupt card does all the visual heavy lifting. Keep each stat to one sentence maximum.

---

### 🥉 Find 6: Ultra-Minimal Copy as a Confidence Statement
**Site:** Reboot Studio — [https://reboot.studio](https://reboot.studio)
**Found on:** Godly — [https://godly.website/website/reboot-1001](https://godly.website/website/reboot-1001)
**What it is:** The entire homepage is basically a few lines of prose. The value prop is one sentence: "We build world-class marketing sites for software startups." The disciplines are listed inline as running text: "Design. / Engineering. / Branding. / Copywriting. / Video. / 3D. / Interaction." — each word punctuated, each standing alone. No hero image. No grid of features. No testimonial carousel. The constraint itself becomes the message: we're confident enough to say less.

**Scores:**
- Uniqueness: 8/10 — Minimal sites aren't rare, but most minimal sites still have a hero image or some visual anchor. Reboot leans entirely into typography and white space. The boldest move is what's NOT there.
- Transferability: 6/10 — Somewhat transferable as a *tone* model — a small repair shop shouldn't be this sparse (customers need reassurance), but the practice of stripping copy down to the one sentence that actually matters is a lesson every small business homepage needs. The inline discipline list is directly stealable for a "What we fix" section.
- Personal taste: 9/10 — I keep coming back to it. There's something almost arrogant about having this little content and it somehow *working*. The period after each discipline word — "Design. Engineering. Branding." — gives each one finality and weight. It's the design equivalent of knowing when to stop talking.
- **Average: 7.7/10**

**Implementation brief:**
For the "What we fix" application: create an inline list inside a paragraph element. "Cracked screens. Broken ports. Dead batteries. Water damage. Bad cameras. Stuck buttons." — each item separated by a space and period, not commas, not bullets. Style the container at `font-size: clamp(1.4rem, 3vw, 2rem)`, `font-weight: 600`, `line-height: 1.5`, `max-width: 700px`. The period-stop rhythm forces each item to register individually rather than blur together as a list. Combine with generous `padding` and a clean white or off-white background — no decorative elements needed. This works especially well as an "About" or "Services" section header before more detailed content below it.

---

## Scout Run — 2026-03-28 14:57 UTC
Sources checked: [Land-book](https://land-book.com/design/landing-page) (page 2), [Awwwards](https://www.awwwards.com/websites/honorable/) (honorable mentions)

### 🏆 Find 7: Timeline Milestone Section ("Here's What You Can Get Done in 30 Days")
**Site:** Playground — [https://www.tryplayground.com](https://www.tryplayground.com)
**Found on:** Land-book — [https://land-book.com/websites/92193-child-care-management-software-and-app-playground](https://land-book.com/websites/92193-child-care-management-software-and-app-playground)
**What it is:** Rather than listing features, Playground structures its trust section as a timeline: "Today / Day 5 / Day 30" — each with 3 bullet-style milestones showing what a new customer will have accomplished at each point. The section header is: "New software shouldn't take a year to implement." It flips the typical feature-pitch into a concrete, time-anchored promise. You're not selling what the product *is* — you're showing what the customer's life *becomes* and exactly when.

**Scores:**
- Uniqueness: 9/10 — I've never seen this pattern on a service business site. Onboarding timelines exist in SaaS, but this is the first time I've seen it used as the primary trust/conversion mechanism on a homepage, with specific day-anchored milestones rather than vague "quick setup" copy.
- Transferability: 10/10 — This is made for a repair shop. "Drop off by noon → Diagnosed within 30 min → Repaired same day → Pick up by 5pm." Or: "Text us → Get a quote in minutes → Bring it in → Fixed the same day." The pattern converts a service into a narrative sequence with known outcomes. Customers don't fear what they don't understand; this eliminates the unknown.
- Personal taste: 9/10 — It respects the customer's time anxiety. When your phone is broken, you want to know *exactly* what will happen. This answers that question visually before they even have to ask.
- **Average: 9.3/10**

**Implementation brief:**
Create a `<section class="timeline">` with a horizontal 3-column layout on desktop, stacked on mobile. Each column gets a `<div class="timeline-step">`. At the top, a `<span class="step-label">` with the time marker — "Drop off", "30 minutes later", "Same day" — in small caps or muted text. Below that, 2–3 short milestone items as `<p>` tags (not `<ul>`) — keep them to one line each. Use a thin vertical or horizontal line connecting the columns (`border-left` on steps 2-3, or a `::before` pseudo-element for a top connecting line). The section should open with a bold objection-crusher headline: "Most repairs done the same day." or "No waiting around. Here's how it works." Keep the milestones concrete and time-specific — "diagnosed within 30 minutes" beats "quick turnaround." Add a muted background color on this section to visually separate it from hero and CTA.

---

### 🥈 Find 8: Selective Bold Within Headlines + Compact Numbered Feature Labels
**Site:** Relace — [https://relace.ai](https://relace.ai)
**Found on:** Land-book — [https://land-book.com/websites/92431-relace-ai-models-and-infrastructure-for-coding-agents-fast-code-generation](https://land-book.com/websites/92431-relace-ai-models-and-infrastructure-for-coding-agents-fast-code-generation)
**What it is:** Two techniques working together. First: section headlines use selective bolding mid-sentence — "Models **built** for coding **agents**" — the surrounding words are normal weight, the key nouns/verbs are bold. It creates emphasis inside the headline rather than requiring a separate subheading. Second: feature bullets are replaced with compact `No. 1 / No. 2 / No. 3 / No. 4 / No. 5 / No. 6` numbered labels in a 3×2 grid, each with a 2–3 word descriptor underneath. No icons, no paragraph copy — just the name.

**Scores:**
- Uniqueness: 7/10 — Bold-in-headline isn't new (Medium pioneered it), but applying it to hero/section H2s rather than body copy is less common and gives it a different energy. The `No. X` grid is the more distinctive piece — it reads like a product spec sheet rather than a features sales pitch.
- Transferability: 8/10 — The selective bold works immediately in any headline ("Screen repairs **done same day**. Charging ports **fixed in an hour**."). The `No. X` numbered grid transfers well to a "What we fix" or "How we're different" section: `No. 1 Same-day repairs / No. 2 Upfront pricing / No. 3 Warranty included / No. 4 Text us anytime`.
- Personal taste: 8/10 — There's something satisfying about how the bold pulls your eye through the sentence to exactly the right words. It makes headlines scannable without sacrificing full readability. The `No. X` format has a deliberately non-marketing feel — confident to the point of being matter-of-fact.
- **Average: 7.7/10**

**Implementation brief:**
For selective bold headlines: use `<h2>` with `<strong>` wrapping only the key words (`font-weight: 700`), surrounding text at `font-weight: 400` or `300`. Keep the entire headline at the same `font-size` — the weight contrast does the work. For the `No. X` grid: create a `<div class="feature-grid">` with CSS Grid at `grid-template-columns: repeat(3, 1fr)` (2 columns on mobile). Each `<div class="feature-item">` gets a `<span class="feature-num">No. X</span>` at `font-size: 0.7rem`, `letter-spacing: 0.15em`, `color: #888`, followed by `<p class="feature-name">` at `font-size: 1rem`, `font-weight: 600`. No icons, no borders, no background cards — just text in a grid. The restraint is the design.

---

### 🥉 Find 9: Zero-Padded Sequential Stat Blocks (Clinical Confidence Format)
**Site:** Diag-Nose — [https://www.diag-nose.io](https://www.diag-nose.io)
**Found on:** Land-book — [https://land-book.com/websites/92439-diag-nose-io](https://land-book.com/websites/92439-diag-nose-io)
**What it is:** Social proof stats are displayed as a sequential list with zero-padded numeric indexes: `001 455M cases worldwide / 002 4M deaths per year / 003 $4.32T economic burden / 004 103.5M DALYs`. Each entry is a single row — index on the left, stat and label on the right. No icons, no cards, no chart. It reads like a data table, but the zero-padding and clean alignment give it the aesthetic weight of a scientific brief. The format implies authority rather than asserting it.

**Scores:**
- Uniqueness: 8/10 — The zero-padded index-as-design-element is genuinely unusual. Most stat sections use large numbers centered in cards, or a 3-up grid. This linear list format feels like a data dump from someone who knows the numbers are so strong they don't need decoration.
- Transferability: 8/10 — A repair shop can adapt this immediately for a proof section: `001 500+ devices repaired in Hailey / 002 Same-day repair rate: 94% / 003 Average repair time: 47 minutes / 004 Warranty: 90 days on all parts`. The clinical format gives small-scale numbers a weight they wouldn't have in a "fun fact" bubble layout. The format elevates the credibility of the data.
- Personal taste: 8/10 — It's the kind of design decision that requires confidence. You're betting that the numbers themselves are interesting enough that readers will follow them down the list. It's designed for people who actually read, not skim — and those are the customers you want.
- **Average: 8/10**

**Implementation brief:**
Create a `<div class="stat-list">` as a vertical stack. Each `<div class="stat-row">` uses `display: flex`, `align-items: baseline`, `gap: 24px`, `padding: 16px 0`, `border-bottom: 1px solid #eee`. Left column: `<span class="stat-index">` at `font-size: 0.7rem`, `font-weight: 400`, `color: #bbb`, `min-width: 32px` — contains `001`, `002`, etc. (pad manually or use CSS counters: `counter-increment: stat-row; content: "00" counter(stat-row)`). Right side: `<span class="stat-value">` at `font-size: 1.8rem`, `font-weight: 700`, followed by `<span class="stat-label">` at `font-size: 0.9rem`, `color: #666`. Keep the container left-aligned, `max-width: 600px`. Works best on a clean white or light gray background with no other visual elements competing.

---

## Scout Run — 2026-03-28 17:00 UTC
Sources checked: [Land-book](https://land-book.com/design/about-us-page) (About Us category), [Land-book](https://land-book.com/design/pricing-page) (Pricing category), [Godly](https://godly.website/) (fresh index pass)

### 🏆 Find 10: The Anti-FAQ Pricing Manifesto
**Site:** Monarch Money — [https://www.monarch.com/pricing](https://www.monarch.com/pricing)
**Found on:** Land-book — [https://land-book.com/websites/79795-pricing-monarch-money](https://land-book.com/websites/79795-pricing-monarch-money)
**What it is:** Instead of an FAQ section, Monarch's pricing page includes a 4-point named manifesto embedded directly *within* the pricing content — not below it. The four items are titled "Never any ads", "Industry-best data connectivity", "We never sell your data", and "We're not going anywhere." Each is a short paragraph making a specific claim about *why paying is better for you than using a free alternative*. It reads as a genuine argument, not a feature list. The page frames the pricing decision as a values alignment question: do you want to be the product, or the customer?

**Scores:**
- Uniqueness: 9/10 — This reframes the pricing objection ("why should I pay?") into a principled argument before the customer even thinks to ask. Most pricing pages just list features. This one argues a philosophy. I've never seen it structured this explicitly and placed this centrally on a pricing page.
- Transferability: 9/10 — A repair shop has an obvious version: "Why use a local repair shop instead of mailing it in?" or "Why us instead of the big-box store?" Same structure: 3–4 named principles — "We do it same day", "We stand behind our work", "You deal with one person, not a call center", "We're in Hailey because we live here." Same energy — a direct argument, not a brochure.
- Personal taste: 9/10 — The line "When you are paying for a service, you are the customer. Free services are incentivized to sell your data" is blunt and true, and it's on a *pricing page*. The boldness is what makes it work. It trusts the reader to process an argument instead of just scanning bullets.
- **Average: 9/10**

**Implementation brief:**
Create a `<section class="why-us-manifesto">` below the main CTA or service list. Open with a framing question: "Why choose a local repair shop?" or "Why pay someone local instead of mailing it in?" Then 3–4 `<div class="manifesto-point">` blocks — each with a `<h3>` (bold, short — "We do it same day", "You'll talk to the person fixing it") and a `<p>` (2–3 sentences, honest and specific). No icons, no checkmarks. Style: clean white or light-gray background, generous vertical padding, `max-width: 640px` centered. The power is in the copy being argumentative rather than declarative — each point should answer an actual objection a customer would have, not just restate a feature. Keep tone conversational. End the section with a single closing line: "That's why we're here." or similar — gives it the feel of a spoken argument, not a list.

---

### 🥈 Find 11: Numbered Journey Arc (Stage-Based Feature Sections)
**Site:** Mixpanel — [https://mixpanel.com](https://mixpanel.com)
**Found on:** Godly — [https://godly.website/website/mixpanel-962](https://godly.website/website/mixpanel-962)
**What it is:** Feature sections are structured as a numbered journey arc — `01 Acquire new customers / 02 Drive engagement / 03 Grow your user base` — where each number represents not just a feature but a *stage in the customer's life* with the product. Each stage gets a number label, a bold headline (the outcome), a one-line description, and a visual. The progression implies: "you don't just use our product, you go on a journey with it." The numbers make it feel like a roadmap rather than a checklist.

**Scores:**
- Uniqueness: 7/10 — Numbered sections are common, but the stage-of-life framing (acquire → engage → grow) rather than feature categories (analytics → reports → integrations) is more narrative and less catalog-like. It maps the customer's goals, not the product's capabilities.
- Transferability: 8/10 — Directly adaptable for a repair shop: `01 Bring it in (or text us a photo) / 02 We diagnose it fast / 03 You get it back, fixed`. That's the customer's journey through a repair. It's more honest and confidence-building than listing services, because it shows the whole experience arc rather than just capability claims.
- Personal taste: 7/10 — Clean, purposeful, and the numbered format gives it a sense of forward motion. Doesn't knock me over the way some other finds do, but it's solid and immediately usable. The "01" left-aligned above the section head is a quietly confident detail.
- **Average: 7.3/10**

**Implementation brief:**
Create a `<div class="journey-arc">` containing 3 `<div class="journey-step">` blocks. Each step: `<span class="step-num">` (e.g., `01`) in `font-size: 0.75rem`, `letter-spacing: 0.15em`, `color: #999`, displayed as a block above the headline. Then `<h3>` for the outcome headline — bold, ~1.5rem. Then `<p>` for a single descriptive sentence. Then an optional CTA link. Stack vertically on mobile; 3-column grid on desktop. Use a thin `border-top` or colored accent line on each block to visually anchor the number above the heading. The key to making this feel like a *journey* rather than a list is the choice of words — each step should be a customer-facing action or outcome ("Get your diagnosis fast"), not an internal product capability ("Advanced diagnostics engine").

---

### 🥉 Find 12: One-Paragraph Opinionated Intro (The Single-Block About)
**Site:** Kons — [https://kons.fyi](https://kons.fyi)
**Found on:** Godly — [https://godly.website/website/kons-1017](https://godly.website/website/kons-1017)
**What it is:** The entire site is a single paragraph of opinionated self-introduction: "It's been 14 years since I got into design. I now have clear principles, the main one being 'value instead of mindless execution'. It's easy to print generic solutions, but what we designers are hired for is our unique point of view and creative thinking." No logo, no nav, no services list — just a person making a case for who they are in plain prose. The directness is disarming. You know exactly what you're getting before you've even seen any work.

**Scores:**
- Uniqueness: 9/10 — Even among minimal sites, this is uncommonly stripped down. Most solo/studio sites still have a project grid or a services list. The decision to let a single paragraph carry all the weight is radical restraint. It works because the paragraph is genuinely opinionated — it says something specific, not generic.
- Transferability: 7/10 — Not for the full homepage, but perfect for the "About" or "Why us" page of a repair shop. A single paragraph like: "I've been fixing phones in Hailey since 2023. I don't waste your time with appointments. I don't give vague estimates. When I tell you it'll be done by 5pm, I mean it. Bring it in." — that paragraph, alone on a page with some breathing room, is more credible than any bullet-point capability list.
- Personal taste: 9/10 — The line "It's easy to print generic solutions" is doing a lot of work. It's a shot at the competition and a statement of values simultaneously. That's hard to write. The fact that a freelancer put this on their homepage instead of a portfolio carousel shows they understand that confidence is a product feature.
- **Average: 8.3/10**

**Implementation brief:**
For an "About" page or a mid-page section: create a `<section>` with `max-width: 680px`, `margin: 0 auto`, `padding: 80px 24px`. Single `<p>` element at `font-size: clamp(1.1rem, 2vw, 1.35rem)`, `line-height: 1.75`, `font-weight: 400`. No heading above it. No subheading after it. Just the paragraph. Let it breathe. The content must be genuinely opinionated — it needs at least one sentence that takes a position or makes a small claim that other shops *can't or wouldn't* make. Without that, it's just a bio. With it, it's a positioning statement. End with your name, a signature font, or a simple `— Sam, Hailey Device Repair` attribution in `font-style: italic`. Add a `background: #fdfdf9` (warm off-white) to distinguish it from the surrounding content. No other elements on this section.

---

## Scout Run — 2026-03-28 19:02 UTC
Sources checked: [CSS Design Awards](https://www.cssdesignawards.com/) (WOTD winners March 20–28), [Land-book](https://land-book.com/design/product-page) (Product Page category)

### 🏆 Find 13: Customer-Type Service Branching ("Three Paths Depending on Your Project")
**Site:** MERSI Architecture Studio — [https://www.mersi-architecture.com/process](https://www.mersi-architecture.com/process)
**Found on:** CSS Design Awards — [https://www.cssdesignawards.com/sites/mersi-architecture-studio/49039/](https://www.cssdesignawards.com/sites/mersi-architecture-studio/49039/)
**What it is:** Instead of a single "How it works" section, MERSI's Process page presents three completely separate service tracks organized by *who the customer is and what they're trying to do*: "Résidentiel pour utilisateur / Résidentiel pour investisseur / Retail concept pour marque." Each track gets its own framing sentence, its own bullet list, and its own CTA. The page starts with "Quel que soit le type de projet, notre méthode repose sur un cadre clair et éprouvé" (Whatever the project type, our method rests on a clear, proven framework) — then immediately branches by customer type. You're never reading about someone else's job.

**Scores:**
- Uniqueness: 8/10 — Most service businesses have one generic "our process" section. Branching it by customer type — who you are, what you want — treats visitors as distinct audiences rather than a monolith. I've seen this in SaaS pricing tiers but not structured as a process/service page for a small creative firm. The execution here is unusually clean.
- Transferability: 10/10 — Exact match for a repair shop with multiple customer types: "Personal device (cracked screen, battery)" vs. "Business devices (multiple phones, fleet management)" vs. "Water damage / emergency same-day." Each customer is coming with a different urgency and different questions. Showing them a path that matches their situation immediately reduces friction and builds trust before they've even texted you.
- Personal taste: 9/10 — It's the kind of organizational decision that shows you've actually thought about your customer instead of just listing your services. Reading the right track feels like the site is talking directly to you. The realization that "this is about me, not about them" is rare and memorable.
- **Average: 9/10**

**Implementation brief:**
Create a `<section class="service-paths">` with a brief intro paragraph ("Whatever brings you in, here's how it works") followed by 2–3 `<div class="path-track">` blocks. Each block opens with a `<h3 class="path-label">` — keep it short and customer-facing: "Cracked screen or battery" / "Water damage or emergency" / "Business / multiple devices". Below it, 4–6 `<li>` items describing the flow from that customer's perspective (e.g., "Text us a photo → get a quote in minutes → drop off when ready → done same day"). End each track with a `<a class="path-cta">` button: "Text us now" or "Book a same-day slot". On desktop use 2–3 columns; on mobile stack fully. Differentiate tracks subtly with `background-color` tint variations (e.g., `#f9f7f4` / `#f4f7f9`) rather than heavy borders. The key: each track should use *second-person* language ("you", "your device") not first-person ("we offer").

---

### 🥈 Find 14: Asymmetric Muted Tile Grid for Service Categories
**Site:** Jacques + Cie Dental Clinic — [https://jacques-cie.com](https://jacques-cie.com)
**Found on:** Land-book — [https://land-book.com/websites/90165-jacques-cie-clinique-dentaire-a-quebec-soins-dentaires-humains-and-professionnels-a-sainte-foy](https://land-book.com/websites/90165-jacques-cie-clinique-dentaire-a-quebec-soins-dentaires-humains-and-professionnels-a-sainte-foy)
**What it is:** The services section uses a CSS grid of muted, warm-gray rectangular tiles where each service category gets its own tile — but the tiles are *asymmetric*: some span two-thirds of the row, others one-third. No icons, no bold colors, no hover drop-shadows. Just the service name inside a softly rounded, lightly tinted background tile. The uneven sizing gives the grid visual rhythm without any decorative elements. The page's overall palette — warm off-white background, sage/gray tiles, pale blue footer — is completely calm for a healthcare site.

**Scores:**
- Uniqueness: 7/10 — Asymmetric grids are common in editorial/portfolio contexts, but applying them to a services list (which usually gets boring equal-width cards or a bullet list) is fresher. The combination with the muted palette and zero icons is the differentiator — most service grids use icons or bold accent colors to add visual interest. This gets there through proportion alone.
- Transferability: 8/10 — Direct steal for "What we fix": "iPhone screens" tile spans full width; "Charging ports" and "Batteries" share a row; "Water damage" spans 2/3; "Other Android" fills 1/3. The asymmetry makes the tile the customer most commonly needs (screen repairs) visually dominant without any hierarchical text needed. Pure layout as communication.
- Personal taste: 8/10 — The restraint here is the point. Dental clinics (like repair shops) are usually visually noisy — aggressive CTAs, stock photos, hard-sell copy. Jacques + Cie looks like a design studio that happens to do dentistry. That visual calm is itself a trust signal. A repair shop that looks this composed communicates competence before you've read a word.
- **Average: 7.7/10**

**Implementation brief:**
Create a `<div class="services-grid">` using CSS Grid: `grid-template-columns: repeat(3, 1fr)`, `gap: 12px`. Each `<a class="service-tile">` has `background: #e8e4df` (warm gray), `border-radius: 8px`, `padding: 24px 20px`, `min-height: 100px`. Set the service name as a `<span>` at `font-size: 1rem`, `font-weight: 500`. For asymmetry, use `grid-column: span 2` on 1–2 tiles (your most important services) and `grid-column: span 1` on the rest. Vary row heights with `min-height` differences — the "big" tile can be `140px`, others `100px`. No icons. No description text inside the tile. The name alone, set at the bottom-left with `align-self: end`, gives a clean label feel. On mobile, everything drops to `grid-template-columns: 1fr 1fr` with consistent sizing. The tile colors can all be the same muted shade or vary slightly (e.g., `#e8e4df` / `#dde0e4`) to add another layer of hierarchy without loudness.

---

### 🥉 Find 15: Brand Name Embedded Inside Hero Copy Word
**Site:** SŌM Power — [https://www.drinksom.eu](https://www.drinksom.eu)
**Found on:** CSS Design Awards — [https://www.cssdesignawards.com/sites/som-power/49068/](https://www.cssdesignawards.com/sites/som-power/49068/)
**What it is:** The CTA section hero reads: "BECOME SŌM[E]ONE POWERFUL" — the brand name "SŌM" is embedded inside the common word "SOMEONE," styled differently (heavier weight, brand color, with the macron over the O). "SOMEONE" becomes "SŌM•E•ONE" where the brand mark is visually distinct within the word. The headline lands its brand name and its aspiration in a single phrase rather than separately. It's typographically dense and confident — the kind of line that makes you read it twice.

**Scores:**
- Uniqueness: 9/10 — I genuinely haven't seen brand-name embedding done this cleanly in a headline. Nested wordmarks exist in logos, but using it as a copy device in a full sentence — where the brand name reads as a meaningful syllable chunk of a real word — is an unusual and clever play. The macron diacritic (Ō) adds a level of craft that signals the brand cares about visual details.
- Transferability: 6/10 — Somewhat low because it requires a brand name that phonetically embeds in a common word or phrase. "Hailey" doesn't embed as cleanly, though variations are possible: "RELI[ABLE] REPAIR" where the brand value is embedded in the adjective, or using the first letters of the shop name as a visual element within a headline. The *principle* transfers even if the exact technique is name-dependent.
- Personal taste: 9/10 — It's genuinely clever. The moment you parse "SOMEONE" and realize "SŌM" is in there, the brand lands twice — once as the visual surprise and once as the meaning. That double-register is the kind of thing that makes a headline memorable. The all-caps treatment with the contrast weight difference between SŌM and the surrounding letters gives it a graphic design poster quality.
- **Average: 8/10**

**Implementation brief:**
To embed a brand element within a headline word: identify a common word or phrase where the brand name (or its first letters, or a brand value word) appears as a syllable chunk. Wrap that fragment in a `<span class="brand-embed">` with `font-weight: 800` or a brand color, while the surrounding characters stay at `font-weight: 400` or a muted shade. The entire word should be one `<span>` container with `display: inline-block` at the same `font-size` — only weight and color vary internally. Keep the full headline in uppercase for maximum contrast impact. For Hailey Device Repair, consider: "PHONE [FIXED]" where "FIXED" is styled as the brand promise in a different weight; or "HAILEY REPAIRED" where HAILEY takes the brand color weight. The key is that the styled fragment has to mean something on its own — brand-colored noise inside a word reads as a typo, but brand-colored *meaning* reads as craft.

