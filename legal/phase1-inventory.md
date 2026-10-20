# Phase 1 — Template Inventory

Source: `templates/` (General Legal, CC0 1.0). All 12 templates read in full on 2026-10-20. The companion checklist of every placeholder and decision point is in `legal/phase1-checklist.md`.

## 1. What exists

| # | Template | What it covers | Parties / audience | Relevance to a SaaS web app |
|---|---|---|---|---|
| 1 | **Terms of Use** (`terms-of-use`) | Website access license, restrictions, account rules, feedback license, indemnity, disclaimers, $-capped liability, termination, state consumer notices, accessibility, arbitration (two alternative clauses: JAMS, or DecisionLayer AI arbitration) with class-action and jury waivers and 30-day opt-out | Company ↔ every visitor/user (click-through) | **Core.** Note: drafted as *website* terms (license is "personal, non-commercial"; no subscription, billing, refund, or cancellation terms). Must be adapted for a paid SaaS. |
| 2 | **Privacy Policy (U.S. only)** (`privacy-policy-us`) | Data categories, sources, uses, sharing, retention, choices, security, children, changes, contact, plus a State Privacy Rights Notice (CCPA/CPRA, VCDPA, CPA, CTDPA, Texas, Nevada, Shine the Light, GPC) | Company → all users | **Core — alternative to #3.** Use only if no EU/UK users are targeted. |
| 3 | **Privacy Policy (GDPR enhanced)** (`privacy-policy-gdpr`) | Everything in #2 **plus** a "Notice to European users": controller identity, EU/UK representatives, DPO, lawful-basis table, retention, sensitive data, data-subject rights, supervisory-authority complaints, international transfer mechanisms | Company → all users incl. EEA/UK | **Core — alternative to #2.** Header states it is for a *U.S. company with no establishment in the EEA or UK*. |
| 4 | **Cookie Notice** (`cookie-notice`) | Cookie definitions, first- vs third-party, five-category cookie table (advertising, analytics, essential, functionality, social), other tech (web storage, Flash, pixels, SDKs, session replay), user controls (banner/dashboard, browser, NAI/DAA opt-outs, mobile ad ID) | Company → all visitors | **Core.** Both privacy policies and the ToS cross-reference it. |
| 5 | **DPA (U.S.)** (`dpa-us`) | Processor-friendly data processing addendum: instructions, security measures, incident notice, data-subject requests, Restricted Data warranty, subprocessors (15-day objection), audits, return/deletion (30-day window), AI-training prohibition, State Privacy Laws annex, security annex, subprocessor list | Provider (you) ↔ business Customer (signed) | **B2B only — alternative to #6.** Needed only if business customers upload *their* users' personal data and you act as their processor. |
| 6 | **DPA (Global)** (`dpa-global`) | #5 plus GDPR/UK GDPR/Swiss FADP: European Annex, DPIA assistance, EU SCCs (Module 2/3, Irish law), UK Transfer Addendum, Swiss variations | Provider ↔ business Customer (signed) | **B2B only — alternative to #5.** Use if any business customer or its data subjects are in the EEA/UK/Switzerland. |
| 7 | **Master Services Agreement** (`master-services-agreement`) | Enterprise license, order forms, connected accounts, support, customer restrictions, IP/data rights (customer data, outputs, aggregated data, generic tools, feedback), fees (Net 60, ACH only, 12% interest), warranties, liability (12-month fees cap), confidentiality, mutual indemnities, 1-year auto-renew, AAA arbitration, Delaware law; Exhibit A order form, Exhibit B customer rider | Company ↔ enterprise Customer (signed) | **B2B only, and heavily product-specific.** Drafted for an *on-premise* AI-testing platform ("Judges", "Customer Environment", source-code delivery). Would need substantial rework for hosted SaaS; see §4 below. |
| 8 | **Mutual NDA** (`mutual-nda`) | Two-way confidentiality, 5-year term, 7-year survival, Delaware law, AI-training prohibition, feedback license | Company ↔ counterparty | Not a public user-facing doc. Optional for partnerships/fundraising. |
| 9 | **One-way NDA** (`one-way-nda`) | One-way confidentiality, 5-year term, Delaware law, AI-training prohibition | Company → Recipient | Not a public user-facing doc. Optional. |
| 10 | **Advisor Agreement** (`advisor-agreement`) | Advisory services, option grant with vesting, IP assignment, confidentiality, CCPA pass-through, at-will termination, non-compete during term | Company ↔ Advisor | Not a public doc. Optional. Template is truncated (no preamble/parties/effective date; starts at §1). |
| 11 | **Business Associate Agreement** (`business-associate-agreement`) | HIPAA BAA for "HIPAA-Eligible Services": permitted uses, safeguards, breach reporting (30 days), subcontractors, return/destroy (60 days) | Company ↔ healthcare Customer | **Conditional.** Only if the product will process protected health information. |
| 12 | **Employee Offer Letter (CA exempt)** (`employee-offer-letter`) | California exempt-employee offer: salary, at-will, no-accrual vacation, JAMS or DecisionLayer arbitration, references Exhibit A CIIAA (not included) | Company → employee | Not a public doc. California-specific. Optional. |

