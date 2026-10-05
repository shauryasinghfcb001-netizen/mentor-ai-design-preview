# Mentor.ai reskin — instructions for Claude Code

GOAL: make the new design live in the EXISTING app (https://cbse-90-board-mentor.netlify.app/). FRONTEND ONLY.
Do NOT rewrite logic, storage, AI calls, routing rules or data. Same features, new look, new name.

## Hard rules
1. Do not break the working flow. Hackathon deadline Oct 11; exams Oct 13. Small commits, one screen per commit, test after each.
2. Work on a git branch `reskin`. Netlify deploy-preview first. Merge only after a human checks the preview.
3. Name: "SHAURYA" -> "Mentor.ai" in all visible text, title, meta, favicon alt, manifest. Keep internal variable/file names unless trivial.
4. Never invent features. If a design element has no logic behind it (badges, credits, skills, games, parent report), render it as UI with clearly marked sample data and a `// TODO(real data)` comment. Never fake claims (guaranteed marks, real board certificates).
5. Certificates must say: "Issued by Mentor.ai — not a CBSE or board certificate."
6. DPDP/under-18: no public leaderboards with names/photos, no ad/analytics pixels on logged-in pages.
7. No new dependencies unless unavoidable (fonts via Google Fonts link only).

## Run order (this folder = /claude-code)
Step 0  Inspect the repo. Report: framework, how screens/tabs are built, where CSS lives, build+test commands. Do not guess.
Step 1  Read `tokens.css` + `01-design-tokens.md`. Add tokens + base components to global CSS.
Step 2  Run PASS A: `03-mobile-pass.md` (phone layout, <= 767px).
Step 3  Run PASS B: `04-laptop-pass.md` (>= 1024px; 768–1023 = scaled laptop layout, see file).
Step 4  Skills section: `05-skills-section.md` (both layouts).
Step 5  `06-rename-domain-checklist.md`.
Step 6  Verify with the checklist at the bottom of each pass. Screenshot every screen at 390px and 1280px.

## Source of truth
`../screens/*.dc.html` hold exact markup + inline CSS for each screen (open as plain HTML; ignore `<x-dc>`, `<helmet>` wrappers, `support.js`, and the final `<script type="text/x-dc">`). Copy structure, spacing, colours and copy from them. Where this doc and a screen file disagree, the screen file wins.
`../canvas.json` = layout map of boards. Live canvas: https://claude.ai/artifact/PoQb45zDkUzv4wx3rJ2MY4

Sample data in the designs (Aarav, Class 12, 119 days to boards, streak 7, 340 credits) is PLACEHOLDER: bind to the app's real values where they exist.
