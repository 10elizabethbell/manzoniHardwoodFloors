---
name: Manzoni Hardwood Floors
description: A one-man floor business in Northern NJ, presented as the floor itself, racked oak taking Special Walnut stain.
colors:
  ground: "#f4f2ec"
  ground-2: "#e9e5dc"
  field-white: "#fffdf9"
  ink: "#2e1f15"
  ink-soft: "#5f4838"
  walnut: "#4a2f1e"
  walnut-deep: "#36221a"
  on-walnut: "#f7efe2"
  on-walnut-soft: "#e6d4bd"
  oak: "#d9b98c"
  tape: "#2a67a8"
  seam: "rgba(46,31,21,.16)"
  error: "#a3321c"
typography:
  display:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(54px, 17.5vw, 124px)"
    fontWeight: 850
    lineHeight: 0.86
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(34px, 9vw, 64px)"
    fontWeight: 850
    lineHeight: 0.95
    letterSpacing: "-0.02em"
  title:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "clamp(24px, 6.6vw, 34px)"
    fontWeight: 820
    lineHeight: 1
    letterSpacing: "-0.015em"
  body:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "17px"
    fontWeight: 400
    lineHeight: 1.55
  label:
    fontFamily: "-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif"
    fontSize: "16px"
    fontWeight: 750
    lineHeight: 1.1
rounded:
  sm: "4px"
  md: "6px"
  round: "50%"
spacing:
  gutter: "20px"
  gutter-wide: "40px"
  gap-sm: "10px"
  gap-md: "16px"
  gap-lg: "22px"
  section: "64px"
  section-wide: "104px"
components:
  button-solid:
    backgroundColor: "{colors.walnut}"
    textColor: "{colors.on-walnut}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    padding: "0 24px"
    height: "58px"
  button-solid-hover:
    backgroundColor: "{colors.walnut-deep}"
  button-line:
    backgroundColor: "transparent"
    textColor: "{colors.walnut}"
    typography: "{typography.label}"
    rounded: "{rounded.md}"
    padding: "0 24px"
    height: "58px"
  button-line-hover:
    textColor: "{colors.tape}"
  input-text:
    backgroundColor: "{colors.field-white}"
    textColor: "{colors.ink}"
    typography: "{typography.body}"
    rounded: "{rounded.md}"
    padding: "14px 16px"
    height: "54px"
  chip-job:
    backgroundColor: "{colors.field-white}"
    textColor: "{colors.ink}"
    rounded: "{rounded.md}"
    padding: "0 16px"
    height: "48px"
  chip-job-checked:
    backgroundColor: "{colors.walnut}"
    textColor: "{colors.on-walnut}"
  service-row-arrow:
    backgroundColor: "{colors.ground-2}"
    textColor: "{colors.walnut}"
    rounded: "{rounded.round}"
    size: "46px"
  service-row-arrow-hover:
    backgroundColor: "{colors.tape}"
    textColor: "#ffffff"
  step-number:
    backgroundColor: "{colors.oak}"
    textColor: "{colors.ink}"
    rounded: "{rounded.round}"
    size: "44px"
---

# Design System: Manzoni Hardwood Floors

## Overview

**Creative North Star: "The Floor Is the Page"**

The site is a racked-out hardwood floor seen from above: random-length oak strips, staggered butt joints, Special Walnut wiped into raw sanded oak. Everything else is the room around that floor. The cream ground is the trim-white wall, the text is walnut ink, and painter's-tape blue shows up only where the visitor touches a control, the way tape marks the edges a tradesman is working to. The floor is live: one shared canvas engine draws the boards, lets a finger wipe stain on, and sands the stain back to raw when the floor is nearly done, so there is always floor to stain.

Density is phone-first and plain-spoken. Heavy uppercase system type, short first-person lines from Kevin, big tap targets (44px floor, 58px buttons), and almost no ornament beyond the wood itself. Depth comes from the floor and from the walnut-coloured bands (care section, footer), not from shadows or cards.

