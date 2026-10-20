# Phase 1 — Placeholder & Decision Checklist

Every placeholder, bracketed variable, optional clause, alternative, and implicit decision point found in `templates/`, grouped by the **fact** it depends on (not by document), because the same fact appears in several templates. "Appears in" uses the template slugs. "Template default" is what the template says today; "Suggested" is a common SaaS default offered so the founder can just say "yes".

Status is tracked in `legal/company-facts.md`. Items here are not answers; they are the questions.

Document slugs: `tou` Terms of Use · `pp-us` Privacy Policy (US) · `pp-gdpr` Privacy Policy (GDPR) · `cookie` Cookie Notice · `dpa-us` · `dpa-global` · `msa` Master Services Agreement · `nda-m` Mutual NDA · `nda-1` One-way NDA · `adv` Advisor Agreement · `baa` · `offer` Offer Letter

---

## 1. Company identity & jurisdiction

- [ ] **Full legal entity name** — exact registered name. Appears in: all 12 (`[Company]`, `[Full Company Name]`, `[CompanyName]`, `[LEGAL NAME OF COMPANY]`, `[COMPANY NAME]`, `[___]`).
- [ ] **Entity type and state of formation** — e.g. "a Delaware corporation". `nda-m` hardcodes "a Delaware corporation"; `baa` has `[STATE OF INCORPORATION OF COMPANY]`. Appears in: `nda-m`, `baa`; implied in `msa`, `tou`.
- [ ] **Short name / brand** used as "CompanyName" throughout. Appears in: `pp-us`, `pp-gdpr`, `cookie`, `dpa-us`, `dpa-global`.
- [ ] **Subsidiaries and affiliates covered?** — optional "[and our subsidiaries and affiliates]" in the privacy policy opener; affiliates are also listed as recipients. Template default: included as optional. Suggested: drop unless affiliates exist. Appears in: `pp-us`, `pp-gdpr`.
- [ ] **Domain name(s) / site URL** — `[DOMAIN NAME]` (tou), `[website]` (cookie); privacy policy covers "digital properties that link to this Privacy Policy". Appears in: `tou`, `cookie`, `pp-*`.
- [ ] **Mobile app?** — optional "[; and our mobile app (App)]" and "[and App]" (cookie); SDK paragraph (cookie); "(our mobile application/the Service)" location choice and "[Mobile location data]" (pp). Suggested: no app → drop all app language. Appears in: `cookie`, `pp-us`, `pp-gdpr`.
- [ ] **Registered / mailing address** — ToS §9.1 California notice `[Address]`, §11.2 informal-dispute address `[address], California [ZIP]`, §11.10 opt-out `[Address], California [ZIP]`; privacy `[Company Address]`; DPA Annex 1 `[INSERT]`; MSA signature/Exhibit A address; NDA/BAA/offer signature blocks. Appears in: `tou`, `pp-*`, `dpa-*`, `msa`, `nda-*`, `baa`, `offer`.
- [ ] **General contact (email or page)** — ToS §10.8 `[Contact]`; cookie `[EMAIL]`; privacy `[Company E-mail]`; MSA `[Company Email Address]` (notices and disputes). Suggested: one `legal@` or `support@` address. Appears in: `tou`, `cookie`, `pp-*`, `msa`.
- [ ] **Privacy / data-request contact email** — `[EMAIL]` for opt-out, Shine the Light, Nevada, GDPR rights, transfer safeguards, `[email for data requests]`; DPA Annex 1 `[Role] [Email]` "Contact Details for Data Protection". Suggested: `privacy@`. Appears in: `pp-us`, `pp-gdpr`, `dpa-us`, `dpa-global`, `tou` (§9.5 Nevada `[CONTACT EMAIL]`).
- [ ] **Disputes / legal-notice email** — ToS §11.2 `disputes@company.com`, §11.10 / Option B §11.9 opt-out email `email@email.com` / `[Insert Email or Address]`; MSA `[Company Email Address]`. Appears in: `tou`, `msa`, `offer` (Option B opt-out).
- [ ] **Accessibility contact** — ToS §10.5 `[ACCESSIBILITY CONTACT EMAIL / PHONE]`. Appears in: `tou`.
- [ ] **Phone number** — privacy "How to contact us" `[Phone Number]`; state notice `[NUMBER]` and toll-free `[1-XXX-XXX-XXXX]` for privacy requests. Template default: listed. Suggested: omit phone if none (CCPA requires two methods; email + webform suffice unless you also operate offline). Appears in: `pp-us`, `pp-gdpr`.
- [ ] **Where you are headquartered and where data is processed** — "We are headquartered in the United States" (pp); GDPR notice "We are a U.S.-based company". Appears in: `pp-us`, `pp-gdpr`.
- [ ] **Where are your users? (US only / EU-UK / global)** — decides `pp-us` vs `pp-gdpr`, `dpa-us` vs `dpa-global`, and whether the ToS needs non-US consumer carve-outs. Consequence: EU/UK users → GDPR obligations (representatives, lawful bases, transfer mechanism). Appears in: document selection.
- [ ] **Any establishment (office, employees, entity) in the EEA or UK?** — `pp-gdpr` header says it is for a U.S. company with **no** EEA/UK establishment; that is why it appoints EU and UK representatives. Appears in: `pp-gdpr`.
- [ ] **Swiss users or customers?** — `dpa-global` covers Swiss FADP; `pp-gdpr` does not mention Switzerland. Appears in: `dpa-global`.
- [ ] **Governing law (state)** — ToS §10.2 `[California]`; MSA §12.1 `[Delaware]`; NDAs hardcode Delaware; DecisionLayer option forces New York. Suggested: state of incorporation or HQ, used consistently. Appears in: `tou`, `msa`, `nda-m`, `nda-1`.
- [ ] **Venue for non-arbitrable claims** — ToS §10.2 `[County], [California]`; §11.7 fallback court `[California]`; MSA arbitration seat `[New Castle County, Delaware]`. Appears in: `tou`, `msa`.
- [ ] **Health data (HIPAA)?** — triggers `baa`; DPA Restricted Data warranty excludes PHI. Appears in: `baa`, `dpa-*`.
- [ ] **Children / minors?** — ToS 18+ gate; privacy "not intended for anyone under 18"; state notice "13–15 opt-in" vs "under 16" alternative; DPA excludes "personal data of children under 16". Consequence: under-13 users → COPPA. Appears in: `tou`, `pp-*`, `dpa-*`.
- [ ] **Signature-block details for signed documents** — name, title, email, address of signatory. Appears in: `dpa-*`, `msa`, `nda-*`, `baa`, `offer`, `adv`.

