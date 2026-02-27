# helm-charts

Central Helm chart repository for douz open source projects.

## Purpose

- Host chart artifacts (`.tgz`) and `index.yaml` for `https://charts.douz.io`.
- Provide a human landing page on the `gh-pages` branch.
- Keep chart source code in each project repository.

## Publishing Model

Each project repository publishes its chart(s) into this repo by using `helm/chart-releaser-action` with:

- `CR_OWNER=douz`
- `CR_GIT_REPO=helm-charts`
- `CR_TOKEN=<token with write access to this repo>`
- `charts_repo_url=https://charts.douz.io`

This allows a single central chart index while preserving chart source in project repos.

## GitHub Pages

- Branch: `gh-pages`
- Custom domain: `charts.douz.io`
- Required files on `gh-pages`: `CNAME`, `index.yaml`, chart packages, and a user-facing `index.html`.

## Notes

- `index.yaml` is managed by chart-releaser.
- `index.html` is a curated landing page and can be updated manually.
