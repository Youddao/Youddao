# Youddao

**Youddao** (https://youddao.com) is a free online AI translation and smart
dictionary tool — no download, no installation, no sign-up. Open the browser
and use it: text translation, word lookup with definitions and examples, and
document summarization, built as a lightweight alternative for quick everyday
lookups.

> **Youddao ≠ Youdao.** Youddao is an **independent product brand**. It has no
> affiliation, endorsement, or partnership with NetEase Youdao (有道) or its
> Youdao Translate product. The similar name is coincidental. See the
> [comparison page](https://youddao.com/en/youdao-alternative) for details.

---

## Links

| | |
| --- | --- |
| Live site | https://youddao.com |
| What is Youddao? (EN) | https://youddao.com/en/what-is-youddao |
| What is Youddao? (中文) | https://youddao.com/what-is-youddao |
| Youdao alternative (EN) | https://youddao.com/en/youdao-alternative |
| 有道翻译替代方案 (中文) | https://youddao.com/compare/youdao-alternative |

## Features

- **Text translation** — short texts and sentences across multiple languages (see the language selector on the homepage for available pairs).
- **Smart dictionary** — word lookups with definitions, parts of speech, and example sentences.
- **Document summarization** — paste or upload long text and get a concise summary.
- **Zero setup** — nothing to install; works in any modern desktop or mobile browser, including shared or public computers.

## Tech stack

- **Next.js 15** (App Router) · **React 19** · **TypeScript**
- **Tailwind CSS v4**
- Pixel-faithful desktop landing page (fixed 1728 × 1530 canvas) with tablet and mobile variants selected purely via CSS — no JS-dependent layout.

## Getting started

```bash
npm install
npm run dev      # http://localhost:3000
npm run build    # production build
npm run start    # serve the production build
```

## Project structure

```
fe/
├── app/
│   ├── layout.tsx                        # root layout — fonts, metadata, Organization/WebSite JSON-LD
│   ├── page.tsx                          # homepage (fixed 1728×1530 desktop canvas + tablet/mobile views)
│   ├── sitemap.ts                        # sitemap.xml with hreflang language alternates
│   ├── robots.ts                         # robots.txt
│   ├── what-is-youddao/page.tsx          # brand page (中文)
│   ├── en/
│   │   ├── what-is-youddao/page.tsx      # brand page (English)
│   │   └── youdao-alternative/page.tsx   # Youdao Translate comparison (English)
│   └── compare/
│       └── youdao-alternative/page.tsx   # 有道翻译替代方案对比 (中文)
├── components/                           # desktop, tablet/, and mobile/ variants
├── lib/
│   └── site.ts                           # SITE_URL / SITE_NAME constants
└── public/                               # images and logo assets
```

## SEO notes

- Bilingual content pairs (中文 / English) linked with `hreflang` + `x-default` in both `<head>` and the sitemap.
- Canonical URLs on every page; `Article` + `FAQPage` structured data on content pages; `WebSite` + `Organization` + `WebApplication` on the homepage.
- `robots.txt` allows all crawlers and points to the sitemap.

## License

MIT
