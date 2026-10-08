# Visual Art Direction

Use this skill when an interface is usable but still feels generic, sterile, template-driven, or visually forgettable.

This skill controls the product's visual personality. It does not replace usability, hierarchy, accessibility, or component rules. It gives those systems a recognizable visual voice.

## Core objective

Make the product feel intentionally art-directed without making familiar interactions harder to understand.

A strong interface should still feel recognizable when the logo is hidden. Recognition should come from a coherent combination of typography, composition, density, shape, color, imagery, motion, copy tone, and detail — not from decorative gimmicks.

## Start with character, not components

Before styling screens, define 3-4 product character words.

Good examples:

- precise;
- quiet;
- technical;
- editorial;
- warm;
- industrial;
- playful;
- premium;
- utilitarian;
- expressive.

Avoid vague words like `modern`, `clean`, `beautiful`, or `sleek` unless they are made more specific.

Translate the character words into visual consequences.

Example:

`precise + compact + technical + quiet`

should tend toward:

- restrained radii;
- compact controls;
- strong alignment;
- neutral surfaces;
- limited accent color;
- dense but readable information;
- minimal decorative motion;
- exact, concrete copy;
- consistent icon geometry.

Do not choose a style first and invent brand words afterward.

## The personality matrix

Define the product on these axes before designing:

### Density

- sparse;
- balanced;
- compact.

### Geometry

- sharp;
- restrained rounding;
- soft;
- pill-heavy only when justified.

### Typography

- neutral;
- technical;
- humanist;
- editorial;
- expressive.

### Color

- monochrome-led;
- muted;
- vivid-accented;
- expressive;
- content-led.

### Motion

- nearly static;
- restrained;
- responsive;
- expressive.

### Imagery

- none/minimal;
- product UI;
- photography;
- illustration;
- 3D;
- diagrams/data.

Do not maximize every axis. Strong art direction usually comes from one or two expressive dimensions surrounded by restraint.

## Signature decisions

Choose 1-3 recognizable decisions that can repeat across the product.

Examples:

- a distinctive headline type treatment;
- a specific accent color behavior;
- a recognizable icon style;
- a characteristic compactness or spaciousness;
- a unique illustration language;
- a distinctive content framing pattern;
- one memorable motion behavior;
- a consistent asymmetrical composition strategy.

Do not make every component unique. Familiar components should remain familiar.

## Composition rules

### Use hierarchy before decoration

Solve the composition with:

1. content order;
2. scale;
3. spacing;
4. alignment;
5. typography;
6. color;
7. imagery;
8. decoration last.

Do not use gradients, floating fragments, glows, or extra cards to rescue a weak composition.

### Create tension deliberately

Useful contrast can come from:

- large type against small metadata;
- dense navigation against a spacious canvas;
- neutral UI against one vivid product object;
- sharp typography against soft photography;
- asymmetrical hero composition against a strict underlying grid.

Tension must strengthen the focal point or brand. Random offsets are not art direction.

### Do not center everything

Centered layouts are appropriate for focused statements, onboarding moments, empty states, and certain marketing compositions.

Do not repeat centered heading + centered paragraph + centered buttons for every section.

Use left alignment, split layouts, editorial columns, offset media, or strong grid placement where they create a better reading path.

### Build around key lines

Major titles, body copy, controls, cards, tables, and media should share intentional alignment anchors.

A professional interface often feels polished because invisible lines repeat across the entire page.

## Typography as personality

Typography is one of the strongest brand signals.

Do not choose a font only because it is popular.

Choose based on:

- readability;
- product character;
- language coverage;
- available weights/styles;
- platform rendering;
- licensing;
- numeric behavior for data-heavy products.

Use a limited role system such as:

- display;
- page title;
- section heading;
- body;
- label;
- caption/metadata.

Do not create a new font size for every component.

Do not make every heading heavy. Contrast can come from size, measure, spacing, position, color, or case before weight.

For productive software, prefer tighter, task-focused typography. For editorial or marketing moments, larger expressive type can be appropriate. Carbon makes a similar distinction between productive and expressive type sets.

## Geometry and shape language

Set a small radius family instead of improvising.

Example restrained system:

- 4px: tiny controls/details;
- 6-8px: buttons and inputs;
- 10-12px: cards/panels;
- 999px: true pills only.

Do not use pills for ordinary rectangular actions just because pills look friendly.

Do not use the same large radius on every surface.

Shape should communicate product character and component function.

## Surface language

Use the least visually heavy separation method that works:

1. whitespace;
2. alignment;
3. background shift;
4. divider;
5. border;
6. contained surface;
7. elevation/shadow.

Do not jump directly to cards and shadows.

Shadows should communicate layering or elevation, not compensate for weak grouping.

## Color as identity

Use color intentionally, not continuously.

A brand accent becomes weaker when it appears on every control, icon, heading, badge, and surface.

