# Visual Hierarchy

Use this skill to decide what users should notice first, second, third, and later across an interface.

Visual hierarchy is created through relative differences in size, position, spacing, typography, contrast, color, alignment, density, isolation, imagery, and motion.

## Core objective

Make importance visible without making everything loud.

A strong interface has intentional levels of emphasis. A weak interface either gives everything equal weight or exaggerates every difference.

## Establish priority before styling

For each screen, identify:

1. primary purpose;
2. primary object or message;
3. primary action;
4. supporting information;
5. secondary actions;
6. metadata and tertiary detail.

Do not style first and decide importance afterward.

## Primary, secondary, tertiary

Every screen should have distinguishable emphasis levels.

### Primary

The content required to understand or complete the main task.

### Secondary

Supporting context and common alternate actions.

### Tertiary

Metadata, rare actions, explanatory detail, and peripheral information.

Avoid making tertiary content visually stronger than the task itself.

## Hierarchy tools

### Size

Larger elements usually attract attention sooner.

Use size differences deliberately and sparingly.

### Position

Top/leading areas often receive earlier attention according to reading direction, but strong contrast or imagery can override this.

### Spacing

More isolation can increase prominence. Tight proximity communicates grouping.

### Typography

Use semantic type roles, moderate weight changes, line-height, and color.

### Contrast

High luminance or color contrast increases salience.

### Color

Reserve saturated/accent colors for priority, state, or brand meaning.

### Alignment

Shared anchors make groups and hierarchy easier to scan.

### Containment

Cards, panels, and surfaces can create hierarchy, but are stronger cues than whitespace and should not be overused.

### Motion

Motion attracts attention strongly; use it only for meaningful state change or feedback.

## Reading order

Apple’s layout guidance recommends placing important information early in the natural reading direction and using alignment and grouping to clarify structure.

For left-to-right interfaces, leading/top regions often have stronger initial visibility.

For right-to-left interfaces, mirror directional assumptions.

Do not treat reading order as a rigid eye path.

## Reduce competition first

When hierarchy feels weak, do not immediately enlarge the primary element.

First reduce:

- unnecessary saturated colors;
- excessive bold text;
- decorative badges;
- heavy borders;
- extra shadows;
- competing filled buttons;
- oversized secondary headings;
- unnecessary images.

Hierarchy often improves more by quieting secondary elements than by amplifying primary ones.

## Typography hierarchy

Use a small set of roles.

Example:

- page title;
- section heading;
- item heading;
- body;
- label;
- caption/metadata.

Repeated roles should look repeated.

Avoid unique typography for every section.

Do not use Black or ExtraBold as a default hierarchy tool.

## Spatial hierarchy

Spacing should mirror conceptual depth.

Example:

heading ↔ description: small gap

description ↔ local actions: medium gap

section ↔ next section: large gap

If every gap is identical, grouping becomes ambiguous.

## Hierarchy without cards

Before adding a card, attempt:

1. spacing;
2. alignment;
3. typography;
4. subtle surface contrast;
5. divider if necessary;
6. full container only if the content behaves as a distinct object or surface.

Avoid “card soup.”

## Button hierarchy

Most action groups should not contain several equally dominant buttons.

Common pattern:

- primary: one strongest treatment;
- secondary: neutral or outlined/subtle treatment;
- tertiary: text/icon treatment;
- destructive: semantic danger treatment when required.

Primary action styling should reflect task priority, not brand enthusiasm.

## Navigation hierarchy

Differentiate:

- global navigation;
- local navigation;
- selected state;
- contextual actions;
- utilities/account/help.

A selected navigation item should be obvious without making every unselected item visually noisy.

## Data hierarchy

In dashboards:

- emphasize metrics tied to current decisions;
- group related metrics;
- keep comparison context available;
- avoid equal-size metric cards when priorities differ;
- do not assign bright colors to every data point.

In tables:

- make the identifying column easy to scan;
- de-emphasize supporting metadata;
- keep statuses clear;
- preserve consistent row anatomy.

## Hero hierarchy

Marketing hero sections may support larger scale, but hierarchy still requires restraint.

A useful structure:

brand/navigation → headline → supporting copy → primary action → supporting visual

The visual should not overpower the message unless the visual itself is the product demonstration.

Keep hero buttons proportionate to their labels; do not stretch them unnecessarily across large widths.

## Density and context

Hierarchy depends on interface type.

Productivity software:

- tighter spacing;
- smaller type scale;
- compact controls;
- strong alignment.

Marketing/editorial:

- more negative space;
- more expressive type scale;
- stronger imagery.

Do not apply marketing hierarchy to an admin panel.

## Accessibility

- Hierarchy must not depend on color alone.
- Semantic heading order should match visual structure.
- Secondary text must remain readable.
- Focus indicators must remain visible regardless of hierarchy.
- Larger text/zoom should not destroy order or overlap content.
- Meaningful sequence should remain correct in the DOM/accessibility tree.

## Diagnose bad hierarchy

Ask:

- What do I notice first?
- Is it actually the most important thing?
- How many elements look primary?
- Are headings distinguishable?
- Are action priorities obvious?
- Are related items visually grouped?
- Does spacing communicate levels?
- Are borders/cards doing work spacing should do?
- Is color being overused?
- Are secondary elements readable but quiet?

## Common AI-generated failures

### Giant-title syndrome

Fix: reduce headline scale and strengthen surrounding hierarchy.

### Fat-button syndrome

Fix: use compact component geometry; let contrast and placement signal priority.

### Rounded-card-everything

Fix: remove containers and use spacing/alignment.

### Bold-everything

Fix: use Regular/Medium/Semibold and create hierarchy with multiple cues.

### Decorative hierarchy

Fix: remove gradients, glows, shadows, and shapes that do not communicate role or state.

## Evaluation checklist

- Can the intended priority order be stated in one sentence?
- Does a five-second glance reveal that order?
- Are there no more primary-looking elements than the task requires?
- Can secondary emphasis be reduced without losing usability?
- Does hierarchy survive dark mode, zoom, mobile, and localization?
- Does semantic HTML/accessibility structure reflect the same order?
- Can unnecessary cards, borders, shadows, or saturated colors be removed?

## Source foundations

This skill synthesizes Apple layout/branding guidance, Carbon grid and spacing guidance, Fluent typography/layout guidance, Nielsen Norman Group visual-design and Gestalt research, and WCAG requirements around semantic structure, contrast, focus, and meaningful sequence.

References:

- https://developer.apple.com/design/human-interface-guidelines/layout
- https://developer.apple.com/design/human-interface-guidelines/branding
- https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/guidelines
- https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview
- https://fluent2.microsoft.design/layout
- https://fluent2.microsoft.design/typography
- https://www.nngroup.com/articles/good-visual-design/
- https://www.nngroup.com/articles/gestalt-proximity/
- https://www.w3.org/WAI/WCAG22/Understanding/
