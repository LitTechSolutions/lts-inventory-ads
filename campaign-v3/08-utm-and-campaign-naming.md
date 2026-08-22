# 8. UTM and campaign-naming matrix

Character set for UTM values: `A–Z a–z 0–9 . _ - ~` and spaces. That matches the marketing-site handoff filter in `lit-solutions-website/js/google-ads.js`. This pack uses lowercase, hyphens, and underscores only — no spaces, no `@`, no slashes.

## Shared parameters

| Parameter | Value | Purpose |
|---|---|---|
| `utm_campaign` | `lts-inv-essentials-trial-v3` | One campaign family |
| `utm_source` | channel (below) | Paid channel |
| `utm_medium` | `paid-social` / `cpc` / `display` | Buy type |
| `utm_content` | asset or copy stem (below) | Creative |
| `utm_term` | Google keyword (search only) | Query |

Do not put emails, names, or free-form comments in UTM values.

## Campaign, ad set, and ad names

Pattern:

```
LTS-Inv_Essentials-Trial_v3_<Channel>
LTS-Inv_Essentials-Trial_v3_<Channel>__<AdSet>
LTS-Inv_Essentials-Trial_v3_<Channel>__<AdSet>__<stem>
```

| Channel | Campaign name | Default ad set |
|---|---|---|
| Meta | `LTS-Inv_Essentials-Trial_v3_Meta` | `Feed`, `Stories`, `Trial-Landscape` |
| LinkedIn | `LTS-Inv_Essentials-Trial_v3_LinkedIn` | `Single-Image` |
| Google Search | `LTS-Inv_Essentials-Trial_v3_Search` | `RSA-Essentials` |
| Google Display | `LTS-Inv_Essentials-Trial_v3_Display` | `Banners` |

## Final URL pattern

Approved destination:

```
https://inventory.lit-solutions.tech
```

With UTMs:

```
https://inventory.lit-solutions.tech?utm_source=SOURCE&utm_medium=MEDIUM&utm_campaign=lts-inv-essentials-trial-v3&utm_content=CONTENT
```

Google Search also appends `{keyword}` only if the platform substitutes a safe value. Prefer a static `utm_term` per ad group if substitution is uncertain:

```
utm_term=inventory-software
```

If the console requires the signup path as the click URL, keep the same host and query:

```
https://inventory.lit-solutions.tech/api/auth/login?mode=signup&utm_source=SOURCE&utm_medium=MEDIUM&utm_campaign=lts-inv-essentials-trial-v3&utm_content=CONTENT
```

Auth0 may drop query parameters. Confirm before relying on UTMs for reporting (see landing-page checklist).

## Matrix

| Channel | utm_source | utm_medium | utm_content | Example ad |
|---|---|---|---|---|
| Meta | `meta` | `paid-social` | `facebook-trial` | Trial landscape |
| Meta | `meta` | `paid-social` | `ig-feed-know` | Square “Know what you have” |
| Meta | `meta` | `paid-social` | `ig-feed-went` | Square “Know where it went” |
| Meta | `meta` | `paid-social` | `ig-portrait-receive` | Portrait receiving |
| Meta | `meta` | `paid-social` | `ig-story-find` | Story Find |
| Meta | `meta` | `paid-social` | `ig-story-scan` | Story Scan |
| LinkedIn | `linkedin` | `paid-social` | `linkedin-square` | Square explain |
| LinkedIn | `linkedin` | `paid-social` | `linkedin-number` | Landscape number |
| LinkedIn | `linkedin` | `paid-social` | `facebook-trial` | Landscape trial (shared asset) |
| Google Search | `google` | `cpc` | `rsa-essentials` | Responsive search |
| Google Display | `google` | `display` | `google-728x90` | Leaderboard |
| Google Display | `google` | `display` | `google-300x250` | MREC |
| Google Display | `google` | `display` | `google-160x600` | Skyscraper |
| Google Display | `google` | `display` | `google-320x50` | Mobile banner |
| Google Display | `google` | `display` | `facebook-trial` | Landscape image asset |

`utm_content` equals the repo stem so Ads Manager names, filenames, and reports line up.

Ready-to-paste destination URLs for every first-flight stem are at the end of `campaign-v3/copy-to-paste.txt`.

## Tracking notes (do not invent coverage)

- Marketing site (`lit-solutions.tech`) can forward bounded UTMs onto signup links after consent. This flight’s approved destination is the **app host**, so that handoff may never run.
- Google tag `AW-18337968564` is on the marketing site, not verified here on `inventory.lit-solutions.tech`.
- Click IDs (`gclid`, `fbclid`, `li_fat_id`) are not configured in this pack.

Treat first-flight reporting as platform-reported clicks and landing-page sessions only, unless a later tracking project lands on the app host.
