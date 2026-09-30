# Nao Select public information site

This repository contains the static public-information site for Nao Select, an
owner-operated, local-first product-content workflow tool under development.

The publishable files are isolated in [`docs/`](docs/):

- [`docs/index.html`](docs/index.html) — service overview
- [`docs/privacy.html`](docs/privacy.html) — privacy policy
- [`docs/styles.css`](docs/styles.css) — responsive styling

No login, form, analytics, advertising, external tracking, product images, or
third-party logos are included.

## Local preview

Run a static server from the repository root:

```powershell
py -m http.server 8088 --directory docs --bind 127.0.0.1
```

Then open `http://127.0.0.1:8088/` and
`http://127.0.0.1:8088/privacy.html`.

## Publication boundary

Only the contents of `docs/` are intended for website publication. Local
application drafts, research notes, and publication checklists are kept in the
Git-ignored `.local/` directory and must not be uploaded.

Publishing, Pinterest app registration, access applications, and support
messages require separate human approval and are not performed by this branch.

## Contact safety

Privacy questions may be opened in the public repository's Issues. Never post
access tokens, app secrets, passwords, personal information, or other
confidential information in a public Issue.
