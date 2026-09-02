# FreightNexus Screenshot Manifest

Captured against the **real production Supabase backend** via `npm run dev` on `localhost:3000` (this app has no local database — local dev talks directly to production per its own CLAUDE.md). All accounts, the truck, and the trip below are real rows created during this run and are being **kept**, not wiped.

Real test accounts used:
- Business Owner: Bhavik Jadav — `imbhavikjadav@gmail.com` — profile id `05d20752-0710-4ceb-bc1a-089638f96309` — display code `BSOW0051`
- Individual Owner-Driver: Akshay Makwana — `jadav.itprof@gmail.com` — profile id `d8a31a65-0e0e-467d-8ba4-84e2fec34d0a` — display code `DRV0043`
- Truck: `GJ01AB1234` — Tata Motors 407 Gold SFC, Closed Container, Gujarat — truck id `702f5b0e-839f-4442-9df4-f23e54dc4991`
- Trip: `TRP00059` — Ahmedabad → Bhavnagar — trip id `ffc745f7-4c41-456c-bb28-5d9b814c06b3` — status: **completed**
- Admin (provisioned via `scripts/create-admin.mjs`, a sanctioned operator script — not the `dev-approve-kyc.mjs` bypass): `freightnexus.showcase.admin@gmail.com`

---

## Public

| File | Description |
|---|---|
| `public/01-landing-page-mobile.png` | Landing page, full page, mobile width (430px) |
| `public/01-landing-page-desktop.png` | Landing page, full page, desktop width (1440px) — flagship screen |
| `public/02-signup-role-picker.png` | Sign-up entry screen — Business Owner / Individual Owner-Driver / Fleet Owner role picker |

## Business Owner registration (Bhavik Jadav)

| File | Description |
|---|---|
| `business-owner/03-signup-form-account-details.png` | Step 1 of 4 — empty account details form (name/phone/email/password) |
| `business-owner/03b-signup-form-filled.png` | Step 1 filled with Bhavik Jadav's real details |
| `business-owner/04-signup-step2-identity-doc-empty.png` | Step 2 of 4 — Government ID form, empty (Aadhaar default) |
| `business-owner/05-signup-step2-identity-doc-filled.png` | Step 2 filled — Aadhaar number + BO-Aadhaar-Card.jpeg uploaded |
| `business-owner/06-signup-step3-photo-empty.png` | Step 3 of 4 — passport-style photo upload, empty |
| `business-owner/07-signup-step3-photo-filled.png` | Step 3 filled — BO-Passport-Photo.jpeg uploaded |
| `business-owner/08-signup-step4-review.png` | Step 4 of 4 — review/submit screen, all items checked |
| `business-owner/09-registration-success-pending-review.png` | Post-submit account screen — "Your profile is under review," Pending Review badge |
| `business-owner/10-dashboard-pre-approval-mobile.png` | Dashboard, pre-approval state, mobile |
| `business-owner/10b-dashboard-pre-approval-desktop.png` | Dashboard, pre-approval state, desktop — flagship screen |

## Individual Owner-Driver registration (Akshay Makwana)

