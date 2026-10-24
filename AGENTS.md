# AGENTS.md

## Architecture
- A static site with no framework and no build. `netlify.toml` publishes `public/`.
- `public/index.html` is the whole site: inline `<style>`, inline `<script>` blocks, and base64 data-URI images and videos.
- Video clips are stored as base64 in `<script type="text/plain">` tags (`plansvid`, `treksvid`, `whyvid`, `inspvid`, `popvid`) and in a JSON tag `dham-clips`. Scripts read them at runtime, so don't rename those IDs.
- `<script id="odata" type="application/json">` holds editable site data. An in-page editor exports a new copy of the HTML by fetching the page and replacing that block. Keep its exact opening tag.
- Bookings, reviews and profiles are written to `localStorage` and handed off to WhatsApp (`wa.me` links). There is no server code.
- The chat helper has an optional `AI_URL` (empty by default). If it is set, the helper POSTs `{message, context}` there and expects `{reply}` back.

## Conventions
- The file is very large (about 12 MB). Edit it with scripts or targeted replacements, not by reading it whole.
- Theme colours are CSS variables in `:root` (`--deep #14402f`, `--accent #c2571a`), with a dark-mode variant.
