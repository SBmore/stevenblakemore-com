# stevenblakemore.com

Personal website, built with Astro and deployed to Cloudflare Workers as static assets.

- `site/`: the Astro site
- `apps/`: small self-contained apps (npm workspaces)

Requires Node 22 (see `.nvmrc`). Install dependencies with `npm install`.

## Local development

```sh
npm run dev
```

## Build

```sh
npm run build
```

Output goes to `site/dist/`, which `wrangler.jsonc` serves as the Worker's assets.
Deploy with `npx wrangler deploy`.

## Deployed

https://stevenblakemore.com
