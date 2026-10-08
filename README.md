# Spex Cloud Plat

Private personal cloud and controlled media sharing.

## Stack
- Next.js
- Supabase Auth
- Supabase Postgres + private Storage
- Vercel-ready

## Environment
Copy .env.example to .env.local and add the Supabase project URL, publishable key and server-only service role key.

## Security model
Files live in a private spex-files bucket. Share tokens are stored only as SHA-256 hashes. The share endpoint checks revocation, expiry, PIN and view limits before issuing a 90-second signed Storage URL.

Browser controls can discourage casual downloading, but a website cannot guarantee that a recipient cannot screenshot or capture the screen.

## Current MVP
- email/password auth
- private uploads
- image/video/PDF support
- expiring share links
- optional PIN
- one-time/burn-after-view shares
- short-lived signed URLs