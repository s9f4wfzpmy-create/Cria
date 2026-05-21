---
name: Cria Artisan Marketplace
colors:
  surface: '#131313'
  surface-dim: '#131313'
  surface-bright: '#3a3939'
  surface-container-lowest: '#0e0e0e'
  surface-container-low: '#1c1b1b'
  surface-container: '#201f1f'
  surface-container-high: '#2a2a2a'
  surface-container-highest: '#353534'
  on-surface: '#e5e2e1'
  on-surface-variant: '#e4beb3'
  inverse-surface: '#e5e2e1'
  inverse-on-surface: '#313030'
  outline: '#ab897f'
  outline-variant: '#5b4038'
  surface-tint: '#ffb59e'
  primary: '#ffb59e'
  on-primary: '#5e1700'
  primary-container: '#ff5a1f'
  on-primary-container: '#541400'
  inverse-primary: '#ae3200'
  secondary: '#d1bcff'
  on-secondary: '#3d0090'
  secondary-container: '#6b05f0'
  on-secondary-container: '#d7c4ff'
  tertiary: '#c6c6c7'
  on-tertiary: '#2f3131'
  tertiary-container: '#919292'
  on-tertiary-container: '#292b2c'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#ffdbd0'
  primary-fixed-dim: '#ffb59e'
  on-primary-fixed: '#3a0b00'
  on-primary-fixed-variant: '#852400'
  secondary-fixed: '#eaddff'
  secondary-fixed-dim: '#d1bcff'
  on-secondary-fixed: '#24005b'
  on-secondary-fixed-variant: '#5700c8'
  tertiary-fixed: '#e2e2e2'
  tertiary-fixed-dim: '#c6c6c7'
  on-tertiary-fixed: '#1a1c1c'
  on-tertiary-fixed-variant: '#454747'
  background: '#131313'
  on-background: '#e5e2e1'
  surface-variant: '#353534'
typography:
  display-xl:
    fontFamily: Bebas Neue
    fontSize: 120px
    fontWeight: '400'
    lineHeight: 100px
    letterSpacing: -0.02em
  display-lg:
    fontFamily: Bebas Neue
    fontSize: 80px
    fontWeight: '400'
    lineHeight: 72px
    letterSpacing: 0.01em
  display-lg-mobile:
    fontFamily: Bebas Neue
    fontSize: 48px
    fontWeight: '400'
    lineHeight: 44px
  headline-md:
    fontFamily: Bebas Neue
    fontSize: 40px
    fontWeight: '400'
    lineHeight: 40px
    letterSpacing: 0.05em
  title-lg:
    fontFamily: Inter
    fontSize: 20px
    fontWeight: '600'
    lineHeight: 28px
  body-md:
    fontFamily: Inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  label-caps:
    fontFamily: Inter
    fontSize: 12px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.1em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 8px
  container-max: 1440px
  gutter: 24px
  margin-desktop: 64px
  margin-mobile: 20px
  section-gap: 120px
---

## Brand & Style
The design system for this artisan marketplace is built on the concept of "Cinematic Craft." It merges the raw, tactile nature of Brazilian handcraft with a high-end, digital gallery aesthetic. The goal is to make every product feel like a curated masterpiece spotlighted in a dark, immersive exhibition space.

**Design Style: Liquid Glass & Dark Luxury**
The UI utilizes a "Liquid Glass" approach—a sophisticated evolution of glassmorphism. Surfaces are deep, translucent black with high-refraction backdrop blurs, making the interface feel like polished obsidian. The atmosphere is emotional and premium, using light not just for visibility, but as a narrative tool to guide the user's eye toward the "Cria" (creation).

**Emotional Response**
- **Curated:** Every element feels intentional and high-value.
- **Immersive:** The dark UI recedes, allowing vibrant product photography and luminous accents to pop.
- **Culturally Rich:** A blend of modern tech precision and organic, soulful artistry.

