---
name: Eco Stone Architectural Editorial
sourceOfTruth: index.html
colors:
  paper: '#f0eae1'
  sand: '#e6ded0'
  ink: '#1a1815'
  ink-soft: '#232019'
  feature-black: '#0b0b0a'
  muted: '#756e62'
  on-ink: '#f0eae1'
  on-ink-muted: '#a79e90'
  dark-muted: '#938d84'
  dark-body: '#aaa49a'
  line: '#d8cfc0'
typography:
  sans: Inter
  serif: Cormorant Garamond
  icons: Material Symbols Outlined
layout:
  content-max: 1320px
  mobile-gutter: 22px
  desktop-gutter: 80px
breakpoints:
  compact: 480px
  small: 640px
  tablet: 768px
  desktop: 1024px
  wide: 1280px
---

# Eco Stone Homepage Design System

## Source And Scope

`index.html` is the sole source of truth for this document. The system described here is the design language currently implemented and rendered on the Eco Stone homepage. It includes the homepage's inline Tailwind configuration, custom CSS, markup, responsive behavior, motion, interactions, and directly referenced visual assets.

Do not use another page to extend or reinterpret this system. When this document and `index.html` disagree, follow `index.html` and update this document.

## Brand Character

The homepage presents Eco Stone as a premium architectural fabrication company through four qualities:

- **Material confidence:** stone, cabinetry, veining, and installed surfaces carry the visual story.
- **Editorial restraint:** large typography, asymmetric composition, fine rules, and controlled negative space replace cards and decoration.
- **Craft credibility:** proof points, process language, project details, and founder content remain specific and direct.
- **Warm permanence:** warm mineral neutrals soften the industrial precision of near-black feature sections.

The overall expression is calm, masculine, exacting, and expensive. It should feel closer to an architecture or interiors publication than a conventional contractor template.

## Visual Principles

1. Use photography at architectural scale. Images are full-bleed panels or large editorial figures, never decorative thumbnails.
2. Alternate warm light sections with near-black feature sections to create deliberate rhythm.
3. Build hierarchy with scale, type contrast, spacing, and 1px rules. Do not introduce cards, shadows, badges, or ornamental containers.
4. Use serif typography for human, premium, and material-led statements. Use sans-serif typography for structure, process, navigation, and monumental graphic statements.
5. Keep green inside the official logo. The interface itself is almost entirely neutral.
6. Preserve square image edges and full-bleed section boundaries. Rounded geometry is reserved for clear controls.

## Logo System

The homepage uses two official transparent PNG lockups, both with a native size of `1071 x 260`:

- `images/eco-stone-white.png`: white wordmark for transparent navigation over the hero and the dark footer.
- `images/eco-stone-dark.png`: dark wordmark for the condensed white navigation and mobile menu.

Rules:

- Never recreate the logo with HTML text, CSS, or a substitute icon.
- Preserve the `1071 / 260` aspect ratio and transparent background.
- The header lockup is `166px` wide by default and `196px` from `768px` upward.
- The scrolled header scales the lockup to `90%` without changing its layout footprint.
- The footer logo is `230px` wide on mobile, `300px` from `768px`, and `340px` from `1200px`.
- Header variants crossfade in the same positioned frame, preventing layout shift.

## Color System

### Core Tokens

| Token | Value | Homepage role |
| --- | --- | --- |
| `paper` | `#f0eae1` | Warm off-white, light CTA fill, dark-section text |
| `sand` | `#e6ded0` | Trust, services, and founder section background |
| `ink` | `#1a1815` | Primary light-section text |
| `ink-soft` | `#232019` | Configured secondary dark neutral |
| `feature-black` | `#0b0b0a` | Selected Work, Process, and footer background |
| `muted` | `#756e62` | Secondary text on warm light backgrounds |
| `on-ink` | `#f0eae1` | Primary text on feature black |
| `on-ink-muted` | `#a79e90` | Global muted dark-section text |
| `dark-muted` | `#938d84` | Project metadata, numbers, and process eyebrows |
| `dark-body` | `#aaa49a` | Paragraphs on near-black sections |
| `line` | `#d8cfc0` | Rules and dividers on warm light sections |

### Local Supporting Values

- `#141412`: project image-frame fallback.
- `#171715`: founder image fallback.
- `#fffaf0`: subtle light hover on dark controls.
- `#5d5549`: restrained hover color for the Google review feature.
- `rgba(240,234,225,.14-.24)`: rules and borders on dark backgrounds.
- `rgba(26,24,21,.12-.32)`: rules and outlines on light backgrounds.
- `rgba(255,255,255,.94)`: scrolled navigation surface.

