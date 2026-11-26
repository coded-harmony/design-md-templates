---
version: alpha
name: Harbour
description: A marketing landing page for a calm B2B SaaS product (a shared support inbox). Light, editorial, product-led.
colors:
  primary: "#15202B"
  secondary: "#5B6670"
  tertiary: "#C4441E"
  neutral: "#F3F1EC"
  surface: "#FFFFFF"
  on-surface: "#15202B"
  hairline: "#DDD8CF"
typography:
  headline-display:
    fontFamily: Fraunces
    fontSize: 64px
    fontWeight: 600
    lineHeight: 1.02
    letterSpacing: -0.03em
  headline-lg:
    fontFamily: Fraunces
    fontSize: 40px
    fontWeight: 600
    lineHeight: 1.1
    letterSpacing: -0.02em
  headline-md:
    fontFamily: IBM Plex Sans
    fontSize: 20px
    fontWeight: 600
    lineHeight: 1.3
  body-lg:
    fontFamily: IBM Plex Sans
    fontSize: 19px
    fontWeight: 400
    lineHeight: 1.55
  body-md:
    fontFamily: IBM Plex Sans
    fontSize: 16px
    fontWeight: 400
    lineHeight: 1.6
  label-sm:
    fontFamily: IBM Plex Mono
    fontSize: 12px
    fontWeight: 500
    lineHeight: 1.3
    letterSpacing: 0.08em
rounded:
  sm: 4px
  md: 8px
  lg: 14px
spacing:
  sm: 8px
  md: 16px
  lg: 32px
  xl: 64px
  section: 128px
components:
  button-primary:
    backgroundColor: "{colors.tertiary}"
    textColor: "{colors.surface}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    height: 48px
    padding: 22px
  button-secondary:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
    typography: "{typography.body-md}"
    rounded: "{rounded.md}"
    height: 48px
    padding: 22px
  product-frame:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: 0px
  page:
    backgroundColor: "{colors.neutral}"
    textColor: "{colors.primary}"
  divider:
    backgroundColor: "{colors.hairline}"
    height: 1px
  pricing-card:
    backgroundColor: "{colors.surface}"
    rounded: "{rounded.lg}"
    padding: 32px
---

## Overview

A harbour office at 7am: fog-coloured paper, deep navy-black ink, one signal-buoy orange. The page sells calm competence to 3 to 15 person support teams who are tired of tools built for call centres. Editorial, not techy. The product itself is the hero image.

## Colors

- **Primary (#15202B):** Harbour ink for all text and the footer background.
- **Secondary (#5B6670):** Supporting copy, captions, FAQ answers.
- **Tertiary (#C4441E):** Signal orange (deep enough for white button text to pass WCAG AA), the only accent. The primary button and at most two highlights on the page (for example, the recommended plan's label).
- **Neutral (#F3F1EC):** Fog paper, the page ground.
- **Surface (#FFFFFF):** Product screenshots and pricing cards, so they read as objects on paper.
- **Hairline (#DDD8CF):** Dividers and card borders.

## Typography

Fraunces (600) for headlines only, with tight tracking. IBM Plex Sans for body copy; IBM Plex Mono, uppercase, for small section labels ("HOW A TICKET MOVES"). Headlines are short: 8 words at most. Body copy is left-aligned with a 64ch max width.

## Layout

1200px content width centred on a 1440px canvas. 128px between sections, 16 to 32px inside groups. Hero: headline, one sentence and two buttons on the left (5 columns); a real slice of the product on the right (7 columns), slightly cropped at the right edge of its section (clip it with `overflow: hidden` on the section; the page itself must never scroll sideways). Then: three benefits with numbers, a 4-step "how it works" strip, pricing (two plans), FAQ, footer.

## Elevation & Depth

Paper and objects. The product frame gets one long, soft shadow (`0 30px 60px -20px rgba(21,32,43,0.25)`); nothing else on the page has a shadow.

## Shapes

8px buttons, 14px cards and product frames. No pills, no blobs, no wavy section dividers.

## Voice & Content Strategy

Calm, competent and a bit dry. Concrete numbers over adjectives: "Most teams answer in under 2 hours by week two." Banned words: revolutionize, supercharge, seamless, AI-powered, unlock, next-generation.

## Components

- **Hero product slice:** a believable inbox with 5 conversations: real-sounding customer names, subjects like "Refund for duplicate charge", assignee initials and status chips. Never an abstract illustration.
- **Benefit row:** three columns, each a label-sm label, a headline-md with a number in it and two lines of body-md. No icons on top.
- **Pricing:** two cards side by side; the recommended one has an orange label, not a different colour card.
- **FAQ:** a two-column list (question in headline-md, answer in body-md secondary), always expanded.

## Do's and Don'ts

- Do show the real product above the fold.
- Do use one orange button per viewport.
- Don't use gradients, glassmorphism, emoji or icon-topped feature cards.
- Don't centre long paragraphs.
- Don't add logo walls or testimonials with invented names; leave a slot for real ones.
- Don't let anything make the page scroll sideways.
