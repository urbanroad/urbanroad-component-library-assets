# Urban Road component assets

Generated browser distribution. Application source and deployment credentials are maintained separately.
Urban Road application code remains proprietary; third-party dependencies retain their own licenses.

## Installation

This release copies every JS/CSS file from the existing Vercel build without changing its bytes, names, imports or lazy loading.
Replace the Vercel base URL with https://cdn.jsdelivr.net/gh/urbanroad/urbanroad-component-library-assets@v1.0.2, keeping the original /assets/ filename and module attributes.
For a page using the one-page forms:

```html
<script defer type="module" crossorigin src="https://cdn.jsdelivr.net/gh/urbanroad/urbanroad-component-library-assets@v1.0.2/assets/client.js"></script>
<link rel="stylesheet" crossorigin href="https://cdn.jsdelivr.net/gh/urbanroad/urbanroad-component-library-assets@v1.0.2/assets/client.css">
<script defer type="module" crossorigin src="https://cdn.jsdelivr.net/gh/urbanroad/urbanroad-component-library-assets@v1.0.2/assets/one-page-form.js"></script>
```

For the wholesale page, use assets/wholesale-registration-form.js as the form entry instead.
If a page uses both APIs, include both form entries and load client.js/client.css once.
Shared dependencies and the country/state selector are imported automatically.
Keep existing form containers, DOMContentLoaded initialization, webhooks, landing attribution and GTM.
Keep type="module" and crossorigin; do not add async. No Shopify asset upload is needed.

## Releases

Current build: **v1.0.2**. Use this same exact version in every URL so cached entry files and their imported chunks stay compatible.
GitHub publishes new releases automatically; update the version in Shopify's URLs when adopting a release.
The mutable @1 alias is also refreshed but is not recommended for multiple interdependent files.
Rollback by restoring all URLs to a prior split-file release. Never move an existing version tag.
The earlier root urbanroad-components.js remains available for compatibility but is no longer rebuilt; remove that tag when switching to these files.

## Files

- assets/client.css (201476 bytes; gzip 30595 bytes)
- assets/client.js (758000 bytes; gzip 209868 bytes)
- assets/country-state-selector.js (507216 bytes; gzip 120861 bytes)
- assets/lead-attribution.js (103 bytes; gzip 111 bytes)
- assets/lead-attribution2.js (1803 bytes; gzip 819 bytes)
- assets/modulepreload-polyfill.js (706 bytes; gzip 394 bytes)
- assets/one-page-form.js (35706 bytes; gzip 10926 bytes)
- assets/wholesale-preview.js (2337 bytes; gzip 1189 bytes)
- assets/wholesale-registration-form.js (48047 bytes; gzip 16799 bytes)

No forms are automatically mounted and no application or conversion is sent by loading this script.
Actual form submissions use the host page's existing webhook and tracking configuration.
