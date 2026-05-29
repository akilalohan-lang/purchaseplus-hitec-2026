# HITEC 2026 Pitch Deck Instructions

Instructions for building the HITEC positioning pitch deck Akila will present to Malcolm. The goal of the deck is to align the CEO on the booth concept, theme, messaging, and run-of-show before any production money is spent.

A reference deck already exists. Use it as the template for structure, voice, and brand. Do not invent a new design language.

## Reference deck

**Local source HTML:** /Users/lmh/Documents/PurchasePlus GTM Strategy/promotion_pitch.html

That file is the 9-slide pitch deck used in the 6 May 2026 promotion meeting. Single-file HTML, self-contained, opens in any browser. Vanilla JS, no framework. Sidebar nav, one slide at a time, arrow keys to advance, click sidebar to jump.

## Live deployment (encrypted)

The promotion deck is encrypted via staticrypt and hosted on GitHub Pages.

- Repo: https://github.com/akilalohan-lang/pp-pitch-2026
- Local repo clone: /Users/lmh/pp-pitch-2026
- Promotion pitch URL: https://akilalohan-lang.github.io/pp-pitch-2026/pitch.html
- GTM Machine demo URL: https://akilalohan-lang.github.io/pp-pitch-2026/demo.html
- Password (both files): PurchasePlusGTM5000

To deploy a new HITEC deck the same way:

1. Write the new deck as `hitec_pitch.html` in /Users/lmh/Documents/Events Agent/HITEC/.
2. Copy it into the deploy folder: `cp hitec_pitch.html /Users/lmh/pp-pitch-2026/hitec.html`.
3. Encrypt in place: `cd /Users/lmh/pp-pitch-2026 && npx staticrypt hitec.html -p "PurchasePlusGTM5000" -d . --short` (re-uses the existing password so Malcolm only needs to remember one).
4. Commit and push: `git add . && git commit -m "Add HITEC pitch deck" && git push`.
5. GitHub Pages redeploys within ~60 seconds. Share https://akilalohan-lang.github.io/pp-pitch-2026/hitec.html with the password.

## Brand and design rules (hard constraints)

These are non-negotiable. They match how PurchasePlus presents itself elsewhere.

- White background, Inter font (weights 200, 300, 500, 600).
- Brand gradient: linear-gradient(90deg, #a956ff 0%, #7c5dff 50%, #3766fe 100%). Applied to key emphasis phrases via a `.grad` class with an animated background-position pulse.
- `text-wrap: balance` applied to the slide root for h1, h2, h3, h4, p. Always. No orphaned words.
- CTA buttons (if any) get `white-space: nowrap` so the label never breaks onto two lines.
- **Never use em-dashes** (the character `—`). Use comma, period, parentheses, colon, or semicolon instead.
- No emojis anywhere.
- Logos live at /Users/lmh/Documents/PurchasePlus GTM Strategy/assets/. Use `logo.png` (horizontal) and `logo-emblem.png` (square mark). Copy them into the deploy folder under `assets/` so the encrypted deck can resolve them.

## Navigation pattern (preserve from reference deck)

- Left sidebar, ~260 px wide, fixed.
- Slide list with two-digit numbers and titles.
- Click a slide to jump.
- Arrow Up / Down / Left / Right, PageUp / PageDown, Space, Home, End all navigate.
- Slide eyebrow number must match the sidebar number for that slide. Cover slide has no eyebrow number.
- Footer: slide counter (01 / 09), thin gradient progress bar, brand stamp on the right.
- Vertical up / down buttons bottom-right.

## Voice rules

- Senior, calm, short. No emotional appeals, no "I'd dedicate my life" pleas.
- US is the headline market. UK is the second move. Do not mention APAC or UAE.
- Investor name is **Strattam** (US PE, B2B SaaS specialist). Never spell it Stratton.
- CEO is **Malcolm Jull**, address as Malcolm.
- Akila's title: **Head of Marketing, Global** at PurchasePlus, with full GTM ownership, reports to CEO. Confirmed and accepted 2026-05-14.
- Always positive framing. Do not talk down on sales, product, brand, or any existing capability. Position the company as ready, with the right people, with the foundation already shipped.

## Slide structure to adapt

The reference deck uses these nine slides. Adapt the same scaffold for HITEC, keeping the numbering and the eyebrow-matches-sidebar rule.

1. Cover. Event name, location, dates, who is presenting, who it is for.
2. The Opportunity. Why HITEC matters and why now. TAM and readiness language, not problem language.
3. The Frame. Akila's positioning at the show. The role he plays, the story he tells, the team he is leading.
4. The Engine. The GTM Machine product story. Live demo plan on the booth.
5. The Team. AI agents do the work. People build and own the product. Lean US footprint.
6. The Show Experience. Booth concept, theme, on-stand experience, run-of-show. (This replaces GEO+ASO from the reference deck.)
7. The 12-Month Plan post-HITEC. Lead capture, follow-up sequences, deal targets, pipeline forecast off the show.
8. The 5-Year Plan reinforcement. How this booth is the start of a 5x trajectory in the US.
9. Why This Bet. The unit economics of the show. $10,580 booth + rentals vs the pipeline it unlocks.

If a slide needs a different sub-topic, replace it but keep the count at nine unless Akila signs off on more.

## Booth and event-specific content cues for slide 3 and slide 6

Akila's theme for the show (from the brief):

- Texas + ambition. Cowboy wild west crossed with Houston space rocket going to the moon.
- Confident, frontier, fast, big.
- A statement booth, not a polite SaaS demo box.

Tagline workshopping (final to be picked):

- PurchasePlus. AI-powered procurement. Built and kept by people, operated by AI agents.
- Built by people, operated by AI agents.
- Made by people, run by AI agents.

The deck should converge on one final tagline and use it across the cover, the closing CTA, and the booth concept slide.

## How to request the deck

In a new Claude session, with this folder as context, say:

> Build me a 9-slide pitch deck for HITEC 2026 at /Users/lmh/Documents/Events Agent/HITEC/hitec_pitch.html. Use /Users/lmh/Documents/PurchasePlus GTM Strategy/promotion_pitch.html as the template. Brief is in 00_BRIEF.md, event facts in 01_EVENT.md, vendor contacts in 04_VENDORS.md. Follow this file's brand and voice rules exactly. Open it in the browser when done.

The agent should:

1. Read the brief, event facts, vendor list, and this instructions file.
2. Read promotion_pitch.html to extract the exact CSS, navigation, and slide patterns.
3. Write hitec_pitch.html in this folder, using PurchasePlus brand and the 9-slide scaffold.
4. Open it in the browser for review.
5. After Akila approves, copy to the deploy folder, encrypt with staticrypt, commit, push. Share the live URL and password.
