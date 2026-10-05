# PASS A — Mobile (viewport <= 767px, design frame 390x844)

Implement as a responsive layout inside the existing app: keep all routes/tabs/handlers, restyle markup. Max content width 430px centred on larger phones. Safe-area padding at bottom for nav.

Global: bg `#F6F7FB`; page padding 20px; bottom nav fixed (78px) — content needs 90px bottom padding.

## Screens -> source file -> notes
1. **Login** `screens/Login.dc.html` — "A · Parent sign-in + consent". Parent phone OTP first, consent checkbox + what we store, link to privacy. Keep existing auth if any; if none, render UI only.
2. **Onboarding** `Onboarding.dc.html` — step flow. NOTE: design shows 2-chip class picker; final product is 3 paths (Class 10 / Class 12 / Just study) — use the 3-path pattern from `DesktopOnboarding.dc.html` stacked vertically as 3 full-width cards. Steps: path -> subjects -> board date -> last marks -> language.
3. **Today** `Main.dc.html` — dark navy hero with progress ring + countdown; "Today's one task"; steps list; Formula Match game card (locked until task done; `done` state toggles lock); streak heatmap (compact 365); pet bubble. Keep existing task logic; bind ring to existing % strong.
4. **Plan** `Plan.dc.html` — week strip + day blocks as cards (time, subject, chapter, method, minutes, why). Primary block highlighted.
5. **Mentor** `Mentor.dc.html` — navy header with pet, context chips (Class, days left, weak subject), action cards (I can't focus / Reduce my workload / Done-Partial-Stuck), chat area, undo toast. Keep existing local mentor logic and AI key flow.
6. **Study** `Study.dc.html` — add-source card (PDF/YouTube/Notes photo/Lecture audio), Skills entry banner (navy, links to Skills), PRACTISE 3x2 tiles, LEARN + REVISE 3x2 tiles, PRO tags.
7. **Progress** `Progress.dc.html` — course strength, subject bars (Physics weakest 41% sample), mistake types, predicted range (label as estimate).
8. **Answer review (Pro)** `AnswerReview.dc.html` — photo upload, marks, mistake tags.
9. **Account/Profile** `Account.dc.html` — avatar, 365 heatmap, badge row, Pro card, settings list (language, notifications, privacy, delete my data).
10. **Parent report** `ParentReport.dc.html` (390x1240, scroll) — week grade, stats, minutes bars, subject grades, credits, mentor note, WhatsApp share button. Plain progress tone, no marketing.
11. **Badges** `Badges.dc.html` — streak + credit tracks, certificate for top tier.
12. **Pet help sheet** `PetHelp.dc.html` — opens when pet tapped. **Pet states** `PetStates.dc.html` — reference only.
13. **Skills** `Skills.dc.html` — see `05-skills-section.md`.

## Mobile-specific rules
- Single column; grids: 3 cols for tiles, 2 cols for skill tiles.
- Heatmap scrolls horizontally, starts scrolled to today.
- Pet: only on Today + Mentor + PetHelp (not every screen).
- Keyboard: inputs `font-size >= 16px` to stop iOS zoom.

## Done-when (per screen)
[ ] Matches screenshot of the .dc.html at 390px (colours, spacing, copy)  [ ] No horizontal page scroll  [ ] All previous handlers still work  [ ] No console errors  [ ] Name says Mentor.ai
