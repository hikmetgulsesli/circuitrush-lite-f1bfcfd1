---
name: CircuitRush Lite
colors:
  surface: '#10131b'
  surface-dim: '#10131b'
  surface-bright: '#363941'
  surface-container-lowest: '#0b0e15'
  surface-container-low: '#181b23'
  surface-container: '#1d2027'
  surface-container-high: '#272a32'
  surface-container-highest: '#32353d'
  on-surface: '#e0e2ed'
  on-surface-variant: '#b9cacb'
  inverse-surface: '#e0e2ed'
  inverse-on-surface: '#2d3038'
  outline: '#849495'
  outline-variant: '#3b494b'
  surface-tint: '#00dbe9'
  primary: '#dbfcff'
  on-primary: '#00363a'
  primary-container: '#00f0ff'
  on-primary-container: '#006970'
  inverse-primary: '#006970'
  secondary: '#ebb2ff'
  on-secondary: '#520072'
  secondary-container: '#b600f8'
  on-secondary-container: '#fff6fc'
  tertiary: '#e1ffd1'
  on-tertiary: '#053900'
  tertiary-container: '#33fb0a'
  on-tertiary-container: '#106e00'
  error: '#ffb4ab'
  on-error: '#690005'
  error-container: '#93000a'
  on-error-container: '#ffdad6'
  primary-fixed: '#7df4ff'
  primary-fixed-dim: '#00dbe9'
  on-primary-fixed: '#002022'
  on-primary-fixed-variant: '#004f54'
  secondary-fixed: '#f8d8ff'
  secondary-fixed-dim: '#ebb2ff'
  on-secondary-fixed: '#320047'
  on-secondary-fixed-variant: '#74009f'
  tertiary-fixed: '#79ff5b'
  tertiary-fixed-dim: '#2ae500'
  on-tertiary-fixed: '#022100'
  on-tertiary-fixed-variant: '#095300'
  background: '#10131b'
  on-background: '#e0e2ed'
  surface-variant: '#32353d'
typography:
  display-lg:
    fontFamily: Sora
    fontSize: 48px
    fontWeight: '800'
    lineHeight: '1.1'
    letterSpacing: -0.04em
  display-score:
    fontFamily: Space Grotesk
    fontSize: 40px
    fontWeight: '700'
    lineHeight: '1'
    letterSpacing: 0.1em
  headline-md:
    fontFamily: Sora
    fontSize: 24px
    fontWeight: '600'
    lineHeight: '1.2'
  body-lg:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: '1.6'
  body-sm:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: '1.5'
  label-caps:
    fontFamily: Space Grotesk
    fontSize: 12px
    fontWeight: '700'
    lineHeight: '1'
    letterSpacing: 0.2em
spacing:
  unit: 4px
  gutter: 16px
  margin-mobile: 20px
  margin-desktop: 40px
  grid-cols: '12'
---

## Brand & Style

The design system is engineered for high-octane, rhythm-based arcade experiences. It evokes a "hacker-space" aesthetic where the user feels like they are navigating the inner pulse of a motherboard. The brand personality is kinetic, precise, and rebellious. 

**Style: Cyber-Vapor Minimal**
The system merges **Glassmorphism** with **High-Contrast Neon**. It utilizes deep, ink-like backgrounds to provide maximum luminosity for "signal" elements. UI components appear as floating HUD overlays rather than static containers, emphasizing speed and transparency. Circuit-line motifs (thin 1px lines with 45-degree angles) should be used as decorative accents to connect UI clusters.

## Colors

The palette is optimized for OLED displays and low-light environments. 

- **Primary (Signal Cyan):** Used for interactive nodes, active paths, and primary "Go" actions.
- **Secondary (Pulse Purple):** Used for rare items, experience meters, and secondary navigation.
- **Tertiary (Gate Green):** Used for "Success" states, health bars, and unlocked gates.
- **Emergency (Overload Red):** Reserved strictly for critical warnings, low health, or system failure.
- **Backgrounds:** Use a deep `#080B12` to allow neon glows to bloom. Surface containers should use semi-transparent variants of `#121826` with a `backdrop-filter: blur(12px)`.

## Typography

This design system uses a hierarchical font strategy to balance readability with a technical aesthetic. 

- **Display & Headlines:** Use **Sora** for its wide, geometric structure. It feels futuristic yet accessible.
- **Data & HUD:** Use **Space Grotesk** for scores, timers, and technical labels. The monospaced feel and "stinging" terminals of the glyphs align with the circuit-board motif.
- **General UI:** Use **Inter** for all descriptive text, settings, and menus to ensure high legibility during fast movement.

Apply `text-shadow: 0 0 8px [color]` to Display and Score elements to simulate a CRT or LED glow.

## Layout & Spacing

The layout follows a **Fluid HUD model**. Instead of a centered page column, elements are anchored to the corners and edges of the viewport to maximize the playable "field" in the center.

- **Grid:** Use a 12-column grid for menus, but apply a "scanline" overlay (1px horizontal lines every 4px) to give the layout structure.
- **Rhythm:** All spacing is based on a 4px module. 
- **Safe Zones:** Maintain a 40px margin on desktop and 20px on mobile to ensure HUD elements do not interfere with physical bezel edges.
- **Connectivity:** UI panels should be "linked" by thin 1px Cyan lines that appear to "plug into" the screen edges.

## Elevation & Depth

Depth is not achieved through traditional drop shadows but through **Luminance and Blur**.

1.  **Level 0 (Background):** Solid dark blue-black with a faint geometric grid pattern.
2.  **Level 1 (The Field):** Interactive game elements (nodes, paths) with intense outer glows.
3.  **Level 2 (HUD Panels):** Glassmorphic surfaces. Use a 1px solid Cyan or Purple border with 40% opacity. 
4.  **Level 3 (Overlays/Modals):** High blur (20px+) backdrop filter. The border-glow intensity increases here to create a "focus" effect.

Avoid using black shadows; instead, use colored glows (`box-shadow: 0 0 15px rgba(0, 240, 255, 0.3)`).

## Shapes

The design system utilizes **Sharp (0px)** corners to reinforce the technical, aggressive nature of a high-speed circuit. 

- **Clipped Corners:** Use CSS `clip-path` to create 45-degree "chamfered" corners on large panels and primary buttons.
- **Nodes:** Key interactive gameplay elements should be perfect circles or diamonds to contrast against the rectangular UI.
- **Connectors:** Lines should only move in 90 or 45-degree increments.

## Components

### Buttons
- **Default:** Sharp corners, 1px Cyan border, transparent background. Text in Label-Caps.
- **Hover/Active:** Background fills with Cyan, text color switches to Neutral Black. A "Bloom" effect (box-shadow) appears around the button.
- **Sound:** Every interaction should trigger a high-frequency haptic or audio pulse.

### HUD Panels
- Transparent backgrounds with a `background: linear-gradient(to bottom, rgba(18, 24, 38, 0.8), rgba(18, 24, 38, 0.4))`.
- 1px top-border in Signal Cyan to act as a "power rail."

### Sliders & Toggles
- **Sliders:** The track is a dim gray line; the "thumb" is a glowing Cyan diamond. 
- **Toggles:** Square-based. "On" state fills the square with Lime Green and adds a small "Power-on" icon.

### Progress Bars
- Segmented into vertical blocks (bits). As the bar fills, each segment lights up with a flicker effect.

### Data Chips
- Small, rectangular tags used for "Multipliers" or "Level Names." These should have a subtle pulse animation.