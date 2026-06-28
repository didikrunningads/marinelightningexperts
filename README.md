# Shiptronics Design System

The brand & UI guideline pack for **Shiptronics** — the visual identity, typography, color, and component recipes used across Shiptronics surfaces.

> Source materials provided by the client (April 2025):
> - `uploads/Shiptronics-Logo-Improvement.pdf` — official logo refresh deck. Documents the move from the old palette (`#23A8E0`, `#1D6395`) to the **new** palette (`#00B3FD`, `#035BD7`) plus shadow-effect treatment notes.
> - `uploads/Shiptronics-logo-horizontal.svg` — primary horizontal logo lockup.
> - `uploads/Shiptronics-logo-stacked.svg` — stacked logomark + wordmark for square placements.
> - Typeface files: full **Inter** family + full **Barlow** family + **Barlow Condensed Bold / Bold Italic**.
> - Client direction: *"Headline and title use Barlow Condensed (uppercase), body text uses Inter (variants). Palette: `#045AD6`, `#00B3FD`, `#FFFFFF`, `#0F1032`."*

---

## 1. Brand context

Shiptronics is a marine/boat **electronics & systems** brand. The logo's three concentric rings around an iris read as a **radar / sonar pulse** — a marker of the technical, navigational, "we see and wire what's beneath the waterline" promise of the product. The wordmark sits in a confident industrial slab. The April 2025 logo refresh tightened curves, equalized stroke thickness, and shifted the palette toward a more vibrant electric blue with a deep cobalt anchor.

The visual system that follows treats Shiptronics as a **technical-but-approachable** marine-electronics brand: deep navy and bright cyan-blue, condensed all-caps display type, generous white space, sharp 2–8px corner radii, no decorative gradients beyond the brand-blue gradient, and zero emoji.

---

## 2. Content fundamentals

> Tone is captured below from the source materials provided. **Limited body copy was supplied** — the voice rules below are scaffolded from the brand category (marine electronics) and the formal, declarative tone of the logo-improvement document. Treat this section as a working starting point and refine with real product copy when available.

- **Voice.** Direct, technical, confident. Speaks like a captain or a senior installer — knows the gear, doesn't oversell.
- **Person.** *We* (Shiptronics) and *you* (the customer / installer). Avoid first-person singular.
- **Casing.** Display headlines are **ALL CAPS** (Barlow Condensed). Section titles are typically Title Case. Body is sentence case. Buttons are sentence case.
- **Punctuation.** Em-dashes for asides. Oxford comma. Periods on full sentences in body, no periods on headlines, eyebrows, or button labels.
- **Numerics.** Spell out one through nine in body prose; numerals for specs, model numbers, dimensions, voltage, channels (e.g. "12 V", "8-channel").
- **Vibe.** Workshop-grade, not lifestyle. No slang, no winking. Imagine the copy printed on a dashboard or a spec sheet — every word earns its space.
- **Avoid.** Emoji. Exclamation marks (≤1 per page, only in CTAs if at all). Marketing fluff like "seamless," "next-gen," "revolutionary." Cute alliteration. Buzzwords.
- **Sample phrasing.**
  - Headline: `BUILT FOR THE WATERLINE.`
  - Eyebrow: `MARINE ELECTRONICS`
  - Body: `Shiptronics designs and installs navigation, lighting, and audio systems for cruisers, sportfishers, and working boats. Every harness is labelled, every ground bonded, every install documented.`
  - CTA: `Request a quote` / `Browse the catalog` / `Talk to an installer`

---

## 3. Visual foundations

### Color
- **Primary action:** `--st-cobalt` `#045AD6`. Used for CTAs, links, focus rings, brand chrome.
- **Accent / highlight:** `--st-electric` `#00B3FD`. Used for hover states, accents, the iris dot in the logomark, and the brand gradient's bright stop. Only sparingly as a fill — it's a highlight, not a workhorse.
- **Anchor / surface dark:** `--st-midnight` `#0F1032`. Used for headlines on light, full-bleed dark sections, and as the body color in dark mode.
- **Paper:** `#FFFFFF` and a tight ramp of cool grays (`--st-gray-50…900`) tuned to the navy.
- **Brand gradient:** `linear-gradient(135deg, #00B3FD → #045AD6)` — used on hero panels, brand glow shadows, and large focal accents only. Never on body text or small UI.

### Typography
- **Display / titles:** `Barlow Condensed Bold`, **uppercase**, tight tracking (0 to -0.005em), short line-height (0.92–1.05). High contrast against body. Reserve italic Bold for editorial pull-quotes only.
- **Subheads / UI titles:** `Barlow` Semibold/Bold (sentence case ok for small UI titles).
- **Body & UI:** `Inter` 400/500. 16px base, 1.6 line-height. Numerals are tabular-ready.
- **Mono:** system mono for serial numbers, model codes, technical specs.
- **Pairing rule:** Barlow Condensed always uppercase; Barlow (regular width) can be sentence case; never mix Condensed + Inter at the same size — set Condensed at least 1.25× the body for visual hierarchy.

### Layout & spacing
- 4px base scale. Section padding tops out at 96–128px. Component padding is 12–24px.
- Container max-width 1200px; narrow editorial 880px.
- Strong horizontal rules and generous white space; we do **not** use decorative dividers, swooshes, or background blobs.

