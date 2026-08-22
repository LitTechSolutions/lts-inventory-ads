# 9. Landing-page consistency checklist

Approved destination: **https://inventory.lit-solutions.tech**

This checklist compares the **ad offer** to what an unauthenticated visitor actually sees. Complete it in a logged-out browser immediately before any human enables spend.

## Ad promise (must all be true)

- [ ] Seven-day trial
- [ ] Essentials plan
- [ ] No card required to start
- [ ] $49 per month after the trial
- [ ] Destination host is `inventory.lit-solutions.tech`

## Observed destination behavior (as of pack writing, 2026-08-20)

| Check | Result | Action before launch |
|---|---|---|
| Root URL loads | Redirects to Auth0 login: “Welcome” / “Log in to LTS Inventory to continue to LTS Inventory.” | Confirm still true. Ads will not land on a marketing page. |
| Signup URL | `https://inventory.lit-solutions.tech/api/auth/login?mode=signup` opens Auth0 signup (email / password). | Prefer this as the click URL if the platform allows a path on the same host. |
| Trial length on the Auth0 screen | Not shown | Gap. Do not claim the landing screen itself restates “7 days.” |
| “No card” on the Auth0 screen | Not shown | Gap. |
| “Essentials” / “$49” on the Auth0 screen | Not shown | Gap. Plan choice is described on the **marketing** site as happening at signup, not on the Auth0 form. |
| Marketing site restates the offer | Yes, on https://lit-solutions.tech (home, pricing, FAQ, terms) | Not this flight’s destination. Do not swap destinations without an owner change to the brief. |

## Consistency checks to run (human)

Open the final URL from the ad preview, including UTMs.

- [ ] HTTPS padlock; host is exactly `inventory.lit-solutions.tech` (or Auth0 as a login redirect from that host)
- [ ] Page is a real login/signup, not a 404, 5xx, or parked screen
- [ ] Visitor can create an account without a payment form on the first screen
- [ ] After account creation, Essentials is selectable for a self-service trial (or is the trial plan)
- [ ] No card is required to begin the seven-day trial
- [ ] Post-trial price shown in-product or at checkout is $49/month for Essentials (checkout shows the charge before pay)
- [ ] Query string (`utm_*`) either survives to the app or is documented as dropped by Auth0
- [ ] Mobile: form is usable; no interstitial that contradicts “no card”
- [ ] Terms and privacy are reachable before payment (marketing legal pages live at https://lit-solutions.tech/terms and https://lit-solutions.tech/privacy)

## Known mismatch (do not paper over in ads)

Ads describe a **seven-day Essentials trial, no card, $49/mo after**. The first screen on the approved destination currently describes **log in / sign up**, not the offer.

That is allowed only if:

1. The signup path still starts the seven-day no-card trial on Essentials, and
2. Copy does not claim the landing **page** displays pricing.

If a reviewer cannot complete a no-card Essentials trial from the destination, **do not enable the flight**. Fix the product onboarding or change the destination in a new brief.

## What ads must not imply about the landing page

- A product tour, pricing table, or comparison grid on `inventory.lit-solutions.tech`
- Instant warehouse access without account creation
- That Operations, Control, or Enterprise is the advertised trial
- That a card will be collected on the first screen
