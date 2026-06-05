---
name: schema.md
description: Generate a complete, valid enterprise JSON-LD @graph for a couplesrehabs.org page (couples detox/rehab, withdrawal, insurance, geo, emergency pages). Use whenever the user provides a page URL/topic/title/meta/H1 and asks for schema, JSON-LD, or structured data. Output is one ready-to-paste <script> tag, Google-valid, with stable @IDs. Pairs with wordpress.md and url.md.
---

# Rehab Schema Skill (couplesrehabs.org)

## Output rule
Output **one valid JSON-LD `<script type="application/ld+json">` block only** — no prose before or after. Single `@graph` array.

## Inputs needed (collect or infer)
Full page URL, page topic, SEO title, meta description, H1, primary + secondary keyword, page type (from url.md), datePublished/dateModified, approx word count, breadcrumb pillar.

## Business typing — the E-E-A-T decision (locked)
Use the **hybrid**: `Organization` + `MedicalOrganization`, joined by shared @IDs. **Do NOT include `LocalBusiness`.**

Rationale specific to this site: couplesrehabs.org *does* publish a real street address (4231 Balboa Avenue #1125, San Diego, CA 92117) and a Google Maps link. That is tempting to mark up as LocalBusiness — but do not. The brand is a **national referral & information network**, not a treatment storefront, and the site's own disclaimer states it does not own, operate, or manage any facility. A LocalBusiness/MedicalClinic node implies on-site care at that address, which contradicts the disclaimer and is a YMYL trust risk. Carry the address only inside a `PostalAddress` on the `#place`/Organization node (it's the business mailing address), not as a LocalBusiness that claims to deliver treatment.

`MedicalOrganization` carries topical authority via `knowsAbout` — positioned as a referral/information network, **not** a treatment provider. Never imply the site delivers care directly. (`Article.author`/`publisher` = Organization.)

> Ranking note to surface to the user when relevant: a named credentialed medical reviewer (Person → `reviewedBy` on the Article/WebPage) is a strong YMYL trust signal. If the page displays a reviewer byline (wordpress.md outputs one), ADD it to schema — don't leave this lever unused. Use a real name + credential; never fabricate one.

## Validity rules (prevent Rich Results errors)
- `medicalSpecialty` must use real schema.org `MedicalSpecialty` enum values. **Valid:** `Psychiatric`. Do NOT use "AddictionMedicine", "MentalHealth", "BehavioralHealth" — not in the enum; they throw warnings. Put those concepts in `knowsAbout` (free text) instead.
- No `aggregateRating`, `review`, or `Review` nodes — no review data exists; fabricating it is a policy violation.
- No recovery guarantees, no diagnosis language anywhere in text values.
- Avoid `Offer`/`price` on the Service node (a price:0 on treatment-adjacent service reads as "free treatment"). Describe the service without a priced Offer.
- FAQ answers: medically cautious, encourage emergency care where relevant, no diagnosis.
- All URLs absolute and real; only link pages that exist (cross-check url.md — link only Status ✅ slugs).
- `inLanguage`: "en-US". Phone: "+1-888-325-2454".

## FAQ rich-result caveat (set expectations)
Google restricts FAQ rich results to recognized authoritative health/gov sites (since 2023). Keep FAQPage markup regardless — Bing and AI engines (ChatGPT/Gemini/Perplexity) still parse it, and the site may qualify as health-authority — but don't promise FAQ star features in the SERP.

## Stable @IDs (site-level constant, page-level templated)
Site: `#organization`, `#medicalorganization`, `#website`, `#place`, `#contact`
Page: `{URL}#webpage`, `{URL}#article`, `{URL}#faq`, `{URL}#service`, `{URL}#breadcrumb`, `{URL}#terms`
Topic Things: `{URL}#primary-topic`, plus `#medical-detox`, `#addiction-treatment`, `#couples-rehab`, `#withdrawal`, `#behavioral-health` (customize to page).

## Site-level constants (couplesrehabs.org)
- name: "Couples Rehabs" (alternateName: "CouplesRehabs.org" / "Couple Rehabs")
- url: "https://couplesrehabs.org/"
- telephone: "+1-888-325-2454"
- logo: "https://couplesrehabs.org/wp-content/uploads/2018/07/logo-1-e1502764175400.png"
- address: 4231 Balboa Avenue #1125, San Diego, CA 92117, US (PostalAddress on #place only)
- foundingDate / copyright span: site active since 2016
- sameAs: ["https://www.facebook.com/CouplesRehab"] (only confirmed profile; add others only if verified real)

## @graph node checklist
1. **Organization** `#organization` — name, alternateName, url, telephone, logo (ImageObject), address (PostalAddress, real San Diego address), contactPoint ref, foundingDate, sameAs (real profiles only — omit placeholders if unknown).
2. **MedicalOrganization** `#medicalorganization` — referral/info network; `medicalSpecialty: ["Psychiatric"]`; `knowsAbout: [...]` full topic list; `areaServed` US; do not mark as treatment provider.
3. **ContactPoint** `#contact` — telephone "+1-888-325-2454", contactType "customer service", areaServed US, availableLanguage English, available 24/7 if stated.
4. **Place** `#place` — PostalAddress with the real San Diego address (streetAddress, addressLocality "San Diego", addressRegion "CA", postalCode "92117", addressCountry "US"). Do NOT add LocalBusiness typing.
5. **WebSite** `#website` — publisher → Organization; SearchAction potentialAction.
6. **WebPage** `{URL}#webpage` — isPartOf website; publisher → Organization; about → #primary-topic; mainEntity → article/faq/service; mentions → topic Things; significantLink → real internal links from the map (✅ slugs only); inLanguage. Add `reviewedBy` → Person if the page shows a reviewer.
7. **Article** (or **MedicalWebPage** where appropriate) `{URL}#article` — headline (H1), description (meta), author + publisher → Organization, mainEntityOfPage → webpage, datePublished/dateModified, articleSection, keywords, wordCount, inLanguage. Add `reviewedBy` → Person if a byline exists.
8. **Service** `{URL}#service` — page-specific name (detox→"Medical Detox Placement & Withdrawal Guidance"; couples→"Couples Addiction Treatment Navigation"; withdrawal→"Withdrawal Education & Detox Guidance"; insurance→"Insurance Verification & Treatment Navigation"; geo→"Couples Rehab Placement — [State]"); provider → MedicalOrganization; areaServed US (or the state for geo pages); audience; serviceOutput list; NO priced Offer.
9. **BreadcrumbList** `{URL}#breadcrumb` — Home › [pillar by page type] › [Page]. Use real pillar/state-hub URLs from url.md. Default pillar for treatment/education pages: `/substance-abuse-treatments/`. Geo city pages: Home › [State hub] › [City]. Only use ✅ URLs.
10. **FAQPage** `{URL}#faq` — 8–12 Question/acceptedAnswer pairs, pulled from the page's actual FAQ; medically cautious.
11. **DefinedTermSet** `{URL}#terms` + **DefinedTerm** children — the page's clinical entities (medical detox, withdrawal, dual diagnosis, MAT, CIWA-Ar, COWS, behavioral couples therapy, codependency, etc.) as a glossary set.
12. **Thing** entities — `#primary-topic` + the mentioned topic Things, each with name + description, referenced by WebPage about/mentions.

## Cross-checks before output
- Page type matches breadcrumb pillar and Service name.
- Every significantLink/breadcrumb URL exists in url.md and is Status ✅ (never link ⬜ planned pages).
- Phone is +1-888-325-2454 everywhere (not 888-325-2454 unprefixed, not any other number).
- No LocalBusiness/MedicalClinic, no ratings, no priced treatment offer, no invalid medicalSpecialty.
- Address only on #place/Organization PostalAddress — never as a care-delivery location.
- Dates, word count, keywords filled (not left as placeholders).
- If the page byline shows a medical reviewer, reviewedBy Person is included with a real credential.
- Valid JSON (no trailing commas), single graph, single script tag.
