# Security Checklist (WordPress)

## 1) Updates & access control
- [ ] Enable auto-updates for WP core (minor/security)
- [ ] Update plugins/themes weekly (or use managed updates)
- [ ] Remove unused plugins/themes (attack surface)
- [ ] Enforce strong passwords + 2FA for admins
- [ ] Least privilege: no “admin for everyone”

## 2) WP hardening
- [ ] Disable file editing in wp-admin (DISALLOW_FILE_EDIT)
- [ ] Protect wp-config.php permissions (server-level)
- [ ] Ensure unique salts/keys (rotate if compromised)
- [ ] Limit login attempts / brute-force protection

## 3) Perimeter protection
- [ ] WAF enabled (host or Cloudflare)
- [ ] Block common bad bots / XML-RPC abuse (only if your site doesn’t need it)
- [ ] Rate limit wp-login.php

## 4) Monitoring & backups
- [ ] Daily backups (files + DB), offsite storage
- [ ] Malware scanning schedule
- [ ] Basic uptime monitoring
- [ ] Log review process (weekly)

## 5) Basic secure headers (careful)
- [ ] X-Content-Type-Options: nosniff
- [ ] Referrer-Policy configured
- [ ] HSTS only if you’re sure HTTPS is permanent
- [ ] CSP only if you can test thoroughly

## 6) Incident readiness
- [ ] Know how to disable plugins via SFTP
- [ ] Restore procedure tested
- [ ] Admin user list audited monthly
