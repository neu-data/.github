# Neudata brand theme for GitHub

Colours are sampled from the Neudata logo and match the business cards and presentation background.

| Token | Hex | Use |
|---|---|---|
| **Neudata Teal** | `#055F56` | Primary accent — outer logo arc, badges, highlights |
| **Deep Navy** | `#04242F` | Headings, inner logo arc, dark backgrounds |
| **Neudata Blue** | `#0B376C` | Secondary accent — lower logo arc, links, data series |
| **Ink** | `#000000` | Wordmark, business-card panels |
| **Mist** | `#EAF2F5` | Light backgrounds, banner gradient |
| **White** | `#FFFFFF` | Page background |

**Tagline:** *Insight. Impact. Innovation.*
**Website:** [www.neu-data.com](https://www.neu-data.com) · **Email:** contact@neu-data.com

## Assets

| File | Purpose |
|---|---|
| [`assets/banner.svg`](assets/banner.svg) | README header banner (1280 × 320) |
| [`assets/neudata-logo.png`](assets/neudata-logo.png) | Logo on white |
| [`assets/neudata-logo-transparent.png`](assets/neudata-logo-transparent.png) | Logo with transparent background |

Use the banner at the top of any repository README:

```markdown
<img src="https://raw.githubusercontent.com/neu-data/.github/main/assets/banner.svg" alt="Neudata Consulting Ltd" width="100%" />
```

## Badges

```markdown
![Neudata](https://img.shields.io/badge/Neudata-Consulting-055F56?style=flat)
![Status](https://img.shields.io/badge/status-active-0B376C?style=flat)
![Client](https://img.shields.io/badge/client-internal-04242F?style=flat)
```

## Figure palette

### R (ggplot2)

```r
neudata_cols <- c(teal = "#055F56", blue = "#0B376C", navy = "#04242F",
                  teal_light = "#5FA39B", blue_light = "#6C8DB8", grey = "#8A99A3")

scale_colour_neudata <- function(...) ggplot2::scale_colour_manual(values = unname(neudata_cols), ...)
scale_fill_neudata   <- function(...) ggplot2::scale_fill_manual(values = unname(neudata_cols), ...)
```

### Python (matplotlib)

```python
NEUDATA_COLS = ["#055F56", "#0B376C", "#04242F", "#5FA39B", "#6C8DB8", "#8A99A3"]

import matplotlib as mpl
mpl.rcParams["axes.prop_cycle"] = mpl.cycler(color=NEUDATA_COLS)
```

## Issue labels

Suggested labels, coloured to the theme (Settings → Repository defaults → Labels for the whole organisation):

| Label | Colour |
|---|---|
| `type: bug` | `#B60205` |
| `type: request` | `#055F56` |
| `type: data-quality` | `#0B376C` |
| `type: docs` | `#5FA39B` |
| `status: triage` | `#04242F` |
| `status: in progress` | `#6C8DB8` |
| `status: blocked` | `#8A99A3` |
| `priority: high` | `#D93F0B` |
