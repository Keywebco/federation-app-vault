# Vault Sync Log — unified-storefront-8

## Sync Date: 2026-09-04
## Job ID: adf61c10-728a-4309-bb2d-b8f0fdeaae8e
## App Name: unified-storefront-8
## Live URL: https://unified-storefront-8.preview.emergentagent.com
## Domain: next-xus.com

### Changes Synced
- Fixed Gumroad seller links: rogerkey.gumroad.com -> keywebster.gumroad.com (all HTML + JSON)
- JIM primary checkout integration (banner + 4-option payment selector)
- Tools Hub navigation link added
- Orbot chat widget integrated
- Schema.org JSON-LD structured data for products

### Vault Structure
- `source/` — Original source HTML files with gumroad fix applied, backend code, assets, configs
- `build/` — Live build output (SPA index.html shell + React bundle.js)

### Verification
- Live site: 16 keywebster.gumroad refs, 0 rogerkey.gumroad refs (confirmed via curl)
- Source files: 0 rogerkey.gumroad refs remaining (sed replacement verified)
- Bundle.js: 6 keywebster.gumroad refs, 0 rogerkey.gumroad refs
