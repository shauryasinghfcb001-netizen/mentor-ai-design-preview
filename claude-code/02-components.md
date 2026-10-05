# Shared components (build once, reuse on both layouts)

| Component | Spec | Seen in |
|---|---|---|
| Card | `.card` in tokens.css | everywhere |
| Chip | `.chip`; variants: neutral (`#F6F7FB`+border), indigo tint, warn (streak), ok (credits) | laptop topbar, phone headers |
| Tag | `.tag`; PRO = `#FED7AA/#7C2D12` | tiles, plans |
| Button | `.btn` + `.bp` primary, `.bo` outline, `.bw` on-dark | all |
| Segmented control | `.seg` | Plan (Week/Day), Practice modes |
| Progress ring | SVG, centre label (grade letter or %) | Today hero, Skills, Report |
| Progress bar | `.sbar` | chapters, skills |
| Year heatmap | 365 cells, 53 weeks × 7 days, GitHub style, levels l0–l3, month labels on top, legend Less→More. Phone: cell 6px gap 2px, horizontally scrollable. Laptop: cell 11px gap 3px | Today, Profile |
| Mentor pet | CSS pet + speech bubble (white, radius 12/12/12/4, 12px/700) | laptop sidebar, phone Today + Mentor, PetHelp |
| Badge | circle medal icon, locked = grey + lock, progress ring when in progress | Badges |
| Certificate card | for top tier only; text "Issued by Mentor.ai — not a CBSE or board certificate" | Badges, Profile |
| Mentor persona avatar | initial in coloured circle + "AI mentor" label (never imply a human) | Skills, Mentor |
| Bottom nav (phone) | 5 items Today · Plan · Mentor(raised centre 52px) · Study · Progress; height 78px; active = indigo | phone |
| Sidebar (laptop) | 224px navy: logo, Today, Plan, Practice, Study, Skills, Progress, Mentor; MORE: Badges, Answer review, Parent report, Profile; pet card; profile row | laptop |
| Topbar (laptop) | 64px white: title+subtitle left; chips right: days to boards, % course strong, streak, credits | laptop |

## Credits + badges (placeholder rules, show as UI; wire to real data only if a store exists)
Streak badges: Spark 3d, Flame 7d, Blaze 30d, Inferno 100d, Legend 365d (certificate).
Credit badges: Bronze 100, Silver 500, Gold 1,000, Platinum 5,000, Diamond 10,000 (certificate).
Earn: study block +10, daily task +25, quiz +5/question, streak day +5, game +20, weekly reset +15.
