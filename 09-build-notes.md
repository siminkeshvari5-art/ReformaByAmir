Stage: Build
Path: Express
Status: Approved
Approved after checkpoint: Yes

# 09 — Build notes: Reforma by Amir

## Design statement
- **Purpose:** turn owner-occupiers arriving from Google or Instagram into requests for a free home visit.
- **Priority visitor:** an owner improving the flat they live in, in upper Barcelona, on a phone.
- **Main action:** Request a free visit.
- **Visual concept:** the spirit level on a warm cream ground. Precise alignment and a calm navy voice, with gold used only where the bubble sits level.
- **Recognisable quality:** the level mark (a pill with a centred gold bubble) plus the four-line ledger; everything else is quiet.

## Participant inputs received at build start (resolutions of items flagged in 08)
| Input | Applied as |
|---|---|
| "Make the request form yourself" | Form built and wired to FormSubmit (AJAX endpoint, delivers to reformabyamir@gmail.com). **Activation pending**: FormSubmit emails the inbox on the first submission and the owner must click the activation link. State: Connection required before launch until activated and one test is received. |
| NIF B26831461 | Legal notice, privacy and footer |
| Estimator ranges and durations from public guides, scaled by scope | See "Estimator data" |
| Amir personally leads everything and heads a professional, experienced team | S08 body: "Amir leads every project personally, from the first visit to handover, and heads an experienced team of professionals." (participant-supplied fact) |
| Works only in Barcelona | S09 areas answer: "Only in Barcelona. We focus on El Putxet i el Farró, Gràcia and Sant Gervasi, and work across the city." Replaces "based near…/often work in…" |

## Estimator data (derived; sources accessed 2026-09-26)
Bands are rounded public-guide figures shown **with IVA included**.
- **Bathroom** (Cronoshare "reformar baño Barcelona", about 5.5 m², IVA incl.): full renovation typically €4,500–8,500. Economical €4,500–6,000 · Mid €6,000–8,500 · Premium €8,500–12,000 (premium upper bound derived). Duration: 2–3 / 3–4 / 4–5 weeks (derived from scope).
- **Kitchen** (Cronoshare "reformar cocina Barcelona", 8–10 m², IVA incl.): Economical €6,000–10,000 · Mid €10,000–15,000 · Premium €15,000–25,000. Duration 4–8 weeks per source → 4–5 / 5–6 / 6–8 weeks.
- **Full apartment** (Cronoshare reforma integral: €300–350 / 400–700 / 800–1,000 per m², IVA status unclear, so ×1.10 applied and rounded): €330–385 / €440–770 / €880–1,100 per m². Duration by size: ≤60 m² 8–10 wks; 61–100 m² 10–14 wks; >100 m² 14–18 wks; +1–2 wks mid, +2–4 wks premium (derived; consistent with 10–16 wks in 02 S3 and about 3 months in 02 S6).
- **Several rooms** (derived at about 75% of full-flat rates, per m² of the rooms involved): €250–290 / €330–580 / €660–825 per m². Duration: ≤30 m² 3–5 wks; 31–60 m² 5–8 wks; >60 m² 8–11 wks; plus the same finish-level uplift.
- These are Demo-grade inputs for a Test offer. Replace them with Amir's own cost data as soon as possible.

## Visual Direction reconciliation (explicit answers > restrictions > defaults)
- Fonts: Nunito and JetBrains Mono are not supplied and CDNs are not allowed, so the export's own fallback stacks are used ("Trebuchet MS", Verdana; ui-monospace, Menlo, Consolas). The browser uses Nunito if it is installed locally.
- Weights: 400/600 only (explicit "no bold").
- Headlines: sentence case (participant resolution).
- Ground: cream #FFFDF7 (60%); navy #000080 text and bands (30%); gold #D4AF37 one moment per section (bubble, active state, focus ring); #151E3F footer only; #ADB4BF fine detail. Raised surface derived: #F3F1EA (a cream tint; derived, not a new brand colour).
- Contrast (calculated): navy on cream 16.4:1 ✓; cream on navy 16.4:1 ✓; gold on navy 8.0:1 ✓ (large and small text); gold on cream 2.0:1 ✗, so gold is never used as text on cream (decorative only); #111 on gold 9.0:1 ✓; #ADB4BF on navy 8.1:1 ✓.
- Separators: "No rules" (explicit) outranks the default title hairline, so sections separate by surface change and spacing.
- Illustration: single-stroke line SVGs drawn locally as **placeholders expressing the system**, not final brand assets.
- Icons: solid filled (check marks).
- Shapes: organic blobs behind the illustration and portrait (one motif family).
- Materiality "glossy coated paper": a subtle sheen gradient on the raised surface only (restrained).
- Photography: none approved beyond Amir.PNG. Pinterest references are not published.