| File | Description |
|---|---|
| `driver/11-signup-form-account-details.png` | Step 1 of 6 — empty account details form |
| `driver/11b-signup-form-filled.png` | Step 1 filled with Akshay Makwana's real details |
| `driver/12-signup-step2-govt-id-empty.png` | Step 2 of 6 — Government ID form, empty |
| `driver/13-signup-step2-govt-id-filled.png` | Step 2 filled — Aadhaar + Driver-Aadhaar-Card.jpeg |
| `driver/15-signup-step3-photo-empty.png` | Step 3 of 6 — passport photo upload, empty |
| `driver/16-signup-step3-photo-filled.png` | Step 3 filled — Driver-Passport-Photo.jpeg |
| `driver/18-signup-step4-dl-empty.png` | Step 4 of 6 — Driving License form, empty |
| `driver/19-signup-step4-dl-filled.png` | Step 4 filled — DL number, expiry date, Driver-Driving-License.jpeg |
| `driver/21-signup-step5-substep1-truck-details-filled.png` | Truck sub-step 1/3 — full truck registration form filled (reg. GJ01AB1234, chassis/engine numbers, Gujarat home state, national permit) |
| `driver/22-signup-step5-substep2-docs-empty.png` | Truck sub-step 2/3 — 5 truck documents form, empty |
| `driver/22-signup-step5-substep2-docs-resumed.png` | Truck documents step resumed after re-login — shows RC/Insurance/PUC already-on-file with Continue/Replace, only Fitness Cert + Permit still needed (demonstrates per-document resumability) |
| `driver/23-signup-step5-substep2-docs-filled.png` | All 5 truck documents filled — RC, Insurance, PUC, Fitness Certificate, Permit (with National Permit checked) |
| `driver/25-signup-step5-substep3-photos-empty.png` | Truck sub-step 3/3 — 4 truck photo uploads, empty |
| `driver/26-signup-step5-substep3-photos-filled.png` | All 4 truck photos attached (front/back/left/right) |
| `driver/27-signup-step6-review.png` | Step 6 of 6 — final review/submit screen |
| `driver/28-dashboard-pre-approval-mobile.png` | Dashboard, pre-approval state, mobile — shows truck card with all 4 photos |
| `driver/28b-dashboard-pre-approval-desktop.png` | Dashboard, pre-approval state, desktop — flagship screen |

## Admin KYC approval

| File | Description |
|---|---|
| `admin/29-admin-kyc-queue-desktop.png` | KYC Queue — 8 pending items across both accounts (3 identity docs + 5 truck docs), each showing the real uploaded document image, masked ID (last 4 digits), and expiry |
| `admin/30-admin-document-review-inline.png` | Document review — this app reviews inline on the queue card (image + metadata + independent Approve/Reject per document), no separate detail page exists |
| `admin/29b-admin-kyc-queue-after-approvals.png` | KYC Queue after all 8 documents approved — "0 pending items" |
| `admin/31-admin-dashboard-desktop.png` | Admin operational dashboard after approvals — 0 pending KYC, Gujarat truck density = 1 |
| `admin/31b-admin-dashboard-mobile.png` | Admin dashboard, mobile |
| `admin/31c-admin-accounts.png` | Admin accounts list |

## Trip posting (Business Owner)

| File | Description |
|---|---|
| `trip/32b-post-trip-origin-autocomplete.png` | Step 1 of 5 — Google Places autocomplete dropdown on pickup address |
| `trip/32c-post-trip-destination-autocomplete.png` | Places autocomplete on delivery address |
| `trip/33-post-trip-step1-route-filled.png` | Step 1 — route filled (Ahmedabad → Bhavnagar, geocoded) |
| `trip/34-post-trip-step2-goods-empty.png` | Step 2 of 5 — goods details form, empty |
| `trip/35-post-trip-step2-goods-filled.png` | Step 2 filled — 3,200kg, General/FMCG cartons, Closed Container required |
| `trip/37-post-trip-step3-timeline-filled.png` | Step 3 of 5 — pickup window + expected delivery filled |
| `trip/39-post-trip-step4-receiver-deposit-filled.png` | Step 4 of 5 — receiver name/phone + 30% deposit filled |
| `trip/41-post-trip-confirmation.png` | Trip posted confirmation — real trip TRP00059 with live Google Maps route render |
| `trip/42-my-trips-list-mobile.png` | "My Trips" list, mobile |
| `trip/42b-my-trips-list-desktop.png` | "My Trips" list, desktop — flagship screen |

## Bidding (Driver)

