# Portfolio v0.1 — Product & Design Direction

This document preserves the agreed product, design, and engineering-process
decisions for the Frank Fulcomer portfolio site. It guides v0.1 implementation
and later evolution. It does not specify implementation details.

## Purpose & audience

The site is a professional portfolio for an experienced software professional
working across software quality, systems, requirements, implementation, automation,
and communication in healthcare, financial services, and enterprise software.
That experience is extending into software development and AI-assisted engineering.

Audience: recruiters, hiring managers, engineers, and interviewers. Content
must present that experience authentically while remaining appropriate for
all of these readers.

First impression goal: experienced, competent, thoughtful, approachable.
More personality may emerge naturally as visitors explore deeper.

## Design & content principles

- Elegant simplicity over showiness. v0.1 must be polished and intentional,
  not elaborate or flashy.
- Clean, mature, technically current visual style: strong typography,
  generous whitespace, restrained visual elements, subtle technical
  character.
- Primarily light presentation; darker/high-contrast sections are acceptable
  where they improve the design.
- Avoid stereotypical developer-portfolio decoration: gratuitous gradients,
  glowing controls, fake terminals, skill meters, excessive animation, walls
  of technology logos.
- A circular professional photo is part of the site's visual identity and
  may be used prominently but understatedly.
- GitHub and LinkedIn are prominent destinations. A resume download/link is
  not required for v0.1.
- Content is authentic without oversharing: "Authentic, edited — not
  manufactured."
- Use plain English; prefer "financial services" to unnecessary industry shorthand.
  Avoid résumé clichés, inflated claims, generic corporate language, AI hype, and
  unnecessary first-person repetition.
- Let meaningful content determine layout. The five Experience dimensions are
  intentional; do not invent or remove a dimension to satisfy grid symmetry.
- Featured projects communicate the engineering problem, purpose, approach,
  and evidence — not just a technology list.

## Engineering & scope principles

- **Enough** is a core engineering principle: documentation, requirements,
  architecture, code, tests, security work, accessibility work, automation,
  and process should be sufficient for their purpose without becoming work
  for its own sake.
- Avoid scope creep and premature engineering.
- At the same time, today's implementation should not make foreseeable
  future development unnecessarily expensive.
- Guiding formulation: **"Right-sized today. Extensible tomorrow."**

## v0.1 scope

Accepted homepage narrative:

- Hero / positioning
- How I Work
- Conductor process
- Featured work
- Experience (software quality, systems & requirements, software
  implementation, test automation, communication)
- GitHub / LinkedIn / contact navigation

The narrative moves from who I am, to how I work, to how I apply AI-assisted
engineering, to evidence of the work, and then professional experience. How I Work
states the six accepted engineering principles explicitly. AI-Assisted Engineering
and Experience are the two dark visual anchors; the other content sections use
the existing light palette, and the pale-gray footer closes the page.

Accepted hero descriptor: "Software Quality · Systems · Requirements · Automation".

Accepted supporting copy: "Experienced software professional working across
software quality, system testing, requirements-based verification, test automation,
and regulated healthcare software, now extending that experience into software
development and AI-assisted engineering."

Likely featured projects:

- Job Search Hub
- Job Search Hub Tests
- AI Development Workflow / Conductor
- QA Automation Framework

Implementation specifics (layout, copy, markup) are intentionally not fixed
here; this document records direction and constraints, not a spec.

## v0.1 responsive design & browser requirements

Responsive Web Design (RWD) and mainstream browser compatibility are release
requirements for v0.1, not optional future polish.

- The minimum supported viewport width is 320 CSS pixels. At that width
  and greater, the site must remain functional, readable, visually coherent,
  and free of horizontal page-level scrolling across desktop, tablet, and
  mobile viewports. Layout and content may reflow as necessary. Below
  320 CSS pixels, graceful degradation is desirable but outside v0.1 scope.
- Content must reflow naturally within the available width. Project cards,
  engineering steps, and experience grids must collapse appropriately.
- Hero text, portrait, profile/contact links, section introductions,
  engineering steps, experience content, and footer must remain readable
  and well balanced, with appropriate spacing and readable line lengths.
- Section introductions may use a wider reading measure, but their width
  must remain fluid and fit their container at every supported viewport.
- Supported layouts must avoid horizontal scrolling, clipped content, and
  overlapping elements, and provide touch-friendly navigation/contact links.
- Use content-driven breakpoints rather than specific device models.
  Validate representative widths of approximately 320, 375, 768, 1024, and
  1440 CSS pixels, breakpoint boundaries, and 200% browser zoom/reflow
  where practical.
- Target current Chrome, Microsoft Edge, Firefox, and Safari on desktop,
  Chrome on Android, and Safari on iOS. Equivalent content, functionality,
  accessibility, and reasonably consistent presentation are required;
  pixel-identical rendering is not.
- Prefer standards-based HTML and CSS. Add compatibility fallbacks or
  browser-specific adjustments only when an actual supported-browser issue
  warrants them. Automated checks and viewport emulation supplement rather
  than replace real-browser and device validation.

Validation evidence and human acceptance results are recorded in
[validation.md](validation.md). Exploratory resizing supplements the defined
representative widths; observations below 320 CSS pixels do not expand support.

## The Conductor process

Conductor is the AI-assisted development process used to build this site
and other featured projects, and is a key differentiator of this portfolio.

Conductor keeps human engineering judgment, intent, review, and approval
central, while AI assists with implementation, analysis, review,
documentation, and testing. AI is presented pragmatically as an engineering
tool, not as a replacement for human judgment.

## Provenance & private records

Significant development-session transcripts and AI provenance are retained
privately when technically available (locally, outside the published site
and outside version control — see the local `.ai/` workflow configuration).

Durable engineering conclusions that belong in the public record are
captured in concise project documentation such as this file. Private
transcripts are a source for that documentation, not publication material
themselves, and are not published as part of site content.

## Future direction (beyond v0.1)

The site itself may become portfolio evidence over time, including:

- Requirements and design/architecture decisions with traceability
- Testing, CI/CD
- Accessibility/WCAG coverage
- OWASP/security coverage
- Evidence and results

None of these are required for v0.1. They are recorded here so that v0.1
choices don't foreclose them.

## Release & approval boundaries

- Development is local-first. Frank reviews the working site before commit,
  push, or deployment.
- Approval of working changes does not authorize commit.
- Commit does not authorize push.
- Push/deployment require separate, explicit authorization.
