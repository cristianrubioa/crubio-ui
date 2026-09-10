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

## Adding a new identity

Create a new folder with a `tokens.css` file. No other changes needed.
