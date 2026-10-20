# Company Fact Sheet

Running record of every answer given during the legal-document interview. Read this at the start of every session. Anything not yet answered is marked `[TBD — needs attorney/founder decision]` or left blank.

Legend: `[CONFIRMED]` answered by founder · `[DEFAULT ACCEPTED]` founder said "yes" to a suggested default · `[TBD — needs attorney/founder decision]` unknown

Last updated: 2026-10-20 (Batches 1–7 recorded)

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
| Free tier / free trial? Length and terms | 14-day free trial; no card required; user picks a plan at trial end. Trial-only organizations that never subscribe are deleted after 90 days (paid organizations: 365 days after lapse) | [CONFIRMED] |
| Paid plans: subscription (monthly/annual), usage-based, one-time? | Monthly and yearly subscriptions, auto-renewing. Payment-processing fees for Chexbill Payments: TBD (batch 6) | [CONFIRMED] |
| Is use "personal, non-commercial" (ToS template default) or commercial/business use? | Internal business use (B2B) → ToS license must be rewritten from "personal, non-commercial" | [CONFIRMED] |
| Any AI / generative features? Which model providers? | Yes: Google Gemini API used to extract data from uploaded receipts and bills. Whether the paid/no-training API tier is used: TBD | [CONFIRMED] |
| Any user-to-user features (sharing, messaging, public profiles)? | No social features. Shareable invoice payment links let a customer's client pay online (payor is not an account holder). Payors deal with the merchant; Chexbill is not a party to the sale and does not handle refunds or disputes over the goods. Payment page shows a short notice linking the Terms and Privacy Policy | [CONFIRMED] |
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
| Categories of personal data collected (from template list: contact, profile, communications, transactional, marketing, user content, payment, device, online activity, location, etc.) | Contact; Profile (account, organization); Communications (support via Zendesk); Transactional (subscriptions, invoices, payments); Marketing preferences; User content and input data (invoices, estimates, bills, expenses, uploaded receipt/bill images, reports); Financial data (bank transactions via Plaid; bank account numbers and KYC for merchant onboarding); Government-issued ID numbers (SSN/EIN/TIN for merchant onboarding and 1099 filing); Payment data (handled by CardConnect/Fiserv tokenizer, not stored by Chexbill); Device and Online activity data (PostHog, Sentry, logs). Also personal data of customers' clients and vendors entered by customers, and of invoice payors. Dropped: Demographic, Relationship, Promotion, precise geolocation | [CONFIRMED] |
| Any sensitive data (government ID, health, biometric, precise geolocation, financial account numbers)? | Yes: SSN/EIN, date of birth, and bank account numbers collected from merchants onboarding to Chexbill Payments and stored by Chexbill; vendors' TINs for 1099 filing; customers' bank transactions via Plaid. No card numbers ever touch Chexbill servers (Fiserv/CardConnect hosted tokenizer). No health, biometric, or precise geolocation data | [CONFIRMED] |
| Data collected from third-party sources (social login, data providers, partners)? | Social login profile data (Google, Microsoft, Apple via Clerk); bank account and transaction data from Plaid (with user authorization); currency rates from currencyapi.com (no personal data). No data brokers or marketing partners | [CONFIRMED] |
| Hosting provider and region | Vercel (web app hosting); Supabase (database and bucket storage), US region | [CONFIRMED] |
| Full subprocessor / service-provider list (name, location, purpose) | Vercel (hosting, US); Supabase (database/storage, US region); Upstash (queueing and Redis cache); Clerk (authentication); Brevo (email delivery); Zendesk (customer support); Sentry (error monitoring); PostHog (product analytics); Google Gemini API, paid tier (receipt/bill data extraction); Plaid (bank connections/transactions); CardConnect / Fiserv (payment processing and merchant underwriting/KYC); TaxBandits (1099 filing); currencyapi.com (exchange rates, no personal data). Entity countries/locations to be confirmed for the DPA Annex (all US-headquartered vendors; Brevo is France-headquartered with US operations) | [CONFIRMED] |
| Email delivery provider | Brevo | [CONFIRMED] |
| Customer support / chat provider | Zendesk | [CONFIRMED] |
| AI / LLM providers and whether they may train on user data | Google Gemini API, paid tier (receipt/bill extraction). Paid-tier terms do not use prompts to improve Google's models; attorney to confirm current Google terms at publication | [CONFIRMED] |
| Do you train your own models on user data (even aggregated/de-identified)? Opt-out mechanism? | May use aggregated/de-identified data to improve the Service; no training on identifiable data; no opt-out needed (privacy policy "Training data" opt-out paragraph dropped) | [CONFIRMED] |
| Retention period(s) for account data, logs, backups, after account closure | (a) Active account/organization data: for as long as the account or organization is active. (b) Organization deletion: on explicit deletion the admin is prompted to export; organizations with no active subscription for 365 days are deleted automatically, with notice 2 months before. (c) Server logs: 365 days. (d) Merchant onboarding (KYC) data (SSN/EIN, DOB, bank account): collected solely to transmit to CardConnect/Fiserv and deleted from Chexbill systems after onboarding; never placed in Zendesk tickets, Sentry reports, or logs. (e) 1099 records: same as organization policy (attorney to confirm against IRS record-keeping requirements). Backup retention window: TBD | [CONFIRMED] |
| Deletion process on account closure | See §3 (user vs organization deletion; export offered; financial check before organization deletion) | [CONFIRMED] |
| Do you share data with advertising partners / "sell" or "share" under CCPA? | No sale, no sharing for targeted advertising, no data brokers, no affiliates. State notice uses the "we do not sell / do not process for targeted advertising" alternatives; interest-based advertising sections dropped (subject to batch 5 answers on pixels) | [CONFIRMED] |
| Any profiling or automated decision-making with significant effects? | None by Chexbill (merchant underwriting decisions are made by CardConnect/Fiserv, not Chexbill) | [DEFAULT ACCEPTED] |
| Identity verification process for privacy requests | Match the request to the email address on the account; request additional information where needed | [DEFAULT ACCEPTED] |
| Privacy request intake: webform URL, email, toll-free number? | privacy@chexbill.com and in-app account settings; no toll-free number | [DEFAULT ACCEPTED] |
| Honor Global Privacy Control (GPC) signals? (CCPA requires it) | Yes | [CONFIRMED] |
| Respond to Do Not Track? (template default: no) | No (template default) | [DEFAULT ACCEPTED] |
| Security certifications (SOC 2, ISO 27001)? | None at this time. All DPA Annex security measures (encryption in transit/at rest, MFA, role-based access, logging, vulnerability management, backups/DR) confirmed true | [DEFAULT ACCEPTED] |
| Data Protection Officer appointed? | No (not required; US only) | [CONFIRMED] |
| EU representative / UK representative appointed (Art. 27 GDPR)? | Not applicable (US only) | [CONFIRMED] |
| Cross-border transfer mechanism (SCCs, UK Addendum, DPF certification)? | Not applicable (US only; data processed in the US) | [CONFIRMED] |
| Previous privacy policy version link to keep? | No (first publication); line dropped | [DEFAULT ACCEPTED] |
| Printable/PDF copy of the privacy policy offered? | No; line dropped | [DEFAULT ACCEPTED] |

