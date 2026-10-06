# BUILD BRIEF — Road to 100 Grand, Batch 1: Monetizable Digital Product Suite

You are building batch 1 of a $0-cost monetization project for Hydrocarbon Forge
(Gavin + Nathan, a build-anything studio: free pitch, $5/hr idea calls,
per-build quotes, pitch→call→build→launch).

## Goal
Create a genuinely useful, sellable digital product pack that costs $0 to
produce and can be sold (templates + content + code) once payment rails exist.
No fabricated claims. Everything must be real, working, high quality.

## Deliverables (all inside ~/HydrocarbonForge/Projects/road-to-100-grand/assets/)

1. `ai-agency-starter-kit/` — a complete business-in-a-box for someone who wants
   to run a one-person AI web dev agency (Gavin's exact business model). Include:
   - `README.md` — how to use the kit, what's inside
   - `business-plan.md` — one-page business plan template, fill-in, specific to
     AI web dev studios (pricing: free pitch → $5/hr idea calls → per-build quotes)
   - `pitch-playbook.md` — how to pitch cold: 3 email templates + 3 DM templates
     (LinkedIn/Discord/Slack), objection handling (price, "can't we just hire a
     dev", "why not use [template site]")
   - `pricing-calculator.html` — self-contained HTML+JS (no CDNs, offline):
     client inputs project scope (page count, features, revisions) → outputs a
     quote breakdown with per-build quote math
   - `client-contract-template.md` — simple 1-page service agreement template
     (placeholder terms; note it's not legal advice)
   - `sops.md` — 5 core SOPs: onboarding, scoping call, build handoff,
     revisions, launch & support
   - `client-email-templates.md` — 10 email templates (lead → welcome → scoping
     → proposal → follow-up → payment → delivery → upsell → referral → winback)
2. `index.html` — product landing page for the starter kit: hero, what's
   inside, sample content, FAQ, "buy" section that links to a DM/lead form
   (mailto placeholder). Self-contained, no external CDNs, dark modern design,
   mobile-friendly. Must reference the kit contents truthfully.
3. `content-pack/` — 12 ready-to-post short posts (Markdown, each < 400 chars,
   no hashtags-only spam) about AI web dev business topics, for X/LinkedIn/
   Reddit-style distribution. Real substance, no engagement-bait.
4. `SUMMARY.md` — what was built, file list, suggested price points ($29–$99
   range rationale), distribution channels that cost $0.

## Rules
- All files real content, zero lorem ipsum, zero fabricated metrics.
- No external dependencies (no CDN, no images requiring network; use inline SVG
  or CSS-only visuals if needed).
- Verify: every referenced file exists; index.html opens (python3 -m http.server
  check via curl for 200).
- When done, print a final summary listing all created files.

Work in ~/HydrocarbonForge/Projects/road-to-100-grand/assets/ (create it).
