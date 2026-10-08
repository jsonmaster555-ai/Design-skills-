# Color Theory and Palette Construction

Use this skill when choosing, generating, reviewing, or correcting a product color system.

This is not a list of pretty palettes. It explains why colors work together and turns color theory into operational UI rules.

## Core objective

Build color systems where every color has a job, relationships are intentional, contrast remains usable, and brand expression does not destroy hierarchy.

A color is not good or bad by itself. Judge it by hue, chroma/saturation, lightness, surrounding colors, area, context, meaning, and accessibility.

## The three variables

### Hue

Hue is the basic color family: red, orange, yellow, green, cyan, blue, violet, and the transitions between them.

Hue changes identity and association, but hue alone does not determine whether a color looks refined, loud, calm, cheap, premium, or readable.

### Chroma / saturation

Chroma describes color intensity.

High-chroma colors attract attention quickly. Low-chroma colors feel quieter and mix more easily with neutrals.

Treat saturation as an attention budget.

If every element is highly saturated, nothing has priority.

Use high chroma deliberately for:

- primary actions;
- meaningful state;
- selected objects;
- brand moments;
- small emphasis areas.

Use lower chroma for:

- large surfaces;
- supporting backgrounds;
- secondary decoration;
- dense application chrome.

### Lightness / value

Lightness is how light or dark a color appears.

Lightness differences are often more important to hierarchy and readability than hue differences.

Two different hues at nearly the same value can still blend together. Two related hues with strong value separation can remain easy to distinguish.

Always inspect a palette in grayscale or by perceived lightness, not only by hue.

## Why some shades feel better

A pure RGB extreme such as `#00FF00` is not inherently wrong, but it has extremely high chroma and can dominate a normal interface.

A more restrained green can preserve the hue while reducing visual aggression.

The question is not:

`Is green ugly?`

The useful questions are:

- Is this green too saturated for the area it occupies?
- Is it too close in lightness to its background?
- Does it compete with the primary action?
- Does green already mean success in this product?
- Does it still work in dark mode and high-contrast settings?

## Area changes perceived intensity

The larger the colored area, the more powerful the color feels.

A vivid accent can work well on:

- a small icon;
- a selected tab;
- a primary button;
- a tiny data marker.

The same color across an entire page background may become overwhelming.

As surface area increases, usually reduce chroma or increase neutrality unless the brand deliberately requires an immersive color field.

## Color relationships

### Monochromatic

One hue with multiple lightness/chroma levels.

Useful for coherent interfaces because the colors are naturally related.

Do not rely on tiny shade differences for critical distinctions.

### Analogous

Nearby hues such as blue, cyan, and green.

Useful for smooth, cohesive palettes.

Watch for weak contrast because neighboring hues can become similar in perceived value.

### Complementary

Opposite regions of the color wheel, such as blue/orange.

Useful for strong contrast and emphasis.

Do not give both colors equal saturation and equal area by default. Usually one should dominate while the other acts as an accent.

### Split complementary

A main hue plus colors near its complement.

Useful when direct complements feel too aggressive.

### Triadic

Three widely separated hues.

Can feel energetic but is easy to overuse. Assign clear dominance rather than treating all three as equal accents.

## Harmony is not enough

A mathematically harmonious palette can still produce bad UI.

UI also needs:

- readable contrast;
- semantic consistency;
- clear emphasis;
- state distinction;
- light/dark adaptation;
- color-vision resilience;
- appropriate surface area.

Do not generate a palette from a color wheel and stop there.

## Build colors by role

Prefer semantic roles over raw color names in product design.

Example roles:

- background;
- surface;
- elevated surface;
- text primary;
- text secondary;
- text disabled;
- border subtle;
- border strong;
- accent;
- accent hover;
- accent pressed;
- focus;
- success;
- warning;
- danger;
- info;
- selection.

Then map those roles to palette values.

Do not scatter hard-coded blue/gray/red values throughout the product.

## Brand color discipline

A brand color becomes less meaningful when it is used everywhere.

Do not automatically color:

- every icon;
- every link;
- every heading;
- every badge;
- every control;
- every card border.

Reserve the brand color for meaningful emphasis and identity.

Apple's current branding guidance explicitly warns that using an accent color too broadly can overwhelm the interface and dilute its impact.

## Semantic consistency

Never use the same color to mean unrelated things in the same interface.

If green means success, avoid using the same green for random decorative text.

If red means destructive action, do not use identical red for a neutral category label.

Apple's color guidance recommends keeping color meanings consistent, especially for status and interactivity.

## Neutrals do most of the work

Professional product interfaces often rely heavily on neutrals.

Neutrals handle:

- backgrounds;
- surfaces;
- text hierarchy;
- separators;
- disabled states;
- structural chrome.

Accents then retain meaning.

Do not interpret `neutral` as `boring`. Personality can come from neutral temperature, typography, imagery, geometry, and selective brand color.

## Warm and cool neutrals

Gray is not one thing.

A neutral scale may lean:

- cool / blue;
- warm / beige;
- greenish;
- truly neutral.

Choose the temperature based on the product character.

Do not mix unrelated gray temperatures accidentally. A cool blue-gray border against warm beige surfaces can look dirty rather than intentionally contrasted.

## Pure black and pure white

`#000000` and `#FFFFFF` are valid colors.

Do not ban them automatically.

Use slightly softened values when they better fit the product or reduce harshness, but do not lower contrast merely to look sophisticated.

Accessibility beats aesthetic subtlety.

## Contrast

Contrast is not only hue difference.

For text and controls, luminance contrast matters heavily.

Follow current WCAG contrast requirements for applicable content and states.

Do not use faint gray text as a default minimalist style.

Do not rely on yellow-on-white, dark-blue-on-black, or other low-luminance-separation combinations for important text.

Test actual rendered combinations rather than assuming a color name guarantees contrast.

## Color is never the only state cue

Do not communicate important state using color alone.

Instead combine color with at least one additional cue when needed:

- icon;
- label;
- shape;
- pattern;
- text;
- position.

Example:

`red border only` is weaker than `red border + error icon + error message`.

This improves usability for people with color-vision differences and also makes states clearer for everyone.

## Status color rules

### Success

Use for confirmed successful states, not general decoration.

### Warning

Use for conditions requiring attention but not necessarily destructive action.

### Danger / error

Use for destructive actions, errors, or severe states.

Do not make the entire interface red just because one object has failed.

### Info

Use when a neutral informational state benefits from color distinction.

Semantic colors should not compete with the primary brand accent unless the state deserves that attention.

## Light mode

A light theme normally needs:

- enough distinction between page and surface;
- readable dark text;
- subtle but visible borders;
- accent colors that remain distinct on light backgrounds;
- status colors that preserve contrast.

Do not make every surface pure white if hierarchy requires visible depth or grouping.

## Dark mode

Dark mode is not simple inversion.

Vivid colors often appear more intense against dark backgrounds.

For dark themes:

- rebalance accent chroma;
- keep text hierarchy readable;
- avoid pure-white text everywhere if a softer high-contrast foreground works;
- make surfaces distinguishable without stacking heavy borders;
- retest semantic colors;
- retest imagery and charts;
- provide explicit dark variants when required.

Apple recommends ensuring colors work in light, dark, and increased-contrast contexts.

## Palette scale construction

When a product needs a tonal scale, build a controlled sequence rather than randomly lightening hex values.

Example conceptual scale:

- 50: near-background tint;
- 100-200: subtle surfaces/selection;
- 300-400: quiet borders or secondary emphasis;
- 500-600: core accent range;
- 700-800: pressed/dark emphasis;
- 900-950: deepest tonal values.

The exact values depend on the hue and color space.

Do not assume every step must have identical numeric lightness differences. Perceptual balance matters more than arithmetic neatness.

## Prefer perceptual color reasoning

When tools permit it, use a perceptual color space such as OKLCH for systematic palette construction because lightness and chroma controls are easier to reason about perceptually than raw RGB/HSL adjustments.

