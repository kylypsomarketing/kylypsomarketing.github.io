# Kylypso Marketing — App shell (GitHub Pages)

Ito ang "balot" ng Customer Purchase System. Ang mismong system (orders, inventory, chat) ay nasa **Google Apps Script**.
Ang GitHub page na ito ay nagbibigay ng: link na madaling tandaan, app icon sa phone, push notifications, voice record, at "Stay logged in".

**Link:** https://kylypsomarketing.github.io/

## Mga file
| File | Para saan |
|---|---|
| `index.html` | Binubuksan ang Apps Script app sa loob (iframe). Nandito ang `APP_URL` (ang /exec link ng Apps Script). |
| `sw.js` | Service worker: offline screen at push notifications. **Itaas ang `CACHE` (v6 → v7) tuwing papalitan ang icon o shell.** |
| `firebase-config.js` | Firebase settings para sa push notifications (hindi sikreto). |
| `manifest.webmanifest` | Pangalan at icon kapag "Add to Home Screen". |
| `icon-*.png`, `apple-touch-icon.png`, `favicon*` | Mga icon. |
| `og-image.png` | Preview kapag ipinost ang link sa Facebook / Messenger. |
| `404.html` | Maling link → ibinabalik sa Home. |
| `.nojekyll`, `robots.txt` | Setting ng GitHub Pages at Google. |

## Kapag nag-deploy ng bagong version ang Apps Script
- Kung **Deploy → Manage deployments → ✏️ Edit → Version: New version** ang ginamit: walang babaguhin dito (pareho ang /exec link).
- Kung **New deployment** ang ginawa: magbabago ang link → i-update ang `APP_URL` sa `index.html`.

## Kapag nagpalit ng domain (hal. kylypso.com)
1. Settings → Pages → Custom domain.
2. Palitan ang `kylypsomarketing.github.io` sa `index.html` (og:url, og:image) at ang `APP_LINK` sa Code.gs.