The green leaf gradient belongs to the supplied logo artwork. Do not promote it into a general UI accent without changing the homepage source first.

## Typography

### Font Families

- **Inter:** weights `400`, `500`, and `600`. Used for body copy, navigation, labels, buttons, process typography, service rows, and the monumental Selected Work headline.
- **Cormorant Garamond:** roman weights `500` and `600`; italic weights `400`, `500`, and `600`. Used for the hero, trust headline, project names, founder statements, testimonial, signatures, and footer invitation.
- **Material Symbols Outlined:** interface arrows, menu controls, close controls, and gallery navigation. Default settings are fill `0`, weight `300`, grade `0`, optical size `24`.

The body enables Inter features `cv11` and `ss01`.

### Typographic Roles

| Role | Implementation |
| --- | --- |
| General display | Inter `clamp(2.5rem, 6.2vw, 5.4rem)`, line-height `1`, tracking `-0.03em` |
| Small display | Inter `clamp(2.1rem, 4.4vw, 3.7rem)`, line-height `1.03`, tracking `-0.028em` |
| Hero | Cormorant Garamond `clamp(3.6rem, 9vw, 8rem)`, weight `500`, line-height `.9` |
| Hero italic | Cormorant Garamond italic, weight `600`, `1.12em`, line-height `.82` |
| Trust headline | Cormorant Garamond `2.9rem` mobile, otherwise fluid to `4.1rem`, line-height `.91` |
| Selected Work headline | Inter `2.75rem` mobile to `10.75rem` ultrawide, weight `500`, line-height `.86` |
| Project title | Cormorant Garamond `3rem` mobile to `4.8rem` desktop, line-height `.92` |
| Process headline | Inter `2.5rem` mobile to `4.75rem` wide desktop, line-height `.96` |
| Founder quote | Cormorant Garamond `2.35rem` mobile to `3.7rem` wide desktop |
| Builder testimonial | Cormorant Garamond `2rem` mobile to `2.7rem` wide desktop |
| Footer invitation | Cormorant Garamond `2.45rem` mobile to `3.35rem` desktop |
| Eyebrow | Inter `11.5px`, weight `500`, tracking `.2em`, uppercase |
| Hero eyebrow | Inter `12px`, weight `500`, tracking `.22em`, uppercase |
| Body | Inter `1rem` default; major editorial paragraphs use `1.0625rem` |
| Lead copy | Inter weight `400`, line-height `1.62`; hero uses `1.125rem` mobile and `1.25rem` from `768px` |
| Metadata | Inter approximately `.68-.8rem`, uppercase where structural, tracking `.1-.18em` |

### Serif Italic

Italic is a controlled brand device, not decoration. It highlights the emotional or human conclusion of a statement:

- `beautiful.` in the hero and footer.
- `custom builders.` in the trust headline.
- `outlast us` in Dom's founder statement.
- `stands behind his work.` in the builder testimonial.

Do not italicize whole paragraphs or use script/calligraphic substitutes.

## Layout System

### Global Frame

- Primary content max-width: `1320px`.
- Mobile outer gutter: `22px`.
- Desktop outer gutter from `768px`: `80px`.
- The page clips horizontal overflow at the root.
- Sections use a mix of constrained content, 12-column grids, and full-bleed media. This is not a universal card or container system.

### Responsive Breakpoints

| Breakpoint | Implemented purpose |
| --- | --- |
| `480px` | Selected Work headline step |
| `640px` | Small/tablet type changes, hero CTA row, trust line breaks |
| `768px` | Desktop gutter, 12-column project grid, three-column process, larger header and footer |
| `1024px` | Desktop navigation, split trust/services/founder layouts, sticky founder portrait |
| `1200px` | Founder and footer refinements |
| `1280px` | Large headline and founder type steps |
| `1400px` | Selected Work headline step |
| `1440px` | Founder type refinement |
| `1536px` | Gallery max-width expansion |
| `1920px` | Featured project duo expands to `80vw` |

Treat `<768px` as mobile, `768-1023px` as tablet, and `>=1024px` as desktop when adding behavior, while respecting the smaller type-specific steps.

### Spacing Rhythm

The homepage does not use a strict 8px spacing scale. Its rhythm is implemented through recurring editorial bands:

