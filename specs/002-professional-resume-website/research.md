# Research: Professional Resume Website

## Decision: Use dependency-free static HTML and CSS

**Rationale**: The feature is a single public resume page with no form, account, or dynamic data requirement. Semantic HTML and CSS satisfy the required reading, navigation, responsive presentation, and print behavior while keeping the site fast and compatible with GitHub Pages. Avoiding JavaScript for essential content also keeps the page useful when scripts are unavailable.

**Alternatives considered**: A client-side framework or server-rendered application would add dependencies and runtime complexity without enabling a required user journey. A backend is outside the initial scope and conflicts with the static-first project constitution.

## Decision: Publish only the `docs/` directory with GitHub Pages branch publishing

**Rationale**: GitHub Pages can publish static site files from a repository's `docs/` directory. This keeps `.specify/` planning files and development guidance outside the public website and avoids adding a custom deployment workflow. Relative links preserve correct asset loading when the site is served from a repository subpath.

**Alternatives considered**: Publishing the repository root risks exposing internal planning files. A custom workflow or third-party hosting service is unnecessary for this no-build static site.

## Decision: Use a restrained, modern editorial visual system

**Rationale**: The user asked for a professional, trendy appearance and decent colors. Use deep ink/navy `#17324D` for headings and high-emphasis elements, warm off-white `#F8F7F4` as the page background, dark readable body text, and teal `#147D7B` for links and small accents. A muted amber `#D4A24C` may be used only for decorative detail, never as small text on a light background. Favor generous whitespace, a clear typographic scale, thin dividers, and restrained experience timeline details over gradients, excessive cards, or motion. Check all text/background pairings against WCAG 2.2 AA contrast requirements.

**Alternatives considered**: Highly saturated backgrounds, gradients, and large decorative effects can reduce readability and undermine a resume's credibility. Remote fonts and embedded imagery add privacy, availability, and performance costs, so use system font stacks and local owner-approved assets only when they add value.

## Decision: Treat owner-approved facts as the source of truth

**Rationale**: The spec and constitution prohibit inventing resume facts. Use only information confirmed by the owner, omit unsupported optional sections, and hold publication of any unapproved personal details until reviewed.

**Alternatives considered**: Filling gaps with plausible sample employers, dates, skills, or achievements would misrepresent the candidate and is prohibited.

## Decision: Use browser-native print/save behavior

**Rationale**: A print-specific stylesheet can produce a clean standalone resume from the same verified page content without maintaining a second, potentially inconsistent copy or adding a PDF-generation dependency.

**Alternatives considered**: A separate downloadable file can be considered if later required, but is not necessary for the specified print/save journey.