Prefer:

- neutral structural UI;
- brand color at meaningful emphasis points;
- semantic colors for state;
- content imagery carrying more expressive color when appropriate.

Apple's branding guidance specifically recommends using accent color judiciously and preserving familiar components even in branded interfaces.

## Iconography

Use one coherent family or create a clearly specified custom family.

Control:

- stroke weight;
- corner treatment;
- optical size;
- fill behavior;
- metaphor style;
- default sizes.

Do not mix unrelated outline, filled, cartoon, and 3D icon languages in the same product without a deliberate system.

Icons should support meaning, not decorate every label.

## Imagery and asset direction

When imagery is important, define an art direction before generating individual assets.

Specify:

- subject matter;
- perspective;
- lighting;
- material treatment;
- saturation;
- background behavior;
- crop rules;
- edge treatment;
- texture/noise policy;
- animation behavior if relevant.

One coherent visual family is stronger than a collection of individually impressive but unrelated assets.

## Motion personality

Motion should match brand character and task.

Technical/productive software:

- quick;
- restrained;
- low travel distance;
- minimal bounce;
- clear state transitions.

Playful consumer software may use more expressive timing or spring behavior.

Do not add motion to every hover. Do not animate merely to prove that the interface is interactive.

## Copy tone is visual identity

Interface language affects personality as strongly as styling.

Choose a voice:

- direct;
- technical;
- conversational;
- formal;
- playful;
- editorial.

Then keep it consistent.

Prefer concrete wording over startup filler.

`Retry failed webhook` is stronger than `Unlock effortless reliability`.

## Product UI vs marketing UI

Do not apply the same density and expressive rules everywhere.

Product UI should prioritize task focus, state, information density, speed, and predictability.

Marketing UI can tolerate more expressive typography, composition, imagery, and pacing.

The two surfaces should still share recognizable brand DNA.

## Anti-template requirements

Reject a design if its identity depends mainly on:

- generic gradient blobs;
- pulsing green dots;
- hero pills;
- oversized rounded cards;
- random glassmorphism;
- fake floating dashboards;
- generic 3-column feature cards;
- stock icon grids;
- decorative command-line windows;
- fake metrics or testimonials.

These patterns are not automatically forbidden, but they require a product-specific reason. See `anti-ai-slop.md`.

## Art-direction workflow

1. Define the product's audience, context, and primary task.
2. Choose 3-4 precise character words.
3. Set density, geometry, typography, color, motion, and imagery direction.
4. Choose 1-3 signature decisions.
5. Establish a grid and spacing rhythm.
6. Establish type roles and text measures.
7. Establish surface and radius rules.
8. Establish color roles.
9. Establish icon and imagery rules.
10. Design one representative screen.
11. Remove anything that exists only to make it look designed.
12. Test whether the visual language survives across a second very different screen.
13. Hide the logo and test whether the product still feels recognizable.

## Failure modes

Reject or revise when:

- personality comes entirely from decoration;
- every screen uses the same centered template;
- every surface is a card;
- typography has no role system;
- accent color is everywhere;
- components use random radii;
- motion intensity changes without reason;
- imagery styles conflict;
- product UI is as spacious as a landing page;
- brand expression breaks familiar interaction behavior;
- the interface looks impressive in one screenshot but cannot form a scalable system.

## Review checklist

A strong result should answer yes to most of these:

- Can the product be described with 3-4 precise visual character words?
- Do the typography, spacing, shape, color, and motion choices support those words?
- Are there only a few signature ideas?
- Is the layout strong without decorative effects?
- Is color restrained enough to preserve hierarchy?
- Are components familiar and usable?
- Does the product still have character with the logo hidden?
- Can the style scale to dense, empty, error, settings, and mobile states?
- Does the interface feel designed for this product rather than copied from a current trend?

## Companion skills

Use with:

- `anti-ai-slop.md`;
- `visual-hierarchy.md`;
- `typographic-hierarchy.md`;
- `spatial-hierarchy-prospacing.md`;
- `alignment-and-grid-structures.md`;
- `color-theory-and-palette.md`;
- `component-craft.md`;
- `motion-and-feedback.md`.

## Source foundations

- Apple Human Interface Guidelines — Design Principles, Branding, Layout, Color
  - https://developer.apple.com/design/human-interface-guidelines/design-principles
  - https://developer.apple.com/design/human-interface-guidelines/branding
  - https://developer.apple.com/design/human-interface-guidelines/layout
  - https://developer.apple.com/design/human-interface-guidelines/color
- IBM Carbon Design System — Typography, Spacing, 2x Grid
  - https://www.carbondesignsystem.com/building-blocks/foundations/typography/overview/
  - https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview/
  - https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/guidelines/
- Atlassian Design System — foundations and components
  - https://atlassian.design/get-started/about-atlassian-design-system
