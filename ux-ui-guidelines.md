# ux-ui-guidelines.md

---
## AI RULES — READ FULLY BEFORE ANY ACTION
---

1. Read this entire file before designing or building any UI element.
2. These guidelines are not suggestions. Every UI decision must satisfy
   both core principles below before implementation.
3. If unsure whether a UI element is needed → default to removing it.
   It is easier to add than to undo.
4. Never invent a navigation pattern or UI convention from scratch.
   Use what already exists and what users already know.
5. Never hardcode icons. Always specify the icon library, icon name,
   and placement. Let the human implement icons from their own system.

---
## CORE PHILOSOPHY
---

### Principle 1 — PURPOSE
Every UI element must earn its place.

Before building any button, label, form, or control → ask:
  "Does this require a human decision, or can the system handle it?"

- If the system can handle it → automate it. No UI.
- If human judgment is genuinely required → show exactly one
  control, clearly labeled, in the expected location.
- Never add UI as a fallback because automation feels uncertain.
  Uncertainty is a reason to ask the human, not to build a button.

### Principle 2 — FAMILIARITY
Use the cognitive map users already have.

Users spend most of their time in other apps and interfaces.
They arrive with expectations built over years of experience.
Never make them relearn something they already know.

- Follow platform conventions for placement — do not improvise
- Use universally recognized icons — do not get creative with symbols
- Use the language users already know — do not rename familiar concepts
- If a pattern exists in major platforms → use it

---
## PLACEMENT CONVENTIONS
---

Follow these unless the project explicitly overrides them:

**Web / Desktop:**
- Primary navigation → top bar or left sidebar
- Settings / account → top right
- Back / cancel → top left or bottom left
- Primary action (save, submit, confirm) → bottom right or top right
- Search → top center or top right
- Breadcrumbs → top left, below main navigation

**Mobile:**
- Primary navigation → bottom tab bar
- Back → top left
- Primary action → bottom center or floating bottom right
- Settings / profile → top right
- Search → top bar

---
## LABEL RULES
---

- One label per concept. One place per label.
- If the sidebar says "Settings" → the header does not repeat it.
  The subtitle does not explain it. The page title does not restate it.
- Never use synonyms for the same concept across the same screen.
  (Settings ≠ Configure ≠ Preferences — pick one, use it everywhere)
- Labels should describe what the section IS, not explain it.
  Users know what Settings means. Do not define it for them.
- Progressive disclosure: reveal depth only when the user goes deeper.
  The top level is for orientation, not explanation.

---
## ICON RULES
---

- Never hardcode icon SVGs, paths, or inline components.
- When an icon is needed → specify:
    - What the icon represents (e.g. "gear for Settings")
    - Which library to pull it from (e.g. Lucide, Heroicons,
      Font Awesome, Material Icons — or ask the human which they use)
    - Where it is placed relative to its label
- Always pair icons with a visible text label unless the icon is
  universally recognized (home, search, close, back, play, pause).
- Use the same icon for the same concept everywhere in the interface.
  Never use two different icons for the same action.
- Do not invent icons for concepts that don't have an established symbol.
  Use a text label instead.

---
## LAYOUT PATTERN RULES
---

Match the layout to the user flow type. Ask this before choosing
any layout pattern:

**Linear flow** (step-by-step, one direction, clear sequence)
→ Use a progress indicator, stepper, or centered single-screen layout
→ Never use a sidebar — sidebars imply many destinations, not steps

**Multi-section app** (many areas, user navigates freely)
→ Use top navigation or left sidebar with clear section labels

**Single-purpose tool** (one task, minimal options)
→ Use a centered minimal layout. No persistent navigation needed.

**Rule:** Before proposing any layout → identify the flow type first.
State it explicitly and explain why the chosen pattern fits.

---
## COMPONENT SIZING RULES
---

- Size components proportionally to the amount of content they hold
- Do not use a full sidebar for 4 navigation items
- Do not use a full-screen modal for a one-line confirmation
- Do not use a data table for fewer than 5 rows — use a simple list
- Do not use a card grid for a single item
- If a layout element would be more than 30% empty → it is too large

---
## STYLE SPECIFICATION RULES
---

"Minimalist", "clean", "modern" are not instructions — they are
vague words that produce generic output. When a style is requested:

- Ask what minimalist means in this context before building anything:
  fewer elements? more whitespace? no decorative elements?
  muted colors? typography-led? all of the above?
- Never interpret a style word as a license to use default spacing,
  default blue, basic sans-serif, and call it done
- If no style is specified → ask before defaulting to anything

---
## STATE RULES
---

Every interactive element must have all relevant states defined.
Never generate only the happy path. Before marking any UI complete,
confirm these states exist where applicable:

