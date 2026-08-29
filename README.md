# Arsenal Edge — legal pages

Public, static hosting for the Arsenal Edge Privacy Policy, Terms of Service, and account
deletion request page. Published with GitHub Pages.

This repository is public **only because Google Play requires these documents to be
reachable without installing the app**. It contains no application source code.

| Page | Purpose |
| --- | --- |
| `index.html` | Landing page linking the three documents |
| `privacy.html` | Privacy Policy — the URL Play's store listing points at |
| `terms.html` | Terms of Service |
| `delete-account.html` | Account deletion request page — the off-device route Play requires in addition to in-app deletion |

## This is a mirror, not the source

The canonical text lives in the private Arsenal Edge repository:

- `docs/legal/PRIVACY_POLICY.md` and `docs/legal/TERMS_OF_SERVICE.md` — canonical prose
- `apps/mobile/src/features/account/legalContent.ts` — the copy bundled in the app
- `site/legal/` — the source these files are copied from

A contracts test in that repository pins the effective date, provider name, governing
state, and contact address across all of those surfaces, so they cannot silently diverge.
**Edit there, then copy the changed files here** — do not hand-edit these pages, or the app
and the website will start telling users different things.

To update:

```bash
cp "<arsenal-edge>/site/legal/"* .
git add -A && git commit -m "Update legal pages" && git push
```

## Hosting

GitHub Pages, served from the `main` branch root (Settings → Pages → Source: Deploy from a
branch → `main` / `/`).

Provider: Aplomb Financial LLC · Kyle@aplombfinancial.com
