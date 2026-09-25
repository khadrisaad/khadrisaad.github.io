# Guidr waitlist

Live at https://khadrisaad.github.io (moves to https://khadrisaad.github.io/waitlist once this repo is renamed to `waitlist`).

- `index.html`: the whole page, no build step. All paths are relative so it works at the root or under `/waitlist`.
- Background: `bg.jpg` (3642x1728, retina) and `bg-1x.jpg` (1821x864) via `srcset`. A tiny blurred preview is inlined so the page never flashes empty.
- Liquid glass: gradient hairline rim, specular sheen and fine grain over a heavy saturated backdrop blur. Solid frosted fallback where backdrop-filter is unsupported.
- Signups go to the Supabase project `wishlist website-guidr` through two RPCs: `join_waitlist` (email, source, referrer, lang, tz) and `waitlist_count`. The table is RLS-locked, with rate limiting and throwaway-inbox blocking server side.
