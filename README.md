# OrdexAI — Order Page (DEV)

Development copy of the OrdexAI customer order page, served at **https://order-dev.ordexai.com**.

This is a mirror of the production page ([`ordexai-order-page`](https://github.com/lishaibs/ordexai-order-page) → order.ordexai.com). The page detects its own hostname at runtime: on `order-dev.ordexai.com` it calls the **dev** backend; everywhere else it calls the **prod** backend. Use this URL to test page changes against **dev data** before promoting them to production.

Customers receive a link in WhatsApp; the page lets them browse the catalog, manage favorites, pre-fill from an existing order, and submit back via WhatsApp.

## Architecture
- Single HTML file at `order/index.html`
- API base chosen automatically by `location.hostname` (dev vs prod)
- Auth via a signed JWT in the URL `?t=<token>` (short-lived, ~6 hours)

## Deployment
GitHub Pages auto-deploys on push to `main`. Custom domain is set via the `CNAME` file (`order-dev.ordexai.com`).
