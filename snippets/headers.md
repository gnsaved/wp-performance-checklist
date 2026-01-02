# Security headers (examples)

> Add via host panel / server config where possible. Test carefully.

## Conservative baseline (usually safe)
X-Content-Type-Options: nosniff
Referrer-Policy: strict-origin-when-cross-origin

## HSTS (ONLY if HTTPS is permanent everywhere)
Strict-Transport-Security: max-age=31536000; includeSubDomains; preload