The first screen carries the name, the number, one focal headline, one line of promise, two actions and the floor. There is no sticky bar; the number lives top-right on the first screen and again in the footer.

**Key Characteristics:**
- Cream wall, walnut ink, oak accents; blue only on interaction.
- System font stack throughout, set very heavy (750-900) and uppercase for headings.
- A single canvas floor engine expressed three ways: hero floor, course dividers, static board field behind the photos.
- Rows divided by thin seam lines instead of cards.
- Flat surfaces; one soft shadow under the solid button.

## Colors

A warm, low-chroma wood palette (wall cream, walnut, raw oak) with one cool accent held back for interaction.

### Primary
- **Special Walnut** (`walnut`): the colour of Kevin's own finished floor. Solid buttons, checked chips, the care band background, the Facebook arrow disc, and the 2px borders on buttons and the Facebook panel.
- **Walnut Deep** (`walnut-deep`): solid-button hover and the footer band. The darkest surface in the system.

### Secondary
- **Raw Sanded Oak** (`oak`): the wood before stain. Step-number discs, the dot separators between facts, the spec line on walnut, checked-chip tick boxes, and text selection background.

### Tertiary
- **Painter's Tape Blue** (`tape`): hover borders, hover text, focus outlines (3px, 3px offset), input focus borders with a 3px 22%-alpha halo, the text caret, and the service-row arrow on hover. Nothing else.

### Neutral
- **Trim-White Wall** (`ground`): the page background and browser theme colour.
- **Sanded Oak Dust** (`ground-2`): the estimate band, the Facebook link panel, resting arrow discs, scrollbar track.
- **Field White** (`field-white`): the inside of inputs, unchecked chips and the "text is ready" panel. Slightly brighter than the wall so fields read as fillable.
- **Walnut Ink** (`ink`): all body and heading text on light grounds.
- **Soft Walnut Ink** (`ink-soft`): secondary copy (promise, facts, step detail, helper text, wordmark subline).
- **Cream on Walnut** (`on-walnut`) and **Soft Cream on Walnut** (`on-walnut-soft`): text on walnut surfaces; headings and button labels take the brighter one, paragraphs and footer copy the softer.
- **Seam** (`seam`): 1px rules between service rows, steps and panel edges, like the joint between two boards.
- **Error Red** (`error`): inline validation text and invalid input borders only.

### Named Rules
**The Tape Rule.** Painter's-tape blue appears only on hover, focus and form outlines (borders, caret, focus halo, the hovered arrow). It is never a resting fill, a heading colour, or a decorative accent. If a screen shows blue with nobody touching it, it is wrong.

**The Wood-Not-Paint Rule.** Every warm colour on the page is a stage of the same floor: raw oak, stain, deep walnut, sanding dust. A new surface colour must be one of these or a wall tone, never a new hue.

## Typography

**Display Font:** system stack (-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, Helvetica Neue, Arial, sans-serif)
**Body Font:** the same stack
**Label/Mono Font:** none; phone numbers use tabular numerals from the same stack

**Character:** one familiar face pushed to its heaviest weights, uppercase and tightly tracked for headings; it reads like a lettered work van, not a brochure.

### Hierarchy
- **Display** (850, clamp(54px, 17.5vw, 124px), 0.86; on desktop clamp(84px, 8.4vw, 120px)): the hero headline only, uppercase, -0.035em.
- **Headline** (850, clamp(34px, 9vw, 64px), 0.95): section headings, uppercase, -0.02em, balanced wrapping. The closing name runs larger (clamp(40px, 12vw, 104px), 0.88).
- **Title** (820, clamp(24px, 6.6vw, 34px), 1): service row names, uppercase. Step headings sit at 800, 20px, 1.25, sentence case.
- **Body** (400, 17px, 1.55): default copy. Lead paragraphs step up to 17-22px fluid with 31-36ch measure.
- **Label** (750, 16px): form labels, button text (17px), linked panel text (800, 18px). Phone number in the header 800, 16px (18px from 720px), tabular numerals.

