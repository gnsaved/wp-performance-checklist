# Quick Wins (30–90 minutes)

## Baseline (10 minutes)
- [ ] Run Lighthouse / PageSpeed on key pages (home + 1 heavy page)
- [ ] Note: LCP, INP, CLS, TTFB, page weight, request count
- [ ] Confirm hosting stack (LiteSpeed? Nginx? Managed WP?)

## Caching (10–20 minutes)
- [ ] Enable one caching layer (plugin or host cache — not both aggressively)
- [ ] Exclude:
  - [ ] /wp-admin/*
  - [ ] logged-in users
  - [ ] cart/checkout/account (WooCommerce)
- [ ] Enable browser cache headers (via cache plugin/host)

## Images (10–25 minutes)
- [ ] Convert new uploads to WebP (and AVIF if supported)
- [ ] Enable lazy-load (native or plugin)
- [ ] Make sure hero images have explicit width/height
- [ ] Compress existing media in bulk

## Cleanup (10–20 minutes)
- [ ] Remove unused plugins/themes
- [ ] Disable heavy page builder modules you don’t use
- [ ] Turn off heartbeat for admin-only (if safe for your workflow)

## Security (10–20 minutes)
- [ ] Turn on 2FA for admins
- [ ] Ensure auto-updates for minor WP releases + security updates
- [ ] Disable WP file editor (wp-config)
- [ ] Confirm backups exist before changes

## Forms / Spam (10–20 minutes)
- [ ] Add Turnstile or hCaptcha to forms
- [ ] Enable honeypot
- [ ] Add basic rate-limit / anti-bot for submissions
