# Design Tokens and Theming

Use this skill to turn design decisions into a repeatable system instead of scattering raw values across components.

Design tokens are named design decisions for color, typography, spacing, sizing, radius, stroke, elevation, and motion.

## Core objective

Make the interface consistent, themeable, maintainable, and easier for both designers and developers to reason about.

## Token layers

A strong model separates raw values from semantic meaning.

### Global/raw tokens

Store primitive values such as:

- color ramps;
- spacing numbers;
- radius values;
- font sizes;
- font weights;
- stroke widths;
- durations.

Example conceptual names:

`blue-600`

`space-4`

`radius-2`

These values do not say how they should be used.

### Semantic/alias tokens

Describe purpose:

- `text-primary`;
- `text-secondary`;
- `surface-canvas`;
- `surface-panel`;
- `border-subtle`;
- `action-primary-bg`;
- `status-danger-fg`;
- `focus-ring`.

Fluent 2 uses a global → alias token model to separate raw values from semantic application.

## Component tokens

Create component-specific tokens only when the shared semantic layer is not expressive enough.

Example:

`button-primary-background-hover`

should ideally reference a semantic action token rather than a raw hex value.

Avoid building an enormous component-token layer before real reuse demands it.

## Color tokens

Create roles for:

- background/surface layers;
- text hierarchy;
- icon hierarchy;
- borders;
- brand/action;
- selection;
- focus;
- success;
- warning;
- danger;
- information.

Do not define colors solely as `gray-200` throughout component code when their semantic purpose differs.

## Spacing tokens

Use a limited spacing scale.

Name by scale or semantic role consistently.

Do not create one-off margins for individual screens unless the layout genuinely requires an exception.

Tokens should support both component-level and layout-level spacing.

## Typography tokens

A text token should encode a semantic style such as:

- body-small;
- body;
- label;
- caption;
- heading-small;
- heading;
- title;
- display.

A typography token may combine:

- family;
- size;
- line height;
- weight;
- letter spacing.

Do not require designers/developers to rebuild each role from separate magic values every time.

## Radius tokens

Use a small radius scale.

Example conceptual roles:

- none;
- small;
- medium;
- large;
- circular.

Do not allow individual components to invent 11px, 13px, 17px radii without reason.

Use circular/pill radius only when component role calls for it.

## Stroke tokens

Keep border/stroke widths consistent.

Use semantic color and stroke tokens together.

Avoid mixing 1px, 1.5px, 2px borders randomly across equivalent controls.

## Elevation tokens

If the product uses shadows/elevation, define a small number of levels.

Map them to meaning:

- raised surface;
- popover/menu;
- dialog;
- dragged/floating object.

Do not create a unique box shadow for each card.

Flat systems may use no shadow for most content surfaces.

## Motion tokens

Define reusable durations/easings for:

- micro state transition;
- panel transition;
- dialog transition;
- navigation transition.

Do not create arbitrary animation timing per component.

Respect reduced-motion preferences regardless of token values.

## Size tokens

Define recurring component size tiers where useful:

- compact;
- default;
- large.

Coordinate height, icon size, text role, and padding.

Avoid a different control height for every feature team.

## Theme architecture

A theme should remap semantic roles rather than rewrite components.

Themes may include:

- light;
- dark;
- high contrast;
- branded themes;
- product sub-brands.

Components should consume semantic tokens so theme changes propagate automatically.

## Dark theme

Do not reverse light colors mechanically.

Check:

- surface hierarchy;
- text contrast;
- border visibility;
- status colors;
- focus rings;
- images;
- elevation/shadows;
- disabled states.

Use theme-specific semantic mappings when necessary.

## High contrast

Do not assume subtle custom colors remain visible.

Use semantic/system values and robust outlines/states.

Test real forced-color/high-contrast environments when the platform supports them.

## Brand theming

Brand color should not overwrite semantic meaning.

A branded theme should preserve:

- danger semantics;
- success semantics;
- focus visibility;
- contrast;
- state differentiation.

Avoid making brand red indistinguishable from destructive red without another semantic distinction.

## Token naming

Names should describe stable meaning, not one current appearance.

Better:

`surface-selected`

Worse:

`light-blue-bg`

because the selected surface may not be light blue in dark or branded themes.

## Token governance

Before adding a token, ask:

- Is this value reused?
- Is the role semantically distinct?
- Can an existing token represent it?
- Will this need theme-specific mapping?
- Is the exception likely to recur?

Do not add tokens for every one-off layout measurement.

## Designer/developer parity

Figma variables/styles and code tokens should map closely.

Use the same semantic names where practical.

A designer should be able to communicate `surface-panel` and a developer should know the matching implementation token.

Fluent explicitly structures its design resources so Figma variables and code libraries map to the same design language.

## Accessibility

Tokens should make accessible choices easier by default.

Provide approved foreground/background pairs.

Focus tokens should remain visible across themes.

Do not create “secondary text” tokens that fail contrast requirements on supported surfaces.

## Migration and refactoring

When converting an inconsistent product into tokens:

1. inventory repeated raw values;
2. identify semantic roles;
3. merge nearly identical values where visual difference is meaningless;
4. define the global scale;
5. define semantic aliases;
6. migrate common components;
7. audit exceptions;
8. test themes and accessibility.

Do not preserve every historical inconsistency as a token.

## Failure modes

### Raw-value soup

Components contain hard-coded hex and pixel values.

Fix: introduce semantic tokens.

### Token soup

Hundreds of near-identical tokens exist without clear meaning.

Fix: consolidate around roles.

### Appearance-based names

Fix: name by semantic purpose rather than current color/size.

### Theme breaks semantics

Fix: remap aliases while preserving role meaning.

### Figma/code mismatch

Fix: align variable/token vocabulary and component states.

## Evaluation checklist

- Are components using semantic values instead of raw values?
- Can light/dark themes change without editing component code?
- Are token names stable if the appearance changes?
- Is the scale restrained?
- Do designers and developers share the vocabulary?
- Are accessible combinations the default?
- Are one-off exceptions kept outside the core token system unless they recur?

## Source foundations

References:

- https://fluent2.microsoft.design/design-tokens
- https://fluent2.microsoft.design/get-started/design
- https://www.carbondesignsystem.com/
- https://m3.material.io/
- https://www.w3.org/WAI/WCAG22/Understanding/
