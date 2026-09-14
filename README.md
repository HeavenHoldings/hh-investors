# Heaven Holdings — Capital Partner Network (Investor Database)

A single-file Cloudflare Worker: investor directory + correspondence
(email/letter mail-merge) tool for Heaven Holdings.

## Deploy

1. In Cloudflare: Workers & Pages -> Create -> Connect to Git -> select this repo.
2. Cloudflare will read `wrangler.toml` and deploy `src/index.js` automatically.
3. After the first deploy, go to the worker's Settings tab and add:
   - KV binding: variable name `INVESTORS`, namespace `INVESTORS_DATA` (create this namespace under Storage & Databases -> KV first)
   - Secrets: `ADMIN_KEY` (required) and `STAFF_KEY` (optional)
4. Every future push to this repo's main branch redeploys automatically — no dashboard code editor involved.
