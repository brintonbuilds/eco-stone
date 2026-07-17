---
name: Monolithic Forest
colors:
  surface: '#fbf9f4'
  surface-dim: '#dcdad5'
  surface-bright: '#fbf9f4'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f6f3ee'
  surface-container: '#f0eee9'
  surface-container-high: '#eae8e3'
  surface-container-highest: '#e4e2dd'
  on-surface: '#1b1c19'
  on-surface-variant: '#434843'
  inverse-surface: '#30312d'
  inverse-on-surface: '#f3f0eb'
  outline: '#737973'
  outline-variant: '#c3c8c1'
  surface-tint: '#4d6453'
  primary: '#1b3022'
  on-primary: '#ffffff'
  primary-container: '#1b3022'
  on-primary-container: '#819986'
  inverse-primary: '#b4cdb8'
  secondary: '#6ea83d'
  on-secondary: '#ffffff'
  secondary-container: '#e8f5e9'
  on-secondary-container: '#6ea83d'
  tertiary: '#9dbf45'
  on-tertiary: '#ffffff'
  tertiary-container: '#f1f8e9'
  on-tertiary-container: '#9dbf45'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#d0e9d4'
  primary-fixed-dim: '#b4cdb8'
  on-primary-fixed: '#0b2013'
  on-primary-fixed-variant: '#364c3c'
  secondary-fixed: '#b5f47f'
  secondary-fixed-dim: '#9ad766'
  on-secondary-fixed: '#0c2000'
  on-secondary-fixed-variant: '#285000'
  tertiary-fixed: '#ccf070'
  tertiary-fixed-dim: '#b0d357'
  on-tertiary-fixed: '#151f00'
  on-tertiary-fixed-variant: '#3a4d00'
  background: '#fbf9f4'
  on-background: '#1b1c19'
  surface-variant: '#e4e2dd'
typography:
  display-lg:
    fontFamily: Cormorant Garamond
    fontSize: 64px
    fontWeight: '700'
    lineHeight: '1.1'
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Cormorant Garamond
    fontSize: 40px
    fontWeight: '700'
    lineHeight: '1.2'
  headline-lg-mobile:
    fontFamily: Cormorant Garamond
    fontSize: 32px
    fontWeight: '700'
    lineHeight: '1.2'
  headline-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.3'
  body-lg:
    fontFamily: Plus Jakarta Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: '1.6'
  label-md:
    fontFamily: Plus Jakarta Sans
    fontSize: 14px
    fontWeight: '600'
    lineHeight: '1.2'
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  base: 8px
  container-max: 1280px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 64px
---

## Brand & Style

The design system embodies a "Monolithic Elegance" aesthetic—a sophisticated blend of architectural brutalism and organic vitality. It targets an audience that values permanence, sustainability, and premium craftsmanship. 

The visual language is rooted in a high-end architectural feel, utilizing heavy whitespace and a restricted, nature-inspired palette. By moving away from vibrant oranges toward a deep forest green, the UI shifts from energetic to grounded and prestigious. The style leverages clean, minimalist structures with high-quality typography to evoke a sense of calm authority and enduring quality.

## Colors

The palette is anchored by the "Monolithic Elegance" core: warm whites (Stone Ivory), soft concrete greys, and matte charcoals. The primary accent is a deep **Forest Green (#1B3022)**, used with deliberate restraint to signify importance without overwhelming the neutral foundation.

- **Primary:** Forest Green (#1B3022) for primary CTAs, active states, and core branding.
- **Secondary/Tertiary:** Mid-leaf greens (#6EA83D, #9DBF45) derived from the logo gradient, reserved strictly for hover states, success indicators, or subtle decorative accents.
- **Neutrals:**
    - `Surface`: Ivory (#F9F8F6)
    - `Muted`: Concrete (#A8A8A8)
    - `Deep`: Charcoal (#2A2A2A)

## Typography

This design system uses a paired typography scale. Headlines and display titles utilize **Cormorant Garamond** to align with the elegant, stone-carved serif style of the logo. Navigation, subtitles, labels, and body copy use **Plus Jakarta Sans** to maintain geometric clarity, high readability, and a clean layout.

Headlines should utilize tight letter-spacing to mimic premium architectural editorial typography. Body copy remains spacious to ensure readability against stone-textured or neutral backgrounds. Use the uppercase label style for navigational elements and small metadata to reinforce the premium, editorial feel.

## Layout & Spacing

The layout follows a **fluid grid** model with generous margins to evoke a gallery-like atmosphere. 

- **Desktop:** 12-column grid with 24px gutters and 64px outer margins.
- **Tablet:** 8-column grid with 24px gutters and 32px margins.
- **Mobile:** 4-column grid with 16px gutters and 16px margins.

Spacing is governed by an 8px linear scale. Use larger increments (64px+) between major sections to emphasize "Monolithic" scale and prevent the UI from feeling cluttered.

## Elevation & Depth

Hierarchy is established through **Tonal Layering** rather than traditional shadows. Surfaces are stacked using subtle variations in the neutral palette (e.g., an Ivory card on a Concrete background).

When depth is required for interactive elements like modals or floating menus, use **Ambient Shadows**: ultra-diffused, 10-15% opacity shadows with a slight tint of Forest Green to ground the element in the brand's color space. Outlines should be used sparingly, favoring high-contrast background shifts to define boundaries.

## Shapes

The shape language is **Soft (0.25rem)**. This subtle rounding prevents the interface from feeling "sharp" or "hostile" while maintaining the structural integrity of the monolithic design style. 

Buttons and input fields should use the base 0.25rem radius. Large containers or image cards can scale up to 0.5rem (rounded-lg) to soften the overall composition, but never reach "pill" or "circular" territory, as that would conflict with the architectural narrative.

## Components

- **Buttons:** Primary buttons use a solid Forest Green (#1B3022) background with white text. Secondary buttons use a Charcoal border with no fill. Hover states for primary buttons should transition to the logo’s mid-green (#6EA83D).
- **Input Fields:** Use a Concrete grey border (1px) that darkens to Charcoal on focus. Labels must be in the uppercase `label-md` style.
- **Chips/Badges:** Use very light tints of the primary green with dark green text for subtle categorization.
- **Cards:** Flat surfaces with a 1px border in a slightly darker neutral than the background. No shadows by default; use tonal shifts to indicate interactivity.
- **Lists:** Clean, border-bottom separation using soft greys. High-contrast typography for list headers.
- **Navigation:** Understated matte charcoal text. The active state is indicated by a 2px Forest Green underline or a subtle weight shift.