| File | Description |
|---|---|
| `trip/43-driver-available-trips-mobile.png` | "Open For Bidding" list showing TRP00059 as eligible (passed body-type/capacity/home-state/document filters) |
| `trip/44-driver-trip-detail-mobile.png` | Trip detail from driver's side, mobile |
| `trip/44b-driver-trip-detail-desktop.png` | Trip detail + bid form combined screen, desktop — flagship screen, shows real Google Directions distance (163km, ~2h45m) |
| `trip/45-driver-trip-detail-bid-form-mobile.png` | Bid form, empty, mobile |
| `trip/46-driver-bid-form-filled.png` | Bid form filled — freight ₹21,000 / driver allowance ₹2,500 / estimated toll ₹950 |
| `trip/47-driver-bid-submitted-confirmation.png` | Bid submitted — PENDING status, ₹24,450 total breakdown |
| `trip/48-driver-trips-and-bids-list-mobile.png` | Driver's Trips & Bids list showing bid under "Your Bids" |

## Bid review & acceptance (Business Owner)

| File | Description |
|---|---|
| `trip/49-bo-bids-received-mobile.png` | Bids-received view, mobile |
| `trip/49b-bo-bids-received-desktop.png` | Bid detail with full trip milestone timeline, driver rating/badge, truck details, itemized bid — flagship screen |
| `trip/50-bo-accept-bid-confirm-dialog.png` | Accept-bid action in progress |
| `trip/51-bo-bid-accepted-confirmation.png` | Bid accepted — Trip Actions vertical timeline appears, deposit payment (₹7,335) now due, Acceptance Invoice generated |
| `trip/51b-bo-bid-accepted-confirmation-desktop.png` | Same state, desktop |

## Execution — deposit, pickup, transit, delivery (Driver + Business Owner)

