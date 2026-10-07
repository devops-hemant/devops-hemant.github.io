<!--
Sync Impact Report
- Version change: 1.1.0 → 1.2.0
- Principles: Added Principle VI for Website and PDF Consistency; Additional Constraint added for resume PDF backup retention
- Sections: Additional Constraints updated to require synchronized website/PDF content updates and PDF backup retention
- Removed sections: none
- Follow-up TODOs: none
-->

# Resume Website Constitution

## Core Principles

### I. Accurate, Useful Resume Content
The resume MUST represent only career, education, skill, and achievement information verified
and approved by its owner. Content MUST prioritize relevance, clarity, and evidence of impact;
it MUST NOT invent facts or imply qualifications the owner has not confirmed. This protects
the candidate's credibility and gives visitors an honest basis for evaluating fit.

### II. Accessibility Is a Release Requirement
All public pages MUST conform to WCAG 2.2 Level AA. Core information and actions MUST be
usable with a keyboard, have meaningful structure and labels for assistive technology, retain
sufficient text and control contrast, and remain usable when text is enlarged. Motion MUST
respect reduced-motion preferences. Accessibility defects in a primary resume or contact
journey MUST be fixed before release because the site must work for every visitor.

### III. Static-First GitHub Pages Delivery
The published site MUST be deliverable as static content through GitHub Pages. A visitor MUST
be able to read the resume and reach its essential links without a server-side service or
client-side scripting being available. Releases MUST work at the configured GitHub Pages URL,
including a repository subpath when applicable. A feature that requires a backend or other
hosting service requires a separate approved specification and an explicit constitution
amendment before adoption.

### IV. Privacy and Safe Public Information
Only information the owner has explicitly approved for public display MAY be published.
Credentials, private keys, tokens, and non-public personal data MUST NOT be committed to the
repository or shipped to visitors. Tracking, cookies, embedded third-party content, and forms
that collect personal information MUST NOT be introduced without a separately reviewed need,
privacy disclosure, and owner approval. External resources MUST be minimized and MUST NOT be
required to access the core resume.

### V. Performance and Maintainability
The site MUST prioritize fast access to resume content, optimized media, and minimal page
weight. When sufficient real-user measurements exist, Core Web Vitals MUST meet the "good"
thresholds at the 75th percentile: Largest Contentful Paint at most 2.5 seconds, Interaction
to Next Paint at most 200 milliseconds, and Cumulative Layout Shift at most 0.1. Before
field measurements exist, release checks MUST use repeatable lab measurements and address
obvious regressions. Changes MUST remain as simple as possible while preserving accessibility,
privacy, accuracy, and the static-hosting constraint.

### VI. Website and PDF Consistency
Any content, styling, or hierarchy change made to the website resume MUST be mirrored in the
printable PDF resume, and any change made to the PDF MUST be reflected in the website unless a
print-specific adjustment is required for page breaks, margins, or other pagination-related
constraints. Both outputs represent the same official resume and MUST retain the same verified
facts, labels, ordering, and visual hierarchy; print-only adjustments may differ only where
necessary to support PDF delivery and legibility.

## Additional Constraints
- The initial product is one candidate's resume and public professional website; multi-user accounts, private dashboards, and job-application management are outside scope.
- The owner MUST approve personal contact details, profile links, and any optional portfolio material before publication.
- The site MUST remain readable on common phone and desktop viewport sizes and printable as a complete resume without controls obscuring its content.
- The website and the downloadable or printable PDF MUST remain synchronized: any update to content, labels, ordering, or styling in one format MUST be reflected in the other unless the change is limited to print-only pagination or margin adjustments.
- A current backup of the official resume PDF MUST be retained at all times so the project can recover the latest approved resume version if a regenerated copy is edited, lost, or replaced inadvertently.
- External fonts, scripts, images, and embeds MUST have a documented purpose and a safe fallback; they MUST NOT prevent visitors from reading the core resume if unavailable.
- Any proposed feature that conflicts with these constraints MUST be explicitly scoped and reviewed as a constitutional exception before implementation.

## Development Workflow

- Before release, the owner MUST review the resume facts and public personal information for accuracy and approval.
- Each release MUST verify primary page navigation and links, keyboard access to key actions, responsive readability, print output, and availability at the configured GitHub Pages path.
- Each release MUST include an accessibility review against WCAG 2.2 AA and a performance regression check appropriate to the available measurement data.
- Reviewers MUST check that no secrets or unapproved personal information are included in published content or assets. Issues violating Principles I, II, or IV block release.
- A change that introduces dynamic services, new data collection, or non-static hosting MUST receive an approved specification and constitution amendment before work begins.

## Governance

This constitution governs product specifications, design decisions, implementation, and
release approval for the resume website. Every change review MUST verify applicable principles
and constraints. The owner approves public content and releases. Exceptions MUST state their
scope, rationale, risk, mitigation, approver, and expiry or review date; exceptions may not
waive factual accuracy, protection of secrets, or accessibility of the core resume.

Amendments require a documented rationale and owner approval before affected work proceeds.
The amendment MUST include a Sync Impact Report, identify affected specifications or practices,
and update the version and amendment date. Versioning follows semantic versioning: MAJOR for
backward-incompatible governance changes, MINOR for new or materially expanded principles or
constraints, and PATCH for clarifications that do not change obligations. Reviewers MUST
resolve conflicts in favor of this constitution until it is formally amended.

**Version**: 1.2.0 | **Ratified**: 2026-10-07 | **Last Amended**: 2026-10-07
