# Guidr waitlist

Live at **https://khadrisaad.github.io/waitlist/** (the root URL redirects there, keeping any `?src=` tag).

- `waitlist/index.html`: the whole page, no build step.
- Images live in the public `site` bucket of the Supabase project `wishlist website-guidr`: `bg-v4.jpg` (3830x2331), `bg-v4-m.jpg` (1915px, phones), `og-v4.jpg` (share card), `icon.png`. When you replace one, upload it under a new version name and update the URL here, since they are cached for a year.
- Liquid glass is rendered with WebGL2: each `[data-glass]` element gets real refraction at the rim, light dispersion, frosted blur, a specular rim that follows the cursor, and soft shadows. Without WebGL it falls back to CSS frosted glass.
- Signups go through two RPCs, `join_waitlist` (email, source, referrer, lang, tz) and `waitlist_count`. The table is RLS-locked, with rate limiting and throwaway-inbox blocking server side.
