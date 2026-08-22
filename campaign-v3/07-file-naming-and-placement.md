# 7. File naming and placement guidance

## Where files live in this repo

```
lts-inventory-ads/
  ads/                         ← v1. Do not use for this flight.
  ads-v2/                      ← v3 creatives (historical folder name). USE THESE PNGs.
  lts-inventory-ads-v3.zip     ← canonical downloadable v3 archive
  campaign-v3/                 ← this packaging set (brief, copy, checklists)
  README.md                    ← repo pointer to v3 zip + this pack
```

Upload from `ads-v2/`, or unzip `lts-inventory-ads-v3.zip` and take the PNGs. Do not mix v1 and v3 in one ad set.

## Keep the v3 filenames

Do not rename the PNG files in git. Existing names are the canonical keys in the manifest.

When an ad console asks for an upload name or an asset label, use:

```
lts-inv_v3_<platform>_<placement>_<stem>
```

Examples:

| Repo file | Console label |
|---|---|
| `facebook-trial.png` | `lts-inv_v3_meta_landscape_trial` |
| `ig-feed-know.png` | `lts-inv_v3_meta_feed_know` |
| `ig-feed-went.png` | `lts-inv_v3_meta_feed_went` |
| `ig-portrait-receive.png` | `lts-inv_v3_meta_portrait_receive` |
| `ig-story-find.png` | `lts-inv_v3_meta_story_find` |
| `ig-story-scan.png` | `lts-inv_v3_meta_story_scan` |
| `linkedin-number.png` | `lts-inv_v3_linkedin_landscape_number` |
| `linkedin-square.png` | `lts-inv_v3_linkedin_square_explain` |
| `google-728x90.png` | `lts-inv_v3_google_728x90` |
| `google-300x250.png` | `lts-inv_v3_google_300x250` |
| `google-160x600.png` | `lts-inv_v3_google_160x600` |
| `google-320x50.png` | `lts-inv_v3_google_320x50` |
| `landscape-fulfill.png` | Do not upload for this flight |

Stem is the existing filename without extension. That keeps Ads Manager, Campaign Manager, and this manifest aligned.

## Ad names inside each platform

Use the same stem after the campaign/ad-set prefix:

```
<campaign>__<adset>__<stem>
```

Example: `LTS-Inv_Essentials-Trial_v3_Meta__Feed__ig-feed-know`

Rules: ASCII letters, numbers, hyphen, underscore. No spaces in campaign/ad-set/ad names (spaces are allowed in UTM values only if needed; this pack avoids them).

## Copy files to paste from

1. Daily paste: `campaign-v3/copy-to-paste.txt` (mirrored at `ads-v2/copy-to-paste.txt`)
2. Channel notes and pairings: `campaign-v3/02-copy-meta.md`, `03-copy-linkedin.md`, `04-copy-google.md`

## Placement map (first flight)

| Placement | Files |
|---|---|
| Meta feed (landscape) | `facebook-trial.png` |
| Meta/IG feed square | `ig-feed-know.png`, `ig-feed-went.png`, `linkedin-square.png` |
| Meta/IG feed portrait | `ig-portrait-receive.png` |
| IG/Facebook stories | `ig-story-find.png`, `ig-story-scan.png` |
| LinkedIn landscape | `linkedin-number.png`, `facebook-trial.png` |
| LinkedIn square | `linkedin-square.png` |
| Google Display | four `google-*.png` banners |
| Google Search | no image; RSA copy only |

## What not to invent

- No new aspect ratios
- No cropped “safe-zone” variants unless a platform rejects an existing file
- No added badges, URLs, or “#1” stickers on the PNGs
