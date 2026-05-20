---
name: Wisdom Cyber-Fintech
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
  on-surface-variant: '#bbc9cf'
  inverse-surface: '#e5e2e1'
  inverse-on-surface: '#313030'
  outline: '#859399'
  outline-variant: '#3c494e'
  surface-tint: '#4cd6ff'
  primary: '#a4e6ff'
  on-primary: '#003543'
  primary-container: '#00d1ff'
  on-primary-container: '#00566a'
  inverse-primary: '#00677f'
  secondary: '#ffb3b2'
  on-secondary: '#680013'
  secondary-container: '#ff525d'
  on-secondary-container: '#5b000f'
  tertiary: '#37fe11'
  on-tertiary: '#053900'
  tertiary-container: '#28de00'
  on-tertiary-container: '#0b5b00'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#b7eaff'
  primary-fixed-dim: '#4cd6ff'
  on-primary-fixed: '#001f28'
  on-primary-fixed-variant: '#004e60'
  secondary-fixed: '#ffdad9'
  secondary-fixed-dim: '#ffb3b2'
  on-secondary-fixed: '#410008'
  on-secondary-fixed-variant: '#92001f'
  tertiary-fixed: '#79ff5b'
  tertiary-fixed-dim: '#2ae500'
  on-tertiary-fixed: '#022100'
  on-tertiary-fixed-variant: '#095300'
  background: '#131313'
  on-background: '#e5e2e1'
  surface-variant: '#353534'
typography:
  display-lg:
    fontFamily: Sora
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  headline-lg:
    fontFamily: Sora
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-lg-mobile:
    fontFamily: Sora
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  title-md:
    fontFamily: Sora
    fontSize: 20px
    fontWeight: '500'
    lineHeight: 28px
  body-lg:
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
    letterSpacing: 0.08em
rounded:
  sm: 0.25rem
  DEFAULT: 0.5rem
  md: 0.75rem
  lg: 1rem
  xl: 1.5rem
  full: 9999px
spacing:
  unit: 8px
  container-padding: 24px
  gutter: 16px
  stack-sm: 8px
  stack-md: 16px
  stack-lg: 32px
---

## Brand & Style
The design system is built on a "Cyber-Fintech" narrative, merging the precision of high-end financial institutions with a futuristic, neon-drenched aesthetic. It targets a modern educational environment where financial transparency and technological advancement are paramount. 

The style is defined by **Glassmorphism** and **High-Contrast Neon accents**. Every interface element should feel like a floating projection—utilizing depth, translucency, and subtle glow to create a sense of three-dimensional space within a digital glass cockpit. The emotional goal is to evoke a sense of absolute security, premium quality, and effortless control over complex data.

## Colors
The palette is rooted in a "Void Black" base to maximize the luminance of the neon accents. 

- **Primary (Neon Blue):** Used for interactive states, key data visualizations, and primary actions. It represents wisdom and clarity.
- **Secondary (Crimson Red):** Reserved for high-importance alerts, negative financial trends, and critical "stop" actions.
- **Success (Neon Green):** Specifically for positive growth and completed transactions.
- **Surfaces:** All containers use a semi-transparent "Glass Gray" to allow background depth and light refraction to peak through, maintaining the futuristic HUD (Heads-Up Display) feel.

## Typography
The typography strategy contrasts the geometric, tech-forward nature of **Sora** for headings with the utilitarian precision of **Inter** for data-heavy body text. 

- Use **Sora** for all brand-facing elements and financial totals to emphasize the futuristic aesthetic. 
- Use **Inter** for descriptions, table data, and labels to ensure maximum legibility against dark, translucent backgrounds.
- Employ **Label-Caps** for category tags and metadata to create a structural, "system-code" feel.

## Layout & Spacing
This design system utilizes a **12-column fluid grid** for desktop and a **4-column grid** for mobile. The layout philosophy is "Floating Modules"—components should never feel cramped; they are separated by generous gutters to allow the "neon glow" of borders to breathe.

- **Margins:** Desktop uses a 40px outer margin, while mobile scales down to 16px.
- **Sidebar:** A sleek, minimal sidebar (width: 280px) remains fixed, using a backdrop-blur effect to maintain context of the underlying dashboard.
- **Grouping:** Related financial metrics are grouped in glass cards with 16px internal padding.

## Elevation & Depth
Depth is achieved through **Backdrop Filtering** and **Luminescent Shadows** rather than traditional gray-scale shadows.

- **Level 1 (Base):** Deep Black (#050505).
- **Level 2 (Cards):** Glass Gray surface with a 12px Backdrop Blur (Saturate 150%). A 1px border using `border_glow` provides definition.
- **Level 3 (Modals/Popovers):** Higher transparency, increased blur (20px), and a soft external drop shadow using the `primary_color` at 15% opacity to create a "hovering light" effect.

## Shapes
The shape language is "Hyper-Rounded Modern." A consistent **16px radius (rounded-lg)** is applied to all primary containers and cards to soften the aggressive nature of the neon colors, making the professional app feel more approachable.

- **Interactive Elements:** Buttons and Input fields follow the 16px rule.
- **Status Pills:** Use a full "Pill" radius for categorical labels to distinguish them from functional buttons.

## Components
- **Buttons:** Primary buttons feature a linear gradient (Neon Blue to a deep Violet/Purple) with a subtle outer glow on hover. Secondary buttons use a transparent background with a 1px Neon Blue border.
- **Input Fields:** Dark glass backgrounds with a 1px bottom-border that "activates" by glowing brighter when focused.
- **Glass Cards:** The cornerstone of the UI. Must feature `backdrop-filter: blur(12px)` and a subtle internal highlight on the top edge to simulate glass thickness.
- **Navigation:** Vertical sidebar with icons that utilize "Dual-Tone" coloring—Neon Blue for the active state and a muted Gray for inactive.
- **Data Visualization:** Charts should use "Neon Glow" lines. Area charts must use gradients that fade from the accent color into the dark background.
- **Chips/Badges:** Small, high-contrast indicators for "Paid," "Pending," or "Overdue," utilizing the Success and Secondary colors respectively.