## 5. Cookies & analytics

| Fact | Answer | Status |
|---|---|---|
| Analytics tools (e.g. Google Analytics, Plausible, PostHog, Mixpanel) | PostHog only (app and marketing site). No Google Analytics / Tag Manager | [DEFAULT ACCEPTED] |
| Advertising / retargeting pixels (Meta, Google Ads, LinkedIn)? | None → Advertising cookie row and interest-based advertising sections dropped | [DEFAULT ACCEPTED] |
| Session replay tools (FullStory, Hotjar, LogRocket, PostHog replay)? | None (PostHog session recording off) → session-replay paragraph dropped | [DEFAULT ACCEPTED] |
| Social login / share widgets | Social login via Clerk (Google, Microsoft, Apple); no share widgets. Cookie table "Social" row limited to login | [DEFAULT ACCEPTED] |
| Essential cookies (auth/session, CSRF, load balancing) | Clerk session cookies; Vercel/Supabase infrastructure cookies | [DEFAULT ACCEPTED] |
| Functionality/preference cookies | Zendesk help/chat widget (embedded); app preferences | [DEFAULT ACCEPTED] |
| Email open/click tracking pixels? | Yes, via Brevo, marketing emails only (not transactional invoices/receipts) | [DEFAULT ACCEPTED] |
| Cookie banner / consent-management platform in use? Preference dashboard URL? | No banner; Cookie Notice linked in the footer; GPC honored → optional "Cookie Preference Dashboard" block dropped | [DEFAULT ACCEPTED] |
| Any browser local storage use beyond cookies? | Yes (web app local storage) → keep browser web storage paragraph | [DEFAULT ACCEPTED] |
| Mobile SDKs (if app exists) | Not applicable (no app) → SDK paragraph dropped | [CONFIRMED] |

## 6. Payments, refunds & cancellation

