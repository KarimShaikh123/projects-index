# AGENTS.md

## Stack

- Plain HTML/CSS/JS, no framework, no build step. CommonJS/ESM n/a — static only.
- Fonts: Manrope (body) + DM Mono (labels) via Google Fonts — matches every other project.
- Tokens in `:root` in `styles.css`: `--ink #19201c`, `--paper #f4f2eb`, `--panel #fff`, `--lime #d8ef62`, `--coral #ff8d73`, `--blue #315eff`, `--line`. New styles reuse these, not raw hex.
- Vercel: `outputDirectory: "."` in `vercel.json` + a no-op `build` script in `package.json` — do not remove either, `vercel dev` fails without them.
- Tests: `npm test` = `node --test`. No runtime deps.

## Facts (all verified 2026-08-13 by fetching the live pages, never from memory; url-shortener verified 2026-08-17)

Live URLs + GitHub repos for the five projects:

- Portfolio → https://portfolio-site-three-kappa-31.vercel.app · KarimShaikh123/portfolio-site
- Markdown Blog → https://markdown-blog-theta-rouge.vercel.app · KarimShaikh123/markdown-blog
- QR Studio → https://qr-generator-nine-rho.vercel.app · KarimShaikh123/qr-generator
- Lahore Weather → https://lahore-weather-one.vercel.app · KarimShaikh123/lahore-weather
- URL Shortener → https://url-shortener-gamma-one.vercel.app · KarimShaikh123/url-shortener (private repo — the card links it anyway, matching the Markdown Blog card)

## Commands

- Local preview: `python3 -m http.server 4317` (fetch is blocked on file://)
- Syntax check: `node --check <file>`
- Tests: `npm test`
- Deploy: push to `main` (auto-deploy), or `vercel --prod`
- Verify a deploy: read the live page content — never a status code alone

## Rules

- Never state a URL from memory — verify the live page before writing it into the site.
- One task, one commit, one review; nothing committed before the owner reviews.
- No code comments unless asked.
- Commit identity: Karim Shaikh <karimhshaikh009@gmail.com>.