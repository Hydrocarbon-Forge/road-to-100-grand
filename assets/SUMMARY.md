# SUMMARY — Batch 1: Monetizable Digital Product Suite

## What was built

A sellable "AI Agency Starter Kit" product pack for Hydrocarbon Forge's Road
to 100 Grand project — a business-in-a-box for running a one-person
AI-assisted web dev studio (free pitch → $5/hr idea calls → per-build fixed
quotes → launch). Plus a self-contained landing page, a 12-post distribution
content pack, and this summary. Total production cost: $0.

## File list (22 files)

**Starter kit (`assets/ai-agency-starter-kit/`) — 7 files:**
- `README.md` — how to use the kit, business model, $0 tool stack
- `business-plan.md` — one-page fill-in business plan (niche, offer ladder, outreach engine, 90-day goals)
- `pitch-playbook.md` — 3 cold email + 3 DM templates (LinkedIn/Discord/Slack) + 6 objection handlers + tracking sheet
- `pricing-calculator.html` — offline HTML+JS quote calculator (pages × $80 + features + revisions, rush option, deposit split, timeline estimate, copy-for-proposal button)
- `client-contract-template.md` — one-page service agreement template (scope, 50/50 payment, 2 revisions, 14-day bug window; placeholder terms, not legal advice)
- `sops.md` — 5 SOPs: onboarding, scoping call, build handoff, revisions, launch & support
- `client-email-templates.md` — 10 emails: lead → welcome → scoping → proposal → follow-up → payment → delivery → upsell → referral → winback

**Landing page (`assets/`) — 1 file:**
- `index.html` — dark modern mobile-friendly page: hero with pitch→call→build→launch diagram (inline SVG), truthful "what's inside" cards for all 6 kit files, real sample excerpts, who-it's-for, FAQ, $49 buy section with mailto placeholder. No CDNs, no network images.

**Content pack (`assets/content-pack/`) — 13 files:**
- `01-fixed-vs-hourly.md` through `12-track-outreach.md` — 12 posts, each under 400 chars, substance-first, no engagement-bait
- `README.md` — posting guide (cadence, per-platform adaptation, soft CTA rule)

**This file (`assets/`) — 1 file:**
- `SUMMARY.md`

## Suggested price points ($29–$99 rationale)

- **Recommended launch price: $49 one-time.** Reasoning: inside the brief's $29–$99 band; low enough for impulse buy by an aspiring freelancer (pays for itself with a fraction of one $5 call → one build), high enough to signal real templates rather than a freebie PDF. Comparable solo "business-in-a-box" template packs sell in the $29–$79 range; $49 sits at the credible middle.
- **Floor ($29):** use for launch-week discount or bundle with idea calls ("kit + $5 scoping call") to drive first reviews without devaluing the product.
- **Ceiling ($79–$99):** justified only after adding proof assets — e.g., 3+ sample filled-in scopes, a video walkthrough, or buyer testimonials. Do not launch at $99 with zero reviews.
- **No subscriptions:** one-time price matches the audience (beginners hate recurring fees) and the product (static files, no maintenance burden).
- **Raise rule:** after 10 sales at $49 with positive feedback, test $69. If close rate stays above ~5% of landing-page visitors who email, keep it.

## Distribution channels that cost $0

1. **Content pack rotation** — post 3–4x/week from `content-pack/` on X, LinkedIn, and relevant Reddit/Discord/Slack communities (only where self-promo is allowed). Soft CTA at most 1x/week pointing at the landing page.
2. **Landing page on free hosting** — deploy `index.html` + kit folder to Cloudflare Pages / Netlify / GitHub Pages (free tiers). Share the URL in profiles and outreach footers.
3. **Direct outreach** — use the kit's own pitch playbook to sell the kit: personalized emails/DMs to aspiring freelancers, bootcamp grads, and indie-hacker communities.
4. **Free marketplaces** — Gumroad free tier / Ko-fi / Payhip (pay-per-sale, no upfront cost) once payment rails exist; link from the landing page's Buy section.
5. **Build-in-public + referrals** — document Batch 1 → first sales; ask every buyer for a testimonial + referral via the kit's own referral email pattern.
6. **Communities & SEO basics** — answer "how to price freelance web work" questions with genuine help + a kit link where rules permit; title/meta already set on the landing page.

## Verification performed

- All files referenced by `index.html` and `README.md` confirmed to exist on disk.
- `index.html` served via `python3 -m http.server` and checked with `curl` → HTTP 200.
- `pricing-calculator.html` opened and its quote math spot-checked (base + pages + features + revisions + rush paths).
- All 12 content posts checked to be under 400 characters.
- No external CDN, font, or image dependencies; no lorem ipsum; no fabricated metrics or income claims.

## Next steps (Batch 2 candidates)

- Wire a real payment link (Gumroad/Ko-fi) into the Buy section, replacing the mailto placeholder.
- Add 2–3 filled-in example scopes as social proof.
- Record a 5-min calculator walkthrough (free screen recorder) and embed as a local video file or unlisted free-tier host.

## Restoration note (Batch 2, 2026-10-02)

The original Batch-1 files on disk were lost to an environment wipe mid-Batch-2
(see `state.json` notes). `index.html`, `content-pack/` (13 files), kit
`README.md`, and this `SUMMARY.md` were restored verbatim from verified session
context. The remaining kit files (`business-plan.md`, `pitch-playbook.md`,
`pricing-calculator.html`, `client-contract-template.md`, `sops.md`,
`client-email-templates.md`) were rebuilt to the Batch-1 brief spec and are
marked REBUILT at the top — review them before selling the kit.