## 2. Product & pricing model

- [ ] **One-sentence description of the business** — `[DESCRIPTION OF BUSINESS]` (pp opener, verbatim); DPA Annex 1 `[Brief Company description]` "Provider Activities"; BAA `[cloud-based software services]`. Appears in: `pp-*`, `dpa-*`, `baa`.
- [ ] **Audience: consumers, businesses, or both** — decides whether the ToS "personal, non-commercial" license (§2.1) must become a business-use license, whether a DPA/MSA is needed, and whether consumer-protection notices (ToS §9) matter. Appears in: `tou`, document selection.
- [ ] **Self-serve click-through vs signed contracts** — `msa`/`dpa`/`baa` are signed; `tou`/`pp`/`cookie` are click-through. DPA "forms part of `[CUSTOMER AGREEMENT]` dated `[Effective Date of the Agreement]`" — name the agreement it attaches to (MSA or online terms). Appears in: `dpa-us`, `dpa-global`, `msa`.
- [ ] **Hosted SaaS vs on-premise** — MSA assumes on-prem install in a "Customer Environment", source-code delivery, customer installs Updates, Company support "per enterprise support plan". Suggested: hosted → these clauses need rewriting (attorney item). Appears in: `msa`.
- [ ] **Product-specific definitions in the MSA** — "Platform… designed to test and validate Customer's generative AI applications", "Generic Judges", "Judges", "Inputs", "Outputs", "Connected Accounts", "Integration Tools". Replace with your product's terms. Appears in: `msa`.
- [ ] **Free tier / free trial?** — not in any template; decision needed for ToS fee section. Appears in: gap.
- [ ] **Plans and billing cycle (monthly/annual/usage)** — ToS has no fee clause; MSA/Exhibit A: 12-month Initial Order Term, 12-month renewal, monthly billing, `$______` fees, optional `[Additional User Tiers]` block pricing. Appears in: `msa`, gap in `tou`.
- [ ] **Support commitment** — ToS §2.4 "no obligation to provide support"; MSA "enterprise-level technical support… then-current plan". Suggested: keep "no obligation" for free users, describe support for paid plans in the ToS. Appears in: `tou`, `msa`.
- [ ] **Uptime / SLA** — none in templates; MSA disclaims uninterrupted operation. Appears in: gap.
- [ ] **AI / generative features** — pp "Chat and other AI technologies" paragraph with `[INSERT Chatbot provider – e.g., Zendesk – and/or generative AI platform provider – e.g., OpenAI]`, `[employ cookies and software code]`, `[chat and/or user input/prompt]`, `[communicate with us and/or input your prompts]`, data accessed `[webpages visited… IP… inputs]`, purpose `[to facilitate the Service / purposes in this Policy]`, optional "[We contractually require… prohibit generalized AI model training]"; sharing list "[AI providers… such as OpenAI]"; DPA §10 AI-training prohibition; MSA Output warranty disclaimer. Appears in: `pp-*`, `dpa-*`, `msa`.
- [ ] **User-to-user / social features** — pp "facilitate social features… chat or messaging", "Other users and the public… `(except for messages)` `[are/may be]` visible", invitations/"Data about others", "Relationship data"; ToS §5.2 "Other Users". Suggested: single-tenant SaaS → drop. Appears in: `pp-*`, `tou`.
- [ ] **Social login / linked third-party accounts** — optional "[Third-party services, such as social media services, that you use to log into…]" source, "Linked third-party services" sharing, "Linked third-party platforms" choice; cookie "Social" row. Appears in: `pp-*`, `cookie`.
- [ ] **Third-party integrations users connect (OAuth, APIs)** — MSA "Connected Accounts" definitions and disclaimers; ToS §5.1 "Third-Party Services". Appears in: `msa`, `tou`.
- [ ] **Events, promotions, contests, sweepstakes** — "Promotion data", "Events, promotions and contests" use, partners "co-sponsor events". Suggested: drop for a pure SaaS. Appears in: `pp-*`.
- [ ] **Order Form fields** — Exhibit A: `[Company] Address/Email`, "Order Form For", "Valid Through", billing contact fields, Anticipated Start Date, Payment Method, Services/Restrictions/Fees rows. Appears in: `msa`.
- [ ] **Customer rider (Exhibit B)** — `[Rider to Form]` placeholder. Suggested: delete Exhibit B unless customers negotiate riders. Appears in: `msa`.

