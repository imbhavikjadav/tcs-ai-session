# FreightNexus Demo Screenshot Manifest

All screenshots captured at a 1440x900 desktop viewport via Playwright (headless Chromium). Zero mobile/narrow-viewport screenshots exist anywhere in this folder (verified: every PNG is 1440px wide).

**Demo trip used throughout:** `TRP00060` — Ahmedabad, Gujarat → Rajkot, Gujarat. Goods: 40 cartons of branded home electronics and small appliances (LED TVs, mixer-grinders, inverter parts), fragile, 3,200 kg, closed-container body type. Business Owner: Bhavik Jadav. Driver: Akshay Makwana (DRV0043, Tata Motors 407 Gold SFC, GJ01AB1234).

**Final settlement:**
- Freight ₹18,000 + Driver allowance ₹1,500 + Toll (actual) ₹1,050 (estimated ₹850 at bid time, delta +₹200) + Misc expense ₹200 (police checkpoint fee) = **Settlement total ₹20,750**
- Deposit (25%, paid on acceptance): **₹5,087.5** — confirmed
- Final payment (remaining after deposit): **₹15,662.5** — confirmed
- Trip status: **Completed**. Both parties rated each other 5★.

Total files: **87** (85 PNG screenshots + 2 PDF invoices). 47 existed prior to this session; 40 were added completing the trip lifecycle from "arrival confirmed" through completion, ratings, dashboards, notifications, and profile pages.

---

## public/ (6 files)
Marketing site and auth pages, unauthenticated.

| File | Description |
|---|---|
| 01-landing-hero.png | Landing page hero section |
| 02-landing-how-it-works.png | Landing page "how it works" section |
| 03-landing-features.png | Landing page features section |
| 04-landing-footer.png | Landing page footer |
| 05-sign-in.png | Sign-in form |
| 06-sign-up-role-picker.png | Sign-up role picker (Business Owner vs Driver) |

## trip/ (19 files)
Trip posting wizard (Business Owner) through bid acceptance and in-transit tracking, for TRP00060.

| File | Description |
|---|---|
| 01-post-step1-route-empty.png | Post-trip wizard step 1 (route), empty |
| 02-post-step1-route-filled.png | Step 1 filled: Ahmedabad → Rajkot |
| 03-post-step2-goods-empty.png | Step 2 (goods details), empty |
| 04-post-step2-goods-nature-open.png | Step 2, "nature of goods" dropdown open |
| 05-post-step2-bodytype-open.png | Step 2, required body type dropdown open |
| 06-post-step2-goods-filled.png | Step 2 filled: electronics/appliances, 3,200 kg, closed container |
| 07-post-step3-timeline-empty.png | Step 3 (pickup window/expected delivery), empty |
| 08-post-step3-timeline-filled.png | Step 3 filled with pickup window and expected delivery date |
| 09-post-step4-receiver-empty.png | Step 4 (receiver details), empty |
| 10-post-step4-receiver-filled.png | Step 4 filled with receiver contact info |
| 11-post-step5-review.png | Step 5, final review before posting |
| 12-post-trip-success.png | Trip posted successfully confirmation |
| 13-bo-trip-with-bid-top.png | BO trip detail page after a driver bid arrives |
| 14-bo-review-bids.png | BO reviewing submitted bids |
| 15-bo-after-accept-top.png | Trip detail top section after BO accepts a bid |
| 16-bo-after-accept-mid.png | Trip detail mid section after acceptance |
| 17-bo-after-accept-bottom.png | Trip detail bottom section after acceptance |
| 18-in-transit-top-bo.png | BO view once trip is in transit |
| 19-in-transit-tracking-map-bo.png | BO view of live tracking map during transit |

## driver/ (37 files)
Full driver-side lifecycle: browsing, bidding, deposit, pickup, in-transit, delivery sign-off, final expenses, payment confirmation, completion, rating, dashboard, notifications, profile.

