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

## Adding a new identity

Create a new folder with a `tokens.css` file. No other changes needed.
