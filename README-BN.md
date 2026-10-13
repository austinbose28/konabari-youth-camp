# Konabari Youth Camp Registration

Live registration site: https://austinbose28.github.io/konabari-youth-camp/

## Registration
- Camp + BBQ: ৳200
- Only Camp: ৳100
- The form collects name, phone, church, and emergency contact.
- ZiniPay checkout is connected through Supabase Edge Functions.
- Registrations are stored in the Supabase `camp_registrations` table.
- Payment status is marked paid only after the server verifies the invoice, amount, completion status, and transaction ID with ZiniPay.

## Organizer dashboard
Open https://austinbose28.github.io/konabari-youth-camp/admin.html

Dashboard login uses Supabase Auth. Read access is restricted by Row Level Security to the authorized organizer email and the `admin` app metadata role. The organizer Auth account still needs to be created and assigned that role before dashboard data can be viewed.

## Services
- GitHub Pages serves the site.
- Supabase project: `txewoknzeeamwpreaeqg`
- Edge Functions: `create-camp-payment` and `verify-camp-payment`
- ZiniPay API key is held as a server-side Supabase Function secret; it is not embedded in the public site.

## Payment readiness
The integration and server functions are deployed. No real payment has been made during setup, so do a controlled low-value live checkout before relying on it for registrations. Confirm the return flow and paid status in the dashboard after the organizer account is enabled.