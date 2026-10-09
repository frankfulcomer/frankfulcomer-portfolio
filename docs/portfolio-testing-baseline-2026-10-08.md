# Portfolio testing baseline — 2026-10-08

## Scope and result

Focused stabilization of the published homepage and Workflow Tracker, Job Search
Hub, Conductor, and Personal Portfolio pages. Baseline source revision:
`20230350be544a2e2c4ffa641769a910e6710489`.

The tested behavior passed, with one minor caption-navigation consistency defect
fixed and one external destination blocked from automated verification. This is
a proportionate browser baseline, not comprehensive accessibility or browser
certification. Application and test repositories were not changed.

## Browser automation actually executed

The Codex in-app browser executed all five pages at 320, 375, 768, 1024, and
1440 CSS pixels, at 900 pixels high: 25 initial combinations and 25 local
post-fix combinations. The homepage was measured with all four stories open.

| Check | Observed result |
| --- | --- |
| Horizontal document overflow and elements extending beyond viewport | 25/25 initial and 25/25 post-fix combinations passed |
| Four story controls: mouse open/bottom collapse, Enter open/bottom collapse, Space toggle | All four passed; bottom collapse returned focus to the corresponding summary |
| Visible focus after keyboard collapse | Solid outline observed on all four summaries |
| Images, captions, alt text, original-image destinations | All 22 evidence-image placements loaded; 11 unique original PNGs opened with their original dimensions |
| Image aspect ratios | Preserved within browser rounding/border differences |
| Homepage/dedicated content comparison | 21 Workflow Tracker, 18 Job Search Hub, 16 Conductor, and 19 Personal Portfolio paragraphs matched; all figures/captions matched |
| Skip link, Back to top, return to Featured Work | Keyboard skip link reached #main; return links reached #top and /#work |
| External navigation | Workflow Tracker QA link opened the correct public GitHub repository |
| Console | No warning/error entries returned during the five-page image checks and local retest |
| Basic semantics | One main landmark and one h1 per page; English language declared; no empty accessible link labels found |
| Basic text contrast | Computed foreground/background pairs met 4.5:1 for normal text or 3:1 for large text; lowest measured ratio approximately 4.85:1 |

Contrast measurements inspect rendered CSS text colors and opaque ancestor
backgrounds. They do not establish contrast for every state, image text,
transparency, or complex background. Native details/summary controls exposed
expanded/collapsed state in the browser accessibility tree.

## Source and HTTP checks actually executed

- Checked 30 unique public page, asset, and external HTTP destinations: 29
  returned HTTP 200. LinkedIn returned HTTP 999, an automation restriction;
  its human-facing availability was not established by that request.
- Checked internal anchor targets, duplicate IDs, balanced source tags,
  image alt attributes, and noopener on new-tab links: no findings.
- All evidence full-size links resolve to the same PNG used by their thumbnail;
  direct browser navigation verified the 11 unique originals and dimensions.
- Inspected the public repository file inventory, page sources, and existing
  documentation. Credential-pattern checks found no private-key, GitHub-token,
  AWS-access-key, or OpenAI-key patterns. No private transcript or database file
  appeared in the public repository inventory. This is basic hygiene review,
  not an exhaustive secret scan or security assessment.
- HTTPS public delivery and Cloudflare deployment checks are used to confirm
  publication. Deployment success remains separate from quality verification.

The HTTP audit covers referenced resources; a complete browser network waterfall
was not recorded. The source checks are not a standards-based HTML validator.

## Visual inspection performed by the assistant

Inspected actual browser captures for each of the 25 page/width combinations,
including narrow text wrapping, image scaling, captions, visible keyboard focus,
spacing, and screenshot borders. Representative evidence sections showed no
clipping or overlap. Screenshot text is necessarily small in mobile thumbnails;
the original-image links provide the readable full-resolution version.

The explanatory verification diagrams reflow without page overflow. No live
wide data table was found in these stories; table content inside screenshots is
handled as an image. Job Search Hub's early-development statement, fictional
demo-data disclosure, and distinction between application CI and the independent
Selenium suite remain intact.

## Defect and regression record

**P3 — inconsistent caption navigation.** Workflow Tracker and homepage Job
Search Hub captions displayed full-size links on a separate line, while the
dedicated Job Search Hub and Conductor links ran into caption text. Personal
Portfolio relied on the clickable image and an instruction instead of an
explicit caption link. Observed at 320/375px and also present at desktop widths.

Expected: a consistent, discoverable full-size caption link across stories.
Fixed: retained the existing styling and assets, added caption links to Personal
Portfolio, and used the existing `project-visual-source` pattern for Conductor
with a shared block rule. No narrative or engineering claims changed.

Retest: all 25 local page/width combinations passed without overflow; all
caption source blocks used block layout; all evidence images loaded and no
console warning/error entries were returned. Matching homepage/dedicated
figures were retained. Final public smoke checks accompany publication of this
report; the publication commit identifies the tested final files.

## Limitations and participation still needed

- Only the in-app browser was exercised in this cycle. No separate Chrome,
  Edge, Firefox, Safari, iOS, or Android execution is claimed.
- No physical-device, touch interaction, screen-reader, actual browser zoom,
  or exhaustive page-by-page exploratory session was performed.
- No axe/Lighthouse/WCAG certification, comprehensive accessibility audit,
  standards HTML validation, penetration test, or dependency scan was performed.
  No new testing dependencies or infrastructure were installed.
- Human follow-up: check LinkedIn, sample Safari/Firefox and a physical phone,
  and perform a screen-reader/200% zoom pass when practical.
- Homepage story subsection headings remain h2, alongside outer section
  headings. There are no skipped heading levels, but a future semantic refinement
  could nest these more clearly under project titles. This was documented rather
  than expanding the stabilization work into structural restyling.
- Existing screenshots and documented test evidence were reviewed; application
  regression suites were not rerun and no new successful execution was invented.

No significant unresolved functional defect was observed within this scope.
