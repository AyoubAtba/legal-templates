# Review Notes for Counsel — Chexbill Legal Documents

Prepared: October 20, 2026. These drafts were produced by adapting the General Legal templates in `templates/` to the facts recorded in `legal/company-facts.md`. Neither the founder nor the drafter is a lawyer. Every judgment call, every unresolved fact, and every place where a template's assumptions may not fit Chexbill is listed here.

**Documents delivered**

| File | Source template | Status |
|---|---|---|
| `output/terms-of-service.md` | `templates/terms-of-use/template.md` (+ fee, data, and warranty clauses adapted from `templates/master-services-agreement/template.md`) | Draft v1.0 |
| `output/privacy-policy.md` | `templates/privacy-policy-us/template.md` | Draft |
| `output/cookie-notice.md` | `templates/cookie-notice/template.md` | Draft |
| `output/data-processing-addendum.md` | `templates/dpa-us/template.md` | Draft |

**Documents deliberately not produced:** Privacy Policy (GDPR) and DPA (Global) — Chexbill serves U.S. users only and has no EEA/UK establishment. MSA and Order Form — sales are self-serve click-through only. BAA — no protected health information. NDAs, Advisor Agreement, Offer Letter — not requested.

---

## Part A — Changelog: what was adapted versus each template

### A.1 Terms of Service (from Terms of Use template)

**Structural changes**
- Retitled "Terms of Service" and the defined term changed from "Site" to "**Service**" (covering chexbill.com and app.chexbill.com) so that the Terms, Privacy Policy, Cookie Notice, and DPA share one concept. The template's "Site" language was replaced throughout.
- Sections renumbered. Template §1–§11 map to output §1, §2, §3, §7, §8, §9, §10, §11, §13, §15, §16. New sections inserted: §4 Your Data and Content, §5 Subscriptions and Fees, §6 Chexbill Payments, §12 Copyright Complaints, §14 Accessibility (moved out of General). The arbitration warning in the preamble, the survival clause (§11), and all internal cross-references were updated to the new numbers.
- Arbitration: **Option A (JAMS)** kept; **Option B (DecisionLayer)** deleted, including its drafting note.

**Filled from the fact sheet:** company name and entity type, domains, Newark DE address, emails (legal@ for notices and disputes, privacy@ for privacy and Nevada notice, support@ for general and accessibility), Delaware law, New Castle County venue, Delaware as the fallback court in §16.7, effective date, copyright line and trademarks.