## 3. User accounts & acceptable use

- [ ] **Minimum age** — ToS "at least 18 years old"; pp Children "under 18". Alternatives in state notice: "[Opt-in… 13–15…]" OR "[Consumers under 16… no actual knowledge]". Suggested: 18 for B2B; if 13–17 allowed, pick the first alternative and revisit COPPA/CCPA. Appears in: `tou`, `pp-*`.
- [ ] **Account creation and credentials** — ToS §1 (accurate info, delete via instructions on Site, security); "Profile data… username and password" (pp); DPA "Authentication details". Decide: password, social login, SSO. Appears in: `tou`, `pp-*`, `dpa-*`.
- [ ] **Self-service account deletion path** — ToS §1.1 "delete your account… following the instructions on the Site"; pp optional "[Delete your content or close your account… please .]" with lost link. Appears in: `tou`, `pp-*`.
- [ ] **Team / organization accounts and Authorized Users** — MSA "Authorized User" (employees/contractors; no shared IDs); ToS is single-user. Appears in: `msa`, gap in `tou`.
- [ ] **Entity acceptance** — ToS "on behalf of yourself or the entity you represent… authority to do so". Keep. Appears in: `tou`.
- [ ] **Acceptable-use restrictions** — ToS §2.2 (no resale, reverse engineering, competing product, copying); MSA §3.1 (a)–(g). Add product-specific prohibitions? Appears in: `tou`, `msa`.
- [ ] **Suspension / termination** — ToS §8 "at any time and for any reason"; MSA 30-day cure for breach, suspension when 30 days overdue. Suggested: keep ToS at-will for free users; paid users may expect notice. Appears in: `tou`, `msa`.
- [ ] **Changes to the Site / discontinuation** — ToS §2.3 "with or without notice". Appears in: `tou`.
- [ ] **Changes to Terms notice method** — ToS §10.1 "email… or prominent notice"; pp "updating the date and posting". Appears in: `tou`, `pp-*`, `cookie`.
- [ ] **Electronic communications consent** — ToS §10.4. Keep. Appears in: `tou`.
- [ ] **Additional guidelines / rules posted on the Site** — ToS opener incorporates them. Any community guidelines, API terms, SLA? Appears in: `tou`.
- [ ] **Customer security and compliance warranties (B2B)** — MSA §3.4–3.5 (customer safeguards, consents for data); DPA §5 customer security responsibilities. Appears in: `msa`, `dpa-*`.

