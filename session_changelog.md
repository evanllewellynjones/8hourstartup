# ELJ Ventures · 8-Hour Plan — Session Changelog

*A record of changes made this working session. Append to `master_plan.md` or keep alongside it. The master plan itself has **not** been rewritten — see "Outstanding: Master Plan Reconciliation" at the foot of this file.*

---

## Summary

This session restructured the project from a single long `index.html` into a **parent hub plus per-hour child pages**, built all eight hour pages, created a reusable child-page template, and reworked the Table of Contents into a visual navigation map.

**Files now in the site (all must sit flat in one folder):**

| File | Role |
|---|---|
| `index.html` | Parent hub — header, TOC-as-navigation, full Hour 0 content |
| `hour_1.html` … `hour_8.html` | Eight per-hour child pages |
| `rules_reference.html` | Appendix page + the canonical child-page template |
| `app_build_paths.html`, `build_paths.html`, `3pl_costs.html`, `ad_platform_setup.html`, `roas_calculator.html` | Existing sub-child pages, now linked from the relevant hours |

---

## 1 · Working Convention Established

- **MD is the source of truth; HTML is mirrored from it.** Edit markdown freely during a session; regenerate HTML at checkpoints (after a major section, every ~90 min, or before a team review) — not on every change.
- Version tracking: a `HTML last synced` line travels with the version number so anyone can see if the visualization is behind the plan.

## 2 · Child-Page Template Created

- `rules_reference.html` is the **canonical template** for all child pages. To make a new one: copy it, change the title/eyebrow/h1, replace the body between the `PAGE BODY START` / `PAGE BODY END` markers, leave the style block / page nav / footer untouched.
- Design tokens are inlined in every child page — no shared CSS file to keep in sync.
- **Rule:** never put `<`, `>`, or `--` inside an HTML comment — it closes the comment early and leaks text onto the page. (Caught and fixed live this session.)

## 3 · Hour 0 Restructured (now on `index.html`)

- Hour 0 renamed **"Formation, Banking & Finance Setup"** (was "Legal & Banking Foundation") and is now the single home for all formation, legal-setup, and accounting decisions.
- Moved **up into Hour 0** from the old Hour 7: bookkeeping, sales tax, terms/privacy.
- Added a **"Where to Go · Formation, Legal & Accounting Partners"** section — four cards: business formation services, legal & compliance, accounting & bookkeeping, sales tax & legal pages.
- Section labels "What's Already Done" and "Still On Us During the 8 Hours" **removed**; the partner section is now the bold orange lead header.
- Cards "Connect payments to bank" and "Connect card to ad platforms" **removed from Hour 0** and **moved to Hour 8**.
- CoWork Ops box converted to a **full-width band** at the foot of the section.

## 4 · Index Page (Parent Hub)

- Title changed to **"The 8-Hour Business Launch Master Plan"**, one line, large font.
- Table of Contents rebuilt as a **3-column visual navigation map**: hour boxes with the number above the title, sub-child pages branching below on a connector spine.
- Column layout: Hours 1–4 / Hours 5–8 / Appendix.
- TOC is now the primary navigation (replaces the old sticky top-nav bar approach for the hours).
- All fonts kept at 10px or above.

## 5 · Hour Pages Built (1–8)

All eight built from the template, each with: header (big hour number + title), The Issue, Where to Go cards, Keys to Success, and a CoWork Ops Layer block.

| Page | Title | Linked sub-pages |
|---|---|---|
| `hour_1.html` | Idea Generation | — |
| `hour_2.html` | Validate Demand & Research | — |
| `hour_3.html` | Sourcing | App Build Paths |
| `hour_4.html` | Brand Messaging | — |
| `hour_5.html` | Product Marketing & Store Build | Shopify Build, Ad Platform Setup |
| `hour_6.html` | Marketing & Content | Ad Platform Setup, ROAS Calculator |
| `hour_7.html` | Operations, Inventory & Fulfillment | 3PL Costs |
| `hour_8.html` | Launch, Marketing & Content | ROAS Calculator, Ad Platform Setup |

**Sub-page link placement:** "Shopify Build" sits under Hour 5 (moved there from Hour 3 at end of session).

## 6 · Hour Sequence Reorganized

The hour order on the **site** was resequenced per a team mockup and now differs from the master plan's original numbering:

- Site **Hour 5** (Product Marketing & Store Build) — payments, photography, store platform.
- Site **Hour 6** (Marketing & Content) — content engine, ad creative, ad platforms, email/SMS, analytics, reviews. *Was the master plan's Hour 8 content.*
- Site **Hour 7** (Operations, Inventory & Fulfillment) — 3PLs, inventory, shipping/returns. *Was the master plan's Hour 6 content.*
- Site **Hour 8** (Launch, Marketing & Content) — the issue + critical warnings, analytics, reviews, the two "Connect…" boxes.

---

## Outstanding: Master Plan Reconciliation

**The body of `master_plan.md` has NOT been updated to this new structure.** It still reflects the pre-session hour numbering and titles. Before the MD can serve as the source of truth again, a reconciliation pass is needed to:

1. Renumber/retitle the hour sections to match the site (see §6 above).
2. Fold the Hour 0 restructure (§3) into the MD's Hour 0 section.
3. Remove the now-defunct "Hour 7 · Customer Operations — Being Repurposed" content or rehome it.
4. Update the Site Structure section to list all eight built hour pages.
5. Bump the version and set `HTML last synced` to match.

Until then, treat **the site as current** and the MD as lagging.
