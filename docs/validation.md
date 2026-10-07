# Portfolio v0.1 validation

## Support boundary and approach

The minimum supported viewport is 320 CSS px. Human exploratory resizing
observed that the layout remained usable below 320 CSS px; this is robustness
outside the support boundary, not an extension of the v0.1 requirement.

Validate representative widths of 320, 375, 768, 1024, and 1440 CSS px,
plus content-driven breakpoint boundaries and exploratory resizing between
and below those widths. Include 200% browser zoom/reflow where practical.
Requirements and intended browser support are defined in PRODUCT.md.

## Automated and static evidence

Local in-app browser viewport checks passed at all five representative
widths without horizontal page scrolling. Additional checks around layout
breakpoints and narrower reflow widths passed. These checks are viewport
emulation, not physical mobile-device acceptance or actual browser zoom.

HTML validation passed with zero errors/warnings; CSS parsing and property
checks and Git whitespace checks passed. Source inspection checked internal
anchor targets, unique IDs, external-link attributes, asset paths, and
Person structured data. Standards-based CSS review found no required
mainstream-browser fallback. Assets loaded locally without reported failures.

All three Back to top links were checked for keyboard activation to #top,
visible 2px focus outlines, 44px target height, and responsive fit at the five
representative widths. The hero returned to the top of the viewport.

## Human browser acceptance, 2026-10-06

Desktop visual review passed. Frank reported usable behavior during
exploratory resizing below the supported 320 CSS px minimum.

Frank accepted testing as sufficient for v0.1 on 2026-10-06. This is the
release acceptance decision; it does not invent missing per-browser test logs.

| Browser | Recorded validation evidence |
| --- | --- |
| Chrome | Installed desktop browser exercised through partial Computer Use checks, including responsive views, keyboard/skip-link behavior, actual 200% zoom, and console inspection. Remaining human checks were planned; no separate detailed final result was supplied. |
| Edge | Direct human acceptance produced the Experience return-navigation finding. Overall testing was subsequently accepted by Frank. |
| Firefox | Intended manual acceptance browser; a separate completed test result is not present in the retained conversation. Physical validation cannot be independently confirmed from this record. |
| Safari, iOS Safari, Chrome on Android | Supported by design; not physically validated in this cycle. |

The manual acceptance scope included rendering, scrolling, keyboard navigation,
skip-link behavior, 200% zoom, link destinations/new tabs, mailto invocation
without sending mail, and obvious asset or site-console failures where practical.
Overall acceptance does not imply every listed check has a separate recorded pass.
No additional browser acceptance is required unless a subsequent change creates
a specific regression risk.

## Manual usability findings and decisions

- Following Experience's see Conductor link reaches AI-Assisted Engineering
  but lacked an obvious return to the hero. Frank visually approved the
  added Back to top link on 2026-10-06.
- Edge acceptance identified the same need after the Experience cards.
- Frank agreed to the shared pattern and requested consistency in Featured
  Work and Experience. All three sections now link to #top using the same
  understated styling, keyboard focus, and 44px target treatment.
- These links are minimally important on desktop, but sections grow much
  taller when content reflows on narrow displays. Consistent return navigation
  improves usability at the supported 320 CSS px minimum.

Hero text width remains intentional. Section introductions and footer
contact messaging use their available responsive container width.

## Validation limitations and follow-up

Computer Use intermittently could not safely establish Chrome's current URL.
A fresh explicit localhost window allowed limited checks, but control remained
unreliable. Frank chose direct human browser acceptance; safety checks were
not weakened or bypassed. Partial tool checks do not establish browser acceptance.

A reusable headed/headless acceptance suite is deferred in enhancements.md.
Detailed Work/Conductor/Claude provenance remains private outside the repository.
Testing is accepted as sufficient for v0.1. Commit and push/deployment remain
separate human approval checkpoints; this record authorizes none of them.