## 4. Data collected, processors & retention

- [ ] **Personal-data categories you actually collect** — keep/drop each: Contact · Demographic · Profile · Communications (optional "[communicate with us via chat features,]") · Transactional · Marketing · User-generated content and input data · Relationship · Financial ("stated income… financial account numbers") · Government-issued ID · Payment · Promotion · Other. Suggested for SaaS: Contact, Profile, Communications, Transactional, Marketing, User content/input, Payment (via processor); drop Demographic/Relationship/Financial/Government ID/Promotion. Appears in: `pp-us`, `pp-gdpr`, GDPR lawful-basis table.
- [ ] **Sensitive personal information** — three alternatives in state notice ("[Limit processing…]" / "[…do not process… for inferring characteristics]" / "[We do not intentionally collect]"); GDPR "No sensitive personal information" paragraph; DPA Restricted Data list. Suggested: "do not intentionally collect". Appears in: `pp-*`, `dpa-*`.
- [ ] **Third-party sources** — Public sources · Data providers · Partners · Customers · Service providers · Business transaction partners · optional "[Third-party services… log into]". Suggested: keep Service providers, Business transaction partners; keep social-login line only if offered. Appears in: `pp-*`.
- [ ] **Automatic data** — Device · Online activity · "(Precise geolocation/Location)" choice when "(our mobile application/the Service)" is authorized · Communication interaction (email pixels). Suggested: drop precise geolocation; keep email interaction only if you track opens. Appears in: `pp-*`.
- [ ] **Referral / invite features ("Data about others")** — keep if you have invite flows. Appears in: `pp-*`.
- [ ] **Hosting provider and region** — needed for subprocessor list and transfer disclosure. Appears in: `dpa-*` Annex 4/5, `pp-*` transfer section.
- [ ] **Full subprocessor / service-provider list** — DPA Annex 4 (US) / Annex 5 (Global) `[Name | Location(s) | Description]`, and the choice "Annex … of this DPA / at `[WEBSITE]` (the Subprocessor Site)". pp "Service providers (such as hosting, IT, customer support, [AI providers…], email delivery, marketing, consumer research, website analytics)". Appears in: `dpa-*`, `pp-*`.
- [ ] **Do you train models on user data?** — pp optional "[and we will not attempt to reidentify]", "[, and to train our AI models…]", "[See the Your choices section… opt-out]", "[Training data… INSERT OPT-OUT INSTRUCTIONS]"; DPA §10 prohibits training on customer personal data unless authorized; MSA grants license to use Customer Data "for providing and/or improving the Services" and Aggregated Data rights. Suggested: no training on identifiable data; aggregated/de-identified only. Appears in: `pp-*`, `dpa-*`, `msa`.
- [ ] **Retention periods** — pp optional "[Retention]" section (criteria-based); GDPR retention paragraph; state notice retention criteria; DPA: 30-day "Post-cessation Storage Period", retention as required by law; BAA: return/destroy within 60 days. Decide concrete periods for account data, logs, backups. Appears in: `pp-*`, `dpa-*`, `baa`.
- [ ] **Deletion / return on termination (B2B)** — DPA §9 return by secure transfer or delete/anonymize at Provider's option; certification of deletion only on request (Global 3.11); MSA §11.5 customer must delete Platform within 30 days. Appears in: `dpa-*`, `msa`.
- [ ] **Advertising partners / "sale" or "share" of personal data** — state notice alternatives: "[We may process… targeted advertising… opt-out]" / "[We do not process… for targeted advertising]"; "[You can opt-out of other sales]" / "[We do not sell]"; "Exercising your right to opt-out… `[LINK]`, `[EMAIL]`, `[NUMBER]`"; GPC honored; "[INSERT ADDITIONAL OPT-OUT PREFERENCE SIGNAL DETAILS]"; Texas "[DESCRIBE…]" optional; Nevada optional paragraph. Suggested for SaaS without ad pixels: "do not process for targeted advertising / do not sell", keep GPC sentence. Appears in: `pp-*`, `tou` §9.
- [ ] **Profiling / automated decision-making** — alternatives "[We may… INSERT DESCRIPTION… opt-out]" / "[We do not… significant effects]"; GDPR "No Automated Decision-Making"; DPA §10(c). Suggested: "do not". Appears in: `pp-*`, `dpa-*`.
- [ ] **Identity-verification process for privacy requests** — `[INSERT DESCRIPTION OF BUSINESS'S AUTHENTICATION PROCESS]`. Suggested: "verify by matching the email address on the account and, where needed, requesting additional information". Appears in: `pp-*`.
- [ ] **Privacy-request intake channels** — `[link to webform]`, toll-free `[1-XXX-XXX-XXXX]`, `[email for data requests]`, opt-out `[LINK]`. Appears in: `pp-*`.
- [ ] **Separate notices for other groups** — "[such as job applicants]". Suggested: keep "job applicants" if you recruit online. Appears in: `pp-*`.
- [ ] **CCPA information-practices chart** — five `[INSERT]` rows: PI category · CCPA statutory category · Purposes · Third parties disclosed to · Third parties sold/shared to. Must be filled from the categories above. Appears in: `pp-*`.
- [ ] **Do Not Track** — "We currently do not respond" + lost URL. Keep. Appears in: `pp-*`.
- [ ] **Global Privacy Control** — "We honor GPC signals" + lost URL. Required by CCPA/CPA/CT. Keep. Appears in: `pp-*`.
- [ ] **Privacy settings offered in-product** — optional "[Privacy settings… options to control [ADD]]". Appears in: `pp-*`.
- [ ] **Security posture statements** — pp "technical, organizational and physical safeguards"; DPA Annex 3/4 Security Measures (long fixed list: encryption in transit/at rest, MFA, logging, DR…). Confirm each measure is true or edit. SOC 2 / ISO report acceptance clause (DPA §8). Appears in: `pp-*`, `dpa-*`.
- [ ] **Incident notification** — DPA "without undue delay"; BAA 30 calendar days. Appears in: `dpa-*`, `baa`.
- [ ] **Data Protection Officer** — optional "[Our Data Protection Officer… email: [insert]]". Suggested: omit unless appointed. Appears in: `pp-gdpr`.
- [ ] **EU representative and UK representative (Art. 27)** — table with `[insert]` name, email, postal address for each. Required for a non-EU company offering services to EU/UK individuals unless exempt. Appears in: `pp-gdpr`.
- [ ] **Controller statement** — garbled sentence to repair; confirm you are controller for your own users. Appears in: `pp-gdpr`.
- [ ] **Lawful-basis table** — adjust data categories per purpose; two rows mislabeled "Events, promotions and contests". Appears in: `pp-gdpr`.
- [ ] **EEA regulator list link and ICO website link** — lost URLs. Appears in: `pp-gdpr`.
- [ ] **International transfer mechanism** — pp-gdpr says U.S. has no adequacy decision and relies on SCCs/derogations (no mention of EU-U.S. Data Privacy Framework); `dpa-global` deems SCCs Modules 2/3 (Irish law, Irish courts), UK Addendum, Swiss variations. Decide: DPF certification? Appears in: `pp-gdpr`, `dpa-global`.
- [ ] **Previous privacy policy version link** — "Please click here to view the previous version". Suggested: drop for first publication. Appears in: `pp-*`.
- [ ] **Printable copy link** — "download a printable copy here". Suggested: drop or link PDF. Appears in: `pp-*`.
- [ ] **DPA Annex 1 data-subject and data categories** — fixed lists (end users, personnel; personal, authentication, technological details). Adjust to product. Appears in: `dpa-*`.
- [ ] **Customer data-protection contact** — Annex 1 Customer `[INSERT]` address, `[Role] [Email]` (filled per customer). Appears in: `dpa-*`.
- [ ] **Subprocessor change notice period** — 15 days to object (DPA §7(d); SCC Clause 9 Option 2). Keep. Appears in: `dpa-*`.
- [ ] **Audit terms** — once per year, two weeks' notice, SOC 2/ISO/NIST report in lieu, customer pays. Keep. Appears in: `dpa-*`.
- [ ] **Restricted Data warranty** — customer promises no SSNs, PHI, biometrics, financial credentials, PCI card data, children under 16, special categories. Confirm compatible with product. Appears in: `dpa-*`.
- [ ] **BAA-specific** — "HIPAA-Eligible Services" designation, security configurations, 30-day breach reporting, 60-day return/destroy, AI de-identification use, §4.4 assumption that Company holds only device identifiers, Customer obligations paragraph (marked). Only if HIPAA applies. Appears in: `baa`.

