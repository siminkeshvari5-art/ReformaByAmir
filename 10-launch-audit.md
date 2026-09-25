Stage: Launch review
Path: Express
Status: Approved
Approved after checkpoint: Yes

# 10 — Launch audit: Reforma by Amir

Date: 2026-09-26 · Site reviewed: `site-v1/` (index.html ES, ca.html, en.html, 3 legal pages), served locally at http://localhost:8766 from a scratchpad copy kept in sync.

## Launch readiness: **Not ready to publish**
Two blockers remain, both outside the code:
1. The request form has not been verified end-to-end.
2. The legal pages contain placeholders.

The site itself (copy, layout, responsiveness, interactions) passed review, and the local defects found were fixed.

## Findings

### Blockers
| # | Location | Evidence | Consequence | Fix | Who |
|---|---|---|---|---|---|
| B1 | S10 request form → FormSubmit | No real submission sent. FormSubmit requires a one-time activation from reformabyamir@gmail.com. The success path is untested (validation and error paths tested; see below). | The site's objective, requests for a free home visit, cannot be confirmed to arrive. Visitors could submit into nothing. | After publishing: send one test from the live site → click FormSubmit's activation email → send a second test and confirm all fields arrive. Or ask Claude to send the test (needs your explicit OK). | Participant |
| B2 | `aviso-legal.html`, `privacidad.html` | Visible placeholders: "[Dirección registrada — pendiente]", "[Registro Mercantil … — pendiente]", "[Plazo — pendiente de definir]", "[Verificar garantías …]". | Spain's e-commerce law (LSSI) requires the registered address and registry data; the privacy notice under GDPR needs a retention period and a processor basis. Publishing with brackets undermines trust and compliance. | Supply the registered address, Registro Mercantil data and retention period (e.g. 12 months for non-converted requests); check the FormSubmit and Gmail transfer terms; legal review recommended. | Participant |

### Important
| # | Location | Evidence | Consequence | Fix | Who |
|---|---|---|---|---|---|
| I1 | S05 estimator | Bands are public-guide derivations (Cronoshare), plus derived premium bath, several-rooms at about 75% and IVA ×1.10 for full-flat. | Visitors anchor on these numbers. If Amir's real quotes differ widely, it contradicts "every cost clear". | Replace them with Amir's own cost build-up after the first 3–5 quotes; edit the `DATA` block in `scripts/main.js` and the noscript table. | Participant |
| I2 | ES/CA copy | Written by Claude; no native review. | Tone or register errors reduce trust with local owners. | A native Spanish and Catalan speaker reads the three pages once. | Participant |
| I3 | Focus ring on light surfaces | The VD gold ring #D4AF37 is 2.1:1 on cream, below the 3:1 non-text contrast guideline. | Keyboard users could lose track of focus. | **Fixed locally:** a navy 6px halo was added behind the gold ring on cream and raised surfaces (`base.css`). | Done |
| I4 | Estimator number format (ES/CA) | "4500 – 6000 €" but "12.000 €" (es-ES skips grouping for 4 digits). | Inconsistent figures look careless on a transparency brand. | **Fixed locally:** explicit grouping (4.500 / 4,500 in EN). Verified: "4.500 – 6.000 € · 6.000 – 8.500 € · 8.500 – 12.000 €". | Done |

### Improve
| # | Location | Fix |
|---|---|---|
| P1 | `<head>` | After the domain is known, make `hreflang` links absolute and add `rel="canonical"` and `og:url`. Add a 1200×630 `og:image`, which is currently omitted rather than broken. |
| P2 | Legal pages | **Fixed:** `lang="ca"` and `lang="en"` added to the translated sections. |
| P3 | Form radio groups | Add `aria-describedby` from each radio group to its error message; errors are already visible and focus moves to the first invalid field. |
| P4 | Illustrations | Line SVGs are Claude-drawn placeholders; commission final drawings in the VD 06 style when budget allows. |
| P5 | Fonts | Add Nunito and JetBrains Mono as local files (OFL licence) to match the VD exactly; fallbacks render acceptably. |
| P6 | Mobile menu | Consider repeating "Request a free visit" inside the open menu panel. |
| P7 | Proof | Replace the "new in Barcelona" framing with real project photos and client words as soon as the first jobs finish (with permission). |

## Passes (checked)
- **Five-second clarity:** the hero states the category (home renovations in Barcelona), the difference (same quality at any budget, every cost shown incl. margin) and one action. It matches Google search and Instagram ad arrival. A competitor could not paste it unchanged (no one reviewed shows their margin).
- **Research payoff and subtraction test:** pass.
  - Occupied-home situation (S02).
  - Verbal-scope, price-growth and silence frictions (S02, S04, S09).
  - Open-book mechanism (S04).
  - Offer and commitment: free visit, itemised quote, programme, change rule (S06).
  - Transparent status "new in Barcelona" plus named founder and NIF (S08, footer).
  - Researched objections and fit list (S09).
  - Real action with a stated next step (S10).
  - Without 02/04 the page would be a generic "quality renovations, free quote" site.
- **D1–D10 rendered coverage:** all present in the expected sections (DOM and text checked in EN, ES, CA).
- **Decision density:** each section adds a new decision input; no slogan-only sections; whitespace follows VD, not missing content.
- **Claim limits:**
  - No leaked internal language, superlatives, guarantee, insurance, showroom, reviews, counts or energy figures (automated grep of all three pages).
  - "Can you guarantee a finish date?" answers honestly *no*.
  - The permit wording keeps "responsibility agreed in writing".
