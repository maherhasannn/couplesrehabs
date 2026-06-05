# Couples Rehabs — Claude Code Instructions

## Project overview

This repo powers content operations for [couplesrehabs.org](https://couplesrehabs.org) — a national couples addiction treatment placement and referral network specializing in couples detox, couples rehab, medical detox, withdrawal care, dual diagnosis, insurance-supported treatment, and emergency placement. Online since 2016. The site runs on WordPress.

All content targets people in crisis: panicking spouses/parents, couples deciding to get help together, someone in active withdrawal, and high-intent searchers who need help today. Every article is written for one conversion goal — phone calls to **(888) 325-2454** — with the couples assessment / confidential consultation as the secondary CTA.

**Positioning guardrail (non-negotiable):** CouplesRehabs.org is a referral & information service / placement network, **not a treatment facility**. It does not own, operate, or manage any rehab, detox center, or clinic. The active voice ("we verify benefits," "we coordinate admission," "available 24/7") is defensible only when paired with that disclosure and with no guarantees on coverage or joint placement. Where natural, disclose the financial relationship: we may be compensated by treatment providers for referrals; this does not affect the caller's cost of or access to care. This framing must hold across every article and the schema.

Canonical model pages for structure, depth, and voice: the deepest live geo pages, e.g. `https://couplesrehabs.org/couples-rehab-monroe-new-york/` and `https://couplesrehabs.org/couples-rehab-seattle-washington/`. As pillar pages are strengthened, prefer the most complete published example for the relevant page type.

---

## Environment

WordPress credentials are loaded automatically from `.env` at session start via the SessionStart hook. They are available as environment variables:

- `WP_USERNAME` — WordPress admin username
- `WP_APP_PASSWORD` — WordPress application password
- `WP_API_ENDPOINT` — `https://couplesrehabs.org/wp-json/wp/v2/posts`  *(confirm — WP default assumed)*

If credentials are missing, run the session-start hook manually:
```bash
CLAUDE_CODE_REMOTE=true CLAUDE_PROJECT_DIR=$(pwd) CLAUDE_ENV_FILE=/tmp/claude-env bash .claude/hooks/session-start.sh
```

---

## Available skills

Three custom skills are installed automatically at session start:

| Skill | File | Purpose |
|---|---|---|
| URL map | `url.md` | Canonical URL map — slug inventory across all clusters (levels of care, substance-specific, mental health/dual diagnosis, therapy modalities, emergency intent, insurance, informational, specialty, geo state hubs, geo cities, news). Tracks build status (✅ live / ⬜ planned). Always pull slugs, page type, parent pillar/state hub, geo, keyword, and CTA mode from here. |
| Article engine | `wordpress.md` | Full article engine — deep-clinical 4,000–6,000+ words, 3 embedded CTA boxes (top/middle/end), 15–25 FAQs, comparison table, crisis blockquotes, medically-reviewed byline, trusted-sources list, editorial + treatment-referral disclaimer. |
| Schema | `schema.md` | Generates the JSON-LD `<script>` block. Requires the article content as input. |

---

## Full content + posting routine

Follow these steps in order every time a new draft is created.

### Step 1 — Pick a slug with `url.md`

Read `url.md` to review the canonical page map. Either:
- Pick a planned slug (Status ⬜) that hasn't been built yet, or
- Identify the right cluster and mint a new slug following that cluster's naming convention

The map gives the slug its **page type** (education / emergency-intent / insurance / geo-city / geo-state / couples / comparison-process / news), **cluster + parent pillar or state hub** (drives internal linking), **geo**, **target keyword**, and **CTA mode** (call-primary or assessment-primary). The slug drives the page URL and all internal linking. Never invent a slug without checking here first. Do not pick a slug already marked ✅ — those are live; avoid duplicates (note San Diego already exists as `/couples-rehab-programs-san-diego/`).

### Step 2 — Write the article with `wordpress.md`

Follow `wordpress.md` with the chosen slug/topic. It will produce:

- Deep-clinical 4,000–6,000+ word article in WordPress Gutenberg block HTML (emergency-intent pages run shorter — see map)
- Clinical depth: named assessment scales (CIWA-Ar, COWS), hour/day withdrawal timelines, specific medication classes, substance-by-substance danger gradients
- 3 embedded CTA boxes, contextually rewritten per page (Box 1 dark navy hero + phone; Box 2 white clinical-assessment card + pillar/insurance links; Box 3 light continuum card + next-stage link)
- Medically-reviewed byline + top and closing crisis blockquotes (911 / 988 / state crisis line + 888 number)
- 15–25 FAQ entries formatted for AI Overview extraction
- At least one comparison table (inpatient vs outpatient, or detox vs rehab)
- Internal links using only confirmed ✅ slugs from `url.md` (up to parent pillar/state hub, sideways to cluster siblings + neighboring geo, plus contact + crisis support). Do not link to planned ⬜ pages — they 404.
- External links to authoritative sources only: SAMHSA, NIDA, CDC, NIH, NIAAA, state behavioral-health department, 988 Lifeline
- Editorial disclaimer ("referral & information service, not a treatment facility" + financial-relationship disclosure) + full deliverables block at the end (SEO title, meta, slug, H1, internal link map, etc.)

**Before moving to Step 3:** Verify every link in the article — internal and external — returns a valid response. Confirm no `[BRACKETED PLACEHOLDER]` text survives in the CTA boxes (topic, geo, headlines, hrefs all customized to this page). Do not skip this check.

### Step 3 — Generate schema with `schema.md`

Follow `schema.md` and pass:
1. The full page URL (`https://couplesrehabs.org/<slug>/`)
2. The complete article content from Step 2

The skill outputs a single `<script type="application/ld+json">` block — ready to paste into WordPress as a Custom HTML block at the bottom of the post content.

The schema includes: `Organization`, `MedicalOrganization` (referral/info network, **not** treatment provider; `knowsAbout` topics, `medicalSpecialty: ["Psychiatric"]` only — no invalid enum values), `ContactPoint`, `Place` (PostalAddress only — see address note), `WebSite`, `WebPage`, `Article` (+ `reviewedBy` Person if the page shows a reviewer byline), `FAQPage`, `Service` (no priced Offer), `BreadcrumbList`, `DefinedTermSet`, and relevant `DefinedTerm` / `Thing` entities for the page's cluster.

**Do NOT include `LocalBusiness`** — although the site publishes a San Diego mailing address, the brand is a national referral network, not a treatment storefront; a LocalBusiness/MedicalClinic node would imply on-site care and contradict the disclaimer (YMYL risk). Carry the address only inside the Organization/`#place` `PostalAddress`. No `aggregateRating` or review nodes.

**The schema skill will refuse to generate if:**
- No FAQ section exists in the article
- Any link hasn't been verified against the valid-links reference / `url.md` ✅ slugs

### Step 4 — Final link check

Before posting, confirm:
- [ ] All internal links resolve to real, live couplesrehabs.org pages (Status ✅ in `url.md`)
- [ ] All external links return HTTP 200
- [ ] No bracketed placeholder text survives in the CTAs (`[EMOTIONAL HOOK HEADLINE]`, `[CLUSTER PILLAR URL]`, `[NEXT-STAGE URL]`, etc.)
- [ ] Phone links point to `tel:8883252454` (displayed "(888) 325-2454") — keep displayed number and tel: target identical
- [ ] Schema JSON is valid (no trailing commas, all brackets matched)

### Step 5 — Post to WordPress

Post the draft using the WordPress REST API:

```bash
python3 post_draft.py
```

The script reads credentials from `.env`, posts to `https://couplesrehabs.org/wp-json/wp/v2/posts` with `status: draft`, and prints the post ID and preview URL on success.

**The content field must include:**
1. The full Gutenberg block HTML from Step 2 (with the 3 CTA boxes already embedded)
2. The `<script type="application/ld+json">` block from Step 3 appended as a `<!-- wp:html -->` block at the bottom

**On success:** Log the post ID. The draft is live in WordPress and ready for review before publishing.

---

## Content standards

- Voice: senior addiction-medicine-literate placement specialist speaking to a panicking partner — specific, calm, clinically credible, never sensational
- Active placement-network voice ("we verify benefits," "we coordinate admission," "24/7") — always paired with the "not a treatment facility" disclosure
- Every section opens with a 2–3 sentence direct answer (AI Overview ready)
- Deep clinical register required — named scales, timelines, medications, substance-specific danger gradients (see `wordpress.md`)
- No unsupported guarantees, no "best" or "top rated" as ranked claims, no recovery/outcome promises
- Medical framing: "can," "may," "in many cases," "depending on the facility/plan" — never "will" or "guaranteed"
- Coverage + joint placement (incl. same-room) always framed as verified/assessed, never guaranteed ahead of time
- 911 / 988 callouts wherever overdose or severe withdrawal is discussed
- Word count: 4,000–6,000+ words per geo/pillar article (emergency-intent pages shorter)
- CTAs: 3 per article, all contextually rewritten — no generic copy, no surviving placeholders

## NAP / brand constants (never change)

- **Name:** Couples Rehabs (alternateName: CouplesRehabs.org / Couple Rehabs)
- **Phone:** (888) 325-2454 / `+1-888-325-2454` / `tel:8883252454`
- **Contact URL:** `https://couplesrehabs.org/contact-us/`
- **Primary pillar:** `https://couplesrehabs.org/substance-abuse-treatments/`
- **CA state hub:** `https://couplesrehabs.org/couples-drug-rehab-california/`
- **News index:** `https://couplesrehabs.org/news/`
- **API endpoint:** `https://couplesrehabs.org/wp-json/wp/v2/posts`  *(confirm)*
- **Address:** 4231 Balboa Avenue #1125, San Diego, CA 92117. Real business mailing address — carry it ONLY in the Organization/`#place` `PostalAddress`. Do NOT use it as a LocalBusiness or treatment-delivery location.
- **Logo:** `https://couplesrehabs.org/wp-content/uploads/2018/07/logo-1-e1502764175400.png`
- **sameAs (confirmed):** `https://www.facebook.com/CouplesRehab` — add others only if verified real.

## Known issues to flag / fix

- The site footer email reads `info@89n.245.myftpupload.com` (a leftover staging artifact). Do not use it in content; flag for correction. Route all contact to the phone number or `/contact-us/`.
- Geo slug formats are inconsistent on the live site (`/couples-rehab-programs-san-diego/` vs `/couples-rehab-seattle-washington/` vs `/couples-rehab-washington-d-c/`). New city pages standardize on `/couples-rehab-{city}-{state}/` per `url.md`.
- Several nav "pillar" pages are currently thin. Strengthen `/substance-abuse-treatments/` into a true hub before scaling geo clusters under it.
- Verify the full live sitemap before mass-building geo so new ⬜ slugs don't collide with pages not yet recorded in `url.md`.
