# AGENTS.md

This repository is a static site for the Abercrave Miners Welfare Hall consultation.
It uses plain HTML and CSS with no build system or test runner configured.

## Quick context
- Audience: community consultation, bilingual (English/Welsh).
- Stack: static HTML/CSS only.
- Assets: logo, photos, and a color palette under `assets/`.

## Build / lint / test commands
There is no build, lint, or test tooling configured in this repo.

If you add tooling later, document it here and keep commands minimal.

### Current (no tooling)
- Build: not required (static files served directly)
- Lint: not configured
- Test: not configured
- Single test: not applicable

### Optional local preview
- Use any static server to preview, e.g.:
  - `python -m http.server 8000`
  - `npx serve .`

## Repository structure
- `index.html` language chooser page
- `en/index.html` English consultation page
- `cy/index.html` Welsh consultation page
- `styles/main.css` global styles
- `assets/` images, logo, palette files

## Source-of-truth content
- Consultation content is in HTML pages (`en/index.html`, `cy/index.html`).
- Avoid duplicating content in multiple places unless needed for bilingual parity.

## Code style guidelines

### General
- Keep content clear, community-first, and accessible.
- Maintain bilingual parity: any structural change in one language should be mirrored in the other.
- Prefer minimal, semantic HTML and readable CSS.
- Avoid introducing JavaScript unless strictly necessary.

### HTML conventions
- Use semantic elements: `header`, `main`, `section`, `nav`, `footer`.
- Keep heading hierarchy logical: one `h1` per page, then `h2`, `h3`.
- Use short, descriptive `alt` text for meaningful images.
- Keep links descriptive (“Download the 10-Year Plan (PDF)”).
- Preserve accessibility: skip link, focusable elements, and readable copy.

### CSS conventions
- Use CSS variables defined in `:root` for colors and layout constants.
- Reuse existing utility classes (`.section`, `.container`, `.panel`, `.grid`).
- Prefer `clamp()` and responsive units for typography.
- Avoid inline styles unless a one-off is truly necessary.
- Keep animations subtle; respect `prefers-reduced-motion`.

### Imports and assets
- Use absolute paths from site root (e.g. `/styles/main.css`).
- Store images in `assets/photos/` and logos in `assets/`.
- Use web-friendly filenames (lowercase, hyphens, no spaces) if adding new assets.
- If renaming assets, update both English and Welsh pages.

### Formatting
- Two-space indentation in HTML and CSS.
- One attribute per line for long tags or when readability improves.
- Keep line lengths reasonable (around 100–120 chars) for readability.

### Naming conventions
- CSS classes: lowercase with hyphens (e.g. `.photo-card`).
- IDs: lowercase, hyphenated, used for anchor navigation (`#consultation`).
- File names: lowercase, hyphenated for new files.

### Copy and content
- Keep sentences short and plain.
- Use inclusive, non-political language.
- Avoid jargon; explain grants or plans in everyday language.
- Maintain consistent terminology across both languages.

### Accessibility requirements
- Ensure contrast remains high enough (use palette thoughtfully).
- Keep body text large (16–18px+).
- Provide visible focus states.
- Do not rely on color alone to convey meaning.

## Error handling
- No runtime logic is present (static site). If adding scripts later:
  - Fail gracefully; avoid blocking content rendering.
  - Validate external links or form URLs.

## External links and forms
- Consultation form links are external (e.g. Google Forms).
- Always update both languages with the same destination.
- If using an external form, include a brief privacy note.

## Bilingual guidance
- Keep structure and section order identical in `en/` and `cy/`.
- Update the language toggle on both pages if paths change.
- Keep meta title/description aligned in meaning.

## Images and logos
- Use `assets/logo.png` for brand mark.
- Primary photo currently in `assets/photos/`.
- If you add images, optimize size (1600–2400px width for hero photos).

## Palette usage
- Reference palette values in `assets/palette/abercrave_palette.md`.
- Do not introduce new colors unless necessary.

## If you add tooling
- Add a `package.json` with explicit scripts for build/lint/test.
- Update this file with exact commands and single-test instructions.
- Prefer lightweight tooling suitable for a static site.

## Missing agent rules
- No `.cursor/rules/`, `.cursorrules`, or `.github/copilot-instructions.md` detected.

## Suggested update checklist
- Update both language pages.
- Check anchors still work.
- Validate external links.
- Run a quick visual check on mobile widths.
