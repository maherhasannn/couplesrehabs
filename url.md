---
name: url.md
description: read on demand. URL inventory and site architecture for couplesrehabs.org — slug, page type, cluster, parent/pillar, geo, target keyword, and CTA mode for every existing and planned page. Look up a slug here before writing to get its structure, internal links, and conversion action. Costs zero tokens until needed.
---

# couplesrehabs.org URL Map

## Site model (read first)

CouplesRehabs.org presents as a national couples addiction treatment **placement and referral network** (online since 2016, San Diego–based front address: 4231 Balboa Avenue #1125, San Diego, CA 92117). Active voice: "we," "our placement team," "we verify benefits," "we coordinate admission," "available 24/7." It coordinates admission into licensed providers nationwide but **is not itself a treatment facility** (per the site's own treatment-referral disclaimer).

**The only conversion goal: drive phone calls to 888-325-2454.** "Take the couples assessment" / "request a confidential consultation" is the secondary CTA. Canonical model/depth reference: the long-form city geo pages (e.g. `/couples-rehab-monroe-new-york/`, `/couples-rehab-seattle-washington/`).

## Hard rules for every page (protects rankings + the call)

- Keep the **"referral & information service, not a treatment facility"** disclosure in the opening and the editorial/treatment disclaimer — this is what makes the active voice defensible. Never write "our facility admits," "our San Diego center," or claim to deliver treatment, detox, or therapy directly. We *connect* couples to vetted licensed providers.
- Never guarantee coverage outcomes, in-network status, out-of-pocket figures, or a specific same-room / joint-placement configuration. Joint placement / same room = "regularly available, never guaranteed ahead of time"; coverage = "verified before any commitment."
- Disclose the financial relationship where natural: we may be compensated by treatment providers for referrals; this does not affect the caller's cost of or access to care.
- CTA language: "Call 888-325-2454," "call a confidential care navigator," "begin the placement process," "verify your benefits," "request a confidential consultation." Keep the urgency.
- Every page touching overdose, detox, or severe withdrawal shows: **call 911 for danger; call or text 988 for crisis** (plus any state crisis line). Crisis blockquote near top AND at close.
- Match the depth and page furniture of the strong geo pages (byline/author, crisis blockquotes, mid-page CTA banners, benefit lists, FAQ block, trusted-sources list linking out to .gov authorities like SAMHSA / CDC / NIDA, editorial + treatment-referral disclaimer).

## Real site pillars / nav (existing — link up to these)

Top nav and confirmed existing pages:
- `/` (home) ✅
- `/about-us/` ✅
- `/substance-abuse-treatments/` (pillar: Substance Abuse Treatment) ✅
  - `/alcohol-addiction-treatment/` ✅
  - `/alcohol-treatment-for-couples/` ✅
  - `/couples-drug-rehab-california/` ✅
  - `/relapse-prevention/` ✅
  - `/couples-drug-treatment/` ✅
- `/news/` (blog index) ✅
- `/contact-us/` ✅
- `/privacy-policy/` ✅
- `/terms-of-service/` ✅

> NOTE: pillars on this site are currently thin. Part of the build job is to strengthen them into real hub pages and route the geo + topic clusters up to them. When in doubt, parent education/topic pages to `/substance-abuse-treatments/` and geo pages to their state hub.

## Page types (each = a different article template)

| Type | Intent | Length | CTA weight | Notes |
|---|---|---|---|---|
| education | informational, top-of-funnel | 1,500–3,000 | light, mid + end | symptom/timeline/explainer pages; build trust, link down-funnel |
| emergency-intent | crisis, "now / near me / same-day" | 800–1,500 | heavy, top + repeated | short, reassuring, call-first; 911/988 prominent |
| insurance | coverage / verification | 1,200–2,500 | medium, verification-focused | carrier-specific; route to free benefits check via call |
| geo-city | local landing page (city) | 1,200–2,500 | medium-heavy | city specifics; "providers serving [city]," never "our [city] facility" |
| geo-state | state hub landing page | 1,500–3,000 | medium-heavy | state overview + links down to its cities; parent for that state's geo-city pages |
| couples | relationship angle on any topic | 1,500–3,000 | medium | layer codependency / joint-recovery / boundaries onto base topic |
| comparison/process | "X vs Y," "what happens in" | 1,200–2,500 | light-medium | explainer; strong internal linking |
| news/blog | editorial post under /news/ | 800–1,800 | light | top-of-funnel, links into pillars + geo |

## CTA modes

- **call-primary:** phone CTA above the fold + repeated; assessment/consultation secondary. (emergency-intent, geo-city, geo-state, insurance)
- **assessment-primary:** consultation/assessment CTA leads, call secondary. (education, comparison, top-of-funnel couples, news)
- Both always include **(888) 325-2454**.

## How to use this map (instruction for the writing skill)

When given a slug or topic:

1. Find its row below (or the closest cluster if it's a new topic).
2. Use **page type** to select the article template/structure.
3. Use **parent/pillar + cluster** to build internal links — always link up to the parent pillar/state hub, sideways to 2–3 cluster siblings, and to `/contact-us/` + the crisis disclosure.
4. Use **CTA mode** to set conversion action (always the call to 888-325-2454).
5. Use **target keyword** as the primary; add natural variations.
6. **FIND A SLUG THAT HASN'T BEEN BUILT** (Status not ✅) and after publishing a page mark its Status ✅.

---

## URL inventory

Status legend: ✅ = confirmed live / built · ⬜ = planned, not yet built.

### Core / structural

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ✅ | `/` | home | core | — | couples rehab | call-primary |
| ✅ | `/about-us/` | core | core | `/` | about couples rehabs | assessment-primary |
| ✅ | `/contact-us/` | core | core | `/` | contact couples rehab | call-primary |
| ✅ | `/news/` | news index | news | `/` | couples rehab news | assessment-primary |
| ✅ | `/privacy-policy/` | core | legal | `/` | — | none |
| ✅ | `/terms-of-service/` | core | legal | `/` | — | none |
| ⬜ | `/how-it-works/` | process | core | `/` | how couples rehab placement works | assessment-primary |
| ⬜ | `/couples-assessment/` | process | core | `/` | couples addiction assessment | call-primary |
| ⬜ | `/insurance-verification/` | insurance | insurance | `/` | verify couples rehab insurance | call-primary |
| ⬜ | `/crisis-support/` | emergency-intent | core | `/` | addiction crisis support couples | call-primary |

### Pillar: Substance Abuse Treatment

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ✅ | `/substance-abuse-treatments/` | education (pillar) | treatment | `/` | couples substance abuse treatment | assessment-primary |
| ✅ | `/couples-drug-treatment/` | education | treatment | `/substance-abuse-treatments/` | couples drug treatment | assessment-primary |
| ✅ | `/alcohol-addiction-treatment/` | education | treatment | `/substance-abuse-treatments/` | alcohol addiction treatment | assessment-primary |
| ✅ | `/alcohol-treatment-for-couples/` | couples | treatment | `/substance-abuse-treatments/` | alcohol treatment for couples | assessment-primary |
| ✅ | `/couples-drug-rehab-california/` | geo-state | treatment | `/substance-abuse-treatments/` | couples drug rehab california | call-primary |
| ✅ | `/relapse-prevention/` | education | treatment | `/substance-abuse-treatments/` | relapse prevention couples | assessment-primary |

### Levels of care (planned cluster, parent `/substance-abuse-treatments/`)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ⬜ | `/couples-detox/` | education | levels-of-care | `/substance-abuse-treatments/` | couples detox | call-primary |
| ⬜ | `/couples-inpatient-rehab/` | education | levels-of-care | `/substance-abuse-treatments/` | couples inpatient rehab | call-primary |
| ⬜ | `/couples-residential-treatment/` | education | levels-of-care | `/substance-abuse-treatments/` | couples residential treatment | call-primary |
| ⬜ | `/couples-outpatient-rehab/` | education | levels-of-care | `/substance-abuse-treatments/` | couples outpatient rehab | assessment-primary |
| ⬜ | `/couples-iop/` | education | levels-of-care | `/substance-abuse-treatments/` | couples intensive outpatient program | assessment-primary |
| ⬜ | `/couples-php/` | education | levels-of-care | `/substance-abuse-treatments/` | couples partial hospitalization program | assessment-primary |
| ⬜ | `/couples-aftercare-programs/` | education | levels-of-care | `/substance-abuse-treatments/` | couples aftercare program | assessment-primary |
| ⬜ | `/couples-sober-living/` | education | levels-of-care | `/substance-abuse-treatments/` | couples sober living | assessment-primary |

### Substance-specific (planned cluster, parent `/substance-abuse-treatments/`)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ⬜ | `/fentanyl-rehab-for-couples/` | couples | substance-specific | `/substance-abuse-treatments/` | fentanyl rehab for couples | call-primary |
| ⬜ | `/heroin-rehab-for-couples/` | couples | substance-specific | `/substance-abuse-treatments/` | heroin rehab for couples | call-primary |
| ⬜ | `/opioid-rehab-for-couples/` | couples | substance-specific | `/substance-abuse-treatments/` | opioid rehab for couples | call-primary |
| ⬜ | `/meth-rehab-for-couples/` | couples | substance-specific | `/substance-abuse-treatments/` | meth rehab for couples | call-primary |
| ⬜ | `/cocaine-rehab-for-couples/` | couples | substance-specific | `/substance-abuse-treatments/` | cocaine rehab for couples | call-primary |
| ⬜ | `/benzo-rehab-for-couples/` | couples | substance-specific | `/substance-abuse-treatments/` | benzodiazepine rehab for couples | call-primary |
| ⬜ | `/prescription-drug-rehab-for-couples/` | couples | substance-specific | `/substance-abuse-treatments/` | prescription drug rehab for couples | call-primary |
| ⬜ | `/suboxone-treatment-for-couples/` | education | substance-specific | `/substance-abuse-treatments/` | suboxone treatment couples | assessment-primary |
| ⬜ | `/medication-assisted-treatment-couples/` | education | substance-specific | `/substance-abuse-treatments/` | medication assisted treatment couples | assessment-primary |

### Mental health / dual diagnosis (planned cluster)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ⬜ | `/dual-diagnosis-treatment-couples/` | education | mental-health | `/substance-abuse-treatments/` | dual diagnosis treatment couples | assessment-primary |
| ⬜ | `/couples-mental-health-treatment/` | education | mental-health | `/substance-abuse-treatments/` | couples mental health treatment | assessment-primary |
| ⬜ | `/couples-rehab-anxiety-depression/` | couples | mental-health | `/substance-abuse-treatments/` | couples rehab anxiety depression | assessment-primary |
| ⬜ | `/trauma-therapy-for-couples/` | education | mental-health | `/substance-abuse-treatments/` | trauma therapy for couples | assessment-primary |
| ⬜ | `/ptsd-treatment-for-couples/` | couples | mental-health | `/substance-abuse-treatments/` | ptsd treatment for couples | assessment-primary |
| ⬜ | `/codependency-treatment-couples/` | couples | mental-health | `/substance-abuse-treatments/` | codependency treatment couples | assessment-primary |

### Therapy / relationship modalities (planned cluster)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ⬜ | `/behavioral-couples-therapy/` | education | therapy | `/substance-abuse-treatments/` | behavioral couples therapy | assessment-primary |
| ⬜ | `/marriage-counseling-addiction/` | couples | therapy | `/substance-abuse-treatments/` | marriage counseling during addiction | assessment-primary |
| ⬜ | `/couples-therapy-during-rehab/` | couples | therapy | `/substance-abuse-treatments/` | couples therapy during rehab | assessment-primary |
| ⬜ | `/online-couples-therapy/` | education | therapy | `/substance-abuse-treatments/` | online couples therapy | assessment-primary |
| ⬜ | `/virtual-couples-rehab/` | education | therapy | `/substance-abuse-treatments/` | virtual couples rehab | assessment-primary |
| ⬜ | `/couples-intervention-services/` | couples | therapy | `/substance-abuse-treatments/` | couples intervention services | call-primary |

### Emergency-intent (planned cluster, parent `/`)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ⬜ | `/couples-rehab-near-me/` | emergency-intent | emergency | `/` | couples rehab near me | call-primary |
| ⬜ | `/same-day-couples-rehab/` | emergency-intent | emergency | `/` | same day couples rehab | call-primary |
| ⬜ | `/24-hour-couples-rehab-helpline/` | emergency-intent | emergency | `/` | 24 hour couples rehab helpline | call-primary |
| ⬜ | `/emergency-couples-detox/` | emergency-intent | emergency | `/` | emergency couples detox | call-primary |

### Insurance (planned cluster, parent `/insurance-verification/`)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ⬜ | `/couples-rehab-that-accepts-insurance/` | insurance | insurance | `/insurance-verification/` | couples rehab that accepts insurance | call-primary |
| ⬜ | `/ppo-couples-rehab/` | insurance | insurance | `/insurance-verification/` | ppo couples rehab | call-primary |
| ⬜ | `/blue-cross-blue-shield-couples-rehab/` | insurance | insurance | `/insurance-verification/` | bcbs couples rehab | call-primary |
| ⬜ | `/anthem-couples-rehab/` | insurance | insurance | `/insurance-verification/` | anthem couples rehab | call-primary |
| ⬜ | `/aetna-couples-rehab/` | insurance | insurance | `/insurance-verification/` | aetna couples rehab | call-primary |
| ⬜ | `/cigna-couples-rehab/` | insurance | insurance | `/insurance-verification/` | cigna couples rehab | call-primary |
| ⬜ | `/united-healthcare-couples-rehab/` | insurance | insurance | `/insurance-verification/` | united healthcare couples rehab | call-primary |
| ⬜ | `/tricare-couples-rehab/` | insurance | insurance | `/insurance-verification/` | tricare couples rehab | call-primary |

### Decision / informational (planned cluster, parent `/substance-abuse-treatments/`)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ⬜ | `/can-couples-go-to-rehab-together/` | comparison/process | informational | `/substance-abuse-treatments/` | can couples go to rehab together | assessment-primary |
| ⬜ | `/can-couples-share-a-room-in-rehab/` | comparison/process | informational | `/substance-abuse-treatments/` | can couples share a room in rehab | assessment-primary |
| ⬜ | `/does-couples-rehab-work/` | comparison/process | informational | `/substance-abuse-treatments/` | does couples rehab work | assessment-primary |
| ⬜ | `/what-happens-in-couples-rehab/` | comparison/process | informational | `/substance-abuse-treatments/` | what happens in couples rehab | assessment-primary |
| ⬜ | `/how-much-does-couples-rehab-cost/` | comparison/process | informational | `/substance-abuse-treatments/` | how much does couples rehab cost | assessment-primary |
| ⬜ | `/how-long-is-couples-rehab/` | comparison/process | informational | `/substance-abuse-treatments/` | how long is couples rehab | assessment-primary |
| ⬜ | `/couples-rehab-vs-individual-rehab/` | comparison/process | informational | `/substance-abuse-treatments/` | couples rehab vs individual rehab | assessment-primary |
| ⬜ | `/my-husband-is-addicted-to-drugs/` | couples | informational | `/substance-abuse-treatments/` | my husband is addicted to drugs | call-primary |
| ⬜ | `/my-wife-is-an-alcoholic/` | couples | informational | `/substance-abuse-treatments/` | my wife is an alcoholic | call-primary |
| ⬜ | `/how-to-convince-partner-to-go-to-rehab/` | couples | informational | `/substance-abuse-treatments/` | convince partner to go to rehab | call-primary |
| ⬜ | `/signs-your-relationship-needs-rehab/` | couples | informational | `/substance-abuse-treatments/` | signs your relationship needs rehab | assessment-primary |

### Specialty programs (planned cluster, parent `/substance-abuse-treatments/`)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ⬜ | `/luxury-couples-rehab/` | education | specialty | `/substance-abuse-treatments/` | luxury couples rehab | call-primary |
| ⬜ | `/executive-couples-rehab/` | education | specialty | `/substance-abuse-treatments/` | executive couples rehab | call-primary |
| ⬜ | `/lgbtq-couples-rehab/` | couples | specialty | `/substance-abuse-treatments/` | lgbtq couples rehab | assessment-primary |
| ⬜ | `/christian-couples-rehab/` | couples | specialty | `/substance-abuse-treatments/` | christian couples rehab | assessment-primary |
| ⬜ | `/holistic-couples-rehab/` | education | specialty | `/substance-abuse-treatments/` | holistic couples rehab | assessment-primary |
| ⬜ | `/pet-friendly-couples-rehab/` | education | specialty | `/substance-abuse-treatments/` | pet friendly couples rehab | assessment-primary |
| ⬜ | `/rehab-for-couples-with-children/` | couples | specialty | `/substance-abuse-treatments/` | rehab for couples with children | call-primary |

### Geo — STATE hubs (planned cluster, parent `/`)

State hubs parent their own cities. `/couples-drug-rehab-california/` already exists and acts as the CA hub.

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ✅ | `/couples-drug-rehab-california/` | geo-state | geo-CA | `/substance-abuse-treatments/` | couples drug rehab california | call-primary |
| ✅ | `/couples-rehab-north-carolina/` | geo-state | geo-NC | `/` | couples rehab north carolina | call-primary |
| ⬜ | `/couples-rehab-arizona/` | geo-state | geo-AZ | `/` | couples rehab arizona | call-primary |
| ⬜ | `/couples-rehab-texas/` | geo-state | geo-TX | `/` | couples rehab texas | call-primary |
| ⬜ | `/couples-rehab-florida/` | geo-state | geo-FL | `/` | couples rehab florida | call-primary |
| ⬜ | `/couples-rehab-new-york/` | geo-state | geo-NY | `/` | couples rehab new york | call-primary |
| ⬜ | `/couples-rehab-washington/` | geo-state | geo-WA | `/` | couples rehab washington state | call-primary |
| ⬜ | `/couples-rehab-nevada/` | geo-state | geo-NV | `/` | couples rehab nevada | call-primary |
| ⬜ | `/couples-rehab-colorado/` | geo-state | geo-CO | `/` | couples rehab colorado | call-primary |
| ⬜ | `/couples-rehab-georgia/` | geo-state | geo-GA | `/` | couples rehab georgia | call-primary |
| ⬜ | `/couples-rehab-new-jersey/` | geo-state | geo-NJ | `/` | couples rehab new jersey | call-primary |
| ⬜ | `/couples-rehab-pennsylvania/` | geo-state | geo-PA | `/` | couples rehab pennsylvania | call-primary |
| ⬜ | `/couples-rehab-ohio/` | geo-state | geo-OH | `/` | couples rehab ohio | call-primary |
| ⬜ | `/couples-rehab-illinois/` | geo-state | geo-IL | `/` | couples rehab illinois | call-primary |
| ⬜ | `/couples-rehab-massachusetts/` | geo-state | geo-MA | `/` | couples rehab massachusetts | call-primary |

### Geo — CITY pages (existing + planned)

City pages parent up to their state hub. Format: `/couples-rehab-{city}-{state}/`.

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ✅ | `/couples-rehab-programs-san-diego/` | geo-city | geo-CA | `/couples-drug-rehab-california/` | couples rehab san diego | call-primary |
| ✅ | `/couples-rehab-seattle-washington/` | geo-city | geo-WA | `/couples-rehab-washington/` | couples rehab seattle | call-primary |
| ✅ | `/couples-rehab-washington-d-c/` | geo-city | geo-DC | `/` | couples rehab washington dc | call-primary |
| ✅ | `/couples-rehab-monroe-new-york/` | geo-city | geo-NY | `/couples-rehab-new-york/` | couples rehab monroe ny | call-primary |
| ⬜ | `/couples-rehab-los-angeles-california/` | geo-city | geo-CA | `/couples-drug-rehab-california/` | couples rehab los angeles | call-primary |
| ⬜ | `/couples-rehab-orange-county-california/` | geo-city | geo-CA | `/couples-drug-rehab-california/` | couples rehab orange county | call-primary |
| ⬜ | `/couples-rehab-san-francisco-california/` | geo-city | geo-CA | `/couples-drug-rehab-california/` | couples rehab san francisco | call-primary |
| ⬜ | `/couples-rehab-sacramento-california/` | geo-city | geo-CA | `/couples-drug-rehab-california/` | couples rehab sacramento | call-primary |
| ⬜ | `/couples-rehab-riverside-california/` | geo-city | geo-CA | `/couples-drug-rehab-california/` | couples rehab riverside | call-primary |
| ⬜ | `/couples-rehab-phoenix-arizona/` | geo-city | geo-AZ | `/couples-rehab-arizona/` | couples rehab phoenix | call-primary |
| ⬜ | `/couples-rehab-scottsdale-arizona/` | geo-city | geo-AZ | `/couples-rehab-arizona/` | couples rehab scottsdale | call-primary |
| ⬜ | `/couples-rehab-houston-texas/` | geo-city | geo-TX | `/couples-rehab-texas/` | couples rehab houston | call-primary |
| ⬜ | `/couples-rehab-dallas-texas/` | geo-city | geo-TX | `/couples-rehab-texas/` | couples rehab dallas | call-primary |
| ⬜ | `/couples-rehab-austin-texas/` | geo-city | geo-TX | `/couples-rehab-texas/` | couples rehab austin | call-primary |
| ⬜ | `/couples-rehab-miami-florida/` | geo-city | geo-FL | `/couples-rehab-florida/` | couples rehab miami | call-primary |
| ⬜ | `/couples-rehab-tampa-florida/` | geo-city | geo-FL | `/couples-rehab-florida/` | couples rehab tampa | call-primary |
| ⬜ | `/couples-rehab-orlando-florida/` | geo-city | geo-FL | `/couples-rehab-florida/` | couples rehab orlando | call-primary |
| ⬜ | `/couples-rehab-new-york-city-new-york/` | geo-city | geo-NY | `/couples-rehab-new-york/` | couples rehab nyc | call-primary |
| ⬜ | `/couples-rehab-seattle-washington-state/` | geo-city | geo-WA | `/couples-rehab-washington/` | couples rehab seattle wa | call-primary |
| ⬜ | `/couples-rehab-denver-colorado/` | geo-city | geo-CO | `/couples-rehab-colorado/` | couples rehab denver | call-primary |
| ⬜ | `/couples-rehab-las-vegas-nevada/` | geo-city | geo-NV | `/couples-rehab-nevada/` | couples rehab las vegas | call-primary |
| ⬜ | `/couples-rehab-atlanta-georgia/` | geo-city | geo-GA | `/couples-rehab-georgia/` | couples rehab atlanta | call-primary |

### News / blog (existing posts under /news/ — link into pillars + geo)

| Status | Slug | Page type | Cluster | Parent/Pillar | Target keyword | CTA mode |
|---|---|---|---|---|---|---|
| ✅ | `/what-role-does-family-communication-play-during-addiction-treatment/` | news/blog | news | `/news/` | family communication addiction treatment | assessment-primary |
| ✅ | `/how-suboxone-treatment-programs-in-west-virginia-coordinate-with-primary-care-providers/` | news/blog | news | `/news/` | suboxone west virginia primary care | assessment-primary |
| ✅ | `/couples-rehab-programs-san-diego/` | news/blog | news | `/news/` | couples rehab programs san diego | call-primary |
| ✅ | `/why-affordable-luxury-rehab-works-better/` | news/blog | news | `/news/` | affordable luxury rehab | assessment-primary |
| ✅ | `/outpatient-anxiety-programs-san-diego/` | news/blog | news | `/news/` | outpatient anxiety programs san diego | assessment-primary |
| ✅ | `/virtual-couples-therapy-san-diego-ca/` | news/blog | news | `/news/` | virtual couples therapy san diego | assessment-primary |

---

## Notes / open questions for the operator

- **Pillar thinness:** the four nav sub-items are the only declared "Other Services." Recommend promoting `/substance-abuse-treatments/` into a true hub and building the levels-of-care + substance-specific clusters under it before scaling geo.
- **Geo slug inconsistency:** existing geo pages mix formats (`/couples-rehab-programs-san-diego/` vs `/couples-rehab-seattle-washington/` vs `/couples-rehab-washington-d-c/`). New city pages standardize on `/couples-rehab-{city}-{state}/`. Don't duplicate San Diego — it already exists as `/couples-rehab-programs-san-diego/`.
- **Phone discrepancy:** site footer email reads `info@89n.245.myftpupload.com` (likely a staging artifact). Always use **888-325-2454** for the call CTA; flag the footer email to fix.
- **Verify before mass-building geo:** confirm the full set of already-published city/state pages via the live sitemap so new slugs don't collide. Statuses above marked ✅ are confirmed from search/fetch; treat unlisted cities as ⬜ but spot-check.
