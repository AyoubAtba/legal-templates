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

A.1–A.4 describe the first draft against the templates; A.5–A.7 describe later revisions. Section numbers in A.1–A.4 and Parts B and C follow the current documents; clauses removed in A.7 are marked as removed. A.5 and A.6 use the numbers of the drafts at the time.

### A.1 Terms of Service (from Terms of Use template)

**Structural changes**
- Retitled "Terms of Service" and the defined term changed from "Site" to "**Service**" (covering chexbill.com and app.chexbill.com) so that the Terms, Privacy Policy, Cookie Notice, and DPA share one concept. The template's "Site" language was replaced throughout.
- Sections renumbered. Template §1–§11 map to output §1, §2, §4, §10.3, §8, §10.1, §10.2, §9.1, removed (state notices), §12 (template §10.8 Contact Information is now §13), §11. New sections: §3 Subscriptions and Fees, §5 Your Data, §6 AI Features, Reports, and Tax Filing, §7 Chexbill Payments. Copyright Complaints and a separate Accessibility section were added in the first draft and removed in A.7. The arbitration warning in the introduction, the survival clause (§9.1), and all internal cross-references were updated to the new numbers.
- Arbitration: **Option A (JAMS)** kept; **Option B (DecisionLayer)** deleted, including its drafting note.

**Filled from the fact sheet:** company name and entity type, domains, Newark DE address, emails (legal@ for notices and disputes, privacy@ for privacy and Nevada notice, support@ for general and accessibility), Delaware law, New Castle County venue, Delaware as the fallback court in §11.4, effective date, copyright line and trademarks.

