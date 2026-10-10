# alexandreb.dev — publisher site

Static Markdown pages (rendered by GitHub Pages / Jekyll) for the developer identity behind all apps.

- Portuguese (pt-BR) is the default, at the root; English (en-US) is under `/en`.
- Shared Privacy Policy and Terms cover every app; each app has its own section.
- Search for `TODO` before publishing.
- If you choose alexandreb.org instead, find-and-replace `alexandreb.dev` everywhere (including `CNAME` and `_config.yml`).

## Deploy

1. Create the repo **`<your-github-user>.github.io`** and push these files to `main`.
2. Settings → Pages → Source: "Deploy from a branch", `main` / root.
3. Settings → Pages → Custom domain: `alexandreb.dev`, then tick **Enforce HTTPS**.
4. DNS at your registrar (apex domain):
   - `A` records → `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - `AAAA` records → `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
   - `CNAME www` → `<your-github-user>.github.io`
5. Verify the domain in your GitHub account settings (Settings → Pages → Verified domains) to prevent takeover.

## URLs to give Google and Meta

Reviewers work in English, so the English URLs are the safer choice for the consoles.

| Field | English (submit these) | Português |
|---|---|---|
| Homepage | https://alexandreb.dev/en/ | https://alexandreb.dev/ |
| Privacy policy | https://alexandreb.dev/en/privacy | https://alexandreb.dev/privacidade |
| Terms of service | https://alexandreb.dev/en/terms | https://alexandreb.dev/termos |
| Data deletion (Meta) | https://alexandreb.dev/en/data-deletion | https://alexandreb.dev/exclusao-de-dados |
| App page (brnf) | https://alexandreb.dev/en/apps/brnf | https://alexandreb.dev/apps/brnf |

## Apps under the same domain

Any other repo in the same account with Pages enabled is served automatically at
`https://alexandreb.dev/<repo-name>/`, deployed independently from this one.
A repo named `brnf` → `https://alexandreb.dev/brnf/`.
Avoid naming a repo `apps`, `en`, `privacidade`, `termos` etc., since it would clash with these paths.

## Adding a new app

1. Create `apps/<name>.md` (Portuguese) and `en/apps/<name>.md` (English).
2. Add it to the app list in both `index.md` files.
3. Add an app-specific section to both privacy policies (and terms, if needed).
4. Update the "Last updated" date.
