# Abercrave Miners Welfare Hall Consultation साइट

This repository hosts a bilingual (English/Welsh) static website for the Abercrave
Miners Welfare Hall 10-year plan consultation. It shares the plan, explains the
phased priorities, and gathers community feedback through an external form.

## Purpose
- Provide a clear, accessible overview of the 10-year plan.
- Invite feedback from residents, families, young people, representatives, and funders.
- Support transparency and community engagement.

## Structure
- `index.html`: language selection landing page
- `en/index.html`: English consultation page
- `cy/index.html`: Welsh consultation page
- `styles/main.css`: global styles and palette usage
- `assets/`: logo, photos, and palette files

## Local development
Option 1 (Python):
```bash
python -m http.server 8000
```
Visit `http://localhost:8000/`.

Option 2 (Node):
```bash
npx serve .
```

Option 3 (Vercel dev):
```bash
npm run dev
```

## Deployment flow (GitHub → Vercel)
1. Push changes to GitHub.
2. Vercel detects the push and deploys automatically.
3. Use Vercel’s preview URLs to review changes before production.

## Notes
- Keep English and Welsh pages in sync (structure and section order).
- Update the consultation form link in both languages.
- Assets should use lowercase, hyphenated filenames.
