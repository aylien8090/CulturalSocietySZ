# Cultural Society SZ

Website for **Cultural Society SZ**, Stara Zagora.
Instagram: https://www.instagram.com/culturalsocietysz/
Live address: https://culturalsocietysz.pages.dev

The homepage (`index.html`) showcases our first event, the Cultural Event on 17 October 2026, and points people to Instagram for what's next.

## What's in this folder

- `index.html`: the public homepage (photos, highlights, Instagram and WhatsApp links).
- `Images/`: logo, event photos and link-preview pictures.
- `admin.html`, `vote.html`, `buzzer.html`, `tv.html` and `functions/`: the ticketing, voting and trivia tools used on event night. They need a Cloudflare D1 database to work, so the homepage does not depend on them.
- `migrations/`: the database tables for the ticket system.

## Hosting on Cloudflare Pages

1. In the Cloudflare dashboard go to **Workers & Pages → Create → Pages → Connect to Git** and pick this GitHub repository.
2. Project name: `culturalsocietysz` (this gives the address `culturalsocietysz.pages.dev`).
3. Build command: leave blank. Build output directory: `.`
4. Only if you want the ticket / vote / trivia tools: in **Settings → Bindings** add a D1 binding called `TICKETS_DB`, and in **Settings → Variables and Secrets** add an encrypted `ADMIN_PASSWORD`.

## Notes

- New ticket codes start with `CSZ-` (for example `CSZ-7K2M`). Older tickets keep their old codes.
- The existing database is still called `asian-society-tickets` in Cloudflare. That name is only a label and can stay.
- Do not put private files (finance sheets, receipts, attendee lists) in this folder. Everything in it is published.
