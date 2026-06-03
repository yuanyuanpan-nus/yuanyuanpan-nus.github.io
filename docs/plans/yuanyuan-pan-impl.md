# Implementation Plan — Yuanyuan Pan

## Task 1 — HTML skeleton
- Single `index.html`, semantic landmarks: `header` sidebar, `main`, `nav`, `footer`
- Load Google Fonts: Fraunces + Source Sans 3
- CSS variables for light/dark themes

## Task 2 — Sidebar
- Portrait `avatar.jpg`, name, affiliation line, email icon link (envelope SVG)
- Theme toggle (sun/moon) top-right of viewport
- Anchor nav to all page-story sections

## Task 3 — About Me
- Render portrait reference in sidebar only; About text from page-story verbatim
- Job market sentence styled with emphasis inside About

## Task 4 — News
- Timeline list with `+` items as chronological entries

## Task 5 — Publications & Preprints
- Each `+` item as publication block: title strong, authors/venue in muted text
- Tag Revise & Resubmit / Accepted / JMP where stated in copy

## Task 6 — Invited Talk, Teaching, Professional
- Prose lists preserving order and wording

## Task 7 — Responsive & a11y
- `@media (max-width: 768px)` stack sidebar above main
- Skip link, `:focus-visible`, `prefers-reduced-motion`, min 44px touch targets on toggle/links

## Task 8 — Theme persistence
- `localStorage` key `theme`, respect `prefers-color-scheme` on first visit