- **Action continuity:** the same CTA appears in the header, hero, estimator result and S10. It leads to a real form (not a scroll-only destination) and states the reply time, method and no repeated calls. WhatsApp and mailto routes open correctly.
- **Language selector:** ES, CA and EN each lead to a complete page with identical structure.
- **Visual Direction fidelity:** cream ground with navy, gold used only as the level bubble or on navy, sentence-case headings, 400/600 weights, flat surfaces, organic shapes, solid check icons, line illustration, no stock imagery. The recognisable quality (level mark plus ledger) is present from the header onward.
- **Links:** all local file links and in-page anchors resolve (automated check).
- **Weight:** 280 KB total, no external requests except the FormSubmit POST.

## Block 05 rule check (rendered + DOM)
| Rule | Result |
|---|---|
| One focal point per section | Pass (10/10 sections have exactly one `data-focal`) |
| No archetype twice in a row | Pass |
| At most one centred section | Pass (S10 heading only; form left-aligned) |
| ≥2 changes between neighbours | Pass |
| ≥3 surface changes | Pass (cream / navy / raised, 9 transitions) |
| Body copy never centred | Pass |
| No text block < 5/12 | Adapted with reason: guest panel widened to 5 cols (planned at 4) |
| Hero 70–90vh, eyebrow/H1/lead/one button | Pass on desktop; adapted on mobile (content height, so the CTA stays in the first screen) |
| Accordion exact pattern, keyboard button, aria-expanded synced | Pass |
| Header sticky, surface change after 80px, menu below breakpoint | Pass (menu below 1180px, VD default 768px; adapted because the five labels + language + CTA do not fit between 768 and 1180) |
| Mobile: splits stack image-first | Pass |

## Visual QA by viewport
| Viewport | Pages | Result |
|---|---|---|
| 360×740 / 360×780 | CA, ES hero, menu, privacy | No overflow; CTA bottom at 729px (in first screen); menu opens and closes |
| 375×812 | EN full page scrolled | All sections stack correctly; estimator result readable; form single column |
| 390×844 | ES estimator | Bath and several-rooms results correct, grouping fixed |
| 529×714 (pane) | EN hero | Header CTA hidden <640px (fixed wrap) |
| 768×1024 | ES | 6-col behaviour, no overflow, balanced headings |
| 1440×900 | EN, every section | Matches the 1440 wireframe; no overlap or clipping |
| 1600×1000 | ES hero, S03 | Content capped at 1280px, margins balanced |

**Wireframe deviations:** S04 ledger is top-aligned rather than centred (reading order); guest panel 5 cols instead of 4 (rule); mobile menu breakpoint 1180px. No unexplained deviations.

**Not tested:** screen reader; real 200% zoom (768px layout used as a proxy); browsers other than the preview engine; real font rendering with Nunito; performance audit.

## Conversion path evidence
| Step | Tested | Result |
|---|---|---|
| Empty submit | Yes | 7 specific errors; focus moves to the first field; no request sent |
| Contact method "Email" | Yes | Phone field hidden; email required |
| Network failure | Yes (non-existent **local** endpoint) | Error message with the WhatsApp fallback; no false success |
| Real submission to FormSubmit | **No** | Needs participant permission and inbox activation. **Blocker B1** |
| Stored record in the inbox | **No** | — |
| WhatsApp / email links | Yes | Correct `wa.me/34661663335` and `mailto:` targets |
| Analytics | n/a | `dataLayer` events only; no tool, no cookies (matches the cookie policy) |

## Four readiness layers
1. **Research readiness:** directional only. The test audience (owner-occupiers, partial reforms) rests on public signals. No interviews yet. The 02 §12 plan stands: 5–8 owners in Putxet, Gràcia and Sant Gervasi.
2. **Commercial readiness:** Test offer. No cost data; estimator bands are public-guide approximations; contribution unknown. Guarantee, insurance and showroom are unconfirmed and absent from the page.
3. **Conversion-instrument readiness:** built but **not verified** (B1). Consent and privacy text are present, but the legal data is incomplete (B2). Owner: Amir, reply within 24 h. The follow-up log (visit → quote → signed/lost) still needs to be set up, e.g. a simple spreadsheet.
4. **Website readiness:** ready apart from the legal placeholders. Copy, layout, responsiveness, accessibility basics and interactions pass; local fixes applied (I3, I4, P2).

## Offer status and remaining gaps
Test offer (04). Remaining gaps:
- Amir's cost build-up and the IVA treatment per job type;
- guarantee terms and insurance;
- the showroom and office address;
- direct customer validation;
- measured reply time;
- the first real projects as proof.

## Next three actions
1. **Complete the legal data** (registered address, Registro Mercantil, retention period) so Claude can replace the placeholders (B2).
2. **Publish to GitHub Pages** (steps given in chat), then **activate and test FormSubmit** from the live site and confirm a request arrives in reformabyamir@gmail.com (B1).
3. **Replace the estimator bands with your own costs** after the first quotes, and start the follow-up log and 5–8 owner conversations to test the audience and open-book pricing.

## Next recommended stage
Complete: the workshop sequence ends here. Publishing requires an explicit request.
