---
version: alpha
name: Allotment
description: A friendly consumer mobile app (iOS and Android) for tracking a vegetable garden. Light theme, big touch targets.
colors:
  primary: "#1B261E"
  secondary: "#5E6B60"
  tertiary: "#C73A26"
  neutral: "#F4F7F2"
  surface: "#FFFFFF"
  on-surface: "#1B261E"
  hairline: "#DCE3D8"
  leaf: "#2F6B40"
  leaf-tint: "#E3EFE4"
  error: "#B42318"
typography:
  headline-display:
    fontFamily: Bricolage Grotesque
    fontSize: 34px
    fontWeight: 700
    lineHeight: 1.1
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Bricolage Grotesque
    fontSize: 22px
    fontWeight: 600
    lineHeight: 1.2
  body-lg:
    fontFamily: Figtree
    fontSize: 17px
    fontWeight: 400
    lineHeight: 1.45
  body-md:
    fontFamily: Figtree
    fontSize: 15px
    fontWeight: 400
    lineHeight: 1.45
  label-md:
    fontFamily: Figtree
    fontSize: 13px
    fontWeight: 600
    lineHeight: 1.3
rounded:
  sm: 8px
  md: 14px
  lg: 22px
  full: 999px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 32px
components:
  button-primary:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.surface}"
    typography: "{typography.body-lg}"
    rounded: "{rounded.full}"
    height: 52px
    padding: 24px
  button-secondary:
    backgroundColor: "{colors.leaf-tint}"
    textColor: "{colors.primary}"
    typography: "{typography.body-lg}"
    rounded: "{rounded.full}"
    height: 52px
    padding: 24px
  card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: 16px
  list-item:
    backgroundColor: "{colors.surface}"
    typography: "{typography.body-lg}"
    height: 60px
  tab-bar:
    backgroundColor: "{colors.surface}"
    typography: "{typography.label-md}"
    height: 83px
  screen:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
  divider:
    backgroundColor: "{colors.hairline}"
    height: 1px
  chip:
    backgroundColor: "{colors.leaf-tint}"
    textColor: "{colors.leaf}"
    typography: "{typography.label-md}"
    rounded: "{rounded.full}"
    height: 32px
---

## Overview

A garden notebook in your pocket. Morning dew on the ground colour, soil-dark ink, and one tomato-red accent for the thing to do today. It should feel warm and a little playful, never childish. Users open it outdoors with dirty hands and bright sun, so contrast is high and targets are big.

## Colors

- **Primary (#1B261E):** Soil. All text and icons.
- **Secondary (#5E6B60):** Captions, timestamps, inactive tab icons.
- **Tertiary (#C73A26):** Tomato, the single accent. The main action on a screen and the "due today" dot. One tomato element per screen.
- **Neutral (#F4F7F2):** The screen background.
- **Leaf (#2F6B40) and leaf tint (#E3EFE4):** Plant status ("growing well"), chips and secondary buttons.
- **Error (#B42318):** Frost warnings and failed syncs only.

## Typography

Bricolage Grotesque for screen titles and big numbers (days to harvest); Figtree for everything else. Respect Dynamic Type: body-lg (17px) is the default reading size, and nothing a user must read goes below 13px.

## Layout

Design at 390 × 844 (iPhone 15/16) and check at 360 wide. 16px side margins, 24px between sections. Respect safe areas: the top 59px and the bottom 34px belong to the system. A large title (headline-display) at the top of each root screen collapses to a 17px centred title on scroll. Four tabs at most: Today, Garden, Journal, Settings.

## Elevation & Depth

Cards sit on the tinted ground with no border and a soft shadow: `0 1px 2px rgba(27,38,30,0.06), 0 4px 12px rgba(27,38,30,0.06)`. Bottom sheets get a 22px top radius and a grabber.

## Shapes

Generous rounding: 22px cards, 14px inputs, fully round buttons and chips. Plant photos are 14px-rounded squares.

## Motion & Micro-interaction

Short and physical. Checking off a task scales the checkbox to 1.15 and back in 180ms with a light haptic. Sheets use the platform spring; never custom bounces on lists.

## Voice & Content Strategy

Talks like a neighbour who gardens: "Water the tomatoes, it's been 3 dry days." Use plant names people actually use. Never guilt ("You missed 4 tasks!"); say what's next instead.

## Components

- **Today list:** list items 60px high with a 28px round checkbox on the left, plant name in body-lg, a reason in body-md secondary below.
- **Plant card:** photo, name in headline-md, a chip for status, days to harvest as a big number.
- **Primary button:** one per screen, full width at the bottom above the tab bar when it's the screen's main action.
- **Tab bar:** 83px including the home indicator area, filled icon plus label for the active tab, outline icon for the rest.

## Do's and Don'ts

- Do keep every tap target at least 44 × 44px.
- Do put the main action within thumb reach (bottom third of the screen).
- Don't use the tomato accent for more than one element per screen.
- Don't use hamburger menus; use the tab bar.
- Don't show plain spinners for more than a second; show the content's skeleton.