## Visual assembly map
| ID | Job (07) | Copy volume | Archetype | Focal | Surface / align / cols | Density |
|---|---|---|---|---|---|---|
| S01-hero | What, for whom, CTA | Short | Split hero | H1 | Cream / left / 6 + 1 + 5 (level illustration) | Low |
| S02-situation | Friction → written answers | Medium | Image-and-text row (illustration left) | 4-item list | Navy / left / 5 + 1 + 6 | Medium |
| S03-standard | Same standard, 3 levels | Medium | Three columns + shared checklist | Shared checklist | Cream / left / 3×4, checklist 8 | Medium |
| S04-ledger | Four-line price + change rule | Medium | Row flipped (text left, ledger right) | Ledger graphic | Raised / left / 6 + 1 + 5 | Medium |
| S05-estimator | Preliminary ranges | Tool | Tool split (inputs 5, result 6) | Result panel | Cream / left / 5 + 1 + 6 | Medium |
| S06-process | Six steps + guest list | High | Steps + side panel | Steps list | Navy / left / 7 + 1 + 4 | Medium–high |
| S07-services | Scope | Medium | Row (illustration left) | Services list | Raised / left / 5 + 1 + 6 | Medium |
| S08-founder | Who | Medium | Row flipped (portrait right) | Portrait | Cream / left / 6 + 1 + 5 | Low |
| S09-questions | Fit + FAQs | High | Fit list + accordions | Accordion list | Raised / left / 4 + 1 + 7 | Medium |
| S10-request | Form + next step | Form | Full-colour closing (the one centred heading) | Form | Navy / heading centred, form left in 8 cols | Medium |

Rules: no consecutive archetype repeat ✓ (S04 and S08 are both "row flipped" but not consecutive); one centred section (S10) ✓; ≥2 changes between neighbours ✓; ≥3 surface changes ✓ (cream, navy, raised); no text block < 5 cols except the S06 guest panel (4 cols). **Adapted:** it becomes 5 cols with the steps at 6, to satisfy the rule.

## Wireframes

390 px
```
[Reforma by Amir          ☰]
[ level line illustration  ]
 eyebrow · H1 (3–4 lines)
 lead · [Request a free visit]
==== navy ====
[ illustration ]  H2 · lead · body · ✓✓✓✓ list · link
---- cream ----
H2 · lead · [Econ] [Mid] [Prem] stacked · ✓ checklist
---- raised ----
H2 · lead · ledger (4 stacked lines) · change rule
---- cream ----
H2 · inputs · [Show my ranges] · result card · drivers · CTA
==== navy ====
H2 · steps 1–6 · guest list panel
---- raised ----
[ illustration ] · H2 · services · also available
---- cream ----
[ portrait ] · H2 · body
---- raised ----
H2 · fit list · accordions
==== navy ====
H2 (centred) · form (single column) · WhatsApp/email · visit note
[ footer #151E3F ]
```

1440 px
```
| logo            links …                [Request a free visit] |
| eyebrow/H1/lead/CTA (6)        ·        level illustration (5) |
|█ illustration (5) · text + list (6)                          █|
| H2 lead                                                       |
| [Econ 4][Mid 4][Prem 4]  → checklist (8)                      |
|░ text + change rule (6)       ·     ledger graphic (5)       ░|
| inputs (5)                    ·     result panel (6)          |
|█ steps 1–6 (6)                ·     guest panel (5)          █|
|░ illustration (5)             ·     services (6)             ░|
| text (6)                      ·     portrait (5)              |
|░ fit list (4)                 ·     accordions (7)           ░|
|█            H2 centred / form 8 cols left-aligned            █|
| footer                                                        |
```

