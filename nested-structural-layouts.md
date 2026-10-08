# Nested Structural Layouts

Use this skill when an interface contains layers of structure such as app shell → workspace → page → region → panel → section → component → control.

Nested layout quality depends on preserving hierarchy across those layers without turning every level into another border, card, inset, or rounded rectangle.

## Core objective

Make parent-child relationships obvious while keeping the interface visually calm.

Users should be able to understand what contains what, what is global versus local, and which actions apply to which scope.

## Think in structural levels

Before styling, map the interface into levels.

Example:

1. Product shell
2. Primary navigation
3. Workspace or project context
4. Page-level content
5. Major region
6. Local panel or section
7. Component
8. Control or data item

Do not give every level equal visual strength.

A deeper level should normally feel subordinate to its parent.

## Parent-child signals

Use combinations of:

- shared alignment;
- indentation;
- tighter internal spacing;
- wider external spacing;
- surface change;
- heading level;
- border only when needed;
- background only when needed;
- position within a grid;
- local navigation;
- persistent context labels.

Prefer subtle structural cues over repeated decoration.

## Containment rule

A visual container should correspond to a meaningful functional or semantic boundary.

Use containers when they communicate:

- an independent object;
- a selectable unit;
- a draggable region;
- a modal surface;
- a panel with its own state;
- an area with a distinct background/elevation role;
- content that must remain grouped while moving or resizing.

Do not create a card merely because a group exists.

## Avoid container recursion

A common AI failure is:

page → rounded card → rounded inner card → rounded row → rounded badge → rounded button

This produces visual noise and destroys hierarchy.

Instead, vary the structural language.

Example:

page background → unboxed section → subtle panel → plain rows → compact controls.

The deeper the nesting, the more important it becomes to reduce unnecessary borders and radii.

## Shared alignment

Use recurring key lines across nesting levels.

Headings, labels, fields, tables, and panels should often share vertical anchors even when they live in different containers.

Carbon’s grid guidance emphasizes recurring key lines because they help users follow content across dense interfaces.

Do not allow each card or panel to invent a slightly different left edge unless the offset communicates hierarchy.

## Indentation

Use indentation to indicate subordination, not as a general decoration.

Good uses:

- tree views;
- nested navigation;
- comment threads;
- file hierarchies;
- subordinate settings;
- outline structures.

Keep indentation increments consistent.

Do not use so much indentation that deep items lose usable width.

At narrow widths, consider alternate representations such as drill-down views instead of preserving desktop indentation indefinitely.

## Nested spacing

Internal spacing should decrease as structural depth increases.

A page-level section may use large separation.

A panel may use medium padding.

A row or button should use compact spacing.

Do not apply marketing-page spacing inside dense nested software interfaces.

A useful mental model:

- macro layout: large intervals;
- section layout: medium intervals;
- component layout: small intervals;
- micro alignment: tiny optical adjustments.

## Surface hierarchy

If multiple surfaces are necessary, establish a finite elevation/surface system.

For example:

- canvas;
- secondary panel;
- nested neutral surface;
- floating overlay.

Do not invent a new gray shade and shadow for every nested level.

Prefer semantic surface tokens rather than hard-coded colors.

Fluent’s token model separates raw/global values from semantic aliases so themes and high-contrast modes can adapt without rewriting each component.

## Navigation hierarchy

Nested layout and navigation hierarchy should agree.

Global navigation should not look like a local tab bar.

Local tabs should not compete visually with the product-level navigation.

Contextual actions should appear near the object or region they affect.

If an action changes the whole workspace, do not place it inside one tiny card where its scope appears local.

## Panels and inspectors

Use side panels when users benefit from referencing the main content while editing or inspecting properties.

Choose behavior deliberately:

- fixed panel: always consumes layout space;
- collapsible panel: optional persistent region;
- slide-in panel: temporarily reduces or shifts content;
- floating panel: overlays content and must be dismissible.

If a panel obscures information required to complete its own task, use reflow or resizing instead.

## Tables inside panels

When dense tables are nested:

- preserve readable column widths;
- avoid excessive container padding;
- maintain alignment with surrounding content where possible;
- provide horizontal overflow only when necessary;
- keep row actions scoped clearly;
- do not nest a table inside multiple decorative cards.

## Responsive behavior

Structural relationships must survive responsive transformation.

Desktop:

sidebar + content + inspector

may become:

content → full-screen navigation route → full-screen inspector route

on a narrow screen.

The mechanism may change, but the hierarchy and scope should remain understandable.

Do not merely shrink a three-column desktop layout until every column becomes unusable.

## RTL and localization

Use logical leading/trailing relationships rather than hard-coding left/right behavior.

Indentation, sidebars, disclosure indicators, and directional icons may need to mirror for right-to-left languages.

Allow text expansion without clipping structural labels.

## Accessibility

- DOM or semantic order should match the meaningful visual order.
- Focus movement must remain predictable across nested regions.
- Temporary overlays must not trap users incorrectly.
- Headings should reflect structural hierarchy.
- Landmark regions should be used where appropriate.
- Zoom and large text must not collapse parent-child relationships into overlapping content.
- Do not rely solely on surface color to communicate nesting.

## Common failure modes

### Card inside card inside card

Fix: remove containers until only meaningful boundaries remain.

### Every level has the same padding

Fix: create a spacing hierarchy from page to component to micro-layout.

### Scope confusion

Fix: move actions nearer to the region they affect and strengthen context labels.

### Broken responsive nesting

Fix: transform deep side-by-side structure into sequential navigation or stacked regions.

### Arbitrary indentation

Fix: use a consistent depth increment or switch patterns when depth becomes excessive.

### Misaligned nested surfaces

Fix: establish shared grid lines and align text, not just container edges.

## Evaluation checklist

- Can users tell which region contains which content?
- Are global, page, and local controls visually distinct?
- Are there unnecessary nested containers?
- Do important text lines share stable anchors?
- Does spacing become appropriately tighter at deeper levels?
- Does the layout remain understandable without borders or shadows?
- Does responsive behavior preserve scope and hierarchy?
- Does semantic order match visual order?
- Can the design support RTL and longer translated strings?

## Source foundations

This skill synthesizes Apple layout guidance, Carbon 2x Grid guidance on key lines and page scaffolding, Fluent layout and token guidance, and WCAG requirements around meaningful sequence, focus order, reflow, and relationships.

References:

- https://developer.apple.com/design/human-interface-guidelines/layout
- https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/guidelines
- https://fluent2.microsoft.design/layout
- https://fluent2.microsoft.design/design-tokens
- https://www.w3.org/WAI/WCAG22/Understanding/
