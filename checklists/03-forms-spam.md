# Forms + Spam Protection Checklist

## 1) Decide your form stack
- [ ] WPForms / Gravity Forms / Ninja Forms / Contact Form 7 (choose based on project needs)
- [ ] Confirm mail delivery approach (PHP mail vs SMTP)

## 2) Spam prevention (layered)
- [ ] Add Turnstile or hCaptcha on all public forms
- [ ] Enable honeypot
- [ ] Add minimum submission time (anti-bot)
- [ ] Block suspicious keywords + countries (if relevant)
- [ ] Add rate limiting (per IP/email)

## 3) Deliverability (optional but recommended)
- [ ] Use SMTP plugin + verified domain (SPF/DKIM/DMARC)
- [ ] Ensure form “From” uses your domain (avoid spoofing)
- [ ] Store submissions safely (avoid exposing PII publicly)

## 4) Testing
- [ ] Submit test entries from:
  - [ ] normal browser
  - [ ] mobile
  - [ ] VPN (optional)
- [ ] Confirm confirmations/notifications work
- [ ] Confirm captcha doesn’t block legit users