**Recommended core set for a SaaS web app:** Terms of Use (adapted) + one Privacy Policy (US or GDPR) + Cookie Notice. **Add one DPA** if you sell to businesses that will put their customers'/employees' personal data into the product. **Add the MSA** only if you sign enterprise contracts. BAA only for health data. NDAs/advisor/offer letter are internal and not part of the app's legal pages.

## 2. Overlaps and cross-references

- **ToS → Privacy Policy** (incorporated by reference; Privacy Policy controls on data conflicts) **→ Cookie Notice / Cookie Policy** (ToS §3.2 links to one). ToS §9 state notices also point to the Privacy Policy.
- **Privacy Policy (both) → Cookie Notice** ("see our Cookie Notice" for tracking tech and "Your choices"). The Cookie Notice → Privacy Policy. These three must use the same company name, contact email, and effective dates.
- **Privacy US vs Privacy GDPR**: identical through the State Privacy Rights Notice; GDPR adds the European notice, the "Notice to European Users" banner, and a transfer paragraph. Pick one.
- **DPA US vs DPA Global**: identical core body; Global adds GDPR definitions, the European Annex (Annex 2), SCC population, UK and Swiss parts, and renumbers annexes (US: Annex 1–4; Global: Annex 1–5). Pick one. Both "form part of" a `[CUSTOMER AGREEMENT]` (the MSA or your online terms).
- **MSA → DPA** (§2.5 requires a DPA before personal data is processed) **→ Order Form (Exhibit A) → Supplemental Customer Terms (Exhibit B)**.
- **BAA → Services Agreement** (addendum to it; inherits its indemnity and liability caps).
- **ToS and Offer Letter** share the same two arbitration alternatives (Option A JAMS / Option B DecisionLayer). The MSA uses a third (AAA Expedited). The NDAs have no arbitration.
- **Mutual vs One-way NDA**: alternatives; Mutual is longer and hardcodes "a Delaware corporation".
- **Advisor Agreement, Offer Letter, NDAs**: standalone.

## 3. Defined terms that must stay consistent

| Term | Used by | Conflict to resolve |
|---|---|---|
| "Site" | ToS | ToS governs a *Site*; Privacy Policy governs the *Service*; MSA governs *Platform* and *Services*. For a SaaS app, one definition should carry across the public docs (recommend "Service" or "Services" everywhere, with the domain named once). |
| "Service" (singular) | Privacy Policies | Includes website, mobile app, social pages, marketing activities, live events. |
| "Services" (plural) | DPAs, MSA, BAA | Defined in the customer agreement. |
| "Sites" / "App" | Cookie Notice | Separate "Sites" and optional "App". |
| "Company" / "we" | ToS, MSA, NDAs, Advisor, BAA, Offer Letter | Fine. |
| "[CompanyName]" short name | Privacy Policies, Cookie Notice, DPAs | Must equal the ToS "Company" entity. |
| "Provider" | DPAs | You are "Provider" in the DPA but "Company" in the MSA/ToS. Acceptable (DPA defines it) but the MSA's DPA reference must match. |
| "Customer" | MSA, DPAs, BAA | B2B counterparty. MSA §9.1 once says "Client" (typo). |
| "Personal Data" vs "personal information" vs "Personal Information" | DPAs / Privacy Policies / State notice | Each defines its own; do not cross-use. |
| "Tracking Technologies" | ToS §3.2 | Cookie Notice does not define the term; fine, but keep wording aligned. |
| "Third-Party Services" | ToS §5.1, MSA §2.6 | Different definitions (links/ads vs. dependencies). Fine within each doc. |
| "Feedback" | ToS, MSA, Mutual NDA | ToS = license; MSA = assignment; NDA = license. Pick one posture for public docs. |

## 4. Jurisdiction-specific content

