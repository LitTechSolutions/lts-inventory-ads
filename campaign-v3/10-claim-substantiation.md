# 10. Claim-substantiation checklist

Only claims with a public or in-repo source belong in ads. If a line cannot be checked here, do not run it.

Sources used:

- https://lit-solutions.tech/pricing and `pricing.html`
- https://lit-solutions.tech/faq and `faq.html`
- https://lit-solutions.tech/ (home) and `index.html`
- `js/inventory-config.js` (`trial.durationDays: 7`, `cardRequired: false`, Essentials `monthlyPrice: 49`)
- https://lit-solutions.tech/terms (trial / price section)
- v3 creatives in `ads-v2/` (visuals only; they do not add new claims)

## Allowed — use in this flight

| Claim | Source |
|---|---|
| Product name is LTS Inventory | Public site, app login |
| Operator is Little Technical Solutions LLC | Company page, footer |
| Destination is inventory.lit-solutions.tech | Brief; public app host |
| Seven-day trial | Pricing, FAQ, terms, inventory-config |
| No card required to start | Pricing, FAQ, terms, inventory-config |
| Essentials is a self-service plan | Pricing comparison; inventory-config `selfServiceTrialEligible: true` |
| Essentials is $49 per month | Pricing card and table; inventory-config `monthlyPrice: 49` |
| Lots, serials, exact lookup, stock positions, history are included on Essentials | Pricing comparison row |
| Core counts, adjustments, receiving, returns, reports, users, facilities are available now on Essentials | Pricing comparison row |
| “Know what you have” / “Know where it went” / “Inventory you can explain.” | Home title and H1; v3 stills |
| Spreadsheets/clipboards as a contrast (rhetorical, not a customer story) | Existing v1/v3 copy; not presented as a case study |

## Allowed with pairing rules

| Claim | Rule |
|---|---|
| Phone-camera / keyboard-style scan | FAQ allows it. Do not say “hardware scanner,” “registered device,” or show scan creative as a dedicated device SKU. Essentials registered-device limit is 0. |
| Permanent / reviewable / attributable history | Home and pricing discuss permanent, immutable, attributable history. Do not upgrade this to “compliance,” “audit-ready,” or “certified.” |
| Demonstration UI in screenshots | v3 stills are product screens. `landscape-fulfill.png` is labeled demonstration/sample data and is **held** for this flight. |

## Do not say (no substantiation in this pack)

| Do not claim | Why |
|---|---|
| Fulfillment, count planning, or inbound workflows as part of Essentials | Pricing: **not included** on Essentials |
| Purchasing / transfers as Essentials inclusions | Not a labeled Essentials row on the public comparison |
| Recall, hold, genealogy, or complete traceability lifecycle | Recall start-and-hold is Control+; FAQ/product bound it tightly |
| Registered hardware scanners or offline replay | Public pages say these are not complete / deferred |
| Customer counts, “trusted by,” logos, testimonials | None published on the current inventory site |
| Savings, ROI, time saved, error-rate reduction | No study in this pack |
| “47” as a real on-hand quantity or customer metric | Rhetorical leftover from v1; replaced with “a number” |
| Veteran-owned, Montross, awards, rankings | Not on the current LTS Inventory company page |
| SOC / ISO / FedRAMP or other attestations | Not published |
| ERP, accounting system, or “complete warehouse OS” | FAQ: not an accounting system or full ERP |
| Operations / Control / Enterprise prices | Out of offer scope for this flight |
| $19.99 grandfathered price | Not a public self-service plan (`earlyAdopterPriceLock.publicPlan: false`) |
| Annual $490 as the advertised trial price | Offer is monthly $49 after trial |
| Performance statistics (“top converting,” CTR, #1) | None |

## Visual claims

- [ ] Every uploaded PNG is a v3 file from the manifest
- [ ] Overlay text does not add capabilities the copy does not allow
- [ ] Fulfillment screenshot is **not** in the Essentials ad set
- [ ] No third-party marks, app-store badges, or fake UI chrome beyond the baked product screens

## Sign-off

| Role | Check | Date |
|---|---|---|
| Copy | Every live line maps to an Allowed row | |
| Creative | Manifest “Use” only | |
| Offer | 7-day + no card + $49/mo Essentials | |
| Legal/owner (optional) | Terms still match the trial and price | |