- Mobile section gutters are commonly `22px` with vertical padding around `5-7rem`.
- Tablet and desktop section gutters are commonly `80px` with vertical padding around `8-10rem`.
- Project chapters separate by `10rem` mobile and `14rem` from `768px`.
- Large gallery compositions use intentionally asymmetric top offsets between `5rem` and `11rem`.
- Major boundaries are expressed with background changes or full-bleed media, not floating section containers.

## Shape, Rules, And Depth

- Image edges and section edges are square.
- Structural dividers are typically `1px` with low-opacity warm or dark color.
- Short rules are `42-48px` and sit beside eyebrows or attributions.
- Rounded pills are reserved for explicit calls to action and the header utility button.
- Circular controls are reserved for the lightbox.
- There are no content cards, image shadows, gradients as standalone decoration, or rounded image frames.
- The only ambient shadow is the subtle scrolled-header shadow: `0 8px 28px rgba(11,11,10,.06)`.

## Photography And Media

Only homepage-referenced assets define the visual system.

### Hero Film

- Desktop: `images/hero.mp4`, H.264, `1920 x 1080`, 24fps, approximately 16.08 seconds.
- Mobile/tablet: `images/hero-mobile.mp4`, H.264, `864 x 1320`, 24fps, approximately 16.08 seconds.
- Poster: `images/hero-poster.jpg`, `1080 x 1650`.
- The film fills a minimum `100vh` hero with `object-cover`.
- A black-to-transparent vertical overlay preserves white type readability.

### Trust, Services, And Founder

- Trust image: `images/eco-stone-installer-black-granite-countertop-backsplash.webp`, `1600 x 1069`, full-bleed right panel on desktop and stacked below on smaller screens. Crop focus is `50% 68%`.
- Services image: `images/services-dsc00863-1400.webp` and `-2400.webp`, full-height left panel on desktop, below the content on smaller screens. Crop focus is `53% 48%`.
- Founder portrait: `images/founder-editorial-900.webp` and `images/founder-editorial.webp` (`1800 x 2694`). It is full-width above content on mobile/tablet and a sticky `46%` left panel on desktop.

### Selected Work Photography

- Project images use responsive WebP sources at `1200`, `2400`, and where available `3200` pixels.
- Landscape frames use `3 / 2`; portrait frames use `2 / 3`.
- The lead image expands to `88vw` on desktop, with controlled black margins.
- The next two featured images use an asymmetric duo. The second remains smaller; the third is dominant and vertically offset.
- Additional images remain hidden until the project is expanded and are hydrated on hover, focus, or open.
- Crops must prioritize stone surfaces, cabinetry, edge details, fireplaces, vanities, and completed installation context.

Do not apply artificial color overlays, rounded frames, borders, or shadows to project photography.

## Homepage Composition

### Adaptive Header

- Fixed above the page.
- At the top: transparent, white logo, white navigation.
- After `60px` of scroll: `94%` white surface, `14px` backdrop blur, dark logo, dark text, fine border, subtle shadow.
- Header height is `80px` mobile and `96px` from `768px`; condensed heights are `68px` and `78px` respectively.
- Primary navigation appears from `1024px`.
- The outlined `Start a project` pill appears from `640px`.
- Below `1024px`, the menu button opens a full-screen warm-paper navigation dialog.

### Hero

- Full-viewport cinematic video with bottom-aligned content.
- Serif headline is the dominant signal; the italic second line is larger and heavier.
- Supporting copy is limited to a narrow measure.
- Primary CTA is a warm-paper pill; secondary CTA is an underlined text link.
- On mobile, the CTAs stack and the primary control stretches across the content width.

### Trust Section

- Warm sand background with an editorial text/image split.
- Desktop uses a `50vw`-based content column and full-height image panel.
- Mobile/tablet stack copy before the image.
- Trust hierarchy: eyebrow, serif headline, introduction, dominant `21` review proof, then quieter supporting facts.
- Google review interaction remains typographic and understated; no badges, stars, or Google branding.

### Selected Work

- Near-black background across the entire gallery.
- Opening headline uses monumental Inter rather than serif, creating graphic contrast with the hero.
- Mobile opening is compact; from `768px` it becomes a `100svh` three-row composition.
- Each project contains editorial metadata, a large lead image, two always-visible featured images, an expandable gallery, and a collapse control.
- Captions stay attached to their corresponding image.

### Services

- Warm sand split section.
- Desktop: image left, content right, both visually full-height.
- Mobile/tablet: content first, image second.
- Service rows use numbering, fine dividers, concise descriptions, and north-east arrows. They are links, not cards.

