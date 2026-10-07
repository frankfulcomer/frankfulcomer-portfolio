# Portfolio validation

## Support boundary and approach

The minimum supported viewport is 320 CSS px. Human exploratory resizing
observed that the layout remained usable below 320 CSS px; this is robustness
outside the support boundary, not an extension of the v0.1 requirement.

Validate representative widths of 320, 375, 768, 1024, and 1440 CSS px,
plus content-driven breakpoint boundaries and exploratory resizing between
and below those widths. Include 200% browser zoom/reflow where practical.
Requirements and intended browser support are defined in PRODUCT.md.

## Original v0.1 evidence, 2026-10-06

Local in-app browser viewport checks passed at all five representative
widths without horizontal page scrolling. Additional checks around layout
breakpoints and narrower reflow widths passed. These checks are viewport
emulation, not physical mobile-device acceptance or actual browser zoom.

HTML validation passed with zero errors/warnings; CSS parsing and property
checks and Git whitespace checks passed. Source inspection checked internal
anchor targets, unique IDs, external-link attributes, asset paths, and
Person structured data. Standards-based CSS review found no required
mainstream-browser fallback. Assets loaded locally without reported failures.

The original three Back to top links were checked for keyboard activation to #top,
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
  Work and Experience. The original three sections were updated to link to #top using the same
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

## Release-preparation history

ChatGPT Work's platform usage limit interrupted release preparation. Before
resuming, repository and private provenance state were inspected to establish
which operations had completed; outstanding documentation work was then finished.

This cycle included Conductor/Claude implementation and a later read-only review
of the three Back to top links through the Windows/WSL live-viewer launcher.
Work also made the small Back to top source refinements before Frank clarified
the implementation-routing boundary, and independently reviewed and validated
the resulting site. Detailed run evidence remains private. General orchestration
policy and usage-preflight enhancements belong to ai-development-workflow.

## Hero / How I Work / Experience episode, 2026-10-07

### Accepted result

Frank accepted the final content and visual state before requesting closeout.
The page order is Hero → How I Work → AI-Assisted Engineering → Featured Work
→ Experience → footer. Backgrounds are white, pale gray, dark, pale gray, dark,
and pale gray respectively. The temporary How I Work divider was removed because
the adjacent dark section provides the boundary.

The hero presents broader professional positioning. How I Work contains six
engineering principles. Experience contains exactly five approved dimensions:
Software Quality, Systems & Requirements, Software Implementation, Test Automation,
and Communication. Its equal-width desktop cards form a centered 3+2 layout;
intermediate widths use 2+2+1 with the fifth centered; narrow widths stack all five.
Content determined the layout; no filler dimension was added. Existing card styling,
navigation and section spacing are preserved.

### Final validation

Independent recommended HTML validation, CSS parsing/supported-property checks,
exact approved-copy checks, unique IDs, valid internal anchors, preserved external
link attributes, and Git whitespace checks passed. CSS custom properties were
verified through computed styles where the static property checker lacks support.

Rendered checks cover 320, 375, 768, 1024 and 1440 CSS px, supplemented by checks
at 600/601, 680/681 and 1100/1101 breakpoint boundaries during implementation.
Equal card widths, centered final rows, readable wrapping, no page/card overflow,
section order and accepted content were verified. Established content-to-heading
gaps remain 144px above 680px and 96px at narrow widths; internal How I Work
spacing is unchanged. Desktop/tablet/narrow visual evidence is retained privately.

All four Back to top links preserve #top navigation, keyboard semantics, visible
focus treatment and 44px minimum targets. GitHub, LinkedIn, Email and project-link
destinations remain intentional; email checks do not send messages. Skip navigation,
heading structure, accessible section labels, portrait alternative text and the
existing reduced-motion behavior are preserved. The reused dark palette has
approximately 15.4:1 heading and 7.0:1 paragraph contrast on its dark background.

Viewport emulation supplements human acceptance in external browser tabs. This
episode does not claim new physical-device, Safari/iOS/Android, per-browser or
actual 200% zoom acceptance beyond the earlier recorded evidence.

### Evidence and scope

Implementation assignments, Claude/Conductor provenance, available user-facing
conversation pages, independent reviews, measurements and meaningful visual states
remain private outside version control. Detailed revision history was retained
there before this closeout summary replaced repetitive provisional entries.
The original before screenshots were later reconstructed partial captures, not a
contemporaneous complete visual baseline; the original committed source remains
available. Later implementation and accepted-state captures are authentic.

Featured Work's visual/project presentation enhancement is deliberately deferred
in enhancements.md. No future case-study page is included in this release.
