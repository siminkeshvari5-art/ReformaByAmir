Stage: Website structure (Express)
Path: Express
Status: Approved
Approved after checkpoint: Yes

# 07 — Website structure: Reforma by Amir

Date: 2026-09-26
Inputs: 00, 02, 04, 06 (approved); `assets/brand/visual-direction.md` (approved with participant resolutions, below); `assets/brand/Amir.PNG`.

## Participant decisions recorded in this stage

| Item | Decision | Consequence |
|---|---|---|
| Brand name | **"Reforma by Amir"** replaces "Reform by Amir" (participant confirmed "Reforma Ba Amir is correct", read as "Reforma by Amir") | All public copy uses "Reforma by Amir". Earlier stage files keep the old spelling and are not edited. The legal entity stays TORRE VIA MP, S.L. |
| Visual block "Distinctive Visual Codes" (missing from export) | Use 06 §08 candidates: spirit-level line motif, four-line cost breakdown, three-finish side-by-side, careful-guest list | Build uses these as the visual codes |
| All-caps conflict (02 vs 08 of export) | Sentence-case headlines; caps only on small labels | Follows 08 Visual Restrictions |
| Colour ground conflict | Cream #FFFDF7 page ground with navy #000080 text; navy bands for contrast; gold #D4AF37 once per section; weights 400/600 only | Explicit answers in export §03 outrank the computed surfaces |
| Pinterest images in `assets/brand/` | Style reference only; **not published** (third-party rights; could imply own work) | Imagery = Amir.PNG + line illustrations + organic shapes; no stock or renders |

## Objective and conversion event

- **Objective:** turn Google, Google Ads and Instagram visitors (owner-occupiers in upper Barcelona) into qualified requests for a free home visit, and learn whether open-book pricing plus "one standard at any budget" produces requests (Test offer, 04).
- **Primary conversion:** "Request a free visit" form submitted successfully.
- **Implementation state:** **Connection required before launch.**
  - Destination: a form service (e.g. Formspree, Basin or similar) delivering to **reformabyamir@gmail.com**.
  - Stored data: renovation type, description, neighbourhood, start timing, name, contact method, phone or email, optional estimator result, consent timestamp, page language, UTM source/campaign.
  - Owner: Amir.
  - Consent and privacy: an unticked consent checkbox, limited to replying by the chosen method; a privacy policy page under GDPR/LOPDGDD, covering the data controller (TORRE VIA MP, S.L., NIF, address), purpose, retention and rights.
  - Confirmation: a success message only when the service returns success.
  - Error: a message plus the WhatsApp fallback.
  - Follow-up: one reply within 24 h by the chosen method → visit → itemised quote; Amir logs contacted / visit / quote / signed / lost + reason.
- **Secondary route (Connected):** WhatsApp link `https://wa.me/34661663335` and `mailto:reformabyamir@gmail.com`.
- Until the form is connected, no submission can be treated or reported as a lead.

## Audience, traffic, device

- Owner-occupiers improving or partially renovating their flat in Putxet i el Farró, Gràcia and Sant Gervasi, including English-speaking residents (Test audience, 02 §4).
- Arrival: problem- or solution-aware search and paid social. Mixed awareness; visitors compare providers and prices.
- **Mobile-first** (ads, Instagram). Three languages: ES (default), CA, EN, each fully implemented.

## Belief journey

Arrival (S01) → relevance and friction (S02) → difference: one standard (S03) → difference and proof: open ledger (S04) → price guidance (S05) → mechanism and careful guest (S06) → scope (S07) → credibility: who (S08) → fit and objections (S09) → action and next step (S10).

## Section plan

| ID | Visitor question | Belief change | Evidence | Claim limit | Visual archetype (VD §05) | CTA / next |
|---|---|---|---|---|---|---|
| S01-hero | What is this, and is it for me? | A Barcelona renovation firm that keeps quality constant and shows every cost | 04 §2, 06 §01 | No superlatives or price promise | Split hero: text 6 cols, image or illustration 5 cols; cream | Request a free visit |
| S02-situation | Will they get what renovating an occupied home is like? | They name my worries and have a written answer | 02 Cards 1–3 | No fear-selling; no prevalence claims | Image-and-text row (illustration left); navy band | Estimate your renovation (text link) |
| S03-standard | Does a smaller budget mean worse work? | Materials differ, the workmanship standard doesn't | 06 §01, §07; founder 00 §5 | Commitment, not proven outcome | Three columns plus a shared checklist; cream | — |
| S04-ledger | Will I understand and control the price? | Four-line breakdown plus written change rule | 04 D5, D6; 02 Card 3 | Illustrative layout, no figures | Row flipped: ledger graphic right; raised surface | — |
| S05-estimator | Roughly what will this cost? | A realistic range, with honest drivers and caveat | 02 §7; 04 D6 | Preliminary, not a quote; IVA stated | Tool block; cream | Request a free visit (carries result) |
| S06-process | How does it actually run? | Six concrete steps plus the careful-guest standards | 04 §1 D4; 06 §05 | Realistic programme, not a guaranteed date | Steps list plus side panel; navy band | — |
| S07-services | Do they do my kind of job? | Full scope with one team; extras clearly secondary | 04 §1 | Permits: responsibility agreed per project; no energy-saving figures | Row: text 6, list; cream | — |
| S08-founder | Who am I trusting? | A named person and company, honest about being new | 04 D7; 06 §09 | No invented history or counts; Iran not mentioned | Image-and-text row with Amir.PNG on 5 cols; raised surface | — |
| S09-questions | What could go wrong, and is it for me? | Fit boundaries plus honest answers | 02 D8; 04 §6 | No guarantee or insurance claims | Fit list plus accordions (VD pattern); cream | — |
| S10-request | What happens if I ask? | Low-effort, respectful request with a clear next step | 04 D9 | Success only on a real send | Full-colour closing (navy), the one centred-allowed section, form left-aligned | Send my request; WhatsApp alternative |