Visual assembly checkpoint: **approved by participant** before coding.

## What was built and how to preview
- `site-v1/index.html` (Spanish, default), `site-v1/ca.html` (Catalan), `site-v1/en.html` (English): the full one-page site. The language switcher links the three complete versions.
- `site-v1/aviso-legal.html`, `privacidad.html`, `cookies.html`: trilingual legal stubs.
- `site-v1/styles/` (tokens, base, layout, archetypes, sections), `site-v1/scripts/main.js`, `site-v1/assets/amir.jpg` (720×960, from `assets/brand/Amir.PNG`), `site-v1/assets/favicon.svg`.
- No framework, no build step, no CDN. Works offline.
- **Preview:** double-click `site-v1/index.html`, or serve the folder (`ruby -run -e httpd site-v1 -p 8766`) and open http://localhost:8766. During this session the site was served from a scratchpad copy, because the local server could not read the Downloads folder. `.claude/launch.json` was added for the in-app preview.
- The three HTML pages were generated from one template (scratchpad `gen.rb` + `page.erb`) so the copy stays identical to 08. The generated HTML is the deliverable; edit the HTML directly or regenerate.

## Sources used
00, 02, 04, 06, 07, 08 (copy verbatim except for the participant resolutions above); `assets/brand/visual-direction.md` (with the 07 resolutions); `assets/brand/Amir.PNG`. Estimator: Cronoshare Barcelona guides (bathroom, kitchen, reforma integral), accessed 2026-09-26.

## Derived implementation decisions
- Pill-shaped controls (radius 999px) echo the level vial; the same radius on every control (VD 03).
- Hero on mobile: illustration capped at 128–190px tall so that H1, lead and CTA fit the first screen (VD 05 image-first kept, compacted). At 360×740 the Catalan CTA bottom sits at 729px.
- Header CTA hidden below 640px (the hero CTA is immediately visible); a menu button below 1180px opens a full-screen panel (VD 05).
- Guest panel on desktop: 5 columns (the rule forbids text blocks under 5 of 12).
- Headings use `text-wrap: balance` to avoid orphans (for example "in" in S02).
- Input borders use the muted navy (10.6:1) because steel #ADB4BF on white is only 2.1:1 (WCAG 1.4.11).
- The estimator shows all three finish levels at once with per-level duration, as the founder asked for "entry-level, typical and higher-specification". The copy's single duration line became a per-row duration (same wording).
- Estimator figures are rounded to €100, or €500 above €10,000.
- Accordions use the exact VD 05 markup and CSS; they collapse only when JS runs (no-JS shows all answers).
- Without JS, the estimator shows a static table of the same bands, and the form posts to FormSubmit's standard endpoint.

## Rule-status checks (DOM check + rendered inspection)
| Rule | Status |
|---|---|
| One focal point per section (`data-focal`) | Pass: 10/10 sections have exactly 1 |
| No archetype repeated consecutively | Pass |
| At most one centred section (S10 heading only) | Pass |
| ≥2 changes between neighbouring sections | Pass (surface plus columns or density each time) |
| ≥3 surface changes | Pass (cream, navy, raised, 9 transitions) |
| Body copy never centred | Pass |
| No text block < 5/12 | Pass (guest panel adapted to 5) |
| No rules as separators (explicit) | Pass: surfaces separate sections; hairlines only inside lists and the ledger |
| Sentence-case headlines; no bold (400/600) | Pass |
| Gold one moment per section; never text on cream | Pass (level bubble; gold only as text on navy for step numbers and the IVA note) |
| Flat, no drop shadows | Pass |
| Visual Restrictions (no retro, neon, all caps, stock, no-margin) | Pass |
| Distinctive codes: level mark, four-line ledger, three-level side-by-side, guest list | Pass: level mark in the header, hero and every eyebrow |

## Contrast (calculated from token values)
Navy on cream 15.7:1 · muted navy on cream 10.6:1 / on raised 9.6:1 · light text on navy 11.5:1 · gold on navy 7.6:1 · gold on cream 2.1:1 (decorative only) · error on cream 8.0:1 · light error on navy 11.0:1 · button label on cream 18.6:1 · cream on footer 16.0:1.