## 5. Cookies & analytics

- [ ] **Cookie categories in use** — table rows Advertising · Analytics · Essential · Functionality/performance · Social, each with `[ADD]` "Who serves" and `[ADD]` "How to control". Suggested: Essential + Analytics (+ Functionality); drop Advertising/Social unless used. Appears in: `cookie`, `tou` §3.2, `pp-*`.
- [ ] **Analytics provider(s)** — pp optional "[For example, we use Google Analytics… here: .]" (lost URL). Name the tool and its opt-out. Appears in: `pp-*`, `cookie`.
- [ ] **Advertising / retargeting pixels** — drives Advertising row, interest-based advertising sections, NAI/DAA opt-outs, "sale/share" answers in §4. Appears in: `cookie`, `pp-*`.
- [ ] **Session-replay tool** — "[FullStory]" placeholder, optional "[and keystrokes/key touches]", opt-out link "at .]" (lost). Suggested: drop if none. Appears in: `cookie`.
- [ ] **Email tracking pixels** — cookie "Web beacons… in our HTML formatted emails"; pp "Communication interaction data". Appears in: `cookie`, `pp-*`.
- [ ] **Browser web storage (localStorage)** — keep paragraph (most SaaS use it). Appears in: `cookie`.
- [ ] **Flash cookies** — outdated paragraph. Suggested: delete. Appears in: `cookie`.
- [ ] **Mobile SDKs** — only with an app. Appears in: `cookie`.
- [ ] **Consent banner / preference dashboard** — optional block "[Cookie Preference Dashboard… Cookie Banner… Cookie Dashboard [hyperlink]… accept all / reject all / manage]". Required in practice for EU users. Appears in: `cookie`, `pp-*` ("store a record of your preferences").
- [ ] **Lost opt-out URLs** — allaboutcookies-type site (twice), NAI, DAA, AppChoices. Supply standard URLs (judgment call; attorney to confirm). Appears in: `cookie`, `pp-*`.
- [ ] **Cookie Notice vs Cookie Policy naming and link** — ToS §3.2 `[Cookie Policy / Privacy Policy – hyperlink]`; pp says "Cookie Notice". Suggested: one name, "Cookie Notice". Appears in: `tou`, `pp-*`, `cookie`.
- [ ] **Cookie Notice date** — `[INSERT DATE]` "Last modified". Appears in: `cookie`.

