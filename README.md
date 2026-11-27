# Inventory Preflight

Free, experimental, browser-only comparison of store and warehouse inventory CSV files.

**Try it:** [Open Inventory Preflight](https://denyslaptiev.github.io/inventory-preflight/) (GitHub Pages must be enabled under Settings → Pages before this URL becomes live).

## Features
- Missing SKU/location pairs and count discrepancies
- Duplicate SKU/location warnings (never silently aggregate duplicates)
- Leading zeros in SKUs preserved
- CSV export of discrepancy report
- Zero external dependencies and no file uploads

## Quick start
1. Open `index.html` in a browser or use the published GitHub Pages URL.
2. Click **Load safe sample** → **Compare CSVs**.
3. For your own CSVs, use columns `SKU,Location,On hand (current)` for the store and `SKU,Location,Quantity` for the warehouse.
4. Review the report and download it.

### Synthetic sample
Store: `000123=10, 000124=5, 000125=7, 000126=3`.
Warehouse: `000123=10, 000124=8, 000125=7, 000127=5`.
Expected: 2 matching rows, 3 discrepancies, 0 duplicates.

## Privacy and limitations
All files are parsed in your browser; the page has no external API calls, analytics, tracking, cookies or signup. Inventory is never modified. The tool is not an official Shopify/Extensiv integration and does not guarantee their export formats are directly compatible. Ensure matching locations, stock-state definitions and snapshot times before comparing. Test on non-sensitive/obfuscated files. Never use as sole basis for inventory adjustments.

**Status:** Public technical preview. No customers, subscriptions, production integrations or claims of commercial validation. Not affiliated with Shopify or Extensiv.

## Source
This repository contains only public demo assets. The private AI Business Lab research repository is not copied or exposed.

## Contact
For now, use a public GitHub issue in this repository to describe general workflow feedback. Do not include proprietary CSV files, credentials, private customer data or business information.
