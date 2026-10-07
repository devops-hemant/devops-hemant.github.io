# Data Model: Professional Resume Website

The website is static and has no persistent database. The following content entities describe the verified information represented in `docs/index.html`.

## Candidate Profile

- **Purpose**: Identify the resume owner and establish their professional focus.
- **Fields**: Full name; professional title or focus; concise summary; optional location; optional approved email and profile links.
- **Validation**: The owner must verify each published value. Do not publish empty labels, private contact details, or invented claims.

## Resume Section

- **Purpose**: Group related qualifications for quick scanning.
- **Fields**: Section heading; display order; zero or more resume entries.
- **Section types**: Experience, skills, education, and optional projects, certifications, or community work.
- **Validation**: Include a section only when owner-provided information supports it. Use descriptive headings and consistent date conventions.

## Resume Entry

- **Purpose**: Describe one role, education item, project, qualification, or skill group.
- **Fields**: Entry type; title or role; organization or institution when applicable; optional dates; optional location; concise description; optional verified outcomes.
- **Validation**: Separate responsibilities from outcomes. Do not infer dates, employers, credentials, or metrics.

## Contact or Profile Link

- **Purpose**: Let a visitor use an owner-approved contact method or professional profile.
- **Fields**: Link label; destination; link type (email or external profile).
- **Validation**: Show only supplied, verified destinations. Omit missing or invalid links; label destinations clearly.

## Relationships and Presentation

- A Candidate Profile has ordered Resume Sections and may have Contact or Profile Links.
- A Resume Section contains zero or more Resume Entries.
- The same verified profile and entry content is presented on screen and in the browser's print/save output.
- Public content requires owner approval before the GitHub Pages publishing source is enabled.
