# Auris — Design system

Derived from `auris-brand-guidelines.pdf` (2026) and the working CSS in `index.html`. The site and the brand guidelines drift slightly on naming (the site uses Albert Sans where the brand doc names Instrument Sans); the working CSS is the source of truth for what ships.

## Color (working system, as deployed)

| Role | Token | Hex |
|---|---|---|
| Ink (page bg) | `--ink` | `#010100` |
| Ink-2 (deep surface) | `--ink-2` | `#040302` |
| Ink-3 (card surface) | `--ink-3` | `#0c0806` |
| Ink-4 (deeper card) | `--ink-4` | `#120f0c` |
| Paper (primary text) | `--paper` | `#ede7df` |
| Paper-2 (secondary) | `--paper-2` | `#bcb6af` |
| Paper-3 (tertiary, captions) | `--paper-3` | `#9b948d` |
| Line | `--line` | `#15110d` |
| Line-2 (divider) | `--line-2` | `#28231f` |
| Line-3 (hover) | `--line-3` | `#3a342e` |
| **Signal** (the only accent) | `--signal` | `#fae353` |
| Signal-soft (hover) | `--signal-soft` | `#efcc36` |
| Signal-deep (border) | `--signal-deep` | `#c4a020` |
| Ember (rare alert) | `--ember` | `#ea6a64` |
| Warn | `--warn` | `#e0a050` |
| OK | `--ok` | `#75d079` |
| Mist (dim text) | `--mist` | `#7a736d` |
| Dim (deepest dim) | `--dim` | `#4a4540` |

**Color strategy: Committed.** Signal yellow (`#fae353`) carries roughly 8–15% of any given surface. It is the ONLY accent. No gradients of color, no secondary accent. Ember/Warn/OK are reserved for system states inside the product UI, not the marketing site.

**Brand guidelines reference colors** (PDF, do not use on the site without reconciling): bg `#0e0e0e`, surface `#161616`, signal `#e8f04a`. The site's `--ink #010100` and `--signal #fae353` supersede.

## Type

- **Sans:** Albert Sans (Google Fonts), weights 400 / 500 / 600 / 700 / 800, italic 400 / 500. Body 15px, line-height 1.55, tabular-nums on.
- **Display weights:** h1 800 with `letter-spacing: -0.034em`, h2 700 at `-0.030em`. Scale uses `clamp()` for fluid sizing.
- **Eyebrows / nav / labels:** 11px, weight 700, `letter-spacing: 0.10em`, uppercase, `--paper-3`.
- **Body copy:** 19px in chapter prose, 15px in cards.
- **Selection:** Signal yellow background, ink text.

Brand guidelines reference Instrument Sans + Jura + JetBrains Mono. The deployed site uses Albert Sans only. Reconcile later if needed; do not introduce new font families without a deliberate decision.

## Layout

- `.page` container: max 1280px, 40px side padding.
- Sections: 64px vertical padding, divided by 1px `--line-2` border-bottom.
- Hero: a 3-column split (`0.85fr 96px 1.15fr`) for raw transcript / waveform spine / polished output.
- Chapter heads: 2-column `1fr 1.3fr` with eyebrow + h2 on left, prose tag on right.
- 1200px+ desktop applies `body { zoom: 0.95 }` to tighten everything by 5%.

## Components in use

- **Pill** with optional LED: hero "recording" eyebrow, pricing badges.
- **`.btn-primary`** signal-on-ink, **`.btn-ghost`** outlined paper.
- **Notify form**: inline email + button, signal accent on focus + on submit. Stays modest, doesn't try to look "luxurious."
- **Kbd** chips: `.kbd` for keyboard shortcuts (Ctrl, Cmd, Win), 4px padding, 1px line border, ink-4 background.
- **Speed bar chart**: horizontal bars with `transform: scaleX(0) → 1` reveal, signal color on the winning row.
- **How cards**: 3-up grid; card 3 is intentionally differentiated (signal-deep border, signal-tinted gradient at bottom) to break "identical card grid" reflex.
- **Control panel**: simulated product UI with sliders, status bar, "private" LED.

## Motion

- Easing: `cubic-bezier(0.16, 1, 0.3, 1)` (ease-out-quart family) on reveal/transitions.
- Durations: 180ms (hover), 700ms (transcript reveal), 1400ms (chart fill).
- The hero raw→polished sequence is a multi-step character reveal driven by JS.
- Waveform: pure CSS keyframe `scaleY(0.36)` → `scaleY(1)` with staggered delays per bar.
- **Never animate** layout properties (use transform/opacity).

## Imagery

- Hero uses NO photography. The raw→polished text animation is the visual.
- Product screenshots live in `assets/screenshots/*-editorial.png`. Available now: HUD, app-aware-modes, brand-voice, data-flow, dictionary-auto, insights, polish-settings, whisper-models. All match the editorial yellow theme.
- No stock illustration. No 3D renders. No abstract gradients.
- Brand mark: 5-ellipse waveform glyph in signal yellow, lockup as `auris.` (lowercase, dot in signal).

## Absolute bans (Auris-specific, in addition to impeccable shared bans)

- **No em-dashes** anywhere (in code, copy, or screenshots). The product strips them; the site doesn't use them either.
- **No `Auris` casing** in the wordmark. Always lowercase `auris.` with the dot in signal yellow.
- **No second accent color.** Signal yellow is the only color.
- **No gradients of color.** Tonal gradients (ink → ink+signal-tint at 6% opacity) are allowed for breaking card monotony, never as decorative meshes.
- **No Wi-Fi-style arc icons** for the brand mark.
- **No photography on the brand mark or hero**. Solid `--ink` or solid `#f2f0ec` light backgrounds only.
- **No subscription pricing copy** (it's a one-time license).
- **No corporate dialect.** No "leverage", "circling back", "per my last email", "AI-powered", "supercharge", "unlock".

## Components I expect to add (informed by Resonant audit)

- **Integration logo row** — Slack, Gmail, Notion, ChatGPT, Claude, Cursor, VS Code, Outlook. Style: monochrome `--paper-2` SVGs on ink, hover lifts to `--paper`, height ~24–28px.
- **Wedge strip** — three or four big numeric/textual claims ("$49 once", "no subscription", "BYOK or local", "Mac + Windows") in a single-row strip near the hero. Treatment: large numerals in Albert Sans 800, tiny eyebrow labels above each.
- **Product screenshot anchor** — one of the existing `*-editorial.png` files as a hero anchor or just-below-hero section, framed by a thin `--line-2` border.
