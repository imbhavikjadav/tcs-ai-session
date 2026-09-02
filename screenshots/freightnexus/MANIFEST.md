# FreightNexus Screenshot Set — MANIFEST

**Trip reference:** TRP00061
**Route:** Ahmedabad, Gujarat → Bhavnagar, Gujarat (geocoded to Tarsimiya Part, Gujarat 364002, on Ghogha Rd — within Bhavnagar city)
**Trip UUID:** `f598af17-38ea-43b2-a401-c49a61f4d97d`
**Business Owner:** Bhavik Jadav (imbhavikjadav@gmail.com, BSOW0051)
**Driver:** Akshay Makwana (jadav.itprof@gmail.com, DRV0043), truck GJ01AB1234 — Tata Motors 407 Gold SFC, Closed Container
**Goods description used (verbatim, everywhere):** `Cartons of Electronics` — always shown in the UI/PDF as `2800kg · fragile — Cartons of Electronics` (weight + nature-of-goods dropdown + this exact free-text field, concatenated by the app). Confirmed short and non-overflowing in both invoice PDFs (see Invoices section below).
**Captured:** 2 September 2026, all screenshots at desktop viewport **1440×900**. Zero mobile/narrow-viewport screenshots exist anywhere in this set.

All screenshots are PNG, captured live against a real running instance of the app (local dev server hitting the production Supabase project), by driving the full trip lifecycle exactly once, in order, end to end. Nothing here is mocked or edited after capture.

---

## Settlement summary

| Item | Amount |
|---|---|
| Freight | ₹16,500 |
| Driver allowance | ₹1,200 |
| Toll — estimated at bid time | ₹650 |
| Toll — actual (submitted at settlement) | ₹980 (delta **+₹330**) |
| Additional expense — Police checkpoint fee near Bagodara (vehicle document verification) | ₹200 |
| **Bid subtotal / Settlement total** | **₹18,880** |
| Deposit (25%, paid on acceptance) | ₹4,587.50 |
| **Final payment (remaining after deposit)** | **₹14,292.50** |

Deposit proof: `Payment-Deposit-Receipt.jpeg`. Toll proof: `Fastag-Toll-Receipt.jpeg`. Misc-expense proof: `Police-Checking-Receipt.jpeg`. Final-payment proof: `Payment-Full-Receipt.jpeg`.

Both parties rated each other 5★ on completion, with distinct, realistic comments (see `business-owner/12-rating-submitted.png` and `driver/31-rating-submitted.png`).

---

## Folder breakdown (85 PNGs + 2 PDFs)

### `public/` — 6 files
Marketing site and auth entry points (no login required).
- `01-landing-hero.png` — landing page hero section
- `02-landing-how-it-works.png` — how-it-works section
- `03-landing-features.png` — features section
- `04-landing-footer.png` — footer section
- `05-sign-in.png` — sign-in form
- `06-sign-up-role-picker.png` — sign-up role picker (Business Owner vs Owner-Driver)

### `trip/` — 19 files
The trip-posting wizard and the Business-Owner-side trip detail page as the trip progresses through acceptance and early execution.
- `01`–`11` — Post-a-trip wizard, every step empty and filled: route, goods (weight/nature/description/body type), timeline, receiver & deposit, review
- `12-post-trip-success.png` — post-submit state (wizard resets to step 1 after successful creation)
- `13-posted-trip-detail-bo.png` — freshly posted trip TRP00061, status ACTIVE
- `14`, `15` — BO viewing the trip with Akshay's bid, and reviewing the bid card
- `16`, `17` — BO after accepting the bid (top and bottom of page)
- `18`, `19` — In-transit state, BO view: live tracking map + milestone timeline

### `business-owner/` — 16 files
BO-side dashboard, verification steps, final approval/payment, ratings, notifications, profile.
- `01-dashboard.png` — BO dashboard (account page)
- `02`, `03` — verifying pickup photos, pickup verified
- `04`, `05`, `06` — verifying delivery photos, delivery photo gallery, delivery verified
- `07`, `08` — reviewing and approving the final settlement amount
- `09-trip-completed-bo-fullpage.png` — full-page capture of the completed trip (milestones, payments, accepted bid, rating, photos, status history)
- `10`, `11`, `12` — rating form empty, filled (5★ + comment), submitted (both ratings visible)
- `13-dashboard-trip-completed.png` — dashboard showing TRP00061 among completed trips, updated stats
- `14-notifications-panel.png` — notification bell dropdown (Pending Actions tab)
- `15-profile-page.png` — BO profile/account page
- `16-notification-preferences.png` — email notification preference toggles

