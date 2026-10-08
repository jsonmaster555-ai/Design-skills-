# Responsive Adaptation

Use this skill whenever a design must work across different viewport sizes, window sizes, orientations, zoom levels, text sizes, input modes, and content lengths.

Responsive design is not “desktop but smaller.” It is the preservation of hierarchy, relationships, and task completion while the available space changes.

## Core objective

Adapt the structure without changing the product’s conceptual model.

A user should recognize the same product and the same task even when navigation, panel arrangement, or component presentation changes.

## Design from content pressure

Choose breakpoints when the content stops working.

Warning signs:

- headings wrap awkwardly;
- controls collide;
- table columns become unusable;
- navigation no longer fits;
- important context moves too far from its action;
- line length becomes excessive;
- touch targets become crowded.

Do not choose breakpoints only from a list of device names.

## Preserve hierarchy, not pixel ratios

Responsive design should preserve:

- primary/secondary priority;
- grouping;
- action relationships;
- information order;
- navigation meaning;
- component roles.

It does not need to preserve exact:

- widths;
- heights;
- column counts;
- spacing values;
- side-by-side composition.

## Structural transformations

Desktop patterns can transform deliberately.

Examples:

sidebar → drawer or nested route

inspector → full-screen detail view

three-column workspace → one primary column with drill-down

horizontal toolbar → primary actions + overflow

two-column form → single-column form

large comparison grid → horizontally scrollable or task-specific comparison view

Do not keep shrinking side panels until none has enough width to function.

## Responsive grids

Reduce or reorganize columns as available width decreases.

Keep margins and gutters appropriate to content density.

Carbon and Fluent both treat grid behavior as contextual rather than one universal layout.

Use fluid, fixed, or hybrid behavior according to the content.

## Typography

Do not scale all text proportionally.

Display sizes may reduce significantly on mobile.

Body text should remain readable.

Allow headings to wrap naturally.

Avoid fixed heights that assume one-line labels.

## Navigation

When primary navigation collapses:

- preserve destination names;
- preserve selected/current location;
- keep primary destinations easy to reach;
- do not bury the entire product behind an ambiguous icon if labels are important;
- maintain keyboard access on desktop responsive windows.

## Actions

Priority should survive responsive transformation.

If five desktop actions become a menu, keep the primary action visible when possible and move lower-priority actions to overflow.

Do not hide the only way to complete the main task.

## Tables

Choose a strategy based on the data.

Options:

- horizontal scroll with key columns retained;
- column priority/hiding;
- stacked key-value rows;
- drill-down detail view;
- alternate mobile summary.

Do not convert a comparison table into cards if that destroys the ability to compare values.

## Forms

Stack fields when side-by-side layout becomes cramped.

Keep related field groups together.

Do not separate a label, field, and error message during responsive reflow.

Primary action should stay near the end of the relevant form/task.

## Dialogs

A desktop dialog may become a full-screen sheet/view on small devices.

Ensure:

- title remains visible;
- actions remain reachable;
- content can scroll;
- focus remains managed;
- keyboard does not cover critical controls on mobile.

## Images and media

Preserve aspect ratio unless intentional cropping is part of the design.

Use object positioning to protect important subject matter.

Do not allow decorative media to consume the screen while pushing the actual task far below the fold.

## Spacing

Adjust spacing by hierarchy level.

Page margins may shrink.

Major section gaps may decrease.

Micro component gaps may remain stable.

Touch-target spacing may increase.

Do not multiply every spacing token by one global scale factor.

## Height responsiveness

Design for short windows, not just narrow ones.

Check:

- laptop screens;
- browser toolbars;
- split-screen/multitasking;
- on-screen keyboards;
- landscape mobile.

Avoid vertical layouts where fixed headers/footers consume most of the usable height.

## Zoom and text scaling

Responsive behavior must work when effective viewport width changes due to zoom or enlarged text.

A layout that works at 390px mobile width but breaks at 400% desktop zoom is not robust.

## Safe areas and platform UI

Respect platform safe areas and system UI.

Do not place important controls under:

- notches;
- browser/system bars;
- home indicators;
- floating OS regions;
- window controls.

Apple explicitly recommends using safe areas and platform layout guides.

## RTL and localization

Translations can create responsive pressure even without viewport changes.

Test:

- long German-like strings;
- compact labels;
- multi-line buttons where allowed;
- Arabic/Hebrew direction;
- date/time/currency expansion.

Use logical leading/trailing layout properties.

## Pointer versus touch

Responsive design may also respond to input capability.

Do not assume width alone tells you whether the user has a mouse or touch input.

Use platform/input media features where appropriate.

Maintain sufficiently large touch targets without making mouse-first UI unnecessarily oversized.

## Reflow accessibility

WCAG 2.2 includes reflow requirements for ordinary content.

Avoid two-dimensional scrolling except where the content fundamentally requires it.

Ensure content remains available and functional after reflow.

## Testing matrix

Test at:

- smallest supported width;
- largest width;
- intermediate widths where layout changes;
- short viewport heights;
- portrait/landscape;
- zoom;
- large text;
- RTL;
- long localization strings;
- empty states;
- maximum-content states;
- error states;
- loading states.

## Failure modes

### Desktop squeezed into mobile

Fix: transform structure rather than only reducing dimensions.

### Breakpoint by device stereotype

Fix: choose breakpoints from content failure.

### Action disappearance

Fix: preserve task-critical actions and move only lower priority items.

### Broken stacking

Fix: keep semantic groups intact when columns stack.

### Giant desktop margins on large screens

Fix: choose a content model: centered editorial, product/docs, or high-density full width.

### Mobile cards replacing useful tables

Fix: preserve comparison behavior and choose a data-appropriate representation.

## Evaluation checklist

- Does hierarchy survive every breakpoint?
- Do groups remain intact?
- Is the primary task always possible?
- Do headings and labels wrap safely?
- Does zoom trigger usable reflow?
- Do tables retain their meaning?
- Do dialogs and panels transform appropriately?
- Does the UI support RTL and long strings?
- Does the layout work in short windows and split-screen modes?

## Source foundations

References:

- https://developer.apple.com/design/human-interface-guidelines/layout
- https://fluent2.microsoft.design/layout
- https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/overview
- https://www.w3.org/WAI/WCAG22/Understanding/
