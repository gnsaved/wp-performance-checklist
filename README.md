# wp-performance-checklist

A practical, field-tested checklist for speeding up and hardening WordPress sites — plus plugin recommendations and setup steps.

**Covers:**
- Caching (page / object / CDN)
- Images (WebP/AVIF, lazy-load, sizing)
- Security hardening (WP + server hygiene)
- Forms + spam protection (Turnstile/hCaptcha, honeypot, rate limits)

**Last reviewed:** 2026-01-02

---

## How to use this repo (fast)
1. Start with **checklists/00-quick-wins.md**
2. Baseline your site using **docs/audit-template.md**
3. Pick ONE plugin per category from **docs/plugin-recommendations.md**
4. Implement in order using **docs/setup-steps.md**
5. Handover using **docs/handover-template.md**

> Tip: Don’t “stack” multiple caching or optimization plugins. Pick one primary tool + minimal add-ons.

---

## Recommended stacks (choose one)

### Stack A — LiteSpeed hosting (simple + powerful)
- Cache: **LiteSpeed Cache**
- Images: **ShortPixel** OR **Imagify** OR **EWWW**
- Security: **Wordfence** OR **Solid Security**
- Forms: **WPForms / Gravity Forms / Ninja Forms**
- Spam: **Cloudflare Turnstile** (or hCaptcha) + honeypot + Akismet (optional)

### Stack B — Any host (managed cache plugin)
- Cache: **WP Rocket** (paid) OR **WP Super Cache** (free)
- Images: **ShortPixel / Imagify / EWWW**
- Security: **Wordfence / Solid Security**
- Spam: **Turnstile/hCaptcha** + rate limiting

### Stack C — Cloudflare-first (CDN edge focus)
- CDN: **Cloudflare** (+ APO if used)
- Cache: Keep WP cache light (avoid double-caching confusion)
- Images: **ShortPixel / EWWW / Optimole**
- Security: Cloudflare WAF rules + WP security plugin

---

## What “good” looks like (targets)
- Fast initial render on mobile, no layout jumps
- Stable caching (no logged-in pages cached)
- Images sized correctly + served as WebP/AVIF
- Forms protected without ruining UX
- Updates + least privilege + monitoring in place

---

## Contents
- **checklists/** actionable checklists (copy into tickets)
- **docs/** setup steps, plugin picks, audit + handover templates
- **snippets/** safe wp-config + header snippets
- **.github/** issue + PR templates for delivery workflow

---

## License
MIT — use freely in your own work.
