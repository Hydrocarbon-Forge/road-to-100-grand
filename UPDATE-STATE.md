# UPDATE-STATE — post-batch checklist for C6

Run this after EVERY build batch, before reporting done. Generic procedure;
Batch-2 values filled in as the worked example.

## 1. Verify files exist (every file the brief promised)

```bash
cd ~/HydrocarbonForge/Projects/road-to-100-grand
find dist assets -type f | sort
```

Batch-2 expected (11 new files):
`dist/landing/index.html`, `dist/landing/sample.html`,
`dist/landing/pricing-calculator.html`, `dist/social/queue.md`,
`dist/outbound/README.md`, `dist/outbound/startup-founders.md`,
`dist/outbound/agency-owners.md`, `dist/outbound/ecommerce.md`,
`dist/outbound/local-biz.md`, `dist/outbound/creators.md`, `dist/README.md`,
plus this file `UPDATE-STATE.md`.

## 2. Verify HTML serves + has no external deps

```bash
cd dist/landing && python3 -m http.server 8131 >/dev/null 2>&1 &
sleep 1
curl -s -o /dev/null -w "index:%{http_code}\n" http://localhost:8131/index.html
curl -s -o /dev/null -w "sample:%{http_code}\n" http://localhost:8131/sample.html
curl -s -o /dev/null -w "calc:%{http_code}\n" http://localhost:8131/pricing-calculator.html
kill %1
grep -r -i -E 'src="http|href="http|<link[^>]*cdn|unpkg|jsdelivr' dist/landing/ || echo "OK: no external refs"
```

All three must return HTTP 200. The grep must print `OK: no external refs`
(`mailto:` links are fine — they contain no `src="/href="http`).

## 3. Verify content rules

```bash
# queue posts are verbatim from content-pack (spot-check 2-3 against source)
diff <(sed -n '/Day 1 /,/^$/p' dist/social/queue.md) assets/content-pack/01-fixed-vs-hourly.md
# outbound: 20 templates? (5 files × 4: email + LinkedIn + Discord/Slack + follow-up)
grep -c '^## ' dist/outbound/*.md
# no lorem / fabricated metrics language
grep -r -i -E 'lorem|guaranteed (income|revenue|results)|10x your' dist/ assets/ || echo "OK: clean"
```

## 4. Update `state.json`

- Append to `assets`: `{"id": "<batch-id>", "status": "verified", ...}` with
  real file count and price (never invent revenue).
- Rewrite `current_step` to the completed batch.
- Rewrite `next_actions`: completed items OUT, new next steps IN.
- Leave `cash_balance_usd` at 0.00 until real payment rails + real sales.
- Keep `blockers` honest (drop resolved ones, keep the rest).

## 5. Report

Print the final file list (`find dist -type f | sort`) + what was verified.
Never claim sales, traffic, or revenue — $0 until real rails.
