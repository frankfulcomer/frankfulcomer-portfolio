# Portfolio enhancement backlog

These enhancements are beyond v0.1. The v0.1 responsive-design and browser
acceptance requirements in PRODUCT.md remain release requirements.

## Reusable cross-browser / responsive acceptance suite

Status: proposed; defer implementation until after v0.1.

Create a small Python/Pytest + Playwright acceptance suite that runs headless
for routine validation and headed when Frank wants to watch execution.
This aligns with the existing QA automation framework. Keep one shared set
of checks, with viewport and browser parameters rather than duplicated tests.

Initial coverage:
- Load the local portfolio and verify important content and assets.
- Check 320, 375, 768, 1024, and 1440 CSS px viewports for reflow and
  unintended page-level horizontal scrolling.
- Verify link destinations, safe external-link attributes, and internal anchors.
- Exercise keyboard focus and skip-link behavior where automation is reliable.
- Capture basic site-related browser console errors.
- Run installed Chrome and Edge channels, plus Playwright-managed Firefox
  where practical. Record that managed Firefox is not the stock installation.

Retain human checks for visual balance, actual browser zoom, mail-client
integration, and physical Safari/iOS/Android behavior. If testing stock
installed Firefox becomes essential, reassess Selenium rather than maintaining
both frameworks by default. Selenium/Pytest with a headed option is already
used in Job Search Hub Tests.

Right-sized first increment: a local server, a few meaningful acceptance
checks, explicit headed/headless selection, and a concise result report.
Defer CI, screenshot baselines, elaborate fixtures, and broader accessibility
or security programs until they address a demonstrated need.

## Work usage warnings and interruption checkpoints

Status: proposed workflow enhancement; not a v0.1 site blocker.

Work reached its platform usage limit during release preparation. Existing
Conductor usage-awareness does not prevent exhaustion of Work's own platform quota.
Recognize visible Work usage/rate-limit warnings when available. When remaining
usage appears constrained, checkpoint current state and pending approvals before
starting substantial new work; defer a non-urgent phase likely to be interrupted.
After interruption, verify repository and provenance state before resuming and
never assume an interrupted operation completed. Do not invent, estimate, or
bypass unavailable platform quota information.
