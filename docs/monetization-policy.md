# Monetization, Ads, and Sponsorship Policy

This document outlines the self-serve advertising rate card, sponsor partnership criteria, and serverless Telegram relay architecture for Awesome Tech Talks.

---

## 1. Overview and Model Comparison

Awesome Tech Talks supports sustainable community maintenance through three distinct engagement channels:

| Channel | Ads (`/ads`) | Sponsors (`/sponsors`) | Donations (`/donate`) |
|---|---|---|---|
| **Relationship** | Transactional, self-serve | High-touch, strategic partnership | Community goodwill, voluntary |
| **Pricing** | Fixed rate card (public) | Custom / negotiated | Any voluntary amount |
| **Placement** | Featured video rail or banner | Landing page "Sponsors" strip | Supporter wall (optional) |
| **Verification** | Payment proof upload required | Inquiry form (followed up by owner) | Payment proof upload optional |
| **Delivery** | Telegram Ads Bot | Telegram Sponsors Bot | Telegram Donations Bot |
| **Activation** | Owner updates `data/ads.json` | Owner replies manually | Owner acknowledges |

---

## 2. Self-Serve Ad Rate Card

| Placement Tier | Format | Position | Duration | Rate |
|---|---|---|---|---|
| **Featured Talk Rail** | Video / Card | Top slot on Watch page right-hand rail | 7 Days | INR 1,500 / day |
| **Homepage Banner** | Image Banner | Above browse feed grid | 7 Days | INR 2,000 / day |
| **Topic Sponsor** | Tag Pill Badge | Fixed badge on specific topic category | 30 Days | INR 25,000 / month |

---

## 3. Serverless Telegram Relay Workflow

To eliminate complex payment gateways and expensive S3 storage:

```
[ Advertiser fills /ads form ]
  - Uploads company info + ad creative
  - Selects payment: UPI QR / Crypto / Razorpay link
  - Uploads screenshot proof of transfer
              │
              ▼
[ Next.js API Route (/api/ads) ]
  - Validates input with Zod schema
  - Calls Telegram Bot API:
      • sendMessage(form_data_text)
      • sendPhoto(payment_proof_blob)
              │
              ▼
[ Telegram Bot Notification ]
  - Site owner reviews proof inside Telegram chat
              │
              ▼
[ Manual Activation ]
  - Owner adds entry to data/ads.json
  - Git commit & push triggers automatic Vercel redeployment
```

---

## 4. Git-Based Ad Store (`data/ads.json`)

Approved ads are configured in `data/ads.json`:

```json
[
  {
    "id": "acme-infra-2026-09",
    "type": "image",
    "companyName": "Acme Cloud",
    "assetUrl": "/ads/acme-banner.png",
    "linkUrl": "https://acme.com",
    "startDate": "2026-09-01",
    "endDate": "2026-09-30",
    "status": "active"
  }
]
```