| Template | Jurisdiction assumptions |
|---|---|
| Terms of Use | U.S. only. Governing law placeholder defaults to **California**; venue `[County], [California]`; informal-dispute and opt-out addresses hardcode "California [ZIP]". §9 state notices for CA (Civ. Code §1789.3, CCPA/CPRA), CO, CT, VA, NV, plus a drafting note to add others (TX, OR, MT, UT, IA, IN, TN "as of 2026"). §5.3 California Civil Code §1542 waiver. Export clause references U.S. export law. Option B forces **New York** law/courts and the FAA. Accessibility: WCAG 2.1 AA (U.S. ADA practice). |
| Privacy Policy (US) | U.S. federal + state laws: CCPA/CPRA (incl. 12-month lookback chart, Shine the Light), VCDPA, CPA, CTDPA, Texas TDPSA, Nevada NRS 603A, GPC. "Headquartered in the United States." Children: under 18. |
| Privacy Policy (GDPR) | All of the above **plus** EU GDPR and UK GDPR; explicitly for a *U.S. company with no EEA/UK establishment* (hence EU + UK representatives under Art. 27). States the U.S. has no adequacy decision (does **not** mention the EU-U.S. Data Privacy Framework; attorney should confirm current status). Lists the UK ICO address. No Swiss coverage. |
| Cookie Notice | Jurisdiction-neutral text but opt-out mechanisms are U.S. (NAI, DAA, AppChoices). The optional consent banner/dashboard paragraph reflects EU ePrivacy practice. |
| DPA (US) | U.S. State Privacy Laws only (CCPA service-provider terms in Annex 2). Restricted Data warranty references HIPAA and PCI DSS. |
| DPA (Global) | U.S. State Privacy Laws + EU GDPR + UK GDPR + Swiss FADP. SCCs (Decision 2021/914) Modules 2 and 3, governed by **Irish law / Irish courts**; UK Transfer Addendum; Swiss FDPIC substitutions. |
| MSA | **Delaware** law, AAA arbitration in **New Castle County, Delaware**; USD; U.S. taxes language; infringement indemnity limited to U.S. IP. |
| Mutual NDA | "a **Delaware** corporation" hardcoded; Delaware law; U.S. export law; ESIGN/UETA. |
| One-way NDA | Delaware law; U.S. export law; ESIGN/UETA. |
| Advisor Agreement | U.S.; CCPA/CPRA pass-through; 18 U.S.C. §1833(b) whistleblower notice; U.S. option-grant mechanics. |
| BAA | U.S. HIPAA/HITECH (45 CFR 160/164) only. |
| Offer Letter | **California** only (exempt classification, PAGA/FEHA/Labor Code carve-outs, Pacific Time hours, CA vacation treatment). Option B forces New York law. |

## 5. Things that look wrong, outdated, or contradictory in the templates

Flagged now so they are not silently worked around. Items marked **(conversion)** are artifacts of the .docx → markdown conversion; the .docx originals in `docx-originals/` may be clean.

**Terms of Use**
- §2.1 license is for "personal, non-commercial purposes" and §2.4 disclaims any support obligation. Both contradict a paid B2B or prosumer SaaS. The template has **no** subscription, fee, auto-renewal, refund, or cancellation clauses at all; those will have to be sourced from the MSA's fee clauses or flagged for the attorney.
- Two sections are numbered "11" (Option A and Option B); intentional, pick one.
- Option A Streamlined/Comprehensive thresholds and batch-arbitration mechanics are JAMS-specific; Option B overrides governing law to New York regardless of §10.2.
- §9.6 drafting note lists states "as of 2026" and tells you to add more; the list is already incomplete (e.g. Delaware, New Hampshire, New Jersey, Minnesota, Maryland have comprehensive laws) — attorney item.
- §10.7 copyright line reads "202[_][Company]" — missing space (conversion).

**Privacy Policies (both)**
- Header row of the **U.S.-only** template says "TEMPLATE PRIVACY POLICY AND COOKIE NOTICE (GDPR compliant for U.S. Company with no 'establishment' in the EEA or UK)" — copy-pasted from the GDPR version; mislabeled.
- Lost hyperlinks (conversion): "visit ." / "here: ." for the cookie-info site, Google Analytics opt-out, Do Not Track info, GPC info, NAI/DAA/AppChoices (Cookie Notice), EEA regulator list, ICO website, PayPal privacy policy. URLs must be supplied.
- List numbering is broken throughout (e.g. "1. Contact data, 2. Demographic data" then unnumbered items; "## Customers" as a lone heading) (conversion).
- "Index" block lists four items only and is not a real table of contents (conversion).
- GDPR Controller paragraph is garbled: "(i.e., the and the so-called ' (as and where applicable, the "GDPR"))" — text missing (likely "the EU GDPR and the so-called 'UK GDPR'").
- GDPR lawful-basis table has **two rows titled "Events, promotions and contests"**; the second describes corporate-transaction sharing and is mislabeled.
- "Exercising other state privacy rights" line has placeholders without `<mark>` tags: `[link to webform]`, `[1-XXX-XXX-XXXX]`, `[email for data requests]`.
- Transfer section says the U.S. lacks an adequacy decision but does not mention the EU-U.S. Data Privacy Framework (in force since July 2023) — attorney should confirm which mechanism to cite.
- Children section says "not intended for anyone under 18" while the State notice offers a 13–15 opt-in alternative; pick consistently.