**Clauses adapted (meaning changed from template)**
| Output | Template | Change and reason |
|---|---|---|
| §1.1 | §1.1 | Added third-party sign-in (Google, Microsoft, Apple); deletion via "account settings". |
| §1.2–1.3 | — (MSA §3.4 Authorized Users) | New: Organizations, Administrator, Authorized Users; responsibility for Authorized Users and "credentials cannot be shared" taken from the MSA. The sentence deeming "you" to include the business an Organization represents is **new language**. |
| §2.1 | §2.1 | License purpose changed from "personal, non-commercial purposes" to "**internal business purposes**" (B2B product). |
| §2.2 | §2.2 | Added restrictions (v)–(x): circumvention (from MSA §3.1(e)), sham invoices/fraud, sanctions/AML/export, malware, credential sharing, fee circumvention. (vi)–(x) are new language at the founder's request for a payments product. |
| §2.4 | §2.4 | Kept verbatim ("no support obligation"). |
| §2.7 | — | New one-line third-party/open-source software notice. |
| §3.3 | — | New pointer to the DPA. |
| §4.1–4.4 | MSA §4.2–4.3, §6.3 | Customer Data ownership, license to Company, customer responsibility for data and consents, the MSA Customer Warranty list (no infringement, defamation, unlawful content, malware; Company may monitor), Aggregated Data — adapted from the MSA with product-specific examples. Customer Data expressly excludes Chexbill Payments application data and usage data (handled under the Privacy Policy). The MSA's right to make Aggregated Data public was not carried (founder: analytics and improvement only). |
| §4.5 | MSA §6.2 (Outputs) | AI extraction disclaimer adapted from the MSA's Outputs disclaimer. |
| §4.6 | MSA §3.2 (last sentence) | "Not professional advice" expanded from the MSA's "shall not be construed as legal or other professional advice" into a full paragraph. **New language.** |
| §4.7 | — | Tax-form filing responsibilities and IRS acceptance notification. **New language.** |
| §4.8 | — | Retention/deletion rules (365-day lapse with 60-day notice, 90-day trial, export prompt, backups). **New language; contains a [TBD].** |
| §5 | MSA §5 (Fees, Taxes, Payment Terms, Suspension) | Trial, auto-renewal, payment via CardConnect, cancellation, no refunds (MSA §5.3 "non-refundable", no exceptions), 30-day price-change notice (MSA §5.1), 7-day grace then suspension of the Organization (MSA §5.4 was 30 days; interest dropped and "no interest" stated), taxes (MSA §5.2 duties to pay, reimburse, and notify of exemption changes carried over). Auto-renewal sentence in capitals added as a conspicuous disclosure. Trial, cancellation, and payment-method sentences are **new language**. |
| §6 | — (structure borrowed from MSA §2.3 Connected Accounts and §6.2 Connected Accounts disclaimer) | Entire Chexbill Payments section is **new language**: role as software provider/referral partner of the "Payment Processor" (named so as not to collide with the DPA's statutory term "Processor"), merchant agreement with CardConnect/Fiserv governs processing, onboarding data collected on Chexbill's own behalf and deleted after onboarding, fees per Pricing Schedule collected by the Payment Processor, equipment billed by Chexbill (non-refundable), merchant obligations, Payors (including that a Payor's use of a payment page is subject to the Terms to the extent applicable). Carries an [ATTORNEY REVIEW] marker. |
| §7.1 | §5.1 | "may display third-party advertisements" removed (no ads); examples added. |
| §7.2 | MSA §2.3 | Connected bank accounts via Plaid, with the MSA's representations (entitlement, good standing, acknowledgement) and no-liability language; Plaid End User Privacy Policy referenced. |
| §7.3–7.4 | §5.2–5.3 | Kept; "Payors" and the Organization's other Authorized Users added to the other-users language; "Payors" added to the release. |
| §8 | §4 | Indemnity extended to (iv) Customer Data and (v) Chexbill Payments transactions, chargebacks, and card-network compliance. **Broadens the customer's indemnity.** |
| §9 | §6 + MSA §6.2 | Added "report, calculation, data extraction, or tax form" accuracy disclaimer and the MSA's third-party-services disclaimer. |
| §10 | §7 | Cap raised from greater of $50 / 6 months to **greater of $100 / 12 months**; excluded damages list extended with "tax penalties or interest, chargebacks, fines, or processing losses". |
| §11 | §8 | At-will suspension kept; added a "reasonable efforts to notify and give an opportunity to cure" commitment for paid Organizations, except for fraud, abuse, non-payment, legal/security risk, or harm. **This narrows the company's at-will right for paying customers; founder's choice.** Added that the Payment Processor may suspend Chexbill Payments under the Merchant Agreement. Survival list follows the template's sweep ("Sections 3 through 16") and therefore includes §5 and §6 in full; counsel may wish to narrow it to §5.5, §5.8, §6.5, and §6.6. |
| §12 | — | Copyright-complaint clause. **New language; no DMCA agent registered.** |
| §13 | §9 | State notices kept (CA, CO, CT, VA, NV); California address replaced with Delaware address; "Other States" drafting note converted to an attorney flag. |
| §16 | §11 Option A | Kept verbatim except: addresses/emails filled, "California" replaced with "Delaware" in §16.2, §16.7, and §16.10. |

**Template clauses dropped**
- §11 Option B (DecisionLayer) in full.
- "may display third-party advertisements" (template §5.1).
- Template §9.6 "Other States" bracketed drafting note (replaced by attorney flag).

**Hierarchy added:** §3.1 now states that the DPA controls over the Privacy Policy for personal data processed on the customer's behalf (consistent with DPA §11(a)); §3.3 says the DPA "applies to" that processing. The template MSA's fallback warranty (customer warrants no regulated personal data if no DPA is signed) was not carried; see B.2.9.

### A.2 Privacy Policy (from Privacy Policy (U.S. only) template)

**Filled:** company name, business description, domains, dates, contact email and mailing address (no phone), PostHog as the analytics example, CardConnect as payment processor, identity-verification process, request channels, CCPA chart (six rows), "under 16" alternative, "do not process for targeted advertising / profiling / sell" alternatives, "process some Sensitive PI but not to infer characteristics" alternative.

**Data categories kept:** Contact, Profile, Communications, Transactional, Marketing, User-generated content and input data, Financial, Government-issued identification number, Payment, Other. **Added:** "Chexbill Payments application data" and "Payor data" (what Chexbill collects from people paying invoices). **Dropped:** Demographic, Relationship, Promotion (no contests), precise geolocation, "chat features" bracket, "salutation", and the metadata-tagging sentence.

**Sources kept:** social sign-in (bracketed optional, kept), Customers, Service providers, Business transaction partners. **Added:** Financial institutions and bank-connection services (Plaid). **Dropped:** Public sources (none used), Data providers, Partners. "Business partners" removed from the automatic-collection sentence (none exist).

**Tracking section:** template's "Chat and other AI technologies" paragraph split into a Zendesk support-widget disclosure (template structure, Zendesk named) and a Gemini paragraph; the optional "we contractually require… prohibit training" sentence was replaced by a factual statement about Google's paid API tier (flagged). The template sentence about storing cookie-preference records was dropped (no banner).

**Uses:** kept Service delivery (edited examples; "social features" bullet dropped), Personalization, Service improvement and analytics (Google Analytics example replaced by PostHog and Sentry), Direct marketing, Compliance and protection, Corporate events, Aggregated data (both bracketed options resolved: "will not attempt to reidentify" kept; AI-training sentence and opt-out dropped), Further uses. **Dropped:** Interest-based advertising, Events/promotions/contests.

**Sharing:** kept Service providers (examples edited), Payment processors (CardConnect, with onboarding-data sentence added), Third parties designated by you, Linked third-party services, Professional advisors, Authorities, Business transferees. **Added:** Bank-connection services (Plaid); "Other users of your organization" replaces the template's "Other users and the public" and keeps the template's "we are not responsible for any such use" sentence for invoice recipients. **Dropped:** Affiliates, Advertising partners, Partners.

**Choices:** kept access/update, opt-out of communications, cookies, blocking images, DNT (URL recovered), declining, linked platforms, delete content/close account (filled). **Added:** Connected financial accounts. **Dropped:** Training data opt-out, Mobile location, Privacy settings.

**Retention:** template's bracketed section kept and extended with Chexbill's concrete periods (new language, two flags).

**State notice:** "Exercising your right to opt-out" paragraph rewritten because the template's fixed sentence ("like many companies, we use services that help deliver interest-based ads") is false for Chexbill; GPC sentence kept. Phone and webform channels removed; email and account settings kept. Shine the Light and Nevada paragraphs kept; Texas paragraph dropped (no sale of sensitive data).

**Added paragraphs with no template source:** "Personal information we process on behalf of our customers" (processor-role clarification, links to the DPA) and the "Connected financial accounts" choice.

**Template defects corrected:** removed the stray "GDPR compliant" header row; removed the "previous version" and "printable copy" lines; fixed the broken list numbering and stray headings; fixed the "Opt-out of marketing section" cross-reference to "Opt-out of communications".

### A.3 Cookie Notice (from Cookie Notice template)

**Filled:** company, sites, date, email, four cookie rows with providers and privacy-policy links.
**Dropped:** Advertising row and all advertising-related text (NAI/DAA/AppChoices opt-outs, mobile advertising ID, "if you opt out of targeted advertisements" paragraphs); mobile app language and SDK paragraph; Flash LSO paragraph (obsolete technology); session-replay paragraph (not used); the optional cookie-banner/dashboard block (no banner); the duplicated allaboutcookies sentence.
**Added:** "We do not use advertising cookies on our Sites" sentence; GPC bullet in Your choices (new, mirrors the Privacy Policy); vendor privacy-policy URLs and concrete control instructions in the table (template cells were "[ADD]"); Brevo named as the source of marketing-email web beacons (the template's Analytics-row sentence about email beacons was removed so beacons are not attributed to PostHog). The Essential and Functionality row descriptions were lightly expanded with examples.
**Recovered URL:** allaboutcookies.org (from the .docx).

### A.4 Data Processing Addendum (from DPA (U.S.) template)

**Structural:** section and sub-section numbering restored (1–11, (a)–(e)) to match the template's own cross-references ("Section 4(a)", "Sections 9(b)–(d)", "Section 6(b)", "Section 7", "Section 8", "Section 11(d)" is now 11(d)); Annex headings restored; security measures numbered.
**Filled:** Provider details, Agreement = Chexbill Terms of Service, Subprocessor Site URL, Annex 1 (provider activities, data subjects, data categories, sensitive data), Annex 4 subprocessor list (twelve vendors).
**Changed:** §6(b) Restricted Data warranty now carves out "**Permitted Sensitive Data**" (the customer's and its vendors' TINs and information-return data, bank account/routing numbers for recording or making payments, connected-account transaction data), limited to the features designed to receive them. **This loosens the template's blanket prohibition; without it the warranty would be breached by ordinary use of the product.** The Personal Data definition now states that Chexbill Payments application data and usage data are processed by Chexbill on its own behalf and are outside the DPA. "Customer Data" is tied to the Terms' definition. "Order form" references removed (self-serve). §9(b) defines the Cessation Date as the date the Organization is deleted (so the DPA's 30-day return window follows the Terms' 365-day/60-day-notice schedule) and points to the export feature; §9(c) adds a backup sentence with a [TBD]. Annex 1 "Categories of sensitive data" changed from "None" to Permitted Sensitive Data; "additional safeguards" points to Annex 3; a "Commercial and financial details" category was added; authentication-detail examples trimmed to what the product uses. Annex 4 lists CardConnect for payments the customer accepts (subscription-fee processing is Chexbill's own activity).
**Kept as drafted:** everything else, including 15-day subprocessor objection, annual audit right, 30-day post-cessation window, AI-training prohibition (§10), liability cap import (§11(d)), signature block.

---

## Part B — Open items for the attorney

### B.1 Unresolved facts marked [TBD] in the documents
1. **Backup retention window** after deletion (Terms §4.8; Privacy Policy "Retention"; DPA §9(c)). Engineering must state how long Supabase backups retain deleted data.
2. **Subprocessor entity names and locations** (DPA Annex 4). Drafted from public information; confirm each from the vendor's current terms. Brevo is French-headquartered.
3. **URLs supplied by the drafter, not the templates:** vendor privacy-policy URLs in the Cookie Notice table; the Fiserv privacy notice cited for CardConnect in the Privacy Policy (CardConnect also publishes its own policy; cite whichever governs merchant and cardholder data); the Plaid End User Privacy Policy; and the internal paths `https://chexbill.com/privacy`, `/cookies`, `/dpa`, and `/subprocessors`, which must exist at launch. The allaboutdnt.com, globalprivacycontrol.org, and allaboutcookies.org links come from the template .docx files.

### B.2 Judgment calls marked [ATTORNEY REVIEW] or otherwise worth a look
1. **Chexbill Payments section (Terms §6).** No template covers a referral-partner/ISV arrangement. Confirm: (a) Chexbill's characterization as "software provider and referral partner" of the Processor matches the ISR/sub-rep agreement; (b) whether the CardConnect/Fiserv program requires any specific disclosures or pass-through terms in Chexbill's own Terms (the Fiserv Program Guide v. GenCP-KB-2907_PG_07.01.26 and MPA v. GenCP-KB-2910_MPA_08.28.26 were provided by the founder); (c) whether the 3-year Fiserv initial term, early-termination fee, and personal guarantee should be flagged to merchants in Chexbill's onboarding flow; (d) PCI DSS scope given use of the hosted tokenizer and in-person terminals; (e) equipment sale/rental terms (§6.4) are stated in one sentence and may warrant their own order terms.
2. **Sensitive data.** Chexbill collects SSN/EIN, date of birth, and bank account numbers for merchant onboarding and vendors' TINs for 1099 filing. The Privacy Policy discloses this and selects the "we process some Sensitive PI but not to infer characteristics" alternative; the DPA §6(b) warranty was carved out (Permitted Sensitive Data). Confirm both, and whether any state law requires a "limit use of sensitive PI" right to be offered notwithstanding the exemption relied on.
3. **KYC data deletion.** Founder states onboarding data is deleted after submission to the processor and never reaches support tickets, error monitoring, or logs. Privacy Policy "Retention" relies on this. Recommend an engineering verification (including Supabase backups and Sentry breadcrumbs) before publication.
4. **Record retention vs. automatic deletion.** Organizations are deleted 365 days after a lapsed subscription (90 days for unconverted trials). IRS guidance generally expects filers to keep copies of information returns for about four years. Decide what Chexbill (versus TaxBandits or the customer) must retain, and whether Terms §4.8 and the Privacy Policy need a carve-out for tax and payment records (a generic "as required by law" sentence is included).
5. **Termination for paid customers (Terms §11).** The template is at-will; at the founder's request a "reasonable efforts to notify and give an opportunity to cure" sentence was added for paid Organizations with carve-outs. Confirm the carve-outs are broad enough.
6. **Liability cap (Terms §10)** raised to the greater of $100 or 12 months' fees, and the exclusions list extended (tax penalties, chargebacks, fines, processing losses). Confirm enforceability of excluding tax penalties where they result from a Service error.
7. **Indemnity (Terms §8)** extended to Customer Data and payments activity. Confirm.
8. **"Not professional advice" and tax-filing clauses (Terms §4.6–4.7).** New language; confirm whether Chexbill's 1099 e-filing role creates any obligations as a transmitter or filer that the Terms should address, and whether "we will inform you whether the tax authority has accepted or rejected the filing" creates an undesired service commitment.
9. **DPA execution model.** Template is countersigned; for a self-serve product, consider incorporating the DPA by reference in the Terms (Terms §3.3 already says it "applies") with a countersigned copy on request. If the DPA is not made automatic, consider carrying the MSA's fallback warranty (customer warrants that no regulated personal data is submitted absent a DPA) into Terms §3.3. Note also the template's own tension: the DPA's Personal Data definition excludes "Customer's business contacts who are Customer personnel" while Annex 1 lists Customer personnel as data subjects; left as in the template.
10. **DPA precedence.** DPA §11(a) says the DPA governs on conflict; Terms §3.1 says the Privacy Policy governs on personal-data conflicts between the Terms and the Privacy Policy. These concern different documents, but confirm the hierarchy is as intended.
11. **Copyright complaints (Terms §12).** No template clause existed; one paragraph was added. Registering a designated agent with the U.S. Copyright Office is needed for DMCA safe-harbor protection.
12. **Arbitration.** JAMS (Option A) selected; DecisionLayer (Option B) removed. The template's batch-arbitration clause, 45/60-day informal process, and $250,000 Streamlined/Comprehensive split are kept verbatim. Confirm enforceability of the class waiver and opt-out mechanics under Delaware law and against business customers.
13. **State consumer notices (Terms §13).** Kept CA (incl. Civil Code §1789.3 notice with the Delaware address), CO, CT, VA, NV. The template's own note says additional states may be needed; the customer base is business users, so some notices may be unnecessary. Prune or extend.
14. **Google Gemini.** Privacy Policy states Google does not train on inputs under the paid API tier. Confirm against Google's current API terms at publication.
15. **Plaid.** Terms §7.2 and the Privacy Policy reference the Plaid End User Privacy Policy, which Plaid requires of apps using its services; confirm the current URL and that Plaid's developer policy does not require additional language.
16. **Payor terms.** Payors (customers' clients paying invoices) are addressed in Terms §6.6 and §7.3; the payment page will carry a short notice linking the Terms and Privacy Policy. Confirm whether Payors need a distinct short-form notice.
17. **Accessibility commitment (Terms §14)** kept at "endeavor to conform to WCAG 2.1 AA". Confirm appetite.
18. **General Legal attribution footnote** kept on each document per the template authors' request (CC0 permits removal).
19. **New operative language with no template source**, for a closer read: Terms §1.2 (deeming the business bound), §4.5–4.8, §5.1–5.4, §6 in full, §12; Privacy Policy processor-role paragraph, Payor-data category, Zendesk and Gemini disclosures, retention bullets, "Connected financial accounts" choice; Cookie Notice "no advertising cookies" statement and GPC item; DPA Permitted Sensitive Data definition, Personal Data carve-out for application and usage data, Cessation Date sentence, backup sentence. Every one of these was checked against the templates in two independent review passes and is listed here so counsel can prioritize.
20. **Representations of fact the product must keep true:** no advertising cookies; Gemini paid tier with no training; KYC data deleted after onboarding and never in support tickets, error reports, or logs; marketing-only email beacons; logs kept 365 days; GPC honored.

### B.3 Template versus jurisdiction mismatches
- The Terms of Use template defaults to **California** law, venue, and notice addresses, and includes California-specific consumer notices (Civil Code §1789.3; §1542 release). Governing law and addresses were changed to **Delaware**; the California notices were kept because they apply by residence of the user, not by the company's location. Confirm.
- The Privacy Policy template is U.S.-only and lists CCPA/CPRA, Virginia, Colorado, Connecticut, Texas, Nevada. Texas sensitive-data "sale" paragraph dropped. No GDPR content (none needed).
- The DPA template is U.S.-only (State Privacy Laws Annex). Appropriate for U.S.-only customers; if an EEA/UK customer ever signs up, the Global DPA template and GDPR privacy notice would be needed.
- The MSA clauses borrowed for fees and data rights were drafted for an on-premise enterprise product with Delaware law; only the clause language was reused, not its deployment assumptions.

### B.4 Template defects noticed (for the template authors or for awareness)
See `legal/phase1-inventory.md` §5. Items that affected these drafts: lost section numbering in the DPA (restored); the privacy template's fixed "we use services that help deliver interest-based ads" sentence (rewritten); the "Opt-out of marketing section" cross-reference (fixed); dropped hyperlinks (recovered from the .docx originals); obsolete Flash cookie paragraph (dropped).

---

## Part C — Deployment checklist

**Where to link each document**
- Terms of Service: footer of chexbill.com and app.chexbill.com; sign-up form; Organization creation; checkout/subscription page; invoice payment page (short notice: "By paying, you agree to Chexbill's Terms of Service and acknowledge the Privacy Policy"); Chexbill Payments application start page. Publish at `https://chexbill.com/terms` (the drafts assume `/privacy`, `/cookies`, `/dpa`, `/subprocessors` on chexbill.com; change the URLs in all four documents if different).
- Privacy Policy: footer of both sites; sign-up form; Chexbill Payments application form (notice at collection — the policy's "California Notice at Collection" line relies on this link being presented where data is collected); invoice payment page; account settings.
- Cookie Notice: footer of both sites; linked from the Privacy Policy and Terms.
- DPA: `https://chexbill.com/dpa`, linked from Terms §3.3 and from account settings; offer a countersigned PDF on request (or incorporate by reference per B.2.9). Maintain the subprocessor list at `https://chexbill.com/subprocessors` and email customers 15 days before adding a subprocessor (DPA §7(d)).

**Acceptance mechanics**
- Sign-up: unchecked checkbox or "By creating an account you agree to the Terms of Service and acknowledge the Privacy Policy" with both hyperlinked; record timestamp, user ID, Terms version, and IP address.
- Organization creation and plan purchase: re-present the Terms (version) and the auto-renewal statement (Terms §5.2) in plain sight before the "Subscribe" button, with price, period, and renewal date; email a confirmation containing the same.
- Material changes: email notice to all account holders (Terms §15.1; Privacy Policy "Changes"); for fee changes, email at least 30 days before the renewal (§5.6).
- Arbitration opt-out: route emails to legal@chexbill.com and log opt-outs by account; 30-day window runs from first acceptance (§16.10).
- Payment page for Payors: short notice with links; no checkbox required by the templates, but consider one.

**Versioning**
- Keep the "Version" and "Last updated" lines; archive each published version with its effective date (the template's "previous version" link was removed for v1.0 and can be reinstated from v1.1).
- Store accepted-version records per user and per Organization.
- Re-run this review when any of the following changes: a vendor is added or replaced (DPA Annex 4, Privacy Policy sharing list, Cookie Notice table); an ad pixel or session-replay tool is added (Cookie Notice and Privacy Policy "sale/share" statements must change); EU/UK customers are accepted (switch to GDPR privacy policy and Global DPA); a mobile app launches; sales tax collection begins; pricing or trial terms change.

**Operational commitments the documents make (make sure they are true in the product)**
- 60-day email notice before auto-deleting a lapsed Organization; 90-day deletion of unconverted trials.
- Export prompt before Organization deletion.
- 7-day grace period on failed payments before suspension.
- 30-day price-change notice before renewal.
- KYC data deleted after submission to the processor.
- GPC signals honored; DNT not honored.
- Privacy requests answered via privacy@chexbill.com and account settings, verified by account email.
- Incident notification to customers "without undue delay" (DPA §4(c)).
- 15-day subprocessor-change notice; annual audit right; SOC 2 report acceptance clause (no report exists today).
- Notification of IRS acceptance or rejection of filed 1099s.