**Clauses adapted (meaning changed from template)**
| Output | Template | Change and reason |
|---|---|---|
| §1.1 | §1.1 | Added third-party sign-in (Google, Microsoft, Apple); deletion via "account settings". |
| §1.2–1.3 | — (MSA §3.4 Authorized Users) | New: Organizations, Administrator, Authorized Users; responsibility for Authorized Users and "credentials cannot be shared" taken from the MSA. The sentence deeming "you" to include the business an Organization represents is **new language**. |
| §2.1 | §2.1 | License purpose changed from "personal, non-commercial purposes" to "**internal business purposes**" (B2B product). |
| §2.2 | §2.2 | Added restrictions (v)–(x): circumvention (from MSA §3.1(e)), sham invoices/fraud, sanctions/AML/export, malware, credential sharing, fee circumvention. (vi)–(x) are new language at the founder's request for a payments product. |
| removed (A.7) | §2.4 | Kept verbatim ("no support obligation"). |
| removed (A.7) | — | New one-line third-party/open-source software notice. |
| §3 | MSA §5 (Fees, Taxes, Payment Terms, Suspension) | Trial, auto-renewal, payment via CardConnect, cancellation, no refunds (MSA §5.3 "non-refundable", no exceptions), 30-day price-change notice (MSA §5.1), 7-day grace then suspension of the Organization (MSA §5.4 was 30 days; interest dropped and "no interest" stated), taxes (MSA §5.2 duties to pay, reimburse, and notify of exemption changes carried over). Auto-renewal sentence in capitals added as a conspicuous disclosure. Trial, cancellation, and payment-method sentences are **new language**. |
| §4 | — | New pointer to the DPA. |
| §5.1–5.4 | MSA §4.2–4.3, §6.3 | Customer Data ownership, license to Company, customer responsibility for data and consents, the MSA Customer Warranty list (no infringement, defamation, unlawful content, malware; Company may monitor), Aggregated Data — adapted from the MSA with product-specific examples. Customer Data expressly excludes Chexbill Payments application data and usage data (handled under the Privacy Policy). The MSA's right to make Aggregated Data public was not carried (founder: analytics and improvement only). |
| §6.1 | MSA §6.2 (Outputs) | AI extraction disclaimer adapted from the MSA's Outputs disclaimer. |
| §6.2 | MSA §3.2 (last sentence) | "Not professional advice" expanded from the MSA's "shall not be construed as legal or other professional advice" into a full paragraph. **New language.** |
| §6.3 | — | Tax-form filing responsibilities and IRS acceptance notification. **New language.** |
| §7 | — (structure borrowed from MSA §2.3 Connected Accounts and §6.2 Connected Accounts disclaimer) | Entire Chexbill Payments section is **new language**: role as software provider/referral partner of the "Payment Processor" (named so as not to collide with the DPA's statutory term "Processor"), merchant agreement with CardConnect/Fiserv governs processing, onboarding data collected on Chexbill's own behalf and deleted after onboarding, fees per Pricing Schedule collected by the Payment Processor, equipment billed by Chexbill (non-refundable), merchant obligations, Payors (including that a Payor's use of a payment page is subject to the Terms to the extent applicable). Carries an [ATTORNEY REVIEW] marker. |
| §8.1 | §5.1 | "may display third-party advertisements" removed (no ads); examples added. |
| §8.2 | MSA §2.3 | Connected bank accounts via Plaid, with the MSA's representations (entitlement, good standing, acknowledgement) and no-liability language; Plaid End User Privacy Policy referenced. |
| §8.3 | §5.2–5.3 | Kept; "Payors" and the Organization's other Authorized Users added to the other-users language. The release (template §5.3) was removed in A.7. |
| removed (A.7) | — | Copyright-complaint clause. **New language; no DMCA agent registered.** |
| §9.1 | §8 | At-will suspension kept; added a "reasonable efforts to notify and give an opportunity to cure" commitment for paid Organizations, except for fraud, abuse, non-payment, legal/security risk, or harm. **This narrows the company's at-will right for paying customers; founder's choice.** Added that the Payment Processor may suspend Chexbill Payments under the Merchant Agreement. Survival list follows the template's sweep (now "Sections 3 through 13") and therefore includes §3 and §7 in full; counsel may wish to narrow it to §3.4, §3.7, §7.5, and §7.6. |
| §9.2 | — | Retention/deletion rules (365-day lapse with 60-day notice, 90-day trial, export prompt, backups). **New language; contains a [TBD].** |
| §10.1 | §6 + MSA §6.2 | Added "report, calculation, data extraction, or tax form" accuracy disclaimer and the MSA's third-party-services disclaimer. |
| §10.2 | §7 | Cap raised from greater of $50 / 6 months to **greater of $100 / 12 months**; excluded damages list extended with "tax penalties or interest, chargebacks, fines, or processing losses". |
| §10.3 | §4 | Indemnity extended to (iii) Customer Data and (iv) Chexbill Payments transactions, chargebacks, and card-network compliance. **Broadens the customer's indemnity.** |
| §11 | §11 Option A | Kept verbatim except: addresses/emails filled, "California" replaced with "Delaware" in §11.2, §11.4, and §11.6. Condensed in A.7. |
| removed (A.7) | §9 | State notices kept (CA, CO, CT, VA, NV); California address replaced with Delaware address; "Other States" drafting note converted to an attorney flag. |

**Template clauses dropped**
- §11 Option B (DecisionLayer) in full.
- "may display third-party advertisements" (template §5.1).
- Template §9.6 "Other States" bracketed drafting note (replaced by attorney flag).

**Hierarchy added:** §4 states that the DPA controls over the Privacy Policy for personal data processed on the customer's behalf (consistent with DPA §11(a)) and that the DPA applies to that processing. The template MSA's fallback warranty (customer warrants no regulated personal data if no DPA is signed) was not carried; see B.2.9.

### A.2 Privacy Policy (from Privacy Policy (U.S. only) template)

**Filled:** company name, business description, domains, dates, contact email and mailing address (no phone), PostHog as the analytics example, CardConnect as payment processor, identity-verification process, request channels, CCPA chart (six rows), "under 16" alternative, "do not process for targeted advertising / profiling / sell" alternatives, "process some Sensitive PI but not to infer characteristics" alternative.

**Data categories kept:** Contact, Profile, Communications, Transactional, Marketing, User-generated content and input data, Financial, Government-issued identification number, Payment, Other. **Added:** "Chexbill Payments application data" and "Payor data" (what Chexbill collects from people paying invoices). **Dropped:** Demographic, Relationship, Promotion (no contests), precise geolocation, "chat features" bracket, "salutation", and the metadata-tagging sentence.

**Sources kept:** social sign-in (bracketed optional, kept), Customers, Service providers, Business transaction partners. **Added:** Financial institutions and bank-connection services (Plaid). **Dropped:** Public sources (none used), Data providers, Partners. "Business partners" removed from the automatic-collection sentence (none exist).

**Tracking section:** template's "Chat and other AI technologies" paragraph split into a Zendesk support-widget disclosure (template structure, Zendesk named) and a Gemini paragraph; the optional "we contractually require… prohibit training" sentence was replaced by a factual statement about Google's paid API tier (flagged). The template sentence about storing cookie-preference records was dropped (no banner).

**Uses:** kept Service delivery (edited examples; "social features" bullet dropped), Personalization, Service improvement and analytics (Google Analytics example replaced by PostHog and Sentry), Direct marketing, Compliance and protection, Corporate events, Aggregated data (both bracketed options resolved: "will not attempt to reidentify" kept; AI-training sentence and opt-out dropped), Further uses. **Dropped:** Interest-based advertising, Events/promotions/contests.

**Sharing:** kept Service providers (examples edited), Payment processors (CardConnect, with onboarding-data sentence added), Third parties designated by you, Linked third-party services, Professional advisors, Authorities, Business transferees. **Added:** Bank-connection services (Plaid); "Other users of your organization" replaces the template's "Other users and the public" and keeps the template's "we are not responsible for any such use" sentence for invoice recipients. **Dropped:** Affiliates, Advertising partners, Partners.

**Choices:** kept access/update, opt-out of communications, cookies, blocking images, DNT (URL recovered), declining, linked platforms, delete content/close account (filled). **Added:** Connected financial accounts. **Dropped:** Training data opt-out, Mobile location, Privacy settings.

**Retention:** template's bracketed section kept and extended with Chexbill's concrete periods (new language, two flags).

**State notice:** "Exercising your right to opt-out" paragraph rewritten because the template's fixed sentence ("like many companies, we use services that help deliver interest-based ads") is false for Chexbill; GPC sentence kept. Phone and webform channels removed; email and account settings kept. Shine the Light and Nevada paragraphs kept; Texas paragraph dropped (no sale of sensitive data). (The notice was later shortened; see A.6.)

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
**Changed:** §6(b) Restricted Data warranty now carves out "**Permitted Sensitive Data**" (the customer's and its vendors' TINs and information-return data, bank account/routing numbers for recording or making payments, connected-account transaction data), limited to the features designed to receive them. **This loosens the template's blanket prohibition; without it the warranty would be breached by ordinary use of the product.** The Personal Data definition now states that Chexbill Payments application data and usage data are processed by Chexbill on its own behalf and are outside the DPA. "Customer Data" is tied to the Terms' definition. "Order form" references removed (self-serve). §9(a) defines the Cessation Date as the date the Organization is deleted (so the DPA's 30-day return window follows the Terms' 365-day/60-day-notice schedule) and points to the export feature; §9(c) adds a backup sentence with a [TBD]. Annex 1 "Categories of sensitive data" changed from "None" to Permitted Sensitive Data; "additional safeguards" points to Annex 3; a "Commercial and financial details" category was added; authentication-detail examples trimmed to what the product uses. Annex 4 lists CardConnect for payments the customer accepts (subscription-fee processing is Chexbill's own activity).
**Kept as drafted:** everything else, including 15-day subprocessor objection, annual audit right, 30-day post-cessation window, AI-training prohibition (§10), liability cap import (now §11(b)), signature block (removed in A.7).

### A.5 Structure aligned with Xero (US) and FreshBooks

On October 20, 2026 the four public documents were reorganized to follow the structure of the Xero US Terms of Use and Privacy Notice (https://www.xero.com/us/legal/) and the FreshBooks Terms of Service and Privacy Policy (https://www.freshbooks.com/policies). **No operative wording was changed**, except that the Privacy Policy's "Children" section was later removed (see below): clauses were moved, renumbered, and given headings, and every cross-reference was updated. A paragraph-by-paragraph comparison against the previous draft confirmed that all other existing text is still present.

**All four documents.** Same header pattern as both peers: title, "Last updated" date, and a one-line note on what changed (for v1.0, "This is the first version"). Numbered sections with short headings. A closing "How to contact us" section (Cookie Notice: formerly "Questions"), followed by a list of related policies with their chexbill.com URLs (Terms and Privacy Policy; Cookie Notice links the Privacy Policy and Terms). The DPA received the header change only.

**Terms of Service.** Order follows Xero's groups (joining and using, pricing, data and privacy, third-party products, termination, liability and indemnity, disputes, housekeeping) and FreshBooks' separate AI Features section and closing contact section:

| New § | Previous § | Change |
|---|---|---|
| Introduction | Preamble | Now headed "Introduction"; one-line description under the title; summary-convention sentence added; arbitration warning now cites §12 |
| 1, 2 | 1, 2 | Unchanged |
| 3 Subscriptions and Fees | 5 | Moved up (Xero: pricing follows joining and using) |
| 4 Privacy | 3 | Subsections 3.1–3.3 → 4.1–4.3 |
| 5 Your Data and Content | 4.1–4.4 | |
| 6 AI Features, Reports, and Tax Filing | 4.5–4.7 | New section heading (FreshBooks §13 "AI Features"; Xero §65 "No professional advice") |
| 7 Chexbill Payments | 6 | |
| 8 Third-Party Services and Connected Accounts | 7 | |
| 9 Copyright Complaints | 12 | |
| 10 Term, Termination, and Data Retention | 11 (→ 10.1) and 4.8 (→ 10.2) | Retention grouped with termination, as in Xero's "Retention of your data" (§60) and FreshBooks' "Inactive Accounts" (§24). Survival sentence unchanged ("Sections 2.2 through 2.7 and Sections 3 through 16") and still covers every section except §1 and §2.1 |
| 11 Disclaimers, Liability, and Indemnity | 9 (→ 11.1), 10 (→ 11.2), 8 (→ 11.3) | Grouped as in Xero's "Liability and indemnity" and FreshBooks §18–19 |
| 12 Dispute Resolution | 16 | Moved ahead of the state notices and general terms, as in both peers |
| 13, 14, 15 | 13, 14, 15.1–15.6 | Unchanged |
| 16 How to Contact Us | 15.7 | FreshBooks §26 "Questions and Comments" |

Each Terms section now opens with a one- or two-sentence plain-language summary in italics, following Xero ("summary paragraphs at the top of each section"). The Introduction states that the summaries are for convenience only and do not limit or change the full text. See B.2.21.

**Privacy Policy.** Order follows Xero's Privacy Notice: 1 Who we are and what this policy covers (the former opening paragraph), 2 Personal information we process on behalf of our customers (the former bold-labelled paragraph, Xero's "What this notice doesn't cover"), 3 Personal information we collect, 4 How we use, 5 Tracking & other technologies, 6 How we share, 7 Retention, 8 Security, 9 International data transfer, 10 Your choices, 11 Other sites and services, 12 Changes, 13 How to contact us, 14 State privacy rights notice (regional section last, as in Xero §14). The template's "Children" section was removed at the founder's request because neither Xero's nor FreshBooks' privacy policy has one; the 18+ requirement remains in the Terms Introduction and the "Consumers under 16" statement remains in the state privacy rights notice (see B.2.22). A numbered contents list follows the notice at collection. Every "above"/"below" reference was checked against the new order.

**Cookie Notice.** Sections numbered 1–6; "Questions" renamed "How to contact us".

**DPA.** Header line only; the body already used numbered sections and annexes.

### A.6 State privacy rights notice shortened to the FreshBooks model

At the founder's request, Privacy Policy §14 was cut from about 1,800 words (the template's full multi-state notice) to about 300, following the FreshBooks Privacy Policy (§11 rights list, §13 "Information for California Residents", §14 deletion, portability, non-discrimination), which names only California, refers back to its collection section instead of a category table, and does not cover Shine the Light, authorized agents, or appeals.

**Kept, in short form:** CCPA scope sentence, with one sentence extending the same handling to residents of other states with comprehensive privacy laws (needed because Terms §13.2–13.4 send Colorado, Connecticut, and Virginia residents to the Privacy Policy); rights to know and access, delete, correct, and portability; categories disclosed by reference to §3, §4, and §6; no sale or sharing; the under-16 statement; GPC (relied on by Cookie Notice §4); the sensitive-information "no inferring characteristics" statement; non-discrimination; request channels (privacy@chexbill.com, account settings); verification by account email; "may decline as permitted by law".

**Dropped:** the "State Privacy Laws" and "Sensitive Personal Information" definitions; the separate-notice sentence for job applicants; the six-item "Information" list; the appeal right; the profiling/automated decision-making opt-out statement; the authorized-agent paragraph; "Information practices" (sources and purposes, retention, deidentification); the six-row CCPA category table; Shine the Light; the Nevada paragraph (Terms §13.5 still gives the Nevada right and contact); the closing "Contact Us" paragraph (§13 covers it). See B.2.23.

### A.7 Simplification pass (all four documents)

At the founder's request, all four documents were cut to the essentials and rewritten in plain language, following the length and tone of the Xero and FreshBooks policies: about 18,000 words down to about 8,750 (Terms 6,937 → 3,934; Privacy Policy 4,172 → 1,856; Cookie Notice 1,158 → 606; DPA 5,736 → 2,357). **Unlike A.5, this pass changes wording throughout**, so every document should be read in full rather than compared clause by clause. Every [ATTORNEY REVIEW] and [TBD] marker was kept. Points that change meaning, not just length:

**Terms of Service** (now §1–§13; old → new: 1.4 → 1.3; 2.5–2.6 → 2.4; 3.4–3.5 → 3.4; 3.6–3.8 → 3.5–3.7; 4.1–4.3 → 4; 10 → 9; 11 → 10; 12 → 11; 15 → 12; 16 → 13)
- Removed: "no support obligation" (old §2.4); third-party/open-source software notice (§2.7); the release of claims with the California Civil Code §1542 waiver (§8.4); copyright complaints (§9); all state-specific notices, including the California §1789.3 notice and the Colorado, Connecticut, Virginia, and Nevada pointers (§13); the accessibility statement (§14); the export clause (§15.3; sanctions and export misuse remain in §2.2(v)); the copyright and trademark notice (§15.6); the list of what an arbitration request must contain (§12.4); the sentence incorporating guidelines for particular features (now folded into §12.4).
- Narrowed: the Organization's duty to use "commercially reasonable efforts to prevent unauthorized access" is gone (users must still keep credentials secure, §1.3); the Customer Data warranty list now reads "infringe anyone's rights, be unlawful, defamatory, or deceptive, or contain malicious code" (drops "obscene, pornographic" and the express privacy and publicity wording); "Company may monitor your use" is now "we may block any use"; the MSA tax clause no longer requires the customer to reimburse collected taxes or report changes in tax-exempt status (§3.7).
- Kept in substance, shorter: restrictions (ten items → eight), the fee clauses, auto-renewal capitals, payments terms, disclaimers (including the 90-day warranty limit), liability cap (aggregate wording), indemnity (now items (i)–(iv)), and arbitration (JAMS, informal step, court-decided threshold issues, jury and class waiver, batch arbitration, opt-out, severability).
- The defined term "Company" was dropped; the Terms use "Chexbill" and "we". Survival (§9.1) still covers every section except §1 and §2.1.

**Privacy Policy** (now §1–§11)
- Data categories merged from eleven into six, plus a card-details sentence; dropped the metadata sentence and "other data". Sources dropped: service providers and business-transaction partners.
- Uses merged into seven bullets; dropped "personalization" (covered by operating the Service), "further uses with consent", and the separate corporate-events purpose (now in sharing as "buyers and investors").
- Sharing: added an express "We do not sell personal information"; dropped "linked third-party services"; Zendesk moved into the service-provider list.
- Choices: dropped "blocking images", "declining to provide information", and "linked platforms".
- "Other sites and services" folded into §2; "Security" and "International data transfer" merged into §7.
- State notice is now **California only** (§11): the other-states sentence was removed together with the Terms' state notices, and the Nevada right is no longer stated anywhere (Nevada's law covers consumers, not business users; see B.2.23).

**Cookie Notice**: shorter explanations, shorter table descriptions, and email-pixel and image-blocking text merged; the per-device reminder and the duplicated allaboutcookies sentence were dropped.

**DPA**
- Now applies automatically as part of the Terms, with a countersigned copy on request; the signature block was removed (resolves B.2.9).
- Personal Data now excludes "the account details of Customer's users" (and, as before, Chexbill Payments applications and usage information) instead of "business contacts who are Customer personnel", which removes the tension with Annex 1. Annex 1 no longer lists login details or IP addresses and device identifiers, since those are Chexbill's own data under the Privacy Policy.
- Definitions trimmed (Affiliate, Data Subject, Services, Security Measures as a separate entry); the consent to Affiliates as Subprocessors was removed (Chexbill has none).
- Security incidents (§4(c)): the "mutually agreed in good faith" qualifier on cooperation was dropped; Customer must consult Chexbill before any notice that refers to it.
- Audits (§8): about 550 words → about 140. Dropped: the detailed audit-plan steps, the customer's duty to share audit reports and report non-compliance, limits on use of reports, and the express "no breach of confidentiality" carve-out. Kept: once a year, two weeks' notice, agreed plan, confidentiality agreement, customer pays (including Chexbill's costs), auditor objection, SOC 2/ISO report substitution.
- Removed: the automated decision-making clause (old §10(c); the Service makes no such decisions) and the "cooperate on amendments" clause (old §11(b)). "Access is not consideration" moved to Annex 2(f). New §11(b) is the liability clause (was §11(d)).
- Annex 3: thirteen template measures → eleven short statements; password history and reset rules dropped; physical security is now provided "through the data centers of Chexbill's hosting providers".

---

## Part B — Open items for the attorney

### B.1 Unresolved facts marked [TBD] in the documents
1. **Backup retention window** after deletion (Terms §9.2; Privacy Policy §6; DPA §9(c)). Engineering must state how long Supabase backups retain deleted data.
2. **Subprocessor entity names and locations** (DPA Annex 4). Drafted from public information; confirm each from the vendor's current terms. Brevo is French-headquartered.
3. **URLs supplied by the drafter, not the templates:** vendor privacy-policy URLs in the Cookie Notice table; the Fiserv privacy notice cited for CardConnect in the Privacy Policy (CardConnect also publishes its own policy; cite whichever governs merchant and cardholder data); the Plaid End User Privacy Policy; and the internal paths `https://chexbill.com/privacy`, `/cookies`, `/dpa`, and `/subprocessors`, which must exist at launch. The allaboutdnt.com, globalprivacycontrol.org, and allaboutcookies.org links come from the template .docx files.

### B.2 Judgment calls marked [ATTORNEY REVIEW] or otherwise worth a look
1. **Chexbill Payments section (Terms §7).** No template covers a referral-partner/ISV arrangement. Confirm: (a) Chexbill's characterization as "software provider and referral partner" of the Processor matches the ISR/sub-rep agreement; (b) whether the CardConnect/Fiserv program requires any specific disclosures or pass-through terms in Chexbill's own Terms (the Fiserv Program Guide v. GenCP-KB-2907_PG_07.01.26 and MPA v. GenCP-KB-2910_MPA_08.28.26 were provided by the founder); (c) whether the 3-year Fiserv initial term, early-termination fee, and personal guarantee should be flagged to merchants in Chexbill's onboarding flow; (d) PCI DSS scope given use of the hosted tokenizer and in-person terminals; (e) equipment sale/rental terms (§7.4) are stated in one sentence and may warrant their own order terms.
2. **Sensitive data.** Chexbill collects SSN/EIN, date of birth, and bank account numbers for merchant onboarding and vendors' TINs for 1099 filing. The Privacy Policy discloses this and selects the "we process some Sensitive PI but not to infer characteristics" alternative; the DPA §6(b) warranty was carved out (Permitted Sensitive Data). Confirm both, and whether any state law requires a "limit use of sensitive PI" right to be offered notwithstanding the exemption relied on.
3. **KYC data deletion.** Founder states onboarding data is deleted after submission to the processor and never reaches support tickets, error monitoring, or logs. Privacy Policy §6 relies on this. Recommend an engineering verification (including Supabase backups and Sentry breadcrumbs) before publication.
4. **Record retention vs. automatic deletion.** Organizations are deleted 365 days after a lapsed subscription (90 days for unconverted trials). IRS guidance generally expects filers to keep copies of information returns for about four years. Decide what Chexbill (versus TaxBandits or the customer) must retain, and whether Terms §9.2 and the Privacy Policy need a carve-out for tax and payment records (a generic "as required by law" sentence is included).
5. **Termination for paid customers (Terms §9.1).** The template is at-will; at the founder's request a "reasonable efforts to notify and give an opportunity to cure" sentence was added for paid Organizations with carve-outs. Confirm the carve-outs are broad enough.
6. **Liability cap (Terms §10.2)** raised to the greater of $100 or 12 months' fees, and the exclusions list extended (tax penalties, chargebacks, fines, processing losses). Confirm enforceability of excluding tax penalties where they result from a Service error.
7. **Indemnity (Terms §10.3)** extended to Customer Data and payments activity. Confirm.
8. **"Not professional advice" and tax-filing clauses (Terms §6.2–6.3).** New language; confirm whether Chexbill's 1099 e-filing role creates any obligations as a transmitter or filer that the Terms should address, and whether "we will inform you whether the tax authority has accepted or rejected the filing" creates an undesired service commitment.
9. **DPA execution model.** Done in A.7: the DPA now applies automatically by incorporation into the Terms (Terms §4 and the DPA preamble), with a countersigned copy on request, and the Personal Data definition no longer conflicts with Annex 1. Confirm the incorporation model is acceptable for customers who need a signed DPA.
10. **DPA precedence.** DPA §11(a) says the DPA governs on conflict; Terms §4 says the Privacy Policy governs on personal-data conflicts between the Terms and the Privacy Policy. These concern different documents, but confirm the hierarchy is as intended.
11. **Copyright complaints.** Clause removed in A.7. Without a registered DMCA agent it gave no safe-harbor protection, and customer content in the Service is not public. Add a clause and register an agent if the Service ever publishes user content.
12. **Arbitration.** JAMS (Option A) selected; DecisionLayer (Option B) removed. The batch-arbitration clause, 45/60-day informal process, and $250,000 Streamlined/Comprehensive split are kept; A.7 condensed the wording and dropped the list of what an arbitration request must contain. Confirm enforceability of the class waiver and opt-out mechanics under Delaware law and against business customers.
13. **State consumer notices.** All removed in A.7 (CA Civil Code §1789.3 notice, CO, CT, VA, NV), as in Xero and FreshBooks. Confirm that none is required for a business-user product, in particular the §1789.3 notice for any sole proprietors who may count as consumers.
14. **Google Gemini.** Privacy Policy states Google does not train on inputs under the paid API tier. Confirm against Google's current API terms at publication.
15. **Plaid.** Terms §8.2 and the Privacy Policy reference the Plaid End User Privacy Policy, which Plaid requires of apps using its services; confirm the current URL and that Plaid's developer policy does not require additional language.
16. **Payor terms.** Payors (customers' clients paying invoices) are addressed in Terms §7.6 and §8.3; the payment page will carry a short notice linking the Terms and Privacy Policy. Confirm whether Payors need a distinct short-form notice.
17. **Accessibility commitment.** Removed from the Terms in A.7; neither Xero nor FreshBooks has one in its terms (both link an accessibility page instead). Consider a separate accessibility page.
18. **General Legal attribution footnote** kept on each document per the template authors' request (CC0 permits removal).
19. **New operative language with no template source**, for a closer read: Terms §1.2 (deeming the business bound), §3.1–3.4, §6.1–6.3, §7 in full, §9.2; Privacy Policy processor-role paragraph, Payor-data category, Gemini disclosure, retention bullets, "Bank connections" choice; Cookie Notice "no advertising cookies" statement and GPC item; DPA Permitted Sensitive Data definition, Personal Data carve-out for application and usage data, Cessation Date sentence, backup sentence. Every one of these was checked against the templates in two independent review passes and is listed here so counsel can prioritize. Since A.7 rewrote all four documents in plain language, the whole of each document now deserves a close read.
20. **Representations of fact the product must keep true:** no advertising cookies; Gemini paid tier with no training; KYC data deleted after onboarding and never in support tickets, error reports, or logs; marketing-only email beacons; logs kept 365 days; GPC honored.
21. **Plain-language section summaries (Terms, all sections).** New, non-operative language modeled on Xero. Confirm (a) that each summary is accurate and does not promise more than its section (for example, the §9 summary on notice before termination and the §10 summary on the liability cap); (b) that the Introduction's convenience-only sentence is enough to keep a summary from being read as a term; and (c) that someone owns keeping the summaries in sync whenever a clause changes.
22. **Children's privacy section removed (Privacy Policy).** The template's "Children" section (Service not intended for anyone under 18; deletion of a child's information collected without parental consent) was removed at the founder's request to match Xero and FreshBooks, neither of which has one. Confirm that this is acceptable given that the Service is not directed to children and Chexbill has no actual knowledge of users under 13 (COPPA), and that the remaining statements are sufficient: the 18+ requirement in the Terms Introduction and the under-16 statement in the California privacy rights section (Privacy Policy §11).
23. **Shortened state privacy rights notice (now Privacy Policy §11, California only).** See A.6 and A.7 for what was dropped. The short form is adequate only if Chexbill is below the applicability thresholds of the CCPA and the other state privacy laws (based on annual revenue or the number of state residents whose data is processed), which `legal/company-facts.md` does not record. Confirm Chexbill's status. If it is or becomes covered, the dropped items are disclosures the laws or regulations expect in a privacy policy, chiefly the category-by-category CCPA table (collection, sources, purposes, disclosure recipients for the past 12 months), how authorized agents can submit requests, and, for Colorado, Connecticut, Virginia and similar states, the appeal process. The §11 text is new language in the FreshBooks style; its wording should be read closely.
24. **Simplification pass (A.7).** Confirm the cuts that change meaning, chiefly: removing the release and §1542 waiver, the state notices, the copyright clause, and the accessibility statement from the Terms; narrowing the Customer Data warranty and dropping the customer's tax-reimbursement duty; the shorter DPA audit and security-incident clauses; and Annex 3 relying on hosting providers for physical security.

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
- DPA: `https://chexbill.com/dpa`, linked from Terms §4 and from account settings. It applies automatically (DPA preamble); offer a countersigned PDF on request. Maintain the subprocessor list at `https://chexbill.com/subprocessors` and email customers when adding a subprocessor; they have 15 days to object (DPA §7(c)).

**Acceptance mechanics**
- Sign-up: unchecked checkbox or "By creating an account you agree to the Terms of Service and acknowledge the Privacy Policy" with both hyperlinked; record timestamp, user ID, Terms version, and IP address.
- Organization creation and plan purchase: re-present the Terms (version) and the auto-renewal statement (Terms §3.2) in plain sight before the "Subscribe" button, with price, period, and renewal date; email a confirmation containing the same.
- Material changes: email notice to all account holders (Terms §12.1; Privacy Policy §9); for fee changes, email at least 30 days before the renewal (§3.5).
- Arbitration opt-out: route emails to legal@chexbill.com and log opt-outs by account; 30-day window runs from first acceptance (§11.6).
- Payment page for Payors: short notice with links; no checkbox required by the templates, but consider one.

**Versioning**
- Keep the "Version" and "Last updated" lines; archive each published version with its effective date (the template's "previous version" link was removed for v1.0 and can be reinstated from v1.1). From v1.1, follow the Xero pattern under the title: replace "This is the first version" with a one-line summary of what changed and link to the archived versions.
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
