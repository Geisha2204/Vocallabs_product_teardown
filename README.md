# Vocallabs.ai — Product Teardown

**Submitted by:** Geisha Polishetty
**Deadline:** 31 May 2026
**Tested on:** Web (Chrome) + Android app

---

## About Vocallabs

Vocallabs.ai builds AI voice agents that automate business calls — for sales, support, and bookings — with human-like fluency. India-first, with support for local languages and workflows.

---

## 5 Feedbacks

### F1 — Broken email verification on signup `UX`

**Observed:**
Signed up on app.vocallabs.ai. The email verification redirect throws an error — the confirmation link loops back to an error page and the account stays unverified.

**Problem:**
A user's very first interaction with the product is an error. In a category where businesses are trusting you to make calls on their behalf, a broken signup damages credibility before the product has a chance to prove itself.

**Ship instead:**
Fix the redirect URL in the email verification handler. Add signup funnel monitoring so this gets caught in analytics, not by a user complaint.

**Priority:** Critical (P0)
**Screenshot:** [f1-email-verification-error.png](<img width="1916" height="929" alt="Screenshot 2026-05-30 185145" src="https://github.com/user-attachments/assets/572ec6fd-7e8c-4680-9e36-c7b7594b66bd" />)

---

### F2 — Blank pricing page and broken demo `GTM & ICP`

**Observed:**
Every CTA routes to "Book a Demo." The pricing page (vocallabs.ai/pricing-policy) loads blank — no tier names, no rates. The demo link (app.vocalassist.ai) shows "Inbound numbers are not available right now, please try again after some time."

**Problem:**
Target customers — small business owners and growth teams — want to evaluate tools quickly without talking to a salesperson first. Buyers who are ready to decide can't find the information they need, so they leave before the sales team gets a chance to speak to them.

**Ship instead:**
Fix the demo environment or replace it with a pre-recorded walkthrough until it's stable. Publish three-tier pricing with INR amounts alongside it so buyers have both pieces of information they need to make a decision.

**Priority:** High
**Screenshots:** [f2-blank-pricing-page.png](screenshots/f2-blank-pricing-page.p<img width="1598" height="942" alt="Screenshot 2026-05-30 194315" src="https://github.com/user-attachments/assets/26dedb80-9f44-4cde-88f9-daae1bc10c59" />) | [f2-broken-demo.png](<img width="1789" height="837" alt="Screenshot 2026-05-30 193806" src="https://github.com/user-attachments/assets/52960241-906e-4b17-a07c-f3edee1356e1" />
)

---

### F3 — n8n node exists on GitHub but zero developer onboarding on the website `Features`

**Observed:**
Vocallabs has published an official n8n community node on GitHub (github.com/Vocallabsai), an SDK (vocal-sdk), and a Chrome extension — all signals of a developer/automation-builder audience. But the website has no documentation link, no quick-start guide, and no workflow templates. A developer landing on the site has no path from "I want to automate calls with n8n" to "I'm live."

**Problem:**
The builder/automation segment — n8n users, indie devs, no-code operators — has high activation intent but zero patience for opaque onboarding. By shipping the n8n node without a visible integration story, Vocallabs is leaving warm inbound intent on the table.

**Ship instead:**
Create a "Build with Vocallabs" section with a 3-step n8n quick-start (connect → configure agent → trigger call) and 2–3 workflow templates for common India use cases — COD verification, lead qualification, appointment reminder. Pin these to the n8n community template library where 200K+ users discover workflows organically.

**Priority:** High
**Evidence:** [github.com/Vocallabsai](https://github.com/Vocallabsai)

---

### F4 — No public TRAI/DND/DPDP compliance documentation `Competitor Analysis`

**Observed:**
Nowhere on the website does Vocallabs mention TRAI DLT registration, DND compliance, or DPDP data handling for businesses running outbound campaigns through the platform.

**Problem:**
When a business in India makes automated outbound calls, they legally need to follow TRAI rules — registering on the DLT portal, checking the DND list before calling, and getting proper consent before storing customer data (DPDP). Enterprise buyers in BFSI, edtech, and healthcare will ask their legal team "is this compliant?" — and without documentation, the answer is no. Deals stall or die silently, even if the product is technically compliant in the backend.

**Ship instead:**
Publish a compliance FAQ or one-pager addressing TRAI DLT, DND, and DPDP handling. It's a one-time content investment that unblocks an entire category of enterprise buyers.

**Priority:** Medium-High

---

### F5 — No native integrations with India's dominant SMB CRMs `Potential Collaborations`

**Observed:**
The website has no integrations page. The blog mentions Salesforce and HubSpot but says nothing about Zoho or Leadsquared — the CRMs most Indian businesses actually use.

**Problem:**
After an AI call, businesses need that data to automatically flow into their CRM — who picked up, who was interested, who needs a follow up. If there's no ready-made connection, the business has to build it themselves. Most small businesses in India can't do that, so they just won't buy the product.

**Ship instead:**
Build native one-click integrations with Zoho and Leadsquared first — that's where most Indian SMB customers are. Both have partner programs, so getting listed there means Indian businesses discover Vocallabs while already looking for tools that work with their CRM. Use the existing n8n node as a connector for everything else in the meantime.

**Priority:** Medium-High

---

## Priority Summary

| # | Pillar | Feedback | Priority | Impact |
|---|--------|----------|----------|--------|
| F1 | UX | Broken email verification — signup blocked | Critical (P0) | Acquisition |
| F2 | GTM & ICP | Blank pricing + broken demo | High | Conversion |
| F3 | Features | n8n node with no developer onboarding | High | Activation |
| F4 | Competitor | No TRAI/DPDP compliance documentation | Medium-High | Enterprise Sales |
| F5 | Collaborations | No native India CRM integrations | Medium-High | Retention/Sales |

---

## Supporting Files

- 📄 [Full report (Word doc)]([Vocallabs_Product_Teardown_GeishaP.docx](https://github.com/user-attachments/files/28423670/Vocallabs_Product_Teardown_GeishaP.docx)
)
- 📸 Screenshots in [/screenshots](screenshots/)

---

*Assignment for Vocallabs.ai Product Intern role — 2026*
