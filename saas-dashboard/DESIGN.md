---
version: alpha
name: Survey Office
description: A dense, calm analytics dashboard for a B2B SaaS product. Light theme, tabular data first.
colors:
  primary: "#17191C"
  secondary: "#646A73"
  tertiary: "#1F7A4D"
  neutral: "#FAFAF7"
  surface: "#FFFFFF"
  on-surface: "#17191C"
  hairline: "#E4E3DD"
  error: "#B42318"
  warning: "#B54708"
  chart:
    series-1: "#17191C"
    series-2: "#1F7A4D"
    series-3: "#8A6D3B"
    series-4: "#5B7DB1"
    series-5: "#A3A8AF"
typography:
  headline-lg:
    fontFamily: Instrument Sans
    fontSize: 24px
    fontWeight: 600
    lineHeight: 1.25
    letterSpacing: -0.01em
  headline-md:
    fontFamily: Instrument Sans
    fontSize: 16px
    fontWeight: 600
    lineHeight: 1.4
  body-md:
    fontFamily: Instrument Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.5
  body-sm:
    fontFamily: Instrument Sans
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.45
  label-sm:
    fontFamily: JetBrains Mono
    fontSize: 11px
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: 0.06em
  data-lg:
    fontFamily: JetBrains Mono
    fontSize: 28px
    fontWeight: 500
    lineHeight: 1.1
    fontFeature: '"tnum" 1'
  data-md:
    fontFamily: JetBrains Mono
    fontSize: 13px
    fontWeight: 400
    lineHeight: 1.45
    fontFeature: '"tnum" 1'
rounded:
  none: 0px
  sm: 4px
  md: 6px
  lg: 10px
spacing:
  xs: 4px
  sm: 8px
  md: 12px
  lg: 16px
  xl: 24px
  2xl: 32px
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    height: 32px
    padding: 12px
  button-secondary:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    height: 32px
    padding: 12px
  card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: 16px
  table-row:
    backgroundColor: "{colors.surface}"
    typography: "{typography.body-sm}"
    height: 40px
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
  divider:
    backgroundColor: "{colors.hairline}"
    height: 1px
  badge-warning:
    backgroundColor: "#FDF0E1"
    textColor: "{colors.warning}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.sm}"
  chart-series-1:
    backgroundColor: "{colors.chart.series-1}"
  chart-series-2:
    backgroundColor: "{colors.chart.series-2}"
  chart-series-3:
    backgroundColor: "{colors.chart.series-3}"
  chart-series-4:
    backgroundColor: "{colors.chart.series-4}"
  chart-series-5:
    backgroundColor: "{colors.chart.series-5}"
  badge-positive:
    backgroundColor: "#E7F2EC"
    textColor: "{colors.tertiary}"
    typography: "{typography.label-sm}"
    rounded: "{rounded.sm}"
---

## Overview

A dashboard people keep open all day, so it has to be quiet. Think of a survey office: tracing paper, graphite, one green pencil for things that went well. Density beats decoration. Numbers are the hero; chrome stays out of the way. The audience is operators and finance leads who scan, compare and export, not marketing visitors.

## Colors

- **Primary (#17191C):** Graphite. Body text, headings, primary buttons and the first chart series.
- **Secondary (#646A73):** Pencil grey for labels, axis text, metadata and secondary icons.
- **Tertiary (#1F7A4D):** Surveyor's green, the only accent. Positive deltas, the selected nav item and focus rings. Never decoration.
- **Neutral (#FAFAF7):** The page ground, a touch warmer than white so white cards lift off it without shadows.
- **Hairline (#E4E3DD):** Every border and divider. One weight, 1px.
- **Error / warning:** Only for states that need action. A red number is an alarm, so don't use red for negative deltas that are normal (use secondary text with a minus sign).
- **Chart series:** Use in order. Two series is the common case: graphite and green.

## Typography

Instrument Sans for interface text, JetBrains Mono for numbers, IDs and labels. All numbers use tabular figures so columns line up. Labels above metrics are mono, uppercase, 11px. Headline sizes stop at 24px: this is a tool, not a magazine.

## Layout

A 240px left sidebar, a 56px top bar, and a content area on a 12-column grid with 24px gutters. Space is tight inside a card (8 to 12px) and generous between groups (24 to 32px). Tables run edge to edge inside their card with 16px cell padding on the sides. Keep the first screen to: KPI row (4 cards), one primary chart, one table.

## Elevation & Depth

Flat. Cards are white on the warm ground with a 1px hairline; no drop shadows. Only menus, popovers and dialogs get a shadow: `0 8px 24px rgba(23,25,28,0.12)`.

## Shapes

Small radii: 6px on controls, 10px on cards, 4px on badges. Never pill-shaped buttons.

## Voice & Content Strategy

Plain, specific and short. "Revenue, last 30 days", not "Your Revenue Insights". Empty states say what to do next in one sentence and offer one button. Dates are absolute in tables ("12 Nov 2026") and relative only in activity feeds.

## Components

- **KPI card:** label-sm label, data-lg value, then a delta line in body-sm (green with ▲ for good, secondary with ▼ for bad-but-normal).
- **Tables:** 40px rows, hairline between rows, no zebra stripes, numbers right-aligned in data-md, the first column left-aligned and medium weight. Sticky header.
- **Filters:** a row of secondary buttons above the table; the active filter shows its value ("Plan: Team").
- **Charts:** line or bar only, no 3D, no pie charts with more than 3 slices. Gridlines in hairline, axis labels in label-sm.

## Do's and Don'ts

- Do right-align every numeric column and use tabular figures.
- Do show units and periods in the label ("MRR, USD", "Last 30 days").
- Don't use the green accent for anything that isn't good news, selection or focus.
- Don't add icons to KPI cards or gradient fills to charts.
- Don't center-align table content or headings.
- Don't use more than two font weights on one screen (400 and 600).
