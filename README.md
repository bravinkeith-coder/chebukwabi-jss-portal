# Chebukwabi JS — Ingwe Ya Matere (Cloudflare Pages)

A Vite + React + TypeScript football-club portal rebuilt from the supplied archive. The original club crest is retained.

## Deploy free on Cloudflare Pages

1. Create a new GitHub repository (for example `chebukwabi-js-portal`).
2. Extract this ZIP and upload **all files and folders inside it** to the repository root. Commit the upload.
3. In Cloudflare, open **Workers & Pages → Create → Pages → Connect to Git** and select the repository.
4. Use these build settings:
   - Framework preset: **Vite**
   - Build command: `npm run build`
   - Build output directory: `dist`
   - Root directory: `/`
5. Save and deploy. Cloudflare will provide your `*.pages.dev` address.

For local preview: `npm install`, then `npm run dev`. To make a production build: `npm run build`.

## Login accounts (starter passwords)

- Administrator: `ADMIN` / `ingwe2026`
- Coach: `COACH01` / `ingwe2026`
- Boys player: `PLAYER10` / `ingwe2026`
- Girls player: `GPLAYER10` / `ingwe2026`
- Fan: `FAN01` / `ingwefans2620`

The portal retains password entry and password-change controls. Password changes are saved in that browser.

## Important data and security note

This archive is a **static Cloudflare Pages starter**. Portal records (news, settings, player edits, fixtures, tickets, etc.) are saved in the visitor's browser using local storage. They do not automatically synchronize between devices or different visitors, and clearing browser data removes them. Login/password checks are also performed in the browser; they are suitable for a demo or private prototype, **not secure production authentication**. Do not use these starter passwords for real confidential accounts.

Before using the portal for official club operations, connect a real backend such as Supabase or Cloudflare D1/Workers, move authentication and role checks server-side, and configure secure file storage for player photos. The existing player photo upload and other app features should be tested with the chosen backend and hosting setup.

## Preserved club content

- Chebukwabi JS name and supplied Ingwe Ya Matere crest
- Green-and-gold identity and existing Boys/Girls squads
- Fixtures, results, competition information and club news
- Academy, fan zone, tickets, shop, sponsors and support sections
- Admin, coach, player and fan portal entry points