| File | Description |
|---|---|
| `payments/52-bo-deposit-payment-proof-uploaded.png` | Deposit payment — Payment-Deposit-Receipt.jpeg attached as proof of transfer |
| `payments/53-bo-deposit-marked-paid-confirmation.png` | Shipper marked deposit paid — awaiting driver confirmation |
| `payments/54-driver-confirm-deposit-received-view.png` | Driver's view of the shipper's uploaded proof, before confirming receipt |
| `payments/55-driver-deposit-confirmed-en-route-ready.png` | Deposit confirmed by both sides — trip now `en_route_to_pickup`, pickup-photo upload step active |
| `trip/56-driver-en-route-confirm-pickup-form.png` | Confirm-pickup step, empty photo upload |
| `trip/57-driver-pickup-photos-selected.png` | All 4 Pickup-Photo-*.jpeg attached |
| `trip/58-driver-pickup-confirmed.png` | Pickup confirmed — trip `pickup_photos_pending_verification` |
| `trip/59-bo-verify-pickup-photos-view.png` | Shipper's pickup-photo verification step, showing the driver's uploaded photos |
| `trip/60-bo-verify-pickup-photos-dialog.png` | Verify-photos action in progress |
| `trip/61-bo-in-transit-live-tracking.png` | Trip `in_transit` — live tracking map with "Location signal unavailable — waiting for the tracker's first update" placeholder (no physical GPS hardware connected, exactly per spec's defined empty state) |
| `trip/61b-bo-in-transit-live-tracking-desktop.png` | Same state, desktop — flagship screen |
| `trip/62-driver-in-transit-delivery-signoff-form.png` | Driver's "Confirm arrival" step, in transit |
| `trip/63-driver-confirm-arrival-checkbox-checked.png` | "I have called the receiver at the number on file" checked |
| `trip/64-driver-arrived-signoff-form.png` | Arrived — delivery sign-off screen: "Is everything in order? Yes / No — damage or shortage" |
| `trip/65-driver-signoff-yes-photo-upload-form.png` | "Yes" selected, delivery-condition photo upload appears |
| `trip/66-driver-delivery-photos-selected.png` | All 4 Delivery-Photo-*.jpeg attached |
| `trip/67-driver-delivery-completed.png` | Delivery completed by driver — shows live final-amount breakdown preview and both pickup + drop-off photo galleries |
| `trip/68-bo-verify-delivery-photos-view.png` | Shipper's delivery-photo verification step |
| `trip/69-bo-delivery-verified-final-expenses-view.png` | Delivery verified — trip now `final_expenses_pending_submission` |

## Final toll, expenses & payment

| File | Description |
|---|---|
| `trip/70-driver-submit-final-toll-expenses-form.png` | Submit final toll & expenses form, empty — shows estimated toll (₹950) with adjustment note |
| `trip/71-driver-toll-filled-add-expense-clicked.png` | Actual toll ₹1,050 + Fastag-Toll-Receipt.jpeg entered, "Add an expense" row opened |
| `trip/72-driver-toll-and-misc-expense-filled.png` | Misc expense added — ₹300 police-checkpoint fee + Police-Checking-Receipt.jpeg |
| `trip/73-driver-final-expenses-submitted.png` | Submitted — trip `final_amount_pending_approval` |
| `trip/74-bo-approve-final-amount-view.png` | Shipper's final-amount approval screen — shows toll delta (+₹100) and the submitted misc expense with driver's note, folded into one approval |
| `trip/75-bo-final-amount-approved.png` | Approved — final payment (₹17,515) now due |
| `payments/76-bo-final-payment-proof-uploaded.png` | Final payment — Payment-Full-Receipt.jpeg attached as proof |
| `payments/77-bo-final-payment-marked-paid.png` | Shipper marked final payment paid |
| `payments/78-driver-confirm-final-payment-view.png` | Driver's view before confirming final payment receipt |

## Trip completion, invoices, ratings & close-out

| File | Description |
|---|---|
| `trip/79-driver-trip-completed.png` | Driver's final view — trip `completed` |
| `trip/80-bo-trip-completed.png` | Shipper's final view, mobile |
| `trip/80b-bo-trip-completed-desktop.png` | Full completed-trip page, desktop — flagship screen: all 14 milestones checked, both Acceptance + Completion invoices downloadable, full settlement breakdown, rating widget, both photo galleries, complete status history |
| `trip/81-bo-rating-widget-empty.png` | Rating widget before rating |
| `trip/81-bo-rating-widget-filled.png` | 5 stars selected + comment written for Akshay Makwana |
| `trip/82-bo-rating-submitted-confirmation.png` | Shipper's rating submitted |
| `trip/83-driver-rating-widget-view.png` | Driver's rating widget for the shipper |
| `trip/83b-driver-rating-widget-filled.png` | 5 stars + comment written for Bhavik Jadav |
| `trip/84-driver-rating-submitted-final-close-out.png` | Both ratings displayed reciprocally — trip fully closed out |

## Profile & account

| File | Description |
|---|---|
| `profile/85-bo-profile-account-page.png` | Business Owner profile/account page — Approved status, editable name/phone, identity documents with last-4-digit masking |
| `profile/86-driver-profile-account-truck-page.png` | Driver profile/account page — Approved status, both identity documents (DL + Aadhaar) shown |
| `profile/87-bo-notification-preferences-page.png` | Notification preferences — per-category email toggles (bidding activity, trip lifecycle, disputes, KYC decisions, account status) |
| `profile/88-bo-notification-bell-widget.png` | Notification bell widget — "9+" unread badge, dropdown panel opening |

---

## Notes on captures

- **Live tracking**: no physical GPS tracker hardware exists for this demo (per spec, tracker integration is a webhook contract only — device provisioning is out of scope), so the live-tracking map correctly shows its defined "Location signal unavailable" placeholder state rather than a live marker. This is the accurate, intended empty state, not a bug.
- **Desktop shots**: captured at 1440×900 for all flagship/key screens (landing page, both dashboards, trip detail, bid comparison, in-transit tracking, completed trip) per instruction, in addition to the mobile-first 430×932 captures used everywhere else.
- Every wizard in this app (KYC registration steps, truck sub-wizard, trip-posting wizard) keeps its in-progress step as **client-side-only state** that resets to step 1 on a hard reload — except the top-level KYC step, which is resumable via re-sign-in (the server remembers `profiles.kyc_status`/submitted documents and the sign-in flow redirects back into the wizard at the correct step). This shaped the automation approach: each wizard was driven in one continuous browser session per stage.
