Scaffold a personal website in this empty directory. It deploys to Cloudflare Workers with static assets, and it will later contain small self-contained apps alongside the site.

Layout: an npm workspace at the repository root, with the Astro site in site/ and an apps/ directory that is currently empty. The root package.json declares workspaces ["site", "apps/*"] and exposes dev and build scripts that delegate to the site.

The site: Astro with static output. Do not add the Cloudflare adapter, because nothing renders on the server yet. A home page at / saying hello, and an index at /apps/ that currently lists nothing, both using a shared layout with a header and footer. Plain CSS, no framework. TypeScript in strict mode.

Cloudflare: a wrangler.jsonc at the repository root naming the Worker stevenblakemore-com, with an assets directory pointing at the site's build output and a current compatibility date. No Worker script, assets only.

Also create a .nvmrc pinning Node 22 with a matching engines field, a .gitattributes containing * text=auto eol=lf, a .gitignore covering node_modules, dist, .astro and .wrangler, and a README.md giving the local dev command, the build command and the deployed URL.

Explain the directory layout and what each config file does before writing anything. Do not run any git commands.