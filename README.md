# crubio-ui

Shared design tokens for [@cristianrubioa](https://github.com/cristianrubioa) projects.

## Identities

| Folder | Projects |
|--------|----------|
| `app/` | celeste, erdos, stringweave — utility apps with sidebar layout |

## Usage

```html
<link rel="stylesheet" href="https://cristianrubioa.github.io/crubio-ui/app/tokens.css">
```

## Section labels vs. field labels

A **section label** groups 2+ distinct controls (e.g. a "Location" heading above latitude and longitude, or "Parameters" above several inputs) — apply `.crubio-section-label` to it. A **field label** names exactly one control (e.g. "Difficulty" above a single selector) — leave it unstyled, no special class. `tokens.css` can't infer this from markup; classify it yourself when adding a label.

## Header chrome dimensions

`--header-gap` (0.75rem), `--hamburger-icon-size` (1.25rem), and `--logo-size` (1.5rem) standardize the app-shell header's hamburger toggle, logo, and inter-element spacing. Apply `--header-gap` as the header's flex `gap`. Apply `--hamburger-icon-size`/`--logo-size` as `font-size` on a font-glyph icon (e.g. a Font Awesome `<i>`), or as `width`/`height` on an inline SVG icon component — whichever matches your icon technology.

## Sidebar footer

The sidebar's "Made with ♥" footer standardizes on two things:

- **Color**: apply `color: var(--footer-text-color)` (`#4b5563`) to the footer text for its light-mode (or only) theme. Dark-mode/dark-theme consumers keep their own override on top — this variable only sets the light-mode default.
- **Structure**: the footer element SHALL be a `shrink-0` (or `mt-auto`) sibling positioned *outside* the sidebar's scrollable content region — not a child of the same `overflow-y-auto` container as the form/nav content — so it stays visible regardless of how tall that content grows. The sidebar's own height SHALL be computed safely against mobile browser chrome, using either `height: 100dvh` (with a `100vh` fallback for older browsers) or `position: fixed` anchored to both `top` and `bottom: 0` (letting the browser compute the height directly). `tokens.css` can't enforce this — it depends on how each consumer nests its own markup — so get it right at authoring time.

## Header title & subtitle

The header brand title uses `font-semibold tracking-wide leading-none`, sized via `--app-name-size`. Color is left to the consumer — it's brand identity (e.g. celeste's blue tint vs. erdos's neutral tone), not something to standardize. The subtitle uses `text-sm font-normal` with no additional letter-spacing; its color is also left to the consumer, since it depends on the app's light/dark theme. Whether the subtitle is hidden below the `md` breakpoint (`hidden md:inline`) is *not* part of this convention — existing consumers are genuinely split on that, so pick whichever fits your header's content.

## Adding a new identity

Create a new folder with a `tokens.css` file. No other changes needed.