## Viewports inspected
360×740 and 360×780 (CA, ES), 375×812 (EN, full page scrolled), 529×714 (pane width), 768×1024 (ES), 1440×900 (EN, every section). No horizontal overflow at 360, 375 or 768 (scrollWidth = clientWidth on EN, ES, CA and privacy).

**Defects found and fixed:**
1. The grid span and start classes collapsed columns to one track (every desktop section).
2. The mobile hero pushed the CTA below the fold.
3. The header CTA wrapped at 529px.
4. The hidden "Include my estimate" checkbox showed because `display:flex` beat `[hidden]`.
5. The estimator hint was unreadable on navy.
6. Orphan words in H2.
7. Weak input borders.

**Wireframe deviations:** none material. The S04 ledger sits at the top of its column rather than vertically centred, for reading order.

## Interactions exercised
- Mobile menu opens and closes (click; Escape).
- The accordion expands (panel height 0 → 108px, aria-expanded synced).
- Estimator: Full apartment 75 m² gives Economical €25,000–29,000 (10–14 weeks) · Mid €33,000–58,000 (11–16 weeks) · Premium €66,000–82,500 (12–18 weeks), IVA included; the "Include my estimate" option appears in the form.
- Form validation: an empty submit shows 7 specific messages and focus moves to the first field.
- Email method hides the phone field.
- Error state: tested against a non-existent **local** endpoint and shows the error message with the WhatsApp fallback.
- **The success path was not tested**: see below.

## Conversion implementation state
**Connection required before launch.**
- Form → `https://formsubmit.co/ajax/reformabyamir@gmail.com` (AJAX), with `https://formsubmit.co/reformabyamir@gmail.com` as the no-JS fallback.
- Fields sent: renovation_type, description, neighbourhood, start_timing, name, contact_method, phone/email, consent, language, utm_source, utm_campaign, estimate (if chosen). Honeypot `_honey`.
- The success message appears only if FormSubmit returns `success: true`.
- **Not yet verified:** no real submission was sent (an external submission needs the participant's explicit permission). To go live, the owner must:
  1. submit one test request from the site;
  2. click the activation email that FormSubmit sends to reformabyamir@gmail.com;
  3. submit a second test and confirm it arrives.

  Until then, no request can be counted as a lead.
- WhatsApp (`wa.me/34661663335`) and `mailto:` links are **Connected** (they open the correct route).
- Analytics: events are pushed to `window.dataLayer` only; no tool is installed and no cookies are set, so the cookie policy says so.

## Image slots and AI handoff
- Hero, S02 and S07 use locally drawn line SVGs: **placeholders** expressing VD 06 (single stroke, suggestive), not final brand illustrations.
- No photography direction beyond Amir.PNG. Pinterest references are not used.
- If images are generated later, use VD 09 exactly:
  - **Base prompt:** "warm and crafted, precise, classic, crafted + modern, gloss, organic, medium, generous, no text, no logo, no watermark, no stock-library look".
  - **Negative prompt:** "playful, bold, minimal, retro nostalgia, neon and fluorescent, all-caps headlines, no margins, anything from a stock library".
  - **Rules:** a single side light source; free space around the subject; no text, logo or watermark.
- Any generated image must be labelled as inspiration, never as a completed project.

## Missing content, assets and integrations
1. FormSubmit activation plus a verified test submission (**launch blocker**).
2. Registered address, Registro Mercantil details and data-retention period in the legal pages (**launch blocker**; legal review recommended). The privacy page names FormSubmit and Gmail as processors; verify their transfer safeguards.
3. Nunito and JetBrains Mono font files (optional; fallbacks in use).
4. Final illustrations and a logo file (the wordmark is typeset).
5. A social preview image (og:image omitted rather than broken).
6. Estimator bands are public-guide approximations; replace them with Amir's own costs.
7. Native-speaker review of the ES and CA copy.
8. Guarantee terms, insurance and showroom when confirmed.

## Checks not performed
- Real browser font rendering with Nunito (not installed).
- Screen-reader pass.
- 200% zoom test.
- 1600px wide view.
- Legal compliance review.
- Real form delivery.
- Lighthouse / performance audit.
