OrdexAI -DEV - Order Page
Static web page served at order-dev.ordexai.com.

Customers receive a link in WhatsApp; the page lets them browse the catalog, manage favorites, edit existing orders, and submit back via WhatsApp.

Architecture
Single HTML file at order/index.html

All authentication via JWT in URL ?t=<token> (2-hour expiry)
Deployment
GitHub Pages auto-deploys on push to main.