### `driver/` — 39 files
Driver-side full lifecycle: login, browse, bid, every execution step, toll/expenses, rating, notifications, profile.
- `01-dashboard.png`, `02-browse-trips.png` — driver dashboard and trip marketplace
- `03`, `03b` — trip detail before bidding (with goods description visible)
- `04`, `05`, `06` — bid form empty, filled (₹16,500 + ₹1,200 + ₹650 = ₹18,350 total), submitted/pending
- `07`, `08`, `08-en-route-milestone` — confirming deposit received, en-route milestone reached
- `09`, `10`, `11` — confirm-pickup: empty form, 4 pickup photos attached, submitted
- `12-in-transit-top-driver.png` — driver's in-transit view
- `13`, `14`, `15` — arrival: "I have called the receiver" checkbox, checked, confirmed (Arrived — Pending Sign-Off)
- `16`, `17` — delivery sign-off question ("Is everything in order?"), "Yes" selected
- `18`, `19`, `20` — delivery photos empty, 4 photos attached, delivery completed/submitted
- `21`–`25` — final toll & expenses: empty form, toll filled (₹980 + Fastag receipt), add-expense form, toll+expense filled (₹200 police checkpoint fee + receipt), submitted
- `26`, `27` — confirming final payment received, trip completed (driver view)
- `28-trip-completed-driver-fullpage.png` — full-page capture of the completed trip, driver perspective
- `29`, `30`, `31` — rating form empty, filled (5★ + comment), submitted (both ratings visible)
- `32-dashboard-trip-completed.png` — driver dashboard showing TRP00061 completed, updated stats (3 trips, ₹64,480 total earned)
- `33`, `33b` — notification bell dropdown (Pending Actions tab, and Notifications-list tab showing live event feed)
- `34-profile-page.png` — driver profile/account page
- `35-notification-preferences.png` — driver's email notification preference toggles

### `payments/` — 6 files
Deposit and final-payment flows (Business-Owner side, the party who pays).
- `01`, `02`, `03` — deposit payment: empty form, receipt attached (`Payment-Deposit-Receipt.jpeg`), marked paid
- `05`, `06`, `07` — final payment: empty form, receipt attached (`Payment-Full-Receipt.jpeg`), marked paid

### `invoices/` — 2 PDFs
Both fetched live from the app's server-action → signed Supabase Storage URL flow (not synthesized).
- `freightnexus-acceptance-invoice.pdf` (140 KB) — generated at bid acceptance. Goods row: `2800kg · fragile — Cartons of Electronics`, single line, no overflow.
- `freightnexus-completion-invoice.pdf` (140 KB) — generated at trip completion. Goods row: `2800kg · fragile — Cartons of Electronics`, single line, no overflow. Full itemized settlement (freight, driver allowance, actual toll with delta note, misc expense, deposit, final payment) and full status history, all render cleanly with no column overlap anywhere on the page.

---

## Goods-description fix verification

This is the third attempt at this demo capture. The first two used a long descriptive sentence in the "Goods Description" field, which overflowed the invoice PDF's fixed-width "Goods" row and overlapped adjacent text. This run used **exactly** `Cartons of Electronics` in that field, with weight (2800 kg) and nature-of-goods (Fragile) set via their own separate controls.

Verified in three independent ways:
1. **UI, both roles, throughout the lifecycle** — every trip detail view (BO and driver, at every step from posting through completion) rendered `Goods: Fragile — Cartons of Electronics` on one line.
2. **PDF text extraction** (`pdftotext -layout`) on both invoices — `Goods` row reads `2800kg · fragile — Cartons of Electronics`, fits on a single line inside the layout, no wrapping.
3. **PDF visual render** (`pdftoppm` → PNG, completion invoice) — inspected directly: the Goods row sits cleanly right-aligned in its column, does not wrap to a second line, and does not overlap the "Pickup window" row below it or any other element on the page.

---

## Verification checklist

- [x] Trip TRP00061 posted, Ahmedabad → Bhavnagar, goods description exactly "Cartons of Electronics" (confirmed in UI and both PDFs)
- [x] Completion invoice "Goods" row does not overflow or overlap — confirmed via text extraction and visual PDF render
- [x] 85 PNG screenshots, all confirmed 1440px wide (desktop), zero mobile-viewport screenshots
- [x] Both invoice PDFs fetched live via the popup-tab → signed-URL → `page.request.get()` flow and saved successfully (140 KB each)
- [x] `git status` in `/Users/jadz/AI Stuff/freightnexus/` is clean — no source files modified, nothing staged, nothing untracked
- [x] Dev server stopped after capture; trip data left as-is in production per standing instructions (no wipe/delete)