**Cookie Notice**
- Flash LSO paragraph is obsolete (Flash reached end-of-life December 2020). Recommend dropping.
- Session-replay paragraph names FullStory and has an empty opt-out link "at .]".
- "[ADD]" cells in the cookie table are not `<mark>`-tagged but are placeholders.
- The "For more information about cookies… visit ." paragraph appears twice (once in §2, once after the list) (likely conversion duplication).
- "Last modified [INSERT DATE]" is at the bottom while the privacy policies put the date at the top.

**DPA (US) and DPA (Global)**
- Section numbering was lost (conversion). The body cross-references "Section 4(a)", "Sections 9(b)–(d)", "Section 6(b)", "Section 7", "Section 7(d)", "Section 8", "Section 11(d)", "Paragraph 3.4 of Annex 2" but no headings are numbered. Numbering must be restored in output.
- "Annex 4 of this DPA/at [WEBSITE]" (US) and "Annex 5 … /at [WEBSITE]" (Global) are untagged either/or choices.
- Global §7(b) says "in accordance with this Section 7" while US says "this Section" — harmless but shows the Global version is the later edit.
- Restricted Data warranty excludes "personal data of children under 16" — if your product is used by schools or consumer-facing customers this conflicts.
- Global Annex 1 "Role: Processor (or Subprocessor…)" and "Controller or Processor" are fixed text, fine; but the signature block says "agree to be legally bound by this Agreement" (US says "this DPA").

**Master Services Agreement**
- Product-specific definitions baked in: "Platform means Company's platform designed to test and validate Customer's generative AI applications", "Generic Judges", "Judges", "Customer Environment", on-premise installation, source-code delivery, "Updates… to Company's on-premise customers". Not a hosted-SaaS MSA.
- Section numbering lost (conversion); body cites "Section 3.3", "Sections 3.1 and/or 6.4", "Section 8" (confidentiality), "Section 2.5".
- §9.1 says "procure for **Client**" (should be Customer). §9.2(b) "any agreement between Customer and a Connected Account or Customer" is garbled.
- §11.2 ("Termination if No Outstanding Orders") and Exhibit A ("Subscriptions are non-cancelable") are consistent, but Exhibit A's "Payment Term: Net 60" and "Billing Frequency: Monthly" conflict with §5.3 "ACH only" unless intended.
- §12.6 "No Assignment" requires "prior written consent of **Company**" for *either* party (one-sided drafting; probably intentional but asymmetric).
- Exhibit B rider is a bare placeholder.

**NDAs**
- Mutual NDA §9 reads "will not reproduce the Confidential Information … in any form **as** required to accomplish the intent" — should read "except as required" (a prior commit tried to fix wording here; it still reads inverted).
- Mutual NDA effective date "__________, 2026__" and "a Delaware corporation" hardcoded.
- One-way NDA §1 party name placeholder is `[___]` with a `<mark>` only around the underscores.

**Advisor Agreement**
- Missing preamble: no title, parties, Effective Date definition, signature block. Starts at "1. Services". §2 and §5 reference an "Effective Date" that is never defined. Treat as incomplete.

**BAA**
- Cross-references "Section 4.1(c)", "4.9(b)", "Section 6.3" but headings are unnumbered (conversion).
- §4.4 "Reporting" assumes Company processes no directly identifying information except device identifiers — a product-specific assumption that may be false for a SaaS.

**Offer Letter**
- References "Exhibit A: Employee Confidential Information and Inventions Assignment Agreement" which is not in the repo.
- JAMS rules link lost ("currently at )") (conversion).
- Hardcoded Pacific Time business hours and California-only carve-outs.

**All templates**
- Each carries a General Legal attribution footnote; CC0 permits removal, but the README asks that it be kept. Decision: keep it in the output documents (recommended) or drop.