Footer: legal notice, privacy policy, cookie policy (stub pages; content needs company data).

**Alternation check:** backgrounds cream / navy / cream / raised / cream / navy / cream / raised / cream / navy. No consecutive archetype repeats. One focal point per section.

## First-screen requirements

- Eyebrow "Home renovations in Barcelona"; H1 purpose line; lead naming the three finish levels plus margin shown; one primary button "Request a free visit" that goes to S10 with the form focused. The header shows the same CTA.
- Hero 70–90vh; on mobile the image comes first, then text. Image: a spirit-level line illustration or Amir.PNG (build decides; no stock).

## Claim-to-proof placement

| Claim | Placed in | Support shown next to it |
|---|---|---|
| Same care at any budget | S01, S03 | Checklist of identical standards (S03) |
| Every cost shown | S01, S04 | Four-line breakdown plus "example layout" note |
| No extras without approval | S02, S04, S06, S09 | Written change rule |
| Reply within 24 h | S06, S10 | Commitment wording; success message |
| Who is responsible | S08 | Name, photo, company |
| Permit guidance | S07, S09 | Responsibility agreed in writing |

## Objections map

| Objection | Where | Answer |
|---|---|---|
| New firm | S08, S09 | Written documents, open quote, honest status |
| Price creep | S04, S09 | Change rule |
| Finish date | S06, S09 | Realistic programme plus early notice |
| Permits | S07, S09 | Partners confirm; written responsibility |
| Mess in an occupied home | S03, S06 | Careful-guest list |
| Not cheapest | S09 fit list | Honest boundary |
| Repeated sales calls | S10 | One reply, chosen method |

## Mobile priorities

Hero message plus CTA within the first screen; sticky header with a compact CTA; estimator inputs large and touch-friendly (min 44 px); the three-column S03 becomes stacked cards with the checklist once below; ledger lines stacked; accordions keyboard-accessible; the form is single-column with contact fields shown according to the chosen method.

## Analytics events (no personal data in events)

`cta_request_click` (location), `estimator_start`, `estimator_result` (type, size band), `form_start`, `form_submit_success`, `form_submit_error`, `whatsapp_click`, `email_click`, `language_switch`. UTM captured into a hidden form field. Analytics tool and cookie consent: **to decide at build** (consent banner required if non-essential cookies are set).

## D1–D10 content-coverage map

| ID | Section jobs and interactions |
|---|---|
| D1 | S01 eyebrow; S02 "home you live in"; S09 areas answer |
| D2 | S02 friction paragraph; S04 change rule |
| D3 | S02 list; S06 step 6 |
| D4 | S06 six steps; S07 services and extras |
| D5 | S01 H1 and lead; S03 side-by-side; S04 ledger |
| D6 | S05 estimator with caveat; S06 steps 2–4; S09 "Is the visit free?" |
| D7 | S04 ledger layout; S06 process; S08 founder and company |
| D8 | S09 fit list and FAQs; S06 careful-guest list |
| D9 | S01 plus header CTA → S10 form; estimator hand-off; WhatsApp and email alternatives; confirmation or error states |
| D10 | Voice across all sections; codes: spirit-level motif, ledger, side-by-side, guest list, "materials change, care doesn't" |

## Assumptions and exclusions

- **Excluded:** Pinterest imagery (rights, implied own work); guarantee, insurance and showroom (unconfirmed); testimonials and portfolio (none yet); Iran experience (founder focus on Spain); energy-saving figures; urgency devices.
- **Assumptions to confirm:** Amir leads every project; base near Av. República Argentina; Spanish *tú* register.
- **Blocked:** estimator kitchen and bathroom ranges, durations and IVA display (founder data); legal and privacy page content (NIF, address); form connection.

## Next recommended stage

`/build`
