# Portfolio site plan

## Goal

Build a static personal portfolio for `yukobayashi0811.github.io`, publishable from the GitHub repository's `main` branch and `/` (root) through GitHub Pages, with no separate app or build step.

## Direction

- Classic, understated, light-only visual direction inspired by the classic feel of https://shinnoguchiphotography.com/.
- A responsive single-column layout, semantic HTML, accessible contrast, and restrained typography.
- Four Markdown pages: Home, About, Work Experience, and Contact; shared navigation and footer.
- Use only the approved public bio: “Full-time MBA Candidate at Berkeley Haas ’27.” Do not invent roles, achievements, projects, dates, or metrics.
- Mark missing biography, detailed experience, and contact destination clearly as placeholders. Do not publish an email address or add a `mailto:` link.

## Implementation

- Put `index.md`, `_config.yml`, page Markdown files, `_layouts/`, `_includes/`, `assets/`, `README.md`, and the favicon directly in the repository root. Use YAML front matter and Jekyll URL filters; leave `baseurl` empty.
- Add GitHub Pages-compatible SEO tags and sitemap, with no backend, database, blog, CMS, trackers, or unnecessary JavaScript.
- Replace the existing workspace app/monorepo scaffold so the **entire project root** is the Jekyll site. This removes the current preview app and API scaffolding rather than nesting the site inside them.
- Document content updates, local preview, GitHub Pages publishing from `main` and `/`, and Lighthouse checks in the README.
- Verify the root structure, links, 375px and 1280px layouts, and aim for Lighthouse scores of at least 90 in all four categories.

## Assumptions and open content

- The site owner’s public display name has not been provided; use a visibly marked placeholder until supplied.
- Detailed About and Work Experience copy has not been provided; do not infer it from the school, sponsor, or reference site.
- No public contact URL was supplied; show a clearly marked placeholder rather than a nonfunctional contact action.
- The reference site is a visual preference, not a source of your personal information or content.

Approved and built as a root-level Jekyll repository. The original app scaffold was removed.