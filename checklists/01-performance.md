# Performance Checklist (WordPress)

## 1) Measure first (don’t guess)
- [ ] Lighthouse (mobile) + note LCP/INP/CLS/TTFB
- [ ] WebPageTest or similar for waterfall + TTFB
- [ ] Identify top offenders: images, JS bundles, fonts, third-party scripts

## 2) Hosting & server fundamentals
- [ ] PHP up to date (latest supported by host)
- [ ] HTTP/2 or HTTP/3 enabled
- [ ] TLS enabled (no mixed content)
- [ ] OPcache enabled (ask host if unsure)
- [ ] Object cache available? (Redis/Memcached)

## 3) Caching strategy (pick a primary)
### Page cache
- [ ] Enable page caching
- [ ] Set exclusions (admin, logged-in, cart/checkout/account)
- [ ] Cache warmup/preload enabled if available

### Object cache (if site is dynamic)
- [ ] Enable Redis/Memcached (host or plugin)
- [ ] Validate it’s actually working (hit count/memory usage)

### CDN
- [ ] Enable CDN for static assets (images/css/js)
- [ ] Confirm proper cache headers + purge workflow

## 4) CSS/JS delivery (avoid breaking pages)
- [ ] Minify CSS/JS (safe mode)
- [ ] Defer non-critical JS
- [ ] Delay third-party scripts where possible (chat widgets, trackers)
- [ ] Remove unused CSS (only if tooling is reliable on your theme)

## 5) Fonts
- [ ] Use WOFF2 only (where possible)
- [ ] Self-host fonts or reduce variants
- [ ] Use font-display: swap
- [ ] Preload only the primary font used above-the-fold

## 6) Images (biggest wins)
- [ ] Serve WebP/AVIF
- [ ] Correct dimensions (no 4000px images displayed at 400px)
- [ ] Lazy-load below the fold
- [ ] Preload hero image (only 1)
- [ ] Use responsive srcset

## 7) Database & content hygiene
- [ ] Limit post revisions
- [ ] Clean transients + orphaned data occasionally
- [ ] Optimize autoloaded options (advanced)

## 8) WooCommerce (if applicable)
- [ ] Don’t cache cart/checkout/account
- [ ] Reduce heavy fragments / ajax calls where possible
- [ ] Audit plugins adding frontend scripts everywhere

## 9) Verify after each change
- [ ] Re-test Lighthouse (mobile)
- [ ] Check critical journeys:
  - [ ] login/logout
  - [ ] search
  - [ ] forms submit
  - [ ] checkout (if any)
- [ ] Confirm caching isn’t serving private content
