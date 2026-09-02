# FreightNexus screenshots — TRP00062 run

Captured against a freshly wiped production Supabase database. Two real accounts registered
from zero, KYC-approved by a real admin account, one real trip run start to finish, both
invoices fetched from Storage. All screenshots are desktop viewport (1440×900) — no mobile
captures in this set.

- **Business Owner**: Bhavik Jadav (`imbhavikjadav@gmail.com`) — BSOW0057
- **Individual Owner-Driver**: Akshay Makwana (`jadav.itprof@gmail.com`) — DRV0053
- **Admin**: `freightnexus.showcase.admin@gmail.com`
- **Truck**: GJ01AB1234 — Tata Motors 407 Gold SFC, closed container, 3.5T, home state Gujarat
- **Trip**: TRP00062 — Memnagar, Ahmedabad, Gujarat → Jweles Circle, Bhavnagar, Gujarat
  - Goods: Fragile — Cartons of Electronics, 2,800kg, closed container required
  - Bid: ₹19,000 freight + ₹1,500 driver allowance + ₹750 estimated toll = ₹21,250
  - Settlement: ₹19,000 freight + ₹1,500 allowance + ₹780 actual toll (+₹30 delta) + ₹200
    loading-labor expense = ₹21,480
  - Deposit (25%): ₹5,312.5 — Final payment: ₹16,167.5
  - Both parties rated each other 5 stars

## Folders

- `public/` — landing page + sign-in/sign-up (6 screenshots)
- `business-owner/` — Bhavik's full 4-step registration wizard through KYC submission (8 screenshots)
- `driver/` — Akshay's registration + truck sub-wizard, then his entire trip lifecycle as the driver:
  browsing, bidding, deposit, pickup, in-transit, delivery sign-off, toll/expense settlement,
  final payment confirmation, trip completion, rating (35 screenshots)
- `admin/` — dashboard, KYC queue before/after approval, accounts list (4 screenshots)
- `trip/` — the business-owner side of the same lifecycle: posting the 5-step trip wizard, reviewing
  and accepting the bid, deposit, verifying pickup/delivery photos, approving the final amount,
  marking final payment paid, the fully completed trip with both ratings visible (24 screenshots)
- `invoices/` — the two real generated PDFs (Acceptance + Completion), fetched via signed URL
  straight from Supabase Storage, not screenshotted

## Known bugs fixed in this run (do not reintroduce)

1. **Goods description overflow** — a long free-text goods description previously overflowed the
   invoice PDF layout. Fixed by using the short value "Cartons of Electronics" everywhere, from the
   very first trip-posting step, not patched after the fact.
2. **Destination address showing a pincode / wrong locality** — caused by clicking a Google Places
   Autocomplete suggestion, which silently substitutes a more specific (and sometimes wrong) result
   for what the user actually typed. Fixed by typing the address directly and dismissing the
   autocomplete dropdown with Escape, so the literal typed text ("Memnagar, Ahmedabad, Gujarat" /
   "Jweles Circle, Bhavnagar, Gujarat") reaches the server's own Geocoding API call untouched. The UI
   and both invoice PDFs correctly show only city/state as the bold headline, with the full geocoded
   address as plain subtext underneath — never a raw pincode line.
3. **Sticky navbar duplicated mid-page on tall screenshots** — every `page.screenshot({ fullPage: true })`
   call composited the site's fixed header a second time at its on-screen scroll position, landing it
   in the middle of the captured image (worst on the truck-documents step, and on several trip-lifecycle
   screens like delivery sign-off, toll settlement, and photo verification). Fixed by never using
   `fullPage: true` again for this gallery — every screenshot below is a plain 1440×900 viewport capture,
   scrolled to the relevant section first. The truck-documents/truck-photos/step-6-review and five
   trip-lifecycle screens (pickup verification, delivery sign-off, delivery photos, delivery
   verification, toll settlement) were re-captured this way, some against a second disposable throwaway
   trip (TRP00063, same route/goods/figures as TRP00062, never carried past the toll-settlement step)
   so the already-completed TRP00062 didn't need to be redone. A literal duplicate screenshot
   (`admin/05-accounts-list.png` used twice) and a near-illegible tiny crop
   (`admin/03-document-review-closeup.png`) were also dropped from the gallery entirely, along with the
   landing-page footer screenshot (same duplicated-header bug), rather than replaced.
