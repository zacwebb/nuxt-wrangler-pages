# Cloudflare Pages (Wrangler) Dev & Nuxt Issue

Reproduction of issue when running `wrangler pages dev` with https, despite http working fine.

## Setup

1. `pnpm i` to install packages
2. `pnpm generate-certs` to generate local ssl certs

## HTTP

To validate everything is fine in http, you can run `pnpm dev` to start the regular nuxt server, or `pnpm wrangler` to start the wrangler pages dev server.

Both these should work fine.

## HTTPS

You can see that the https server for nuxt starts fine when running `pnpm dev:https`, but when running `pnpm wrangler:https` to run nuxt through wrangler, the following error message will appear when trying to open the page:

```
[wrangler] Could not proxy request: TypeError: fetch failed
```