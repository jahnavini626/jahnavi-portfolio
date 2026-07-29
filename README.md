# Jahnavi N I — Portfolio

A single-page static site. No build step, no dependencies.

## Folder structure
```
jahnavi-portfolio/
├── index.html      ← the whole site
├── assets/
│   └── profile.jpeg
└── vercel.json
```

## Run locally in VS Code
Open the folder in VS Code, then either:
- Install the **Live Server** extension → right-click `index.html` → "Open with Live Server", or
- Run `npx serve .` in the terminal and open the printed localhost URL.

Don't just double-click `index.html` in the file explorer for final testing — some browsers block relative asset paths from `file://` URLs. Live Server / `npx serve` avoids that.

## Deploy to Vercel

**Option A — Vercel CLI (fastest)**
```bash
npm i -g vercel
cd jahnavi-portfolio
vercel
```
Follow the prompts (link/create a project, keep defaults — it's a static site, no build command needed). Run `vercel --prod` to push to your production URL.

**Option B — GitHub + Vercel dashboard**
1. Push this folder to a new GitHub repo.
2. Go to vercel.com → **Add New → Project** → import the repo.
3. Framework preset: **Other** (or "Static"). Leave build command empty, output directory as `./`.
4. Deploy.

Either way, Vercel will pick up `index.html` as the site root automatically.

## Editing
Everything — styles, content, the custom cursor, the network background, the flip animations — lives in `index.html` in a single `<style>` block and a single `<script>` block at the bottom. Search for the section id (`#hero`, `#about`, `#skills`, `#experience`, `#projects`, `#certs`, `#contact`) to find what you're looking for.
