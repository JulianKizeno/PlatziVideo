# Security review — 2026-11-14

This is a partial remediation, not a certification that the repository is free of vulnerabilities. Changes remain in a draft pull request pending review.

## .

npm findings before: {"info": 0, "low": 8, "moderate": 22, "high": 61, "critical": 21, "total": 112}. After remediation: {"info": 0, "low": 7, "moderate": 15, "high": 25, "critical": 0, "total": 47}.
Counts refer to dependency findings in this project, including development dependencies. Projects without a committed lockfile were first resolved to create an auditable baseline. Production builds were checked on Node.js 24 with CI=true, npm ci --ignore-scripts --legacy-peer-deps and NODE_OPTIONS=--openssl-legacy-provider for legacy Webpack compatibility; these builds are not browser end-to-end tests.

Production build/test result: `{   "project": "PlatziVideo",   "manifest_sha256": "942167c3cb8b46b3383711f4a5e8ebc1abe17d5d82a1d0828fbdb31063460de4",   "lock_sha256": "09529c6fc54a8bf1e698c91f309da44712d720c517ba159bf7e57b405266ca65",   "install_exit": 0,   "build_exit": 0 }`.

### Remaining advisories

- `css-loader`: moderate; requires dependency migration. 
- `eslint`: high; requires dependency migration. 
- `file-loader`: moderate; requires dependency migration. 
- `html-loader`: high; requires dependency migration. 
- `html-webpack-plugin`: high; requires dependency migration. 
- `mini-css-extract-plugin`: moderate; requires dependency migration. 
- `webpack`: high; requires dependency migration. 
- `webpack-cli`: moderate; requires dependency migration. 
- `webpack-dev-server`: high; requires dependency migration. https://github.com/advisories/GHSA-4v9v-hfq4-rm2v https://github.com/advisories/GHSA-79cf-xcqc-c78w https://github.com/advisories/GHSA-9jgg-88mc-972h https://github.com/advisories/GHSA-f5vj-f2hx-8m93 https://github.com/advisories/GHSA-m28w-2pqf-7qgj https://github.com/advisories/GHSA-mx8g-39q3-5c79

Do not treat compatible lockfile updates as completion of the framework migrations above.
