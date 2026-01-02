# Plugin Recommendations (Pick ONE per category)

> Goal: minimal plugins, maximum impact. Don’t install 3 optimization plugins that overlap.

## Caching (page/cache)
- LiteSpeed hosting: **LiteSpeed Cache**
- General free options: **WP Super Cache**, **W3 Total Cache**, **Cache Enabler**
- Paid (often simplest): **WP Rocket**

## Object cache (if available)
- **Redis Object Cache** (when Redis is enabled on host)

## Images (compression + WebP)
- **ShortPixel**
- **Imagify**
- **EWWW Image Optimizer**
- **Smush**
- **Optimole** (CDN-style optimization)

## Security (pick one primary)
- **Wordfence**
- **Solid Security** (formerly iThemes Security)
- **Sucuri Security** (site monitoring, hardening)

## Forms
- **WPForms** (easy)
- **Gravity Forms** (advanced)
- **Ninja Forms** (flexible)
- **Contact Form 7** (simple, add anti-spam layers)

## Spam protection
- **Cloudflare Turnstile** integration (best UX)
- **hCaptcha** (privacy-friendly alternative)
- **Akismet** (comment spam; can help form spam in some setups)
- **Antispam Bee** (comments, lightweight)

## Notes on conflicts (avoid these combos)
- Don’t use two page caching plugins together
- Don’t run multiple minify/asset-optimization plugins together
- If host has full-page cache, keep plugin caching conservative