## 6. Payments, refunds & cancellation

- [ ] **Payment processor(s)** — pp alternatives "[such as PayPal… / mobile carrier billing / such as Stripe… https://stripe.com/privacy]"; "Payment data" category. Consequence: if card data touches your servers → PCI DSS; DPA Restricted Data excludes PCI data. Suggested: Stripe, card data never stored by you. Appears in: `pp-*`, `dpa-*`.
- [ ] **Fees, billing cycle, auto-renewal, price changes** — absent from ToS; MSA §5.1 (price increases on 30 days' notice before renewal), Exhibit A (12-month auto-renew, 90-day non-renewal notice, non-cancelable). Decide ToS equivalents. Appears in: `msa`, gap in `tou`.
- [ ] **Payment method and terms** — MSA "ACH only", "Net 60", Exhibit A "Net 60 / Monthly". Suggested for self-serve: card via processor, charged in advance. Appears in: `msa`.
- [ ] **Late payment** — MSA 12% p.a. interest after 30 days; suspension after 30 days overdue. Appears in: `msa`.
- [ ] **Refunds** — MSA "all fees non-refundable"; §11.5 no refund on termination and remaining term payable; §9.1(d) refund of unused prepaid fees only on IP-infringement termination. Decide consumer refund policy. Appears in: `msa`, gap in `tou`.
- [ ] **Cancellation mechanics** — Exhibit A "Subscriptions are non-cancelable"; ToS says only that users can delete the account. Decide: cancel anytime, effective end of period? Appears in: `msa`, `tou`.
- [ ] **Taxes** — MSA §5.2 (exclusive of taxes; customer pays; exemption certificates). Appears in: `msa`.
- [ ] **Currency** — MSA "United States Dollars"; ToS cap in "$50 USD". Appears in: `msa`, `tou`.
- [ ] **Transactional data wording** — pp "orders… order numbers and transaction history". Keep for paid plans. Appears in: `pp-*`.

## 7. IP, user content & licensing

- [ ] **License scope to users** — ToS §2.1 "limited, non-exclusive, non-transferable, revocable… for your own personal, non-commercial purposes". Suggested: "internal business purposes" (B2B) or "personal or internal business purposes". Appears in: `tou`.
- [ ] **Ownership of user content / Customer Data** — MSA §4.2 Customer owns Customer Data and Outputs; grants Company a license "for providing and/or improving the Services" and to create Aggregated Data. ToS has no user-content clause (template assumes a site without uploads). Decide and add. Appears in: `msa`, gap in `tou`, `pp-*` ("User-generated content and input data").
- [ ] **Ownership of AI outputs** — MSA: Customer owns Outputs; Company disclaims accuracy/IP status. Appears in: `msa`.
- [ ] **Aggregated / de-identified data rights** — MSA §4.3 Company owns Aggregated Data, may publish; pp aggregated-data paragraph. Appears in: `msa`, `pp-*`.
- [ ] **Generic Tools / know-how retention** — MSA §4.4 (incl. "Generic Judges"). Appears in: `msa`.
- [ ] **Feedback** — ToS §2.6 license (perpetual, irrevocable, royalty-free, no attribution); MSA §4.5 assignment; NDA-m §10 license. Suggested: keep license form in public docs. Appears in: `tou`, `msa`, `nda-m`.
- [ ] **Copyright notice** — ToS §10.7 "Copyright © 202[_] [Company]"; trademarks statement. Year and holder. Appears in: `tou`.
- [ ] **Publicity / logo use** — MSA §12.7 Company may list Customer and use logo. Keep or make opt-in. Appears in: `msa`.
- [ ] **Confidentiality marking regime (B2B)** — MSA §8.1 requires marking and 30-day written summary of oral disclosures. Appears in: `msa`.
- [ ] **Export control clause** — ToS §10.3; NDAs. Keep. Appears in: `tou`, `nda-*`.
- [ ] **DMCA / copyright-complaint process** — not in any template. Decision: add if users upload content (attorney item). Appears in: gap.
- [ ] **NDA Permitted Use** — nda-1 `[enable Recipient to evaluate or pursue a business relationship with the Company]`; nda-m fixed. Appears in: `nda-1`, `nda-m`.
- [ ] **NDA term/survival** — 5-year term; nda-m 7-year survival, 30-day termination, 10-day breach termination; nda-1 termination on notice. Appears in: `nda-*`.
- [ ] **Advisor terms** — `[(describe services)]`, `[(provide dates of services)]`, non-compete field `___________`, `[__]` option shares, `_____`-year vesting, `_____` monthly installments, 12-month inactivity termination, 30-day expense submission; missing preamble/parties/Effective Date/signature block. Appears in: `adv`.

## 8. Liability, disputes & governing law

- [ ] **Arbitration provider** — ToS `[OPTION A – JAMS]` vs `[OPTION B – DecisionLayer AI arbitration]` ("Select one and delete the other"); offer letter has the same pair; MSA uses AAA Expedited. Suggested: Option A (JAMS) for the ToS; attorney to confirm DecisionLayer enforceability. Appears in: `tou`, `offer`, `msa`.
- [ ] **Arbitration opt-out address/email** — Option A §11.10 `[Address], California [ZIP]` or `email@email.com`; Option B §11.9 `[Insert Email or Address]`; 30-day window. Appears in: `tou`, `offer`.
- [ ] **Informal dispute notice address** — Option A §11.2 `disputes@company.com` or `[address], California [ZIP]`; 45-day meet, 60-day window; MSA 60 days via `[Company Email Address]`. Appears in: `tou`, `msa`.
- [ ] **Arbitration seat** — Option A "county where you live"; MSA `[New Castle County, Delaware]`; Option B New York courts for confirmation. Appears in: `tou`, `msa`.
- [ ] **Fallback court if class waiver unenforceable** — Option A §11.7 `[California]`. Appears in: `tou`.
- [ ] **Class-action and jury-trial waivers** — both options; offer letter. Keep. Appears in: `tou`, `offer`.
- [ ] **Batch arbitration (100+ demands)** — Option A §11.9. Keep. Appears in: `tou`.
- [ ] **JAMS thresholds** — $250,000 Streamlined vs Comprehensive rules. Keep. Appears in: `tou`.
- [ ] **Liability cap** — ToS §7 greater of $50 USD or amounts paid in prior 6 months; MSA §7.2 fees paid in prior 12 months with Excluded Liability carve-outs. Suggested: keep ToS formula; consider 12 months for paid plans. Appears in: `tou`, `msa`.
- [ ] **Warranty disclaimer and 90-day statutory-warranty limit** — ToS §6. Keep. Appears in: `tou`, `msa` §6.
- [ ] **Indemnification by users** — ToS §4 (use, breach, law violation; Company controls defense). MSA mutual indemnities (Company: U.S. IP infringement with remedies; Customer: breach of restrictions/warranties, Connected Accounts, Outputs). Appears in: `tou`, `msa`.
- [ ] **Release of claims incl. Cal. Civ. Code §1542** — ToS §5.3. Keep (California-specific wording is harmless elsewhere). Appears in: `tou`.
- [ ] **Survival clause** — ToS §8 "Sections 2.2–2.6 and 3–11"; must be renumbered if sections change. Appears in: `tou`, `msa`, `nda-*`.
- [ ] **State-specific consumer notices** — ToS §9 CA (Civ. Code §1789.3 `[Company Name]`, `[Address]`, `[Email]`), CO, CT, VA, NV `[CONTACT EMAIL]`, §9.6 drafting note to add other states. Decide which to keep; attorney to update list. Appears in: `tou`.
- [ ] **Accessibility commitment (WCAG 2.1 AA)** — ToS §10.5. Keep only if you intend to meet it. Appears in: `tou`.
- [ ] **Assignment** — ToS "you may not assign… we may assign freely"; MSA §12.6 asymmetric consent. Appears in: `tou`, `msa`.
- [ ] **MSA term mechanics** — 1-year initial, 1-year auto-renew, 90-day non-renewal notice, 30-day termination when no orders, 30-day cure, 10-day payment of remaining fees. Appears in: `msa`.
- [ ] **Force majeure, independent contractor, counterparts, entire agreement** — fixed boilerplate; confirm. Appears in: `msa`, `nda-*`.
- [ ] **Offer-letter employment terms** — `[Date]`, `[Employee Name]`, `[Address]`×2, `[First Name]`, `[position]`, `[duties]`, `[manager]`, work location alternative `[office at [location] / home office (remote)]`, `[city, California]`, `$[annual salary]`, pay frequency `[monthly / semimonthly / every two weeks]`, acceptance deadline and start date blanks, signatory `[Name], [Title]`, `[Email]`, Exhibit A CIIAA (missing), JAMS rules URL (lost), reference-check and work-authorization conditions, Pacific Time hours. California-only. Appears in: `offer`.

## 9. Document selection

- [ ] **Terms of Use** — needed; must be adapted from website terms to SaaS terms (fees, user content, business use).
- [ ] **Privacy Policy** — choose `pp-us` or `pp-gdpr` (one only).
- [ ] **Cookie Notice** — needed (cross-referenced by both).
- [ ] **DPA** — only if business customers upload their own users' personal data; choose `dpa-us` or `dpa-global`.
- [ ] **MSA + Order Form** — only for signed enterprise deals; heavy rework from on-prem.
- [ ] **BAA** — only for protected health information.
- [ ] **Mutual / One-way NDA, Advisor Agreement, Offer Letter** — internal; include only on request.
- [ ] **Keep the General Legal attribution footnote?** — README asks to keep it; CC0 allows removal. Suggested: keep. Appears in: all.

## 10. Other

- [ ] **Effective / last-updated dates** — ToS "Version 1.0 Last revised: Date, 202[_]"; pp "Effective as of [DATE]" and header "Last Updated: [DATE]"; cookie "Last modified [INSERT DATE]"; MSA/NDA effective dates. Suggested: same publication date on all public docs; version number on ToS. Appears in: all.
- [ ] **Section numbering restoration** — DPAs, MSA, BAA lost their numbering in conversion while the text cross-references numbered sections; ToS has two "11"s. Output must renumber consistently. Appears in: `dpa-*`, `msa`, `baa`, `tou`.
- [ ] **Lost hyperlinks to supply** — allaboutcookies (×2 cookie, ×1 pp), Google Analytics opt-out, DNT info, GPC info, NAI, DAA, AppChoices, PayPal privacy, EEA regulators list, ICO website, JAMS rules, FullStory opt-out, previous policy, printable copy, cookie dashboard, account-closure link, opt-out webform. Appears in: `cookie`, `pp-*`, `offer`.
- [ ] **Template text defects to fix in output** — pp-us header mislabeled; GDPR controller sentence garbled; duplicate lawful-basis row; MSA "Client" typo and garbled §9.2(b); nda-m §9 "as required" → "except as required"; advisor preamble missing. See `legal/phase1-inventory.md` §5. Appears in: various.
