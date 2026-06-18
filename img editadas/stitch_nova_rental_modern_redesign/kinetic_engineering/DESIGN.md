---
name: Kinetic Engineering
colors:
  surface: '#10141a'
  surface-dim: '#10141a'
  surface-bright: '#353940'
  surface-container-lowest: '#0a0e14'
  surface-container-low: '#181c22'
  surface-container: '#1c2026'
  surface-container-high: '#262a31'
  surface-container-highest: '#31353c'
  on-surface: '#dfe2eb'
  on-surface-variant: '#c3c5d8'
  inverse-surface: '#dfe2eb'
  inverse-on-surface: '#2d3137'
  outline: '#8d90a1'
  outline-variant: '#434655'
  surface-tint: '#b6c4ff'
  primary: '#b6c4ff'
  on-primary: '#00287e'
  primary-container: '#1357f0'
  on-primary-container: '#dfe3ff'
  inverse-primary: '#004fe5'
  secondary: '#ffb77f'
  on-secondary: '#4e2600'
  secondary-container: '#ff8a00'
  on-secondary-container: '#613100'
  tertiary: '#acc7ff'
  on-tertiary: '#002f67'
  tertiary-container: '#0063cc'
  on-tertiary-container: '#dbe5ff'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#dce1ff'
  primary-fixed-dim: '#b6c4ff'
  on-primary-fixed: '#00164f'
  on-primary-fixed-variant: '#003bb0'
  secondary-fixed: '#ffdcc4'
  secondary-fixed-dim: '#ffb77f'
  on-secondary-fixed: '#2f1500'
  on-secondary-fixed-variant: '#6f3900'
  tertiary-fixed: '#d7e2ff'
  tertiary-fixed-dim: '#acc7ff'
  on-tertiary-fixed: '#001a40'
  on-tertiary-fixed-variant: '#004491'
  background: '#10141a'
  on-background: '#dfe2eb'
  surface-variant: '#31353c'
typography:
  display-lg:
    fontFamily: Archivo Narrow
    fontSize: 72px
    fontWeight: '900'
    lineHeight: 72px
    letterSpacing: -0.04em
  headline-lg:
    fontFamily: Archivo Narrow
    fontSize: 48px
    fontWeight: '800'
    lineHeight: 48px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Archivo Narrow
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 36px
    letterSpacing: -0.01em
  headline-sm:
    fontFamily: Archivo Narrow
    fontSize: 24px
    fontWeight: '700'
    lineHeight: 28px
  body-lg:
    fontFamily: DM Sans
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: DM Sans
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-md:
    fontFamily: DM Sans
    fontSize: 14px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.05em
  label-sm:
    fontFamily: DM Sans
    fontSize: 12px
    fontWeight: '500'
    lineHeight: 14px
    letterSpacing: 0.02em
  headline-lg-mobile:
    fontFamily: Archivo Narrow
    fontSize: 36px
    fontWeight: '800'
    lineHeight: 36px
spacing:
  unit: 4px
  gutter: 24px
  margin: 48px
  container-max: 1440px
---

## Brand & Style

This design system embodies "Engineering Authority"—a high-performance aesthetic rooted in precision, structural integrity, and industrial innovation. The target audience includes engineers, data scientists, and technical leaders who value clarity, speed, and robust functionality.

The design style is a hybrid of **High-Contrast Minimalism** and **Technical Skeuomorphism**. It utilizes dark, metallic surfaces to create a sense of depth, accented by vibrant "live" data indicators and neon edge glows. Every element should feel deliberate and manufactured. 

Key visual motifs include:
- **Diagonal Geometry:** Use 45-degree cuts on corners and chevron patterns to suggest forward motion.
- **Blueprint Accents:** Subtle grid lines and coordinate markers (e.g., small "+" or "L" bracket icons) at container corners.
- **Glassmorphism:** High-density glass with metallic top-edge highlights (1px solid borders) to simulate machined hardware.

## Colors

The palette is anchored in a near-black graphite base to minimize eye strain and maximize the impact of functional color. 

- **Primary (Cobalt Blue):** Used for primary actions, active states, and technical branding.
- **Accent (Blue Glow):** Reserved for data visualizations, neon edge highlights, and indicating "system-on" states.
- **CTA (High-Vis Amber):** Strictly for critical path actions and urgent status warnings. It provides a stark contrast against the cool-toned foundation.
- **Surfaces:** Use `#11161F` for background containers and `#161C28` for elevated cards or floating panels. All surfaces must be framed with the `#2A3344` metallic border.

## Typography

Typography follows an "Information First" hierarchy. Headlines are aggressive, condensed, and always uppercase to mimic technical specifications and industrial marking. 

- **Headlines:** Use tight tracking (letter spacing) for a dense, high-impact feel.
- **Body:** DM Sans provides a clean, geometric counterpoint that ensures readability in data-heavy contexts.
- **Labels:** Use uppercase for small UI labels (e.g., table headers, status tags) to maintain the technical authority of the interface.

## Layout & Spacing

This design system utilizes a **12-column Fixed Grid** for desktop and a **4-column Fluid Grid** for mobile. 

The layout philosophy emphasizes generous negative space to prevent the high-contrast elements from feeling cluttered. Alignment should be strict and rigid; avoid center-aligning content unless it is a specific hero element. 

- **Padding:** Use an 8px base grid. Larger containers should utilize 32px or 48px internal padding to create a premium, spacious feel.
- **Technical Margins:** Use thin `#2A3344` lines to separate global navigation and sidebars, creating a clear architectural split in the layout.

## Elevation & Depth

Depth is conveyed through material properties rather than traditional shadows.

1.  **Base Layer:** The darkest `#0A0E14` background.
2.  **Surface Layer:** `#11161F` with a 1px solid `#2A3344` border.
3.  **Active/Elevated Layer:** `#161C28` with a 10px backdrop blur and a subtle inner glow (`#3E8BFF` at 10% opacity).
4.  **Accent Elevation:** Apply a vertical gradient to metallic borders (top being lighter than the bottom) to simulate top-down lighting on a physical chassis.

## Shapes

The shape language is strictly **Sharp (0px)** or **Chiseled**. 

- **Diagonal Cuts:** For primary buttons and high-level cards, use a `clip-path` or SVG mask to create a 45-degree diagonal cut on the top-right or bottom-left corner.
- **Chevrons:** Use 45-degree angle brackets for directional cues and breadcrumbs.
- **Containers:** All containers should have perfectly sharp corners. Avoid any rounding to maintain the "machined" aesthetic.

## Components

- **Buttons:** Primary buttons use Cobalt Blue with a 45-degree cut on the top-right corner. Text is white, uppercase Archivo. CTA buttons use Amber with a subtle outer glow on hover.
- **Cards:** Use the Dark Steel background with a metallic top border (2px). Background should have a 10% transparency with a heavy backdrop blur (20px) when overlapping other elements.
- **Input Fields:** Dark base (`#0A0E14`) with a 1px border. Focus state changes the border to Cobalt Blue with a 2px neon glow effect. Labels are uppercase DM Sans.
- **Chips/Status Tags:** Rectangular with no rounding. Use small 1px border indicators. Use Amber for "Caution", Cobalt for "Processing", and a muted Grey for "Idle".
- **Technical Accents:** Use "Crosshair" icons in the corners of major dashboard modules to reinforce the engineering theme.