### Backgrounds
- Solid white or solid `--st-midnight`. Occasional `--st-bg-subtle` (`#F6F8FB`) for alternating sections.
- The brand gradient (cobalt → electric) appears on hero panels and on the logo's "shadow-effect on dark" treatment. It is the **only** gradient that ships.
- No background images of office stock photography. Marine product imagery is welcomed when the client supplies it (cool, neutral, no warm sunset filters); it should sit full-bleed inside generously padded containers.

### Borders & shadows
- Borders: 1px `--st-border` (#DBE2EC). 2px `--st-border-strong` for emphasis. Brand-colored borders only for selected/active states.
- Shadows: a 5-step elevation ramp (`xs → xl`) tuned with **navy-tinted alpha**, not pure black, so shadows feel cool, not muddy. A dedicated `--st-shadow-glow` (cyan halo + cobalt drop) is the brand-blue glow used on the hero CTA and the on-dark logo treatment from the PDF.
- Inner shadows are reserved for the logomark's inner-fill treatment (per the April 2025 refresh).

### Radii
- 2px / 4px / 8px / 12px / 16px / 24px / pill. Most UI lives at 8–12px; pills only on tags/badges.

### Hover & press
- Default hover: drop one elevation step (or, on cobalt CTAs, switch fill to `--st-cobalt-600` and add `--st-shadow-glow`).
- Press: scale `0.98`, shadow drops to `xs`, transition 120ms `--st-ease-out`.
- Links: underline by default, color shifts to `--st-cobalt-700` on hover.

### Motion
- Easing: `cubic-bezier(0.22, 1, 0.36, 1)` for entrances, `cubic-bezier(0.65, 0, 0.35, 1)` for symmetric movement.
- Durations: 120ms / 200ms / 320ms.
- Style: short, confident slides + fades. **No bounce, no spring overshoot, no parallax floats.** This is a marine-electronics brand, not a wellness app.

### Imagery vibe
- Cool palette. Daylight to overcast, never warm-sunset. Slight grain ok if matched to product photography. B&W reserved for portrait/feature spreads.

### Cards
- 1px `--st-border` + `--st-shadow-sm`, 12px radius, white surface. Hover lifts to `--st-shadow-md`. No left-border accent stripes — that's not in this system.

### Transparency & blur
- We don't use frosted-glass / backdrop-blur. Transparency is reserved for shadow alphas and a 6%-tinted overlay used on hero gradients to anchor display text.

---

## 4. Iconography

> **No proprietary icon set was supplied.** The brand identity package only included logos and typefaces.
>
> **Recommended substitution:** [Lucide](https://lucide.dev) — open-source, 24×24, **2px stroke**, rounded line caps. Lucide's stroke weight matches the proportions of the Shiptronics logomark's outer ring, and its rounded line caps echo the refreshed curves the April 2025 PDF specified. Pull from CDN:
> ```html
> <script src="https://unpkg.com/lucide@latest"></script>
> ```
> or import individual SVGs from `https://lucide.dev/icons/<name>`.
>
> **Substitution flag — please confirm.** If Shiptronics has an official icon library or product-photography sprite, please attach it and we'll swap Lucide out.
>
> **Rules.**
> - 2px stroke, never filled (except the iris/dot in the logomark).
> - Use `--st-fg` for default, `--st-cobalt` for active/selected, `--st-fg-muted` for disabled.
> - Sizes: 16 / 20 / 24 / 32. Inline icons sit on the cap-height baseline of body text.
> - **No emoji.** Not in marketing, not in UI, not in social posts.
> - **No unicode glyphs as icons** (✓ ✗ → etc.) except inside their literal semantic role (e.g. checkbox check is fine, decorative arrows are not).

---

## 5. Index — what's in this folder

```
.
├── README.md                 ← you are here
├── SKILL.md                  ← invocation rules for the design agent / Claude Code
├── colors_and_type.css       ← all CSS variables + semantic .st-* classes
├── assets/
│   ├── Shiptronics-logo-horizontal.svg
│   ├── Shiptronics-logo-stacked.svg
│   └── Shiptronics-Logo-Improvement.pdf
├── fonts/                    ← Inter + Barlow + Barlow Condensed (TTF)
└── preview/                  ← visual review cards (registered to the Design System tab)
```

### Quick start

```html
<link rel="stylesheet" href="/colors_and_type.css">
<h1 class="st-h1">Built for the waterline</h1>
<p class="st-p">Shiptronics designs and installs marine electronics…</p>
<button class="st-btn st-btn-primary">Request a quote</button>
```

---

## 6. Open questions / caveats

- **No production codebase, Figma file, or product UI screenshots were supplied.** Therefore this design system ships **without UI kits** for the website or app. We need either a codebase import, a Figma design-system link, or screenshots of live screens to build pixel-faithful UI components.
- **No slide template was supplied.** No sample slides have been generated — please attach a deck if you'd like the system extended to presentation surfaces.
- **No icon set was supplied.** Lucide is the recommended substitute; flagged in §4 above.
- **Voice & tone is partly inferred** from the brand category (marine electronics) and the formal cadence of the logo PDF. Real product copy will sharpen this.
- **Font coverage is complete** for what was uploaded. Note that Barlow Condensed shipped only in **Bold / Bold Italic** — the system uses Bold-only for display, which matches the client's "headline / title use Barlow Condensed" direction.