| Fact | Answer | Status |
|---|---|---|
| Payment processor(s) (e.g. Stripe, Paddle, PayPal) and whether any card data touches your servers | Chexbill's own subscription fees are charged through Chexbill's CardConnect/Fiserv account (hosted tokenizer; Chexbill stores only a payment token, never the card number). Chexbill Payments is powered by CardConnect / Fiserv (First Data Merchant Services LLC, KeyBank as member bank). Merchants sign Fiserv's Merchant Processing Application and Agreement + Program Guide directly (3-year initial term, early-termination fee, personal guarantee). Chexbill's role: ISV / referral partner (sub-rep under an ISR); sets pricing per its Schedule A and charges its own processing markup plus other fees (annual fee, PCI fees, CardPointe platform fee, terminal rentals, ACH monthly fee, etc.). Card data never touches Chexbill servers (hosted tokenizer). Processor for Chexbill's own subscription fees: TBD (batch 6) | [CONFIRMED] |
| Billing cycle and auto-renewal | Monthly or yearly, charged in advance at the start of each period; renews automatically for the same period until cancelled | [DEFAULT ACCEPTED] |
| Refund policy (none / pro-rata / X-day money-back) | All fees non-refundable; no pro-rata refunds on yearly plans; no exceptions | [DEFAULT ACCEPTED] |
| Cancellation mechanics and effect (end of period vs immediate) | Cancel in-app at any time; stops future charges; organization stays active until the end of the paid period, then becomes a lapsed subscription (365-day deletion clock, 2 months' notice) | [DEFAULT ACCEPTED] |
| Price-change notice period | At least 30 days' notice by email; takes effect at the next renewal | [DEFAULT ACCEPTED] |
| Late payment / failed payment handling (suspension, interest) | Retry the charge; 7-day grace period; then the organization is suspended and treated as a lapsed subscription. No interest charges | [CONFIRMED] |
| Taxes: exclusive of tax? Who collects VAT/sales tax? | Prices exclusive of sales tax; Chexbill will collect tax where required. Not collecting US sales tax today; may begin once economic-nexus thresholds are reached in customers' states | [CONFIRMED] |
| Currency | USD | [DEFAULT ACCEPTED] |
| Invoiced / enterprise terms (Net days, ACH/wire) if B2B | Not applicable (self-serve card billing only) | [CONFIRMED] |
| Chexbill Payments fee mechanics (merchant-facing) | (1) Rates and fees are those in the merchant's pricing schedule and merchant application; may change on notice. (2) Processing and recurring fees appear on the Fiserv merchant statement and are deducted from the merchant's bank account by the processor; Chexbill does not bill them separately. Exception: payment terminals/equipment are sold or rented by Chexbill and billed separately by Chexbill, either paid up front or monthly for a set period. (3) Chargebacks, reserves, funding holds, underwriting, and account closure are governed by the merchant's CardConnect/Fiserv agreement; Chexbill does not control those decisions. (4) Merchant must be approved by and contract with CardConnect/Fiserv and its sponsor bank; Chexbill is a referral partner and software provider, not a processor or bank | [CONFIRMED] |

## 7. IP, user content & licensing

| Fact | Answer | Status |
|---|---|---|
| Who owns user-uploaded content / inputs? (template default: customer owns, grants company a license to operate) | Customer owns all its business data (invoices, bills, expenses, receipts, contacts, reports). Chexbill gets a limited license to host, process, display, transmit, and back it up to provide the Service, and to create aggregated, de-identified data | [DEFAULT ACCEPTED] |
| Who owns AI outputs (if any)? | Customer owns data extracted from receipts/bills by the AI feature; Chexbill disclaims accuracy and requires the customer to review before relying on it (incl. for tax purposes) | [DEFAULT ACCEPTED] |
| License users grant you over their content (scope: operate/improve service; aggregated data) | Operate, maintain, secure, and improve the Service; aggregated/de-identified data for analytics and product improvement. Reports and 1099 filings are prepared from the customer's own data; Chexbill is software, not an accountant or tax advisor; customer is responsible for accuracy and deadlines. Chexbill will inform the customer whether a 1099 filing was accepted or rejected by the IRS (via TaxBandits) | [CONFIRMED] |
| Aggregated / de-identified data rights retained by company? | Yes | [DEFAULT ACCEPTED] |
| Feedback license (template: perpetual, irrevocable, royalty-free) | Keep template clause | [DEFAULT ACCEPTED] |
| Trademarks / logos to list | "Chexbill" and "Chexbill Payments" claimed as trademarks (not registered) | [DEFAULT ACCEPTED] |
| Copyright notice year and holder | © 2026 Chexbill LLC | [DEFAULT ACCEPTED] |
| DMCA / copyright-infringement notice process and agent (not in template; decision) | One-paragraph clause: report claimed infringement to legal@chexbill.com. No DMCA agent registration (attorney to advise on safe-harbor registration) | [DEFAULT ACCEPTED] |
| Open-source or third-party components to disclose? | Generic line that the Service includes third-party and open-source software under its own licenses; no list | [DEFAULT ACCEPTED] |

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
- Automatic deletion of organizations 365 days after a lapsed subscription (with 2 months' notice) must be disclosed in the Terms and reconciled with record-retention duties (tax, payments, 1099). IRS guidance generally requires filers to keep copies of information returns for at least 4 years; attorney to confirm what Chexbill (vs. TaxBandits or the customer) must retain.
- Merchant KYC data: founder confirmed it is deleted from Chexbill after onboarding and does not land in support tickets, error reports, or logs. Engineering should verify that Supabase backups and Sentry breadcrumbs honor this before publication.
- Backup retention window after deletion (Supabase point-in-time backups) is undefined; needed for the retention section and DPA §9.

