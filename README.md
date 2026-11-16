# Urban Road component assets

Generated browser distribution. Application source and deployment credentials are maintained separately.
Urban Road application code remains proprietary; third-party dependencies retain their own licenses.

## Installation

Replace the old Urban Road component-library Vercel script and stylesheet tags with this one tag in your theme head:

```html
<script src="https://cdn.jsdelivr.net/gh/urbanroad/urbanroad-component-library-assets@1/urbanroad-components.js" defer></script>
```

This file includes the matching styles and exposes window.multiStepForm and window.onePageForm.
Keep existing form containers, DOMContentLoaded initialization, webhooks, landing attribution and GTM.
Do not add type="module" or async. No Shopify asset upload is needed.

## Releases

Current build: **v1.0.1**. The @1 URL follows successful version-1 releases. CDN and browser caches can delay updates.
The publisher purges the CDN alias and verifies the returned bytes after each release.
For a fixed release, use https://cdn.jsdelivr.net/gh/urbanroad/urbanroad-component-library-assets@v1.0.1/urbanroad-components.js instead.
Use a previous release's fixed URL for immediate rollback; never move an existing version tag.
In the browser, inspect window.UrbanRoadComponentsBuild to identify the loaded release.

No forms are automatically mounted and no application or conversion is sent by loading this script.
Actual form submissions use the host page's existing webhook and tracking configuration.