### Named Rules
**The House Stack Rule.** Every pitch site uses the system font stack (Ellie's house rule). Hierarchy comes from weight, case, size and tracking, never from adding a second family or a web font.

**The Heavy-Headings Rule.** Headings are uppercase at 820-900 weight with negative tracking and line-height under 1. Body copy stays sentence case at 400.

## Layout

A single centred column (max 1180px) with 20px gutters on phones and 40px from 720px. Sections stack with 64px vertical padding, 104px from 1024px. Breakpoints are 720px (CTA buttons go side by side, photos go two-up at 1.337fr / 1.065fr, course dividers grow from 52px to 64px) and 1024px (hero becomes a two-column grid, copy left at 1.15fr and floor right at 1fr, min-height min(88svh, 780px); content sections become a 1fr / 1.2fr "split" with the heading left and the content right, 64px gap).

On phones the hero floor is a strip clamp(200px, 32svh, 320px) tall under the copy. The work photo field bleeds to the screen edge on phones (negative gutter margin) and sits inside the column on wider screens.

Rhythm is built from 10, 12, 16, 20, 22 and 26px gaps; there is no strict scale.

**The First-Screen Number Rule.** The phone number appears once on the first screen, top-right, as a plain tap-to-call link. There is no sticky bar or floating call button. The footer carries the number a second time, with Facebook.

## Elevation & Depth

The system is flat. Depth comes from the floor canvases and from full-bleed walnut bands, not from lifted cards. The few shadows present are functional.

### Shadow Vocabulary
- **Solid button lift** (`box-shadow: 0 6px 16px -8px rgba(54,34,26,.7)`): resting state of solid walnut buttons only, a soft contact shadow.
- **Focus halo** (`box-shadow: 0 0 0 3px rgba(42,103,168,.22)`): inputs, chips and the form submit button on focus or hover. A state, never a resting shadow.
- **Inlay set** (`box-shadow: inset 0 1px 3px rgba(40,22,10,.6), 0 0 0 2px #24150c`): photos framed like inlays let into the board field.

### Named Rules
**The Flat-Floor Rule.** Surfaces don't float. Use a walnut band, a seam line or the floor itself to separate content; add a shadow only for the solid button or a state.

## Shapes

Gently softened corners (6px) on buttons, inputs, chips and panels; 4px for the focus outline and the hint tag; 3px on the chip tick box; full circles (50%) for arrow discs and step numbers. Section bands, the floor canvases and the photo inlays are square-edged: wood is cut straight. Borders are 2px on controls and 1px seam lines between rows.

## Components

### Buttons
Solid and plain, like a work truck's lettering.
- **Shape:** softened corners (6px), 58px tall, 24px side padding, 2px walnut border, optional 20px stroke icon left of the label.
- **Solid:** walnut fill, cream label, soft lift shadow. The primary text action ("Text Kevin a photo").
- **Line:** transparent with walnut label and border. The secondary action.
- **Hover / Focus:** solid darkens to walnut-deep and its border turns tape blue; line button's border and label turn tape blue. Transitions 0.18s. Active nudges down 1px. In the form, the submit button also gains the blue focus halo.

### Chips
- **Style:** job-type checkboxes shown as 48px chips with a 16px tick box, field-white fill, 2px border at 28% walnut.
- **State:** hover turns the border blue; checked wipes a walnut fill in from the left (background-size 0.35s, cubic-bezier(.2,.7,.2,1)) like stain going on, with cream text and an oak tick box.

### Cards / Containers
There are no cards. Containers are full-width bands (walnut for the care section, ground-2 for the estimate, walnut-deep for the footer) and two small panels: the Facebook link (ground-2 fill, 2px walnut border, 6px radius, 68px tall) and the "text is ready" panel (field-white fill, 1px seam border).

### Inputs / Fields
- **Style:** field-white fill, 2px border at 28% walnut, 6px radius, 54px minimum height (textarea 110px), 17px text.
- **Focus:** border turns tape blue with the 3px blue halo; hover turns the border blue without the halo. Caret is tape blue.
- **Error:** border and 14px message in error red; the message appears under the field only after a failed submit.

### Navigation
There is no menu. The header is the wordmark (name in 900 uppercase 21px, "Hardwood Floors" beneath at 12px tracked uppercase in soft ink) on the left and the phone number on the right, both 44px tap targets. The number turns blue on hover.

### Service Rows
Each service is a full-width row (76px min) between seam lines: the name in Title style and a 46px arrow disc on the right. The whole row is the link (an SMS with a pre-written message), but **only the arrow reacts**: on hover or focus the disc fills tape blue with a white arrow, and focus draws the outline around the disc, not the row. The row itself never changes background or gains a shadow. The Facebook panel uses the same arrow disc (walnut at rest, blue on hover).

### Steps
A numbered list between seam lines; each number sits in a 44px oak disc beside a bold one-line step and a soft-ink detail line.

### Floor Engine (signature)
One canvas engine draws a racked floor (random-length strips, staggered joints, per-board grain, flecks and shading, seeded so it is stable), runs a wet-stain simulation on a 5px grid, and blends between a raw-oak and a Special Walnut board palette through the stain mask. A single shared `requestAnimationFrame` loop ticks every instance, pauses instances that are off-screen (IntersectionObserver) or when the tab is hidden, and caps device pixel ratio at 1.5. It is expressed three ways:
- **Hero floor:** auto mode, starts half-stained to a ragged line like a job in progress. After 2.6s without a touch a rag works along the least-stained course; at 90% coverage the floor is left alone for 3.2s, then a sanding pass lifts it back to raw. A "Wipe on the stain" hint tag fades on first touch.
- **Course dividers:** 52px (64px from 720px) strips between sections, exactly two courses tall, auto mode, alternate ones starting half-done.
- **Board field:** a fully stained, still floor behind the work photos; it only computes while being touched or while wet stain is still settling. The photos sit on it as inlays in an oak frame.

Tunables live at the top of the engine: `CELL` 5, `ALONG` 0.12, `ACROSS` 0.05, `SEAM` 0.004 (stain runs fast along the grain, slow across, barely over seams), `SOAK` 0.07, `DRY` 0.992, `BRUSH` 1.25 rows, `RAG` 0.7 rows, `AUTO_SPEED` 240px/s, `SAND_SPEED` 260px/s, `HOLD` 3200ms, `SAND_AT` 0.9, `IDLE` 2600ms. Under reduced motion auto mode is off and the floor is a still frame that still stains under a finger. A CSS gradient fallback draws stained and raw courses until the canvas paints.

## Do's and Don'ts

### Do:
- **Do** keep tape blue (`tape`) for hover, focus and form outlines only.
- **Do** use the system font stack for every role and get hierarchy from weight (750-900), uppercase and tight tracking.
- **Do** drive any new floor surface through the shared Floor engine and its single animation loop, and tune behaviour through the named tunables rather than per-instance code.
- **Do** separate list content with 1px seam lines and full-width bands rather than cards.
- **Do** keep tap targets at 44px minimum and primary buttons at 58px.
- **Do** let only the arrow disc react on service-style rows.
- **Do** keep warm colours to wall, oak and walnut stages of the floor.

### Don't:
- **Don't** add a sticky call bar or floating button; the number lives top-right on the first screen and in the footer.
- **Don't** use blue as a resting fill, heading colour or decoration.
- **Don't** add a web font or second family.
- **Don't** start a second `requestAnimationFrame` loop for a floor surface.
- **Don't** add cards, lifted panels or hover backgrounds to rows.
- **Don't** reuse the wordmark's tracked 12px uppercase subline as a label above section headings; it belongs to the name only.
