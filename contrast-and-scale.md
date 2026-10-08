# Contrast and Scale

Use this skill to control visual importance through differences in size, weight, color, spacing, density, and position.

Contrast is not simply black versus white. It is the perceptual difference between elements. Scale is one of the strongest contrast tools because larger elements usually attract attention sooner and imply greater importance.

## Core objective

Create enough difference that hierarchy is immediately understandable without making the interface loud, oversized, or inaccessible.

## Types of contrast

Use contrast across several dimensions:

- size;
- typographic weight;
- color and luminance;
- position;
- spacing and isolation;
- shape;
- density;
- surface/background;
- stroke or border strength;
- motion when necessary.

Do not rely on one dimension for every hierarchy decision.

## Scale should represent importance

Larger elements generally attract more attention.

Use larger scale for:

- page titles;
- key values;
- major product messages;
- primary objects;
- hero content;
- high-level section anchors.

Use smaller scale for:

- metadata;
- helper text;
- timestamps;
- tertiary labels;
- low-priority controls.

Do not make text large merely because the page has unused space.

## Avoid exaggerated scale

AI-generated interfaces often overuse huge typography, enormous buttons, and oversized cards.

For product interfaces, hierarchy can often be achieved with modest differences:

14 → 16 → 20 → 28

rather than:

14 → 28 → 48 → 80

The exact scale depends on the typeface and context, but the principle is restraint.

Marketing/editorial interfaces can support more expressive scale than dense productivity software.

## Relative scale matters more than isolated numbers

A 24px heading can feel large in a compact admin panel and small in a marketing hero.

Evaluate scale relative to:

- surrounding text;
- available viewport;
- component density;
- reading distance;
- platform conventions;
- typeface x-height;
- line length;
- user task.

## Typographic contrast

Build hierarchy using a combination of:

- font size;
- weight;
- line height;
- color;
- spacing;
- position.

Do not jump to Bold or Black when hierarchy feels weak.

First try:

1. increase size slightly;
2. improve contrast;
3. add surrounding space;
4. reposition the element;
5. reduce the emphasis of competing elements.

Prefer Regular, Medium, and Semibold for most product UI.

## Large text needs less weight

A large heading already has visual mass.

Heavy weight + large size + high contrast can become visually aggressive.

Use moderate weight and let scale provide the emphasis.

## Color contrast versus visual prominence

Accessibility contrast and hierarchy contrast are related but not identical.

Text and interactive elements must maintain sufficient contrast for readability and operability.

WCAG 2.2 commonly requires at least 4.5:1 for normal text and 3:1 for qualifying large text; non-text interactive boundaries and important graphical objects also have contrast requirements.

Do not make secondary text so faint that it becomes inaccessible.

Hierarchy should not be created by making useful information unreadable.

## Contrast is contextual

A medium-gray label may feel subtle on white but strong on a darker neutral surface.

Always evaluate color against its actual background.

Do not assume a token that works on one surface works on another.

## Isolation as contrast

Whitespace creates contrast by isolating an element.

A small title with generous space can command more attention than a large title trapped inside dense UI.

Use isolation when increasing size would distort the interface.

## Shape contrast

Reserve unusual shapes for meaningful roles.

If every button is pill-shaped, pill shape no longer communicates anything.

If every card has a different radius, shape contrast becomes noise.

Use consistent component families and introduce shape contrast only where it supports role or state.

## Density contrast

Dense and sparse regions create hierarchy.

A page can contain a compact data table and a more spacious summary region.

Do not make the entire product equally dense or equally spacious.

Let density reflect task intensity and information importance.

## Primary actions

A primary action can use stronger contrast, but avoid making every action a filled brand-color button.

Typical hierarchy:

- primary: strongest action treatment;
- secondary: lower-emphasis button or neutral treatment;
- tertiary: text/icon treatment;
- destructive: distinct semantic treatment when necessary.

Do not rely solely on red/green color differences to communicate meaning.

## Scale in components

Component size should correspond to context and input requirements.

Compact desktop productivity UI can use visually small controls while maintaining an adequate interactive hit area.

Touch interfaces need larger target regions than mouse-first desktop interfaces.

WCAG 2.2 defines a 24 by 24 CSS pixel minimum target-size criterion with exceptions; platform design systems may recommend larger touch targets.

Do not solve touch accessibility by making the visible label or icon enormous. Increase the hit target or container appropriately.

## Data visualization

Contrast should encode importance or difference, not decoration.

Use scale carefully for quantitative comparisons; area-based scaling can distort perception.

Use stronger color or stroke for selected/high-priority series and quieter treatments for context.

Do not use dozens of equally saturated colors.

## Responsive scale

Do not scale every element proportionally with viewport width.

Responsive hierarchy should preserve roles, not ratios.

A 64px desktop hero might become 40px on mobile, while 14px body text remains near the same readable size.

Controls may change arrangement rather than simply shrink.

## Accessibility

- Maintain WCAG text and non-text contrast.
- Do not convey state only through color, size, or position.
- Preserve readable text when zoomed or resized.
- Ensure large display text still reflows without clipping.
- Keep focus indicators visually distinct.
- Test light, dark, high-contrast, and custom theme surfaces.

## Failure modes

### Everything is large

Result: nothing feels important.

Fix: reduce secondary scale and restore a clear hierarchy.

### Everything is bold

Result: noisy, tiring UI with little differentiation.

Fix: use fewer weights and combine size, spacing, and contrast.

### Secondary means unreadable

Result: low contrast breaks accessibility.

Fix: lower emphasis without dropping below usable contrast.

### Giant controls

Result: low information density and amateur visual balance.

Fix: separate visible component size from required interactive target size.

### Too many contrast dimensions at once

Result: huge + bold + saturated + shadowed + isolated elements shout unnecessarily.

Fix: use the minimum number of cues required.

## Evaluation checklist

- Is the most important element noticeably stronger than its neighbors?
- Are secondary elements still readable?
- Are size differences proportional to actual importance?
- Could hierarchy improve by reducing competitors instead of enlarging the primary?
- Are touch targets adequate without bloating visible controls?
- Does the contrast survive light/dark/high-contrast themes?
- Does the scale remain usable on narrow screens and large text settings?
- Is color used as one cue rather than the only cue?

## Source foundations

This skill synthesizes Apple layout and branding guidance, Fluent typography/accessibility guidance, Carbon grid guidance on contrast and hierarchy, Polaris color accessibility guidance, and WCAG 2.2 contrast and target-size criteria.

References:

- https://developer.apple.com/design/human-interface-guidelines/layout
- https://developer.apple.com/design/human-interface-guidelines/branding
- https://fluent2.microsoft.design/typography
- https://fluent2.microsoft.design/accessibility
- https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/guidelines
- https://polaris.shopify.com/design/colors
- https://www.w3.org/WAI/WCAG22/Understanding/
