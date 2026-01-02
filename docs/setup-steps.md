# Setup Steps (Implementation Order)

## Step 0 — Safety
1. Backup (files + DB)
2. Work in staging if possible
3. Record baseline metrics (see audit-template)

## Step 1 — Remove bloat
1. Delete unused plugins/themes
2. Disable heavy features you don’t use
3. Identify and remove duplicate functionality

## Step 2 — Caching (biggest ROI)
1. Pick a caching approach (host cache OR plugin cache)
2. Configure exclusions (admin/logged-in/cart/checkout)
3. Enable browser cache headers
4. Purge cache and re-test

## Step 3 — Images
1. Enable WebP (and AVIF if supported)
2. Bulk optimize media library
3. Ensure lazy-load below fold
4. Fix huge hero images (dimension + compression)

## Step 4 — JS/CSS + fonts (careful)
1. Minify
2. Defer/delay non-critical JS
3. Optimize fonts (WOFF2, fewer weights)

## Step 5 — Security hardening
1. Enable 2FA for admins
2. Disable WP file editor
3. Verify file permissions (server-level)
4. Add WAF / rate limiting to login + forms

## Step 6 — Forms + spam protection
1. Add Turnstile/hCaptcha + honeypot
2. Add rate limiting
3. Test deliverability and confirmations

## Step 7 — Verify & document
1. Re-test Lighthouse/WebPageTest
2. Confirm user journeys
3. Complete handover template