- Default / idle
- Hover / focus
- Loading / in-progress
- Success / confirmation
- Error / failure (with a specific message — not "something went wrong")
- Empty (when there is no data to show)

---
## RESPONSIVE RULES
---

- Never design for one screen size only
- Before building any layout → confirm which platforms this runs on
  (web desktop, web mobile, native iOS, native Android, all of them)
- Do not replicate desktop patterns on mobile
  (no sidebars, no hover-dependent interactions, no tiny tap targets)
- Flag any layout that will break at a different screen size
  before implementing it

---
## TYPOGRAPHY RULES
---

- Use Regular (400) for all body text and general UI text
- Use Semibold (600) for headings, labels, and emphasis
- Do not use Bold (700) or heavier — it feels heavy and outdated
  in modern interfaces
- Do not use more than 2 font weights in the same interface
- Never use italic for UI labels or navigation items
- Font size hierarchy must be consistent across all pages —
  define sizes once and never deviate per page or section

---
## EMOJI RULES
---

- Never use emojis anywhere in the UI — not in labels, headings,
  buttons, navigation, status messages, or placeholders
- Emojis are not clarity. They are visual noise in functional
  interfaces.
- If iconography is needed → use a proper icon from the project's
  icon library, not an emoji as a substitute

---
## CONSISTENCY RULES
---

Consistency means the interface behaves and looks the same across
every page, section, and state. A header that changes size when
navigating to a sub-section is a consistency failure.

- Persistent elements (header, navigation, footer) must have
  fixed dimensions and fixed position — never change regardless
  of which page or section the user is on
- The same component must look and behave identically everywhere
  it appears in the interface
- Spacing, font sizes, colors, and border radius must come from
  a defined set of values — never arbitrary numbers
- If a value is used once → it must be reused everywhere that
  context applies. Never invent a new value for the same purpose.
- Before marking any page complete → check it matches every other
  page in: header height, font sizes, spacing, color usage,
  button styles, and interactive behavior

---
## LAYOUT SHELL RULES
---

Any element that appears on more than one page belongs in the
layout shell — not inside the individual page.

- Header → layout shell
- Navigation → layout shell
- Footer → layout shell
- Sidebar (if used) → layout shell
- Any persistent status bar, toolbar, or banner → layout shell

Elements placed inside the page instead of the shell will move,
shift, resize, or disappear on navigation. This is always wrong.

**Rule:** Before building any multi-page interface → define the
layout shell first. Every page renders inside it.
The shell never re-renders when the user navigates.
Only the content area changes.

---
## SPACING AND SYMMETRY RULES
---

Use the 8px grid system for all spacing. Every margin, padding,
gap, and dimension must be a multiple of 8:
8 — 16 — 24 — 32 — 40 — 48 — 64 — 80 — 96

Use 4px only for tight spaces: icon gaps, small text adjustments.
Never use arbitrary values like 13px, 22px, or 37px.

**Symmetry:**
- Align elements to a consistent central axis or grid column
- Elements at the same level of hierarchy must have equal spacing
  on both sides
- If the layout uses a left and right element of the same type
  → they must be visually balanced in size and weight
- Intentional asymmetry is acceptable but must be deliberate
  and consistent — not accidental

**Root cause of the header-resize problem:**
Header height defined in px on one page but not another, or
padding inconsistent between sections.
Fix: define header height once as a CSS variable or token.
Reference it everywhere. Never hardcode it per page.

---
## INSPIRATION RULES
---

Before designing any UI section, screen, or component → search
for 2 to 3 reference examples from well-designed, widely-used
products. Do not default to patterns already known from training.

- Search specifically for the pattern being built:
  e.g. "student portal upload screen", "queue progress indicator",
  "exam results page UI"
- Present the references to the human before building
- Extract the specific pattern that works — layout, hierarchy,
  spacing approach — and apply it deliberately
- Never generate UI in a vacuum. The best UI borrows from what
  already works well in the real world.

---
## WHAT MUST NEVER HAPPEN
---

- Do not duplicate labels across sidebar, header, subtitle, or page title
- Do not use synonyms for the same concept on the same screen
- Do not invent navigation patterns that don't follow platform conventions
- Do not place primary actions in unexpected locations without flagging
- Do not hardcode icons — always reference a library and ask if unsure
- Do not add explanatory text to labels users already understand
- Do not build UI for a step that can be automated
- Do not duplicate calls to action — if a Sign In link exists in
  the header, there is no Sign In button elsewhere on the same screen.
  One action, one trigger, one place.
- Do not use a sidebar for a linear step-by-step user flow
- Do not generate only the happy path — all states must be defined
- Do not interpret vague style words as instructions — ask first
- Do not design for one screen size and ignore others
- Do not use oversized components for small amounts of content

---
