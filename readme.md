# GoodLife website starter

Responsive website starter inspired by the general category of Nigerian fintech/VTU platforms, using original GoodLife branding rather than copying RetpicAfrica source code.

## Files
- `index.html` — landing page, services, rewards, FAQ, responsive nav and sign-up/login demo modal
- `styles.css` — responsive visual design
- `app.js` — front-end interactions only
- `dashboard.html` — sample customer dashboard
- `admin.html` — sample admin dashboard layout
- `privacy.html`, `terms.html` — draft policy pages; replace with professionally reviewed versions

## Preview
Open `index.html` in a browser. Or run a local server from this folder with `python -m http.server 8000`, then open `http://localhost:8000`.

## Important limitations
This is a static front-end starter, not a production financial platform. The login form does not create accounts. Wallet amounts and transactions are illustrative sample data. There is no real authentication, database, wallet ledger, payment, airtime, bill payment, referral payout or withdrawal. `admin.html` is intentionally only a preview and must not be treated as a protected admin system. Do not collect real passwords or money using this demo.

## Production integrations required
1. **Backend/API and database:** for example, Node.js with Express/NestJS or Laravel/Django, and PostgreSQL.
2. **Authentication:** secure server sessions or a managed auth service, password hashing (Argon2id/bcrypt), email/phone verification, reset flow, MFA for admins and role-based access.
3. **Payments/wallet funding:** onboard with a supported provider such as Paystack or Flutterwave. Use hosted/secure checkout, server-side verification and signed webhooks. Never trust a browser redirect as proof of payment.
4. **Airtime/data/electricity/cable:** business account and API contract with a VTU aggregator/provider. Keep secrets server-side; implement idempotency, timeouts, provider status checks, reversals/refunds and reconciliation.
5. **Wallet accounting:** immutable ledger (preferably double-entry), atomic balance updates, idempotency keys, transaction limits, audit trails and daily reconciliation. Do not treat a front-end number as a balance.
6. **Referrals/tasks/rewards:** eligibility rules, proof submission and moderation, fraud detection, duplicate-account prevention and ledgered reward balances. Review applicable advertising and platform rules.
7. **Withdrawals:** payout provider, bank-account ownership verification, admin review policies, fraud controls and status reconciliation.
8. **Launch readiness:** legal/privacy review for Nigeria, clear terms/refund policy, support contact, security testing, backups, monitoring, rate limiting, incident plan and provider approval.

## Hosting and domain
- **Static demo:** deploy this folder on Netlify, Vercel or Cloudflare Pages. Netlify can provide a temporary `*.netlify.app` address and supports custom domains.
- **Production:** host the front end separately from the protected API/database. Use managed PostgreSQL and a server host that supports secrets/environment variables. Enforce HTTPS.
- **Domain suggestions:** check `goodlife.com`, `goodlife.ng`, `goodlife.com.ng`, or a more distinctive variation such as `mygoodlife.ng` or `goodlifehub.com.ng`. Availability is not checked, and the word “GoodLife” may already be used by other businesses; check domain availability and trademark/business-name conflicts before purchase.
- Compare renewal prices, DNS controls and support before paying. Do not send domain registrar passwords to a developer.
