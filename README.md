# Guidr waitlist

Live at https://khadrisaad.github.io

- Single file: `index.html` (no build step).
- Backdrop (sky, clouds, landmarks, plane) is drawn in CSS + SVG, so it stays sharp on every screen.
- Liquid glass: real refraction in Chrome/Edge via a generated SVG displacement map; Safari/Firefox get a frosted fallback.
- Signups go to the Supabase project `wishlist website-guidr` through two RPCs: `join_waitlist` and `waitlist_count`. The table itself is locked by RLS.