Still validate the resulting colors in actual sRGB/P3 rendering and for accessibility. A mathematically neat OKLCH ramp is not automatically a good UI palette.

## Color hierarchy

Establish an attention order.

Example:

1. critical state when present;
2. primary action / selected state;
3. important data emphasis;
4. secondary interactive accents;
5. neutral structural UI.

Do not let decorative color outrank functional color.

## Common bad combinations

No pair is universally forbidden, but these require care:

### Highly saturated red + highly saturated blue

Both can demand equal attention and create visual vibration.

Fix by changing dominance, chroma, value, or area.

### Neon green + neon pink

Can work in an intentionally loud identity but is usually too aggressive for large productive surfaces.

### Yellow text on white

Often lacks sufficient luminance contrast.

### Dark navy on black

Often lacks sufficient luminance contrast.

### Red vs green as the only distinction

Creates accessibility and interpretation problems.

### Many fully saturated accents

Destroys hierarchy because everything competes.

The correction is usually not `never use these hues`; it is `control value, chroma, area, semantics, and contrast`.

## Data visualization

Charts require more than a pretty palette.

Ensure:

- series are distinguishable;
- adjacent colors differ sufficiently;
- categories do not rely only on red/green distinction;
- text/labels remain readable;
- semantic colors are not reused misleadingly;
- dark mode remains legible;
- selected/hover states remain visible.

For ordered data, consider sequential scales. For values around a meaningful midpoint, consider diverging scales. For unrelated categories, use a categorical palette with controlled distinctness.

## Background and foreground interaction

The same color looks different depending on what surrounds it.

Always review colors inside the actual interface.

Do not approve palette swatches in isolation.

Test:

- real page background;
- cards/surfaces;
- text;
- selected states;
- borders;
- images;
- dark mode;
- disabled states.

## Palette workflow

1. Define product character.
2. Choose neutral temperature.
3. Choose one primary accent hue.
4. Set accent chroma appropriate to the product.
5. Build useful lightness/chroma variants.
6. Define semantic colors separately.
7. Map raw values to semantic tokens.
8. Test hierarchy in a representative screen.
9. Test text and control contrast.
10. Test color-blind resilience and non-color cues.
11. Test dark mode and increased contrast.
12. Reduce colors that do not have a specific role.
13. Validate on more than one display when possible.

## Anti-slop rules

- Do not default to purple-blue gradients for AI products.
- Do not use neon accents simply to make dark mode feel futuristic.
- Do not color every badge differently.
- Do not add green status dots without real state.
- Do not create rainbow dashboards without information need.
- Do not use brand color on every control.
- Do not use gradients to compensate for weak layout.
- Do not lower contrast merely to look premium.
- Do not create color tokens that differ by imperceptibly tiny amounts.
- Do not invent semantic colors with inconsistent meanings across screens.

## Review checklist

- Does every non-neutral color have a role?
- Is one accent clearly dominant?
- Can the interface still be understood without color?
- Are critical text and controls readable?
- Are status colors used consistently?
- Are large surfaces less visually aggressive than small accents unless intentionally immersive?
- Does the palette work in light and dark themes?
- Does the palette support the product personality?
- Would removing any accent improve hierarchy?
- Are colors being judged in real context rather than as isolated swatches?

## Companion skills

Use with:

- `color-weight-and-dominance.md`;
- `visual-art-direction.md`;
- `visual-hierarchy.md`;
- `design-tokens-and-theming.md`;
- `accessibility-and-interaction.md`;
- `anti-ai-slop.md`.

## Source foundations

- Apple Human Interface Guidelines — Color and Branding
  - https://developer.apple.com/design/human-interface-guidelines/color
  - https://developer.apple.com/design/human-interface-guidelines/branding
- Material Design 3 — Color
  - https://m3.material.io/styles/color/overview
- IBM Carbon Design System — Color
  - https://www.carbondesignsystem.com/elements/color/overview/
- W3C WCAG 2.2 Understanding documents
  - https://www.w3.org/WAI/WCAG22/understanding/
