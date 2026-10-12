# Konabari Youth Camp Registration — 2026

## Included
- `index.html`: Complete responsive website preview.
- Package choices: **Camp + BBQ — ৳200** and **Only Camp — ৳100**.
- Registration form fields: name, phone, church, emergency contact.
- Demo registration receipt with print/copy actions.

## Run locally
1. Extract this ZIP.
2. Open `index.html` in Chrome or Edge.

## Important: before accepting real donations/payments
This is the complete **front-end preview**, not a production payment system. The form currently does not store registrations in a database and does not initiate a real ZiniPay payment. The displayed receipt is marked as demo and must not be treated as payment confirmation.

For a live deployment, connect:
1. Supabase database and Row Level Security policies.
2. A Supabase Edge Function to create payment sessions on the server.
3. ZiniPay's official API credentials stored as server-side secrets (never in `index.html`).
4. A server-side callback/webhook that verifies payment status before marking a receipt as paid.
5. An authenticated admin dashboard with admin-only permissions.

You will need the exact ZiniPay merchant/API documentation and credentials to complete the live checkout securely.
