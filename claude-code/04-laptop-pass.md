# PASS B — Laptop (viewport >= 1024px, design frame 1280x800)

Layout shell for every logged-in screen: `display:flex` — sidebar 224px + column(topbar 64px + main). Main padding 18px 24px, gap 14px. Content must FILL the space (user disliked empty laptop layouts): use 2-column grids (main + 300px side column) as in the files.
768–1023px: keep the sidebar but collapse to 72px icon rail; side column drops below main.
Below 768px: use PASS A.

Sidebar items (order): Today, Plan, Practice, Study, Skills, Progress, Mentor. MORE: Badges, Answer review, Parent report, Profile. Bottom: pet card (bubble + pet + Hide), profile row (avatar, name, "Class 12 · Free · Go Pro").
Topbar chips: `119 days to boards` · `59% course strong` · streak `7` · `340 credits` (bind to real values).

## Screens -> source file
1. Sign-in `DesktopSignIn.dc.html` — split layout, parent OTP + consent.
2. Onboarding `DesktopOnboarding.dc.html` — left navy rail with steps + pet; right: 3 path cards (Class 10 / Class 12 [MOST STUDENTS] / Just study), then "Next, for Class 12" subject chips, Back/Next.
3. Today `DesktopToday.dc.html` — hero (ring, countdown, today's task + Done/Partial/Stuck/Skipped), 365-day grid, mentor note, Formula Match game card, badges link.
4. Plan `DesktopPlan.dc.html` — left week list (select a day), centre day detail blocks, right side cards. Switching days must NOT reload.
5. Practice `DesktopPractice.dc.html` — 5 mode cards (what each does in one line) + MCQ practice panel with timer, mistake tagging after answer.
6. Study `DesktopStudy.dc.html` — add-source dashed card, PRACTISE row (6), LEARN+REVISE row (6), notes library, right column: mentor picks, flashcards due, spaced revision.
7. Skills `DesktopSkills.dc.html` — see `05-skills-section.md`.
8. Progress `DesktopProgress.dc.html`. 9. Mentor `DesktopMentor.dc.html` (3 columns: context, chat, actions).
10. Badges `DesktopBadges.dc.html`. 11. Profile `DesktopProfile.dc.html` (365 grid, badges, certificates, settings).
12. Answer review `DesktopAnswerReview.dc.html`. 13. Parent report `DesktopParentReport.dc.html`.

## Done-when
[ ] 1280x800 screenshot matches the file  [ ] 1440 and 1024 widths do not break (no overlap, no empty half-screens)  [ ] Sidebar active state correct on every route  [ ] Keyboard focus visible  [ ] Previous handlers still work
