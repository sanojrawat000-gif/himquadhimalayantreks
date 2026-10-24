# Himquad – Himalayan Treks

The website for Himquad Himalayan Treks: small-group Himalayan treks (Kedarkantha, Har Ki Dun, Roopkund and 20+ more), Char Dham yatra plans, gear rental, Himachal trips, traveller stories, and booking over WhatsApp.

## Technologies

- One self-contained static HTML page (`public/index.html`). The CSS, JavaScript, images and short video clips are all embedded in it.
- Hosted on Netlify, with no build step.

## Running locally

Open `public/index.html` in a browser, or serve it:

```bash
npx serve public
# or, with Netlify emulation:
netlify dev
```

## Possible next steps

- Move the embedded images and videos into separate files and serve them through the Netlify Image CDN. The page is about 12 MB today, so this would make the first load much faster.
- Connect the built-in chat helper to an AI endpoint by setting the `AI_URL` value in the page script. A Netlify Function using the AI Gateway would work.
