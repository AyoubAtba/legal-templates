# Company Fact Sheet

Running record of every answer given during the legal-document interview. Read this at the start of every session. Anything not yet answered is marked `[TBD — needs attorney/founder decision]` or left blank.

Legend: `[CONFIRMED]` answered by founder · `[DEFAULT ACCEPTED]` founder said "yes" to a suggested default · `[TBD — needs attorney/founder decision]` unknown

Last updated: 2026-10-20 (Batches 1–3 recorded)

---

## 0. Document selection

| Question | Answer | Status |
|---|---|---|
| Which templates are in scope for drafting? | | |
| Is a B2B Master Services Agreement / Order Form needed (signed enterprise contracts)? | No (self-serve only) | [CONFIRMED] |
| Is a Data Processing Addendum needed (do business customers upload their end users' personal data)? | Yes: customers enter their clients' data (invoices) and vendors' data incl. TINs (1099 filing). Use DPA (US), with the Restricted Data warranty modified | [CONFIRMED] |
| Is a Business Associate Agreement needed (any protected health information)? | No | [CONFIRMED] |
| Are NDAs, Advisor Agreement, or Offer Letter wanted as part of this project? | | |

## 1. Company identity & jurisdiction

| Fact | Answer | Status |
|---|---|---|
| Full legal entity name | Chexbill LLC | [CONFIRMED] |
| Entity type and state/country of formation (e.g. Delaware C-corp) | Delaware limited liability company (LLC). Note: Mutual NDA template says "a Delaware corporation"; must read "a Delaware limited liability company". | [CONFIRMED] |
| Short/brand name used in documents ("CompanyName") | Chexbill | [CONFIRMED] |
| Registered/mailing address (used for notices, California §1789.3 notice, arbitration opt-out) | 257 Chapman Rd #208, Newark, DE 19702 (New Castle County) | [CONFIRMED] |
| Product domain(s) / website URL(s) the documents cover | chexbill.com (marketing website) and app.chexbill.com (the SaaS application) | [CONFIRMED] |
| Any mobile app covered? | No | [CONFIRMED] |
| General contact email | support@chexbill.com | [CONFIRMED] |
| Privacy / data-requests contact email | privacy@chexbill.com | [CONFIRMED] |
| Disputes / legal notices email | legal@chexbill.com | [CONFIRMED] |
| Accessibility contact email or phone | support@chexbill.com | [DEFAULT ACCEPTED] |
| Phone number (privacy policy lists one; optional) | None provided; phone contact lines will be omitted (email + web form remain) | [DEFAULT ACCEPTED] |
| Where the company is headquartered / where data is processed | United States (Delaware address); hosting region TBD in batch 4 | [CONFIRMED] |
| Subsidiaries or affiliates to cover? | None; affiliates language will be dropped | [DEFAULT ACCEPTED] |
| Where are users located? (US only / US + EU/UK / global) | US only → use Privacy Policy (US) and DPA (US); no GDPR notice, no EU/UK representatives, no SCCs | [CONFIRMED] |
| Any establishment (office, staff, entity) in the EU or UK? | None | [CONFIRMED] |
| Any users in Switzerland? | No (US only) | [CONFIRMED] |
| Governing law (state) | Delaware (state of incorporation) | [CONFIRMED] |
| Venue (county, state) for non-arbitrable claims | New Castle County, Delaware (county of the registered address; founder to confirm) | [DEFAULT ACCEPTED] |
| Any planned business in healthcare (HIPAA) or with children (COPPA)? | No health data (no BAA). No users under 18 (keep 18+ gate; use "under 16: no actual knowledge" alternative in state notice) | [CONFIRMED] |

## 2. Product & pricing model

| Fact | Answer | Status |
|---|---|---|
| One-sentence description of the business/product (used verbatim in Privacy Policy) | Cloud-based accounting and point-of-sale solution for businesses (comparable to QuickBooks): issue invoices and estimates, track bills, capture expenses, generate reports, bank-feed reconciliation, and online/in-person payment acceptance ("Chexbill Payments") | [CONFIRMED] |
| Audience: consumers (B2C), businesses (B2B), or both | B2B (businesses, incl. sole proprietors). Non-account "payors" (the customer's clients) also interact via invoice payment links | [CONFIRMED] |
| Self-serve signup vs. sales-led contracts | Self-serve click-through only → no MSA/Order Form; fee terms go into the Terms of Service | [CONFIRMED] |
| Free tier / free trial? Length and terms | 14-day free trial | [CONFIRMED] |
| Paid plans: subscription (monthly/annual), usage-based, one-time? | Monthly and yearly subscriptions, auto-renewing. Payment-processing fees for Chexbill Payments: TBD (batch 6) | [CONFIRMED] |
| Is use "personal, non-commercial" (ToS template default) or commercial/business use? | Internal business use (B2B) → ToS license must be rewritten from "personal, non-commercial" | [CONFIRMED] |
| Any AI / generative features? Which model providers? | Yes: Google Gemini API used to extract data from uploaded receipts and bills. Whether the paid/no-training API tier is used: TBD | [CONFIRMED] |
| Any user-to-user features (sharing, messaging, public profiles)? | No social features. Shareable invoice payment links let a customer's client pay online (payor is not an account holder) | [CONFIRMED] |
| Any third-party integrations / connected accounts (OAuth to other services)? | (1) Plaid bank feed: user connects bank; transactions pulled for reconciliation. (2) CardConnect / Fiserv powers "Chexbill Payments": merchant onboarding data collected and sent to CardConnect for underwriting and KYC; online and in-person (POS) card acceptance | [CONFIRMED] |
| Any mobile app or SDKs? | No mobile app for now | [CONFIRMED] |
| Do you provide support? Any SLA/uptime commitment? | No support commitment, no SLA (keep template "no support obligation") | [CONFIRMED] |

## 3. User accounts & acceptable use

| Fact | Answer | Status |
|---|---|---|
| Minimum age (template default: 18) | 18+ (business users) | [CONFIRMED] |
| Account creation: email/password, social login (which providers), SSO? | Email/password plus Google, Microsoft, and Apple sign-in. No SSO | [CONFIRMED] |
| Can users delete their own account in-app? How? | Two account types. (1) User account: deletable from user settings; on deletion the user chooses to delete the organizations they own or transfer them to other users. (2) Organization (tenant, the paid unit): only the admin/creator can delete; deletion passes a financial check first, the admin is warned, and can request a data export (emailed as an attachment). Organizations whose subscription has been cancelled and not renewed for 365 days are deleted automatically | [CONFIRMED] |
| Multiple users per account / team or organization accounts? | Each user is independent; a user creates an Organization (tenant) that is paid for; the creator is admin by default and can invite other users to join | [CONFIRMED] |
| Specific prohibited uses beyond template defaults (scraping, resale, competing product)? | Template restrictions plus payments-specific prohibitions: no unlawful or card-network-prohibited / high-risk activity, no fraudulent or sham invoices, no use of payment links for transactions that are not bona fide sales by the merchant, no sharing of credentials, no circumventing fees, no malware or interference, no sanctions/AML violations. Founder asked for hints if defaults miss something | [DEFAULT ACCEPTED] |
| Suspension/termination policy: at will, or with notice/cure? | At-will during trial; for paying customers, notice and opportunity to cure for breach, immediate for fraud, abuse, non-payment, or legal risk. Chexbill Payments access is also subject to the Fiserv/CardConnect merchant agreement and card-network rules | [DEFAULT ACCEPTED] |

## 4. Data collected, processors & retention

| Fact | Answer | Status |
|---|---|---|
| Categories of personal data collected (from template list: contact, profile, communications, transactional, marketing, user content, payment, device, online activity, location, etc.) | | |
| Any sensitive data (government ID, health, biometric, precise geolocation, financial account numbers)? | Yes: SSN/EIN, date of birth, and bank account numbers collected from merchants onboarding to Chexbill Payments and stored by Chexbill; vendors' TINs for 1099 filing; customers' bank transactions via Plaid. No card numbers ever touch Chexbill servers (Fiserv/CardConnect hosted tokenizer). No health, biometric, or precise geolocation data | [CONFIRMED] |
| Data collected from third-party sources (social login, data providers, partners)? | | |
| Hosting provider and region | | |
| Full subprocessor / service-provider list (name, location, purpose) | | |
| Email delivery provider | | |
| Customer support / chat provider | | |
| AI / LLM providers and whether they may train on user data | Google Gemini API, paid tier (receipt/bill extraction). Paid-tier terms do not use prompts to improve Google's models; attorney to confirm current Google terms at publication | [CONFIRMED] |
| Do you train your own models on user data (even aggregated/de-identified)? Opt-out mechanism? | | |
| Retention period(s) for account data, logs, backups, after account closure | | |
| Deletion process on account closure | | |
| Do you share data with advertising partners / "sell" or "share" under CCPA? | | |
| Any profiling or automated decision-making with significant effects? | | |
| Identity verification process for privacy requests | | |
| Privacy request intake: webform URL, email, toll-free number? | | |
| Honor Global Privacy Control (GPC) signals? (CCPA requires it) | | |
| Respond to Do Not Track? (template default: no) | | |
| Security certifications (SOC 2, ISO 27001)? | | |
| Data Protection Officer appointed? | | |
| EU representative / UK representative appointed (Art. 27 GDPR)? | | |
| Cross-border transfer mechanism (SCCs, UK Addendum, DPF certification)? | | |
| Previous privacy policy version link to keep? | | |
| Printable/PDF copy of the privacy policy offered? | | |

## 5. Cookies & analytics

| Fact | Answer | Status |
|---|---|---|
| Analytics tools (e.g. Google Analytics, Plausible, PostHog, Mixpanel) | | |
| Advertising / retargeting pixels (Meta, Google Ads, LinkedIn)? | | |
| Session replay tools (FullStory, Hotjar, LogRocket, PostHog replay)? | | |
| Social login / share widgets | | |
| Essential cookies (auth/session, CSRF, load balancing) | | |
| Functionality/preference cookies | | |
| Email open/click tracking pixels? | | |
| Cookie banner / consent-management platform in use? Preference dashboard URL? | | |
| Any browser local storage use beyond cookies? | | |
| Mobile SDKs (if app exists) | | |

## 6. Payments, refunds & cancellation

| Fact | Answer | Status |
|---|---|---|
| Payment processor(s) (e.g. Stripe, Paddle, PayPal) and whether any card data touches your servers | Chexbill Payments is powered by CardConnect / Fiserv (First Data Merchant Services LLC, KeyBank as member bank). Merchants sign Fiserv's Merchant Processing Application and Agreement + Program Guide directly (3-year initial term, early-termination fee, personal guarantee). Chexbill's role: ISV / referral partner (sub-rep under an ISR); sets pricing per its Schedule A and charges its own processing markup plus other fees (annual fee, PCI fees, CardPointe platform fee, terminal rentals, ACH monthly fee, etc.). Card data never touches Chexbill servers (hosted tokenizer). Processor for Chexbill's own subscription fees: TBD (batch 6) | [CONFIRMED] |
| Billing cycle and auto-renewal | | |
| Refund policy (none / pro-rata / X-day money-back) | | |
| Cancellation mechanics and effect (end of period vs immediate) | | |
| Price-change notice period | | |
| Late payment / failed payment handling (suspension, interest) | | |
| Taxes: exclusive of tax? Who collects VAT/sales tax? | | |
| Currency | | |
| Invoiced / enterprise terms (Net days, ACH/wire) if B2B | | |

## 7. IP, user content & licensing

| Fact | Answer | Status |
|---|---|---|
| Who owns user-uploaded content / inputs? (template default: customer owns, grants company a license to operate) | | |
| Who owns AI outputs (if any)? | | |
| License users grant you over their content (scope: operate/improve service; aggregated data) | | |
| Aggregated / de-identified data rights retained by company? | | |
| Feedback license (template: perpetual, irrevocable, royalty-free) | | |
| Trademarks / logos to list | | |
| Copyright notice year and holder | | |
| DMCA / copyright-infringement notice process and agent (not in template; decision) | | |
| Open-source or third-party components to disclose? | | |

## 8. Liability, disputes & governing law

| Fact | Answer | Status |
|---|---|---|
| Arbitration: JAMS (Option A) or DecisionLayer AI arbitration (Option B) or none? | | |
| Arbitration opt-out notice address/email (template: 30 days) | | |
| Informal dispute notice address | | |
| Liability cap: template default = greater of $50 USD or fees paid in prior 6 months (ToS); 12 months fees (MSA) | | |
| Warranty disclaimer period where law requires warranties (template: 90 days) | | |
| Class-action waiver and jury-trial waiver (template: yes) | | |
| Batch arbitration clause (template: 100+ demands) | | |
| Governing law and venue (see §1) | | |
| Indemnification by users (template: yes, broad) | | |
| Insurance / other coverage facts the attorney should know | | |

## 9. Open items for the attorney

(Running list of every `[TBD]` and every judgment call; mirrored in output/REVIEW-NOTES.md at handoff.)

- Chexbill Payments (CardConnect/Fiserv): merchant onboarding collects KYC data (likely SSN/EIN, DOB, government ID, bank account). This is sensitive personal information under state privacy laws and conflicts with the DPA template's Restricted Data warranty. Attorney to confirm (a) Chexbill's role (referral partner / ISO / payment facilitator), (b) whether CardConnect's sub-merchant agreement must be incorporated into or linked from the Terms, (c) PCI DSS scope given the integration method.
- 1099 filing: vendors' taxpayer identification numbers are stored → "Government-issued identification number data" category must stay in the privacy policy and the DPA Restricted Data list must carve it out.
- Plaid: bank credentials are entered with Plaid, not Chexbill; Plaid's End User Privacy Policy must be referenced in the privacy policy (Plaid requires this disclosure).
- Google Gemini API: confirm API tier/terms so the privacy policy can truthfully say whether the provider may use uploaded receipts for training.
- Invoice payors (customers' clients) are not account holders; privacy policy and Terms must cover them.
- Chexbill Payments fee schedule (Schedule A with CardConnect, provided by founder as screenshots) lists Chexbill's own fees to merchants (annual fee $25, PCI annual $25, PCI non-compliance $10/mo, CardPointe platform $15/mo, Fiserv ACH $10/mo, terminal rentals, bps markups, per-item auth fees). The Terms should state that Chexbill Payments fees are disclosed in the merchant's pricing schedule/application and may change on notice. Attorney to confirm whether Chexbill may bill these itself or only via the processor statement, and whether the 3-year Fiserv term / early-termination fee must be flagged in Chexbill's own Terms.
- Reference documents provided by founder (not committed to the repo): Fiserv "Merchant Processing Application and Agreement" (GenCP-KB-2910_MPA_08.28.26) and "Program Terms and Conditions (Program Guide)" (GenCP-KB-2907_PG_07.01.26); Schedule A screenshots.
- Automatic deletion of organizations 365 days after a lapsed subscription must be disclosed in the Terms and reconciled with record-retention duties (tax, payments, 1099).

