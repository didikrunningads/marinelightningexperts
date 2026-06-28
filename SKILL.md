---
name: shiptronics-design
description: Use this skill to generate well-branded interfaces and assets for Shiptronics, either for production or throwaway prototypes / mocks / decks. Contains essential design guidelines, colors, type, fonts, assets, and component recipes for prototyping marine-electronics-flavored UI in the Shiptronics brand voice.
user-invocable: true
---

Read the `README.md` file within this skill, and explore the other available files (`colors_and_type.css`, `assets/`, `fonts/`, `preview/`).

If creating visual artifacts (slides, mocks, throwaway prototypes, etc), copy the relevant assets out and create static HTML files for the user to view. The fastest path is:

1. Link `colors_and_type.css` from your HTML.
2. Use the `--st-*` CSS variables and the `.st-h1 / .st-p / .st-eyebrow / …` semantic classes.
3. Pull logos from `assets/` (`Shiptronics-logo-horizontal.svg` and `Shiptronics-logo-stacked.svg`).
4. For icons: link Lucide from CDN (`https://unpkg.com/lucide@latest`) and use 2px stroke / rounded line caps. (No proprietary icon set was provided — flag any substitution to the user.)

If working on production code, copy assets and read the rules in `README.md` to become an expert in designing with this brand. The non-negotiable rules:

- **Display & section titles** are **Barlow Condensed Bold, ALL CAPS**, tight tracking.
- **Body & UI** are **Inter** 400/500.
- **Primary action / link** is `--st-cobalt` (#045AD6); **accent / highlight** is `--st-electric` (#00B3FD); **anchor / dark surface** is `--st-midnight` (#0F1032).
- **No emoji**, no decorative gradients beyond the brand cobalt→electric gradient, no parallax, no spring overshoot.
- **Cards** are 12px radius, 1px `--st-border`, `--st-shadow-sm`. Hover lifts to `--st-shadow-md`.
- **Buttons** are 8px radius, 12×18 padding, 14px Inter SemiBold, primary fill `--st-cobalt` with `--st-shadow-glow` on hover.

If the user invokes this skill without any other guidance, ask them what they want to build or design (a hero, a product card grid, a quote-request form, a deck, a print spec sheet, etc), ask 3–5 clarifying questions about audience and surface, and act as an expert designer who outputs HTML artifacts *or* production code, depending on the need.

## Caveats — read these before you start

- **No UI kit was supplied.** The brand pack only contained logos, fonts, and a logo-improvement document. There is no website / app codebase to reference. If the user asks to "match an existing screen," ask them to attach screenshots, a Figma link, or the codebase.
- **Voice & tone is partly inferred.** Voice guidance in `README.md` §2 is scaffolded from category and the formal cadence of the source PDF — confirm with the user before shipping copy.
- **Iconography substitution.** Lucide is recommended; flag the substitution in any deliverable.
- **Font coverage.** Inter and Barlow are full families. Barlow Condensed is **Bold and Bold Italic only** — that is the intended display weight per the brand direction; do not request other Condensed weights.