## Colors
The palette is rooted in a "Void Black" foundation to create maximum depth. 

- **Primary (Artistic Orange):** Used for calls to action and primary brand moments. It represents the heat of creation and traditional clay/terracotta textures.
- **Secondary (Electric Purple):** Used for secondary accents, hovering states, and cinematic glow effects. It adds a digital, "neon-metropolis" edge to the artisanal theme.
- **Surface Strategy:** Backgrounds are `#050505`. Elevated surfaces use translucent blacks with a 40px blur radius.
- **Cinematic Lighting:** Use radial gradients of Orange and Purple (at 10-15% opacity) behind product cards or in the corners of the viewport to simulate light leaks from a gallery projector.

## Typography
The typography contrasts massive, industrial-strength headlines with precise, utilitarian UI text.

- **Display Text:** Bebas Neue provides an authoritative, "poster-like" feel. Use it for hero sections, category titles, and large numbers. It should always feel monumental.
- **UI & Body Text:** Inter provides the necessary "Apple-esque" clarity. Its neutral tone balances the expressive nature of the display font.
- **Styling Note:** Display headers should occasionally use "text-stroke" effects or subtle orange-to-purple gradients to emphasize the cinematic theme.

## Layout & Spacing
The layout follows a "Wide Frame" philosophy, similar to cinematic aspect ratios. 

- **Grid:** A 12-column fluid grid for desktop with generous 24px gutters. 
- **Rhythm:** We use a strict 8px base unit. However, section vertical spacing is intentionally exaggerated (120px+) to create "white space" (or rather, "dark space") that allows the eye to rest between artisanal collections.
- **Reflow:** On mobile, margins tighten to 20px, and large display type scales aggressively to ensure the "impact" remains without breaking layout bounds.

## Elevation & Depth
Depth is not created with traditional drop shadows, but through **light and refraction.**

- **Z-Axis Hierarchy:**
    1. **Level 0 (Base):** Deep black `#050505`.
    2. **Level 1 (Cards/Panels):** Translucent black with `backdrop-filter: blur(40px)`. High-sheen top border (1px white at 15% opacity).
    3. **Level 2 (Modals/Popovers):** Higher transparency, subtle inner glow (`box-shadow: inset 0 1px 1px rgba(255,255,255,0.2)`).
- **Reflections:** All glass surfaces should have a very faint gradient (top-left to bottom-right) to simulate a physical glass sheet catching a distant studio light.

## Shapes
The shape language is "Soft-Precision." We avoid the "bubbly" look of consumer apps, opting for sophisticated, architectural corners.

- **UI Elements:** Buttons and input fields use a tight 0.25rem (4px) radius to maintain a professional, sharp look.
- **Containers:** Large cards and glass panels use 0.75rem (12px) to feel more approachable and like "framed" art.
- **Media:** Product photography should always have the same corner radius as its container to maintain the "liquid" enclosed feel.

## Components
- **Buttons:** 
  - *Primary:* Solid Orange (#ff5a1f) with black text. On hover, a purple outer glow appears.
  - *Secondary:* Liquid Glass style with a 1px luminous border.
- **Cards:** The "Gallery Card" has no visible background until hovered. Upon hover, the glass surface fades in, and the luminous border glows with a purple-to-orange gradient.
- **Input Fields:** Minimalist. Only a bottom border (1px white @ 20%). When focused, the border turns Orange and a subtle "light leak" glow appears beneath the field.
- **Chips/Badges:** Small, all-caps Inter font. Backgrounds are deep purple at 20% opacity with a vibrant purple text color.
- **Curated Lists:** Horizontal scrolling carousels with "peek" behavior, where the next item is partially visible, encouraging discovery of the artisan's story.
- **The "Signature" Component:** A "Story Overlay"—a full-screen glass modal that uses cinematic video backgrounds to tell the artisan's process, with typography overlaid in white Bebas Neue.