# Design tokens (full values in tokens.css)

## Fonts
- Display: Bricolage Grotesque 600/700/800 — headings, big numbers, logo.
- Body: Plus Jakarta Sans 400–800 — everything else.
- Sizes: page title 26px (phone) / 22px (laptop topbar); card title 15px/800; body 13–14px; muted 12px; label 11px/800 letter-spacing 1px uppercase; hero numbers 34–56px display 800.

## Colour roles
- Page bg `#F6F7FB`, card `#FFF` + 1px `#E4E6EF`, text `#12142B`, muted `#5B6178`.
- Dark surfaces (sidebar, hero, pet card, mentor header): navy `#1E1B4B`, raised navy `#312E81`.
- Primary action / active: indigo `#4338CA`; hover `#3730A3`; tint `#EEF2FF`; border-tint `#C7D2FE`; on-dark text `#C7D2FE`/`#A5B4FC`.
- Status: success `#15803D` on `#F0FDF4`; warning `#C2410C` on `#FFF7ED` (border `#FED7AA`); danger `#B91C1C` on `#FEF2F2`.
- PRO tag: bg `#FED7AA`, text `#7C2D12`.
- Heatmap levels l0..l3: `#E4E6EF #C7D2FE #818CF8 #4338CA`.
- Ratio: ~70% light surfaces, ~30% dark navy/indigo (user asked 30% dark, not 70%).

## Shape + spacing
- Card radius 18 (laptop) / 14–16 (phone); buttons radius 12, min height 44 (touch target); chips radius 17 height 34; tags radius 7.
- Gaps 8/10/14. Page padding: phone 20px; laptop main 18px 24px.
- Icons: 24×24 viewBox stroke icons, stroke-width 1.9, round caps. Copy SVG paths from the screen files (class `.ic`).

## Motion
- Pet `.bob` 2.4s float. Respect `prefers-reduced-motion`. Progress rings = SVG circle, `stroke-dasharray=2πr`, `stroke-dashoffset=2πr·(1-p)`, svg rotated -90°.

## Pet states (PetStates.dc.html): idle, wave, dance (celebrate), sleepy (no activity), thinking (AI loading)
Tap pet -> quick-help sheet (PetHelp.dc.html). A "Hide" button minimises it (persist choice).

## Accessibility
Contrast AA on all text; every icon-only button has aria-label; focus ring 2px `#4338CA` offset 2px; touch targets >= 44px.
