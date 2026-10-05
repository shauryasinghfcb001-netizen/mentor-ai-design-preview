# Skills section (new) — "learn more skills", with grades and a personal mentor per skill

Files: `screens/Skills.dc.html` (phone), `screens/DesktopSkills.dc.html` (laptop).
Entry points: laptop sidebar item "Skills"; phone: navy banner "Learn new skills" at top of Study tab (opens Skills, bottom nav keeps Study active, back arrow returns).

## Concepts
- **Skill** = short course (about 8 lessons) outside school syllabus. Sample catalogue (placeholder, editable data array): Python basics (Tech), Public speaking (Speak), Sheets & Excel (Tech), Money basics (Money), Speed reading (Study), Design thinking (Create), Typing speed (Tech), Note-making (Study).
- **Personal mentor per skill** = an AI persona (e.g. Kavya for Python, Rohan for speaking). Always labelled "AI mentor". Mentor knows the student's level, suggests next lesson, answers in chat. Reuse the existing mentor chat component with a different system prompt/persona; do not build a new AI backend. If no AI is wired, show persona UI + "coming soon" state.
- **Grade** per skill: letter A / B / C+ / D from quiz scores + practice tasks (A needs 85%+). Show in progress ring centre. Placeholder maths: grade = f(average of last 5 scores). Mark "sample" until real data exists.
- **Slots**: free = 3 skills at a time (design shows "2 of 3 free slots used"), Pro = unlimited. 
- **Exam-first rule**: skills capped 30 min/day until boards end; pause skills if weekly plan slips. Show the orange note in UI (design includes it). This protects students and the hackathon story.

## Layout (laptop)
Main grid `1fr + 300px`.
Left: MY SKILLS (2 cards in a 2-col grid: ring+grade, level, progress bar, mentor strip, Continue + Ask buttons) then EXPLORE SKILLS (category chips All/Tech/Speak/Money/Study/Create, 3-col tiles, "Start skill").
Right: dark "Your Python mentor" card (persona, speech bubble, Chat button), "Skill grades" list, "Exam-first rule" warn card.
## Layout (phone)
Back + title; MY SKILLS cards (ring, name, % · grade · mentor); EXPLORE chips + 2-col tiles; exam-first note.

## States to build
Empty (no skills yet: show 3 suggested), Start-skill sheet (pick mentor tone: Friendly / Strict / Hinglish), Lesson screen (lesson text + quick quiz, +credits), Grade detail (history of scores), Certificate for completing a skill (text: "Issued by Mentor.ai — not a CBSE or board certificate").
Only the two screens in /screens are designed; build the extra states with the same components, simple and consistent.

## Done-when
[ ] Skills reachable from sidebar and Study banner  [ ] Tile -> start -> appears under My skills  [ ] Grade ring shows letter  [ ] "AI mentor" label visible  [ ] Exam-first note visible
