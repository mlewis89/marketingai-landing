# MarketingAI — $149 AUD Setup Offer Landing Page

Public-facing landing page converting cold email responses into paying customers.

---

## Live URL

**https://mlewis89.github.io/marketingai-landing/**

GitHub Pages — auto-deploys within ~60s of any push to `main`.

---

## Deployment Status

| Component | Status | Detail |
|-----------|--------|--------|
| GitHub repo | ✅ Live | https://github.com/mlewis89/marketingai-landing |
| GitHub Pages | ✅ Live | https://mlewis89.github.io/marketingai-landing/ |
| Calendly CTA | ✅ Secondary | https://calendly.com/mark-neutrino/30min (secondary CTA only — Stripe is primary) |
| Stripe payment link | ✅ Live | https://buy.stripe.com/cNi8wR0wZd8lePh01cbsc00 |

---

## Pending Actions

### 1 — Stripe payment link (founder)
Once the founder completes Stripe setup (see [NMA-37](/NMA/issues/NMA-37)):

In `index.html`, find:
```html
<a href="#" class="btn-secondary disabled" id="buy-now-btn" aria-disabled="true">
  Buy now — coming soon
</a>
```

Replace with:
```html
<a href="STRIPE_PAYMENT_LINK_URL" class="btn-primary" id="buy-now-btn" target="_blank" rel="noopener">
  Buy now — $149 AUD
</a>
```

Then push:
```bash
cd product/code/marketingai-landing
git add index.html && git commit -m "Add Stripe payment link" && git push
```

### 2 — Custom domain (optional, founder)
To serve from a custom subdomain (e.g. `go.getmarketingai.com.au`):
1. Add CNAME DNS record pointing to `mlewis89.github.io`
2. Add a `CNAME` file to this repo containing the subdomain
3. Enable custom domain in GitHub Pages settings

---

## Page Structure

| Section | Content |
|---------|---------|
| Hero | Headline + subheadline + Calendly CTA |
| Problem | 3 pain points of AU SMB marketing |
| Solution | 3 systems: AI Funnel Machine, Outbound Engine, Creative Goldmine |
| Offer | $149 AUD one-off, what's included, no lock-in |
| Social proof | Honest placeholder — "be our first client" |
| Footer | ACL-compliant legal disclaimer |

---

## Reuse for Client #2

1. Copy this directory to `product/code/[client-slug]-landing/`
2. Update branding, copy, and CTA links in `index.html`
3. Create a new GitHub repo and push
4. Enable GitHub Pages
5. ~30 minutes per new client