| File | Description |
|---|---|
| 01-dashboard.png | Driver dashboard, initial state |
| 02-browse-trips.png | Browse available trips/bids listing |
| 03-trip-detail-before-bid.png | Trip detail page before placing a bid |
| 04-bid-form-empty.png | Bid form, empty |
| 05-bid-form-filled.png | Bid form filled (freight, allowance, estimated toll) |
| 06-bid-submitted.png | Bid submitted confirmation |
| 07-confirm-deposit-view.png | Driver view while deposit payment is pending |
| 08-after-confirm-deposit.png | Driver view after confirming deposit received |
| 09-confirm-pickup-empty.png | Confirm-pickup form, empty |
| 10-confirm-pickup-photos-selected.png | Confirm-pickup form with 4 pickup-condition photos selected |
| 11-pickup-submitted-awaiting-verify.png | Pickup submitted, awaiting BO verification |
| 12-in-transit-top-driver.png | Driver view once trip is in transit |
| 13-delivery-signoff-step-arrival.png | Delivery sign-off step, arrival stage |
| 14-confirm-arrival-checked.png | (Prior session) "I have called the receiver" checkbox checked |
| 15-confirm-arrival-checked.png | (This session, continuation) checkbox re-checked after session reload, before clicking Confirm arrival |
| 16-after-confirm-arrival.png | Immediately after clicking Confirm arrival (transition in progress) |
| 17-delivery-signoff-question.png | "Is everything in order?" Yes/No damage question |
| 18-delivery-photo-upload-empty.png | Delivery-condition photo upload section, empty, after answering Yes |
| 19-delivery-photos-selected.png | All 4 delivery-condition photos selected, Complete delivery button visible |
| 20-delivery-photos-submitted.png | Delivery photos submitted — milestone updated, step 6 now "waiting on Business Owner" |
| 21-awaiting-bo-photo-verify.png | Driver view scrolled to "Verify delivery photos" step, awaiting BO |
| 22-final-toll-expenses-empty.png | Submit final toll & expenses form, empty (shows ₹850 estimate) |
| 23-final-toll-filled-expense-form.png | Toll amount (₹1,050) + FASTag receipt uploaded, "Add an expense" row opened |
| 24-final-toll-and-expense-filled.png | Full form filled: toll ₹1,050 + receipt, expense ₹200 (police checkpoint fee) + description + receipt |
| 25-final-toll-expenses-submitted.png | Submit clicked, "Submitting..." transitional state |
| 26-toll-expenses-confirmed-view.png | Confirmed view: step 7 done, step 8 "Approve final amount — waiting on Business Owner" |
| 27-final-amount-breakdown.png | Final amount breakdown showing toll delta (+₹200) and misc expense folded in |
| 28-confirm-final-payment-view.png | "Confirm final payment received" step, BO's proof visible, before confirming |
| 29-trip-completed-driver.png | Trip completed, top viewport (all milestones dated) |
| 29-trip-completed-driver-fullpage.png | Trip completed, full page scroll capture |
| 30-rating-form-empty.png | Driver's rating form for Bhavik Jadav, empty |
| 31-rating-form-filled.png | Rating form: 5 stars selected + comment typed, before submit |
| 32-rating-submitted.png | Rating submitted: "You rated: 5★ — ..." confirmation |
| 33-dashboard-trip-completed.png | Driver dashboard: 2 trips this month, ₹45,600 total earned, 6,400 kg cargo carried, both trips shown COMPLETED, reviews section with 5.0 average |
| 34-notifications-panel.png | Notifications panel opened (bell icon, 9+ pending) |
| 35-profile-page.png | Driver's "Your Profile" / account details page |
| 36-notification-preferences.png | Driver's notification preferences page (email toggle categories) |

## business-owner/ (16 files)
BO-side pickup/delivery verification, final settlement approval, payment, completion, rating, dashboard, notifications, profile.

| File | Description |
|---|---|
| 01-dashboard.png | BO dashboard, initial state |
| 02-verify-pickup-photos.png | BO verifying pickup-condition photos |
| 03-pickup-photos-card.png | Pickup photos card detail view |
| 04-verify-delivery-photos.png | BO trip detail at "Verify delivery photos" step, before clicking |
| 05-delivery-photos-modal.png | Delivery-photo verification in progress ("Saving...") |
| 06-delivery-photos-verified.png | Delivery photos verified — step 7 (final toll & expenses) now waiting on driver |
| 07-approve-final-amount-view.png | BO view of "Approve final amount" step with toll delta and misc expense listed |
| 08-final-amount-approved.png | Final amount approval clicked, "Saving..." transitional state |
| 09-trip-completed-bo-fullpage.png | Trip completed, full-page scroll capture (BO perspective) |
| 10-rating-form-empty.png | BO's rating form for Akshay Makwana, empty |
| 11-rating-form-filled.png | Rating form: 5 stars + comment, before submit |
| 12-rating-submitted-both-visible.png | Both invoices (Acceptance + Completion) and both parties' 5★ ratings visible together |
| 13-dashboard-trip-completed.png | BO dashboard/account page showing TRP00060 and TRP00059 both COMPLETED |
| 14-notifications-panel.png | Notifications panel opened (bell icon, 21 pending) |
| 15-profile-page.png | BO's "Your Profile" / account details page (Aadhaar KYC doc, Approved) |
| 16-notification-preferences.png | BO's notification preferences page |

## payments/ (7 files)
Deposit and final-payment flows.

| File | Description |
|---|---|
| 01-deposit-pay-form-empty.png | Deposit payment form, empty |
| 02-deposit-pay-form-filled.png | Deposit payment form with proof uploaded |
| 03-deposit-marked-paid-bo.png | BO marks deposit as paid |
| 04-deposit-paid-status-top.png | Deposit-paid status reflected at top of trip page |
| 05-final-payment-form-empty.png | Final payment ("Pay the final amount") form, empty |
| 06-final-payment-form-filled.png | Final payment form with Payment-Full-Receipt.jpeg proof uploaded |
| 07-final-payment-marked-paid-bo.png | BO marks final payment as paid ("I've paid this") |

## invoices/ (2 files)
PDF invoices fetched via signed Supabase Storage URL (response interception on the download server action).

| File | Description |
|---|---|
| freightnexus-acceptance-invoice.pdf | Acceptance invoice, generated on bid acceptance/deposit. 1 page. |
| freightnexus-completion-invoice.pdf | Completion invoice (INV-TRP00060-18095E), generated on trip completion. 2 pages. Full charge breakdown: Freight ₹18,000, Driver allowance ₹1,500, Toll (actual) ₹1,050, Misc expense ₹200, Settlement total ₹20,750, Deposit ₹5,087.5 confirmed, Final payment ₹15,662.5 confirmed. Includes full status-history timeline and shipper/driver/truck details. |

---

## Notes
- `driver/14-confirm-arrival-checked.png` and `driver/15-confirm-arrival-checked.png` are two distinct captures of the same UI moment (checkbox checked, pre-submit) taken in different sessions — both retained, no duplicates were deleted per instructions.
- `driver/29-trip-completed-driver.png` (viewport-only) and `driver/29-trip-completed-driver-fullpage.png` (full scroll) share the numeric prefix by design — both capture the same completed-trip milestone at different scroll extents.
- No trip data was wiped or reset after capture, per standing instructions.
- No application source files were modified during this session (`git status` in `/Users/jadz/AI Stuff/freightnexus` is clean).
