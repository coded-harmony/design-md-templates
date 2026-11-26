---
version: alpha
name: Reading Room
description: Developer documentation for an API product. Light theme, long-form reading, lots of code.
colors:
  primary: "#111418"
  secondary: "#5A6270"
  tertiary: "#2E6B4F"
  neutral: "#FFFFFF"
  surface: "#F6F6F3"
  on-surface: "#111418"
  hairline: "#E6E5E0"
  code-ground: "#14171C"
  code-ink: "#E6E3DA"
  note: "#EAF2EC"
  caution: "#FBF1E2"
typography:
  headline-lg:
    fontFamily: Newsreader
    fontSize: 40px
    fontWeight: 600
    lineHeight: 1.15
    letterSpacing: -0.015em
  headline-md:
    fontFamily: IBM Plex Sans
    fontSize: 22px
    fontWeight: 600
    lineHeight: 1.3
  headline-sm:
    fontFamily: IBM Plex Sans
    fontSize: 17px
    fontWeight: 600
    lineHeight: 1.4
  body-md:
    fontFamily: IBM Plex Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.7
  body-sm:
    fontFamily: IBM Plex Sans
    fontSize: 14px
    fontWeight: 400
    lineHeight: 1.55
  code-md:
    fontFamily: IBM Plex Mono
    fontSize: 13.5px
    fontWeight: 400
    lineHeight: 1.6
rounded:
  sm: 4px
  md: 8px
spacing:
  xs: 4px
  sm: 8px
  md: 16px
  lg: 24px
  xl: 48px
components:
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
  divider:
    backgroundColor: "{colors.hairline}"
    height: 1px
  code-block:
    backgroundColor: "{colors.code-ground}"
    textColor: "{colors.code-ink}"
    typography: "{typography.code-md}"
    rounded: "{rounded.md}"
    padding: 16px
  inline-code:
    backgroundColor: "{colors.surface}"
    textColor: "{colors.primary}"
    typography: "{typography.code-md}"
    rounded: "{rounded.sm}"
    padding: 2px
  callout-note:
    backgroundColor: "{colors.note}"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: 16px
  callout-caution:
    backgroundColor: "{colors.caution}"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: 16px
  sidebar-link:
    textColor: "{colors.secondary}"
    typography: "{typography.body-sm}"
    height: 32px
  sidebar-link-active:
    textColor: "{colors.tertiary}"
    typography: "{typography.body-sm}"
---

## Overview

A library reading room: white pages, black type, a green banker's lamp. The job is reading and copying code, for an hour at a time. Nothing moves, nothing glows. Developers should find the answer in under a minute and trust it.

## Colors

- **Primary (#111418):** All text and headings.
- **Secondary (#5A6270):** Sidebar links, captions, "last updated" lines.
- **Tertiary (#2E6B4F):** Lamp green, the only accent: links, the active sidebar item, the "Copy" confirmation.
- **Neutral (#FFFFFF) / surface (#F6F6F3):** The page is white; the sidebar and inline code sit on the warm surface.
- **Code ground (#14171C) / code ink (#E6E3DA):** Code blocks are dark even in the light theme, so they read as copyable objects.
- **Note / caution tints:** Callout backgrounds. No icons in brand colours; a one-word label is enough.

## Typography

Newsreader for the page title only (one per page). IBM Plex Sans for headings and body at 16px with 1.7 line height; IBM Plex Mono for code. Body measure is 72ch maximum.

## Layout

Three columns on desktop: a 260px sidebar, the article (max 760px), and a 220px "On this page" table of contents that tracks scroll. Below 1100px the table of contents disappears; below 800px the sidebar becomes a drawer. 48px between H2 sections, 16px between paragraphs.

## Elevation & Depth

None. Hairline borders separate the sidebar and the table of contents. The search dialog is the only floating element.

## Shapes

4px on inline code and inputs, 8px on code blocks and callouts.

## Voice & Content Strategy

Second person, present tense, task-first headings ("Create an API key", not "API key creation"). Every page starts with one sentence saying what you'll be able to do, and every code block runs as pasted: no `...` in the middle of a working example.

## Components

- **Code block:** language label top-left in body-sm, a Copy button top-right, line numbers off by default, highlighted lines in a 6% lighter band.
- **Tabs for languages:** curl, Node, Python, in that order; the choice persists across pages.
- **Parameter table:** name in code-md, type in secondary, a "Required" label in tertiary, description in body-sm.
- **Callouts:** Note and Caution only. Never more than one callout in a row.

## Do's and Don'ts

- Do make every heading linkable with a hover anchor.
- Do show the full request and the full response for each endpoint.
- Don't use more than one accent colour, or coloured icons in the sidebar.
- Don't put marketing copy or upgrade banners inside articles.
- Don't truncate code with ellipses.