### Process

- Near-black full-width band.
- Large Inter headline and muted eyebrow.
- Three equal process columns from `768px`; stacked rule-separated steps below that.
- Titles are warm white; descriptions and numbers are secondary grey.

### Founder And Builder Perspective

- Warm sand editorial profile.
- Desktop: sticky portrait at `46%`, content at `54%`, unfolding in two vertical beats.
- Mobile/tablet: portrait, founder statement, then builder testimonial.
- Founder and testimonial use Cormorant Garamond with restrained italic emphasis.
- Attribution uses uppercase Inter and short architectural rules.

### Footer

- Near-black conclusion using the official white logo as the primary anchor.
- Project invitation remains moderate in scale.
- Navigation, contact details, legal text, and back-to-top link are quiet and rule-separated.
- Footer content stacks on mobile and uses a 12-column alignment from `768px`.

## Interaction System

### General Reveal

- `.reveal` begins at opacity `0` and `translateY(24px)`.
- Intersection threshold is `.12`, with a bottom root margin of `-8%`.
- Reveal duration is `1s` using `cubic-bezier(.22,.61,.36,1)`.
- Stagger delays are `90ms`, `180ms`, and `270ms`.

### Selected Work Scroll Reveal

- Eyebrow, two headline lines, and summary respond to forward and reverse scroll.
- Text begins visible in low-contrast grey rather than disappearing.
- Movement is limited to `6-10px` vertical settling.
- No character-level animation, pinning, scale, rotation, or blur is used.

### Header Motion

- Header surface, height, spacing, and logo scale transition over `.45s`.
- Logo opacity crossfade takes `.28s`.
- State is applied on initial load, scroll, and `pageshow` to avoid incorrect refresh states.

### Project Gallery

- Image hover scale: `1.001` to `1.018` over `.8s`.
- Expand/collapse uses height, opacity, and an `18px` vertical offset over approximately `.42s`.
- Expanded images are lazy-hydrated before display.
- The lightbox supports previous/next controls, keyboard arrows, Escape, a contained Tab loop, touch swipes, and focus return to the opening image.
- Opening the lightbox locks body scrolling.

### Link Feedback

- Text links use subtle color shifts or a 1px underline reveal.
- North-east arrows translate only a few pixels on hover.
- Focus-visible states use high-contrast `1-2px` outlines with `3-6px` offsets.

## Reduced Motion And Resilience

When `prefers-reduced-motion: reduce` is active:

- Hero video sources are removed and the poster remains visible.
- General reveals resolve immediately.
- Header, logo, image, project expansion, review, and lightbox transitions are disabled.
- Selected Work text is immediately shown in its finished state.
- Smooth scrolling is disabled.

If `IntersectionObserver` is unavailable, reveal content is shown immediately. If JavaScript is disabled, the header remains visible through the `<noscript>` fallback.

## Accessibility Conventions

- Semantic sections, headings, figures, captions, navigation landmarks, and footer landmarks structure the page.
- Images use descriptive alt text; decorative logo duplicates and symbols use empty alt text or `aria-hidden` where appropriate.
- The mobile menu and lightbox expose dialog semantics and labelled controls.
- Project toggles expose `aria-expanded` and `aria-controls`.
- The review link announces that it opens in a new tab.
- Interactive rows and gallery controls provide visible keyboard focus states.
- Mobile links and footer controls generally maintain a minimum `44px` interactive height.
- Warm white is used instead of pure white for large dark-section surfaces, while primary text maintains strong contrast.

## Content Voice

Homepage copy is concise, specific, and craft-led. It favors material and process language such as fabrication, templating, installation, proportion, surfaces, veining, and permanence.

- Use direct evidence rather than generic superlatives.
- Keep service-area language to Burlington and GTA.
- Keep headlines short enough for deliberate line breaks.
- Avoid unverified affiliations, awards, statistics, or business claims.
- Avoid decorative marketing language that competes with the photography.

## Do Not Introduce

The homepage does not establish any of the following as part of the Eco Stone system:

- Card grids or nested cards.
- Rounded image containers.
- Decorative gradients, glows, or floating shapes.
- Generic green UI surfaces or green CTA buttons.
- Heavy shadows or raised panels.
- Star ratings, badges, chips, or testimonial carousels.
- Script fonts, generic heavy serif substitutes, or calligraphic styling.
- Dense iconography or social-media clutter.
- New content, links, claims, or affiliations without verification.
