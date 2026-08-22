# 12. Manual launch instructions — first flight

**Do not launch or fund from this document.** Build everything **paused**. Enabling spend is a separate owner action after preflight.

Work in the live ad consoles (Meta Ads Manager, LinkedIn Campaign Manager, Google Ads). There is no API launch in this repo.

## 0. Before any console

1. Read `01-campaign-brief.md` and `11-preflight-checklist.md`.
2. Confirm destination: https://inventory.lit-solutions.tech
3. Confirm the signup path still opens without a card field: https://inventory.lit-solutions.tech/api/auth/login?mode=signup
4. Stage PNG uploads from `ads-v2/` (skip `landscape-fulfill.png`).
5. Keep `copy-to-paste.txt` open.

Stop if the trial path requires a card or does not offer Essentials.

---

## A. Meta (Facebook / Instagram)

1. Ads Manager → **Campaigns** → Create.
2. Objective: **Traffic** (safest without an app conversion pixel). Do not select a conversion event that is not verified on the app host.
3. Campaign name: `LTS-Inv_Essentials-Trial_v3_Meta`
4. Buying: Auction. Advantage+ catalog **off**.
5. Budget: leave blank or enter a figure **only if the campaign stays paused**. This pack does not set an amount.
6. Create three ad sets, all **Off**:
   - `Trial-Landscape`
   - `Feed`
   - `Stories`
7. Geo: United States unless the owner specifies otherwise. Age 25+; no detailed targeting that implies a regulated industry LTS does not serve.
8. Placements: start with **manual** — Feeds for Feed/Landscape; Stories/Reels for Stories.
9. Create ads:

| Ad set | Image | Primary | Headline | Description | utm_content |
|---|---|---|---|---|---|
| Trial-Landscape | `facebook-trial.png` | A | 7 days free. $49/mo after. | 7-day trial. No card. | `facebook-trial` |
| Feed | `ig-feed-know.png` | C | Know what you have. | Lots, serials, history. | `ig-feed-know` |
| Feed | `ig-feed-went.png` | A | Know where it went. | Lots, serials, history. | `ig-feed-went` |
| Feed | `ig-portrait-receive.png` | D | Track lots and serials. | Essentials is $49/mo. | `ig-portrait-receive` |
| Stories | `ig-story-find.png` | C | Know what you have. | 7-day trial. No card. | `ig-story-find` |
| Stories | `ig-story-scan.png` | C | Know where it went. | 7-day trial. No card. | `ig-story-scan` |

10. Destination: `https://inventory.lit-solutions.tech?utm_source=meta&utm_medium=paid-social&utm_campaign=lts-inv-essentials-trial-v3&utm_content=<stem>`
11. CTA: **Sign up**.
12. Identity: LTS Inventory Page (create/verify the Page first if missing). Do not use a personal profile.
13. Save. Confirm status is **Off / Paused**.
14. Preview each placement. **Do not click Publish as Active.**

---

## B. LinkedIn

1. Campaign Manager → Create → **Awareness** or **Website visits** (visits if the account can run it without a Insight Tag conversion).
2. Campaign group name: `LTS-Inv_Essentials-Trial_v3_LinkedIn`
3. Campaign: `Single-Image`. Format: Single image ad.
4. Objective that does not require an unverified conversion.
5. Audience: United States; company size 1–200 as a starting filter if available; job functions Operations / Purchasing / Owner. Do not upload a customer list unless counsel approved it.
6. Ads:

| Image | Intro | Headline | utm_content |
|---|---|---|---|
| `linkedin-square.png` | A | Inventory you can explain. | `linkedin-square` |
| `linkedin-number.png` | B | Know what you have. Know where it went. | `linkedin-number` |
| `facebook-trial.png` (optional landscape) | C | 7-day Essentials trial. No card. | `facebook-trial` |

7. Destination with UTMs (`utm_source=linkedin`, `utm_medium=paid-social`, `utm_content` as above).
8. CTA: **Sign up**.
9. Budget: none, or saved with campaign **Paused**.
10. Save as draft/paused. **Do not launch.**

---

## C. Google Ads — Search

1. Create campaign → **Search**.
2. Name: `LTS-Inv_Essentials-Trial_v3_Search`
3. Conversion goals: do not import a purchase goal unless it fires on the app host. Use clicks for this flight.
4. Networks: Search only. Display expansion **off**. Partners **off**.
5. Geo: United States. Language: English.
6. Bidding: manual CPC or “maximize clicks” only if the campaign remains paused and no budget is live.
7. Ad group: `RSA-Essentials`
8. Keywords (phrase + exact): `lts inventory`, `inventory software`, `lot tracking inventory`, `serial number inventory`, `inventory lot and serial`
9. Negative: `free download`, `career`, `salary`, `ERP` if those queries appear in preview. Do not add competitor brands without owner approval.
10. Responsive search ad: paste all 15 headlines and 4 descriptions from `04-copy-google.md`.
11. Final URL: `https://inventory.lit-solutions.tech?utm_source=google&utm_medium=cpc&utm_campaign=lts-inv-essentials-trial-v3&utm_content=rsa-essentials`
12. Paths: `trial` / `essentials`
13. Optional pin: H1 `LTS Inventory`, H2 `7-day trial. No card.`
14. Save. Status **Paused**.

---

## D. Google Ads — Display

1. Create campaign → **Display** (or add an asset group only if already using a paused Search campaign’s shared library).
2. Name: `LTS-Inv_Essentials-Trial_v3_Display`
3. Upload banners: `google-728x90.png`, `google-300x250.png`, `google-160x600.png`, `google-320x50.png`.
4. Optional landscape: `facebook-trial.png` only — not `landscape-fulfill.png`.
5. Business name: `LTS Inventory`
6. Paste short headlines, long headlines, and descriptions from `04-copy-google.md`.
7. Final URL with `utm_source=google&utm_medium=display&utm_campaign=lts-inv-essentials-trial-v3&utm_content=<banner-stem>`
8. Audience: in-market inventory / supply chain if available; otherwise contextual keywords from the search list. No remarketing list unless pixels exist on the destination.
9. Save. Status **Paused**.

---

## E. After all three consoles

1. Run `11-preflight-checklist.md`.
2. Screenshot paused campaigns into an internal note (not required in this repo).
3. Send the draft PR / pack to the owner.
4. **Stop.** Do not attach spend, do not enable, do not A/B beyond the saved paused ads.

Owner enable sequence (not performed here):

1. Re-run the destination trial path.
2. Attach billing in each ads account.
3. Set a budget the owner chooses.
4. Enable **one** channel first (recommended: Google Search RSA or Meta trial landscape).
5. Watch landing-page errors for 24 hours before enabling the rest.
