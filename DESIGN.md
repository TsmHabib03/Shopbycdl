---
name: Shopbycdl
description: Luxury personal shopping by Chay Deluna
colors:
  green: "#1A2421"
  gold: "#D4AF37"
  paper: "#EFEDE6"
  sheet: "#F7F5EF"
  muted: "#61685D"
  line: "#C7C8BB"
  product-ground: "#E5E5DA"
  product-border: "#D9DBCD"
  inverse-copy: "#E3E3D5"
  inverse-rule: "#6B633E"
typography:
  display:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(62px,7.4vw,96px)"
    fontWeight: 400
    lineHeight: 0.96
    letterSpacing: "-0.035em"
  headline:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "clamp(34px,4vw,56px)"
    fontWeight: 400
    lineHeight: 1.1
    letterSpacing: "-0.025em"
  product-title:
    fontFamily: "Newsreader, Georgia, serif"
    fontSize: "25px"
    fontWeight: 400
    lineHeight: 1.2
  body:
    fontFamily: "Inter Tight, system-ui, sans-serif"
    fontSize: "15px"
    fontWeight: 400
    lineHeight: 1.8
  label:
    fontFamily: "Inter Tight, system-ui, sans-serif"
    fontSize: "11px"
    fontWeight: 500
    lineHeight: 1.4
    letterSpacing: "0.16em"
  button:
    fontFamily: "Inter Tight, system-ui, sans-serif"
    fontSize: "11px"
    fontWeight: 600
    letterSpacing: "0.13em"
rounded:
  square: "0px"
spacing:
  tight: "8px"
  compact: "12px"
  standard: "20px"
  grid-gap: "24px"
  section-heading: "30px"
  section: "56px"
components:
  button-primary:
    backgroundColor: "{colors.green}"
    textColor: "{colors.paper}"
    typography: "{typography.button}"
    rounded: "{rounded.square}"
    height: "44px"
    padding: "0 20px"
  button-primary-hover:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.green}"
  button-gold:
    textColor: "{colors.gold}"
    typography: "{typography.button}"
    rounded: "{rounded.square}"
    height: "44px"
    padding: "0 20px"
  button-gold-hover:
    backgroundColor: "{colors.gold}"
    textColor: "{colors.green}"
  filter:
    textColor: "{colors.green}"
    rounded: "{rounded.square}"
    height: "40px"
    padding: "0 16px"
  filter-selected:
    backgroundColor: "{colors.green}"
    textColor: "{colors.gold}"
  product-media:
    backgroundColor: "{colors.product-ground}"
    rounded: "{rounded.square}"
    height: "330px"
---

# Design System: Shopbycdl

## Overview

**Creative North Star: "Luxury personal shopping"**

This system governs [shopbycdl.html](shopbycdl.html) and future Shopbycdl surfaces only. The preserved VHS archive in `index.html` has its own identity and is excluded.

The supplied gold monogram and script emblem set the brand character. Forest green supports gold and pale text, while neutral product grounds let the actual bag photographs carry color and material. Serif display type creates a considered pace; compact sans-serif controls keep browsing direct.

**Key Characteristics:**

- Forest green and gold identity.
- Straight rules and square interface geometry.
- Real product photography with intact silhouettes.
- Serif titles and concise sans-serif controls.

## Colors

**The Brand Pair Rule.** Use green and gold together for branded surfaces and primary actions. Gold is a flat brand color; photography supplies the material detail.

Paper is the general product-browsing field. Sheet is the detail surface. Product ground and product border distinguish photographic frames without competing with the cutouts. Muted text belongs on light grounds; inverse copy belongs on green. Use the line and inverse-rule tokens for fine divisions on their respective surfaces.

## Typography

**The Two Voices Rule.** Newsreader carries display, section, product and detail titles. Inter Tight carries navigation, descriptions, specifications and controls. Both fonts are embedded in the copied HTML.

Display and section titles use regular serif weight, compact leading and restrained negative tracking. The product detail title grows to a desktop maximum of 70px and uses 43px on phones. Phone hero display is 65px, decreasing to 58px below 361px. Functional labels and buttons stay at least 11px; product descriptions use 12–15px according to context.

Use tracked uppercase only for short labels. Body sentences and footer copy have minimal tracking. Index numerals use tabular figures.

## Layout

The desktop shell uses 4vw horizontal margins. The header is 92px tall; phone margins are 20px and the header is 74px. Catalogue columns change from three to two below 1024px. Below 768px, the hero action flows beneath the title, secondary navigation moves into a menu, the product index reduces to numerals, and the detail sheet becomes a scrolling column.

Catalogue image frames are 330px high on desktop and 220px on phones, with narrower phone frames reduced to 190px. Each photo uses containment rather than cropping. Desktop detail uses two columns and generous side padding; phone detail puts the photograph first at 42svh.

## Elevation & Depth

**The Product Depth Rule.** Apply diffuse shadows to product cutouts, rather than to every interface container. Actual bag silhouettes remain the basis of those shadows. Cards and controls use borders or tonal separation.

The featured showroom adapts the original archive's perspective to front-facing bags, with size and depth falloff, gentle hover lift, and a focused active product. One animation loop drives this interaction. Caption masks and the square detail sheet use Web Animations. Reduced-motion preferences make spring movement and reveals immediate.

## Shapes

**The Square Edge Rule.** Every component, border, card and divider uses rigid right angles. Radius is zero, including clip-path expansion into the detail sheet. The supplied circular logo is artwork and retains its emblem outline; it does not introduce rounded interface controls.

SVG controls use consistent thin strokes with square caps and miter joins. The interface contains no pill controls or rounded card shells.

## Components

Primary buttons are green on light grounds. Gold outlined buttons sit on green surfaces and fill gold on hover. Actions are at least 44px tall. Visible keyboard focus uses green on light grounds and gold on green grounds.

Brand filters share a straight bordered group; the selected segment uses green and gold. Product cards pair a contained photograph, house, serif title, material, inquiry price label, explore action and save toggle. Save state persists locally, with a visible empty shortlist and brief status message.

The detail sheet provides the photograph, supplied product facts, descriptive copy, save control and Instagram inquiry. It protects focus, closes with Escape and returns focus to the originating control. Failed product photos show an explicit retry action instead of a broken image.

## Do's and Don'ts

- **Do** use the supplied logo and actual product photographs.
- **Do** keep every interface corner square.
- **Do** preserve silhouettes with image containment.
- **Do** maintain keyboard focus and reduced-motion behavior.
- **Don't** invent prices, stock, founding dates or commercial guarantees.
- **Don't** apply Shopbycdl tokens to the preserved original archive.
- **Don't** shrink functional labels below 11px to fit a layout.
