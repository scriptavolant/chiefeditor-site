# Chief Editor — Sito Web

Sito Astro per il blog e landing page di Chief Editor.

## Stack

- **Astro 4** con MDX e sitemap
- **Content Collections** per post, serie e tag
- **CSS puro** — zero framework, zero dipendenze runtime
- Font: Playfair Display + DM Sans + DM Mono (Google Fonts)

## Struttura

```
src/
├── content/
│   ├── blog/          ← Articoli in Markdown/MDX
│   ├── series/        ← Definizioni delle serie
│   └── config.ts      ← Schema Zod dei content types
├── layouts/
│   ├── Base.astro     ← Layout con nav e footer
│   └── BlogPost.astro ← Layout per i singoli post
├── pages/
│   ├── index.astro    ← Home (download + video + post + sidebar)
│   ├── blog.astro ← Elenco tutti i post
│   ├── about.astro    ← Chi sono
│   ├── aiuto.astro    ← Guida (identica all'app)
│   ├── contatti.astro ← Contatti + beta tester
│   ├── download.astro ← Download page
│   ├── privacy.astro  ← Privacy policy
│   ├── blog/[...slug].astro  ← Singolo post
│   ├── tag/[tag].astro       ← Post per tag
│   └── serie/[slug].astro    ← Post per serie
└── styles/
    └── global.css     ← Variabili, tipografia, utility
```

## Installazione e sviluppo

```bash
npm install
npm run dev         # dev server su localhost:4321
npm run build       # build statica in dist/
npm run preview     # preview del build
```

## Come aggiungere un post

Crea un file `.md` o `.mdx` in `src/content/blog/`:

```markdown
---
title: "Titolo del post"
description: "Breve descrizione"
pubDate: 2025-05-01
tags: ["chief editor", "scrittura"]
series: "Come funziona Chief Editor"   # opzionale
seriesOrder: 2                          # opzionale
pinned: true                            # opzionale, appare in evidenza in home
heroImage: "/images/mia-immagine.jpg"   # opzionale
---

Testo del post in Markdown...
```

## Come aggiungere una serie

Crea un file `.md` in `src/content/series/`:

```markdown
---
title: "Nome della serie"
description: "Descrizione della serie"
color: "#7c3aed"
order: 1
---
```

## Download files

Metti i binari in `public/downloads/`:
- `chief-editor-setup-1.0.7.exe`
- `chief-editor-1.0.7.msi`
- `chief-editor-1.0.7.dmg`
- `chief-editor-1.0.7.AppImage`
- `chief-editor-1.0.7.deb`

## Deploy

Il sito genera HTML statico — funziona su Netlify, Vercel, Cloudflare Pages, GitHub Pages.

```bash
# Netlify
npm run build  # → output in dist/

# Vercel — aggiungere vercel.json se necessario
```

## Video home page

Sostituisci l'URL dell'iframe in `src/pages/index.astro`:

```html
<iframe src="https://www.youtube.com/embed/TUO_VIDEO_ID" ...>
```

## Configurazione

Modifica `astro.config.mjs` per impostare il dominio definitivo:

```js
export default defineConfig({
  site: 'https://chiefeditor.app',
  ...
});
```
