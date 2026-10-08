# Color Weight and Dominance

Use this skill to control how color attracts attention, communicates state, creates hierarchy, and supports brand identity without overwhelming the interface.

Color has visual weight. Saturated, bright, warm, high-contrast, or unusual colors can dominate a composition even when used on a small element.

## Core objective

Use color intentionally enough that users can infer priority and meaning without color becoming the only communication channel.

## Start with semantic roles

Do not design the interface around a pile of raw hex values.

Define roles such as:

- canvas background;
- raised or secondary surface;
- primary text;
- secondary text;
- tertiary text;
- border/divider;
- brand/accent;
- selected state;
- focus state;
- success;
- warning;
- danger;
- information.

Then map actual colors to those roles.

Fluent’s design-token model separates raw/global colors from semantic aliases. This makes light mode, dark mode, high-contrast themes, and brand swaps easier to maintain.

## Brand color is scarce attention

Treat strong brand color as a limited resource.

Good uses include:

- primary action;
- selected navigation state;
- active control;
- important status indicator;
- key data emphasis;
- small identity accents.

Avoid painting every icon, heading, button, border, and card with the brand color.

Apple’s branding guidance recommends using accent color judiciously because overuse weakens its impact.

## Dominance hierarchy

A useful hierarchy often looks like:

1. one dominant accent or focal area;
2. neutral primary content;
3. quieter secondary information;
4. semantic status colors used only when state requires them.

If five saturated colors compete simultaneously, none functions as a clear signal.

## Saturation and area

Visual dominance depends on both intensity and surface area.

A tiny saturated badge can be prominent.

A large saturated background can dominate the entire experience.

When increasing colored area, consider reducing saturation or contrast.

When using a highly saturated color, consider limiting its area.

## Color and hierarchy

Color can emphasize or de-emphasize text and controls, but do not use low contrast as a shortcut for hierarchy.

Secondary information can be quieter while remaining readable.

Tertiary information can be lower emphasis but must still satisfy accessibility needs when it conveys meaningful content.

## Semantic color

Use status colors consistently.

Do not use red decoratively if red also means destructive/error elsewhere.

Do not use green as a generic accent if users need green to mean success.

Do not map the same color to conflicting meanings in different parts of the product.

## Never use color alone

Pair color with another cue:

- icon;
- label;
- shape;
- text;
- pattern;
- position;
- state indicator.

For example, an error field should not be communicated solely by a red border. Include error text and, where appropriate, an icon.

Shopify Polaris explicitly reinforces this principle for merchant interfaces.

## Surface systems

Use a restrained set of surfaces.

Example:

- page/canvas;
- secondary panel;
- nested subtle surface;
- overlay or floating surface.

Avoid creating a different gray tint for every card and component.

The number of visual surface levels should reflect actual structural levels.

## Borders and dividers

Borders should be strong enough to communicate separation but not so dark that the page becomes a spreadsheet of boxes.

Use borders for:

- interactive boundaries when necessary;
- data tables where row/column separation helps comprehension;
- form controls;
- selected states;
- surfaces requiring clear containment.

Use whitespace instead of borders when spatial grouping already communicates the relationship.

## Dark mode

Dark mode is not color inversion.

Review:

- text hierarchy;
- surface separation;
- icon contrast;
- borders;
- shadows/elevation;
- semantic colors;
- images;
- focus indicators;
- disabled states.

Bright saturated colors can appear more intense against dark backgrounds and may need adjustment.

## High-contrast modes

Do not assume custom fills or subtle borders survive forced/high-contrast themes.

Preserve state and structure using semantic system colors, outlines, text, icons, and programmatic state.

## Data visualization

Reserve highly saturated colors for data that deserves focus.

Use neutral context series where possible.

Ensure categorical palettes remain distinguishable without relying only on hue.

Use direct labels, patterns, line styles, markers, or annotations when required.

Do not assign colors randomly between screens; stable mappings help users learn meaning.

## Selected and active states

Selection should remain clear even when brand color is unavailable or overridden.

Combine color with:

- background change;
- indicator bar;
- checkmark;
- border;
- icon change;
- type emphasis.

## Destructive actions

Danger color communicates consequence, not general importance.

Do not make the main “Save” action red just because red is the brand color if the product also uses red for destructive actions.

Avoid large danger-filled buttons when a lower-emphasis treatment communicates the role more appropriately until confirmation is required.

## Accessibility contrast

WCAG 2.2 includes minimum contrast requirements for text and meaningful non-text UI.

Common AA thresholds include:

- 4.5:1 for normal text;
- 3:1 for qualifying large text;
- 3:1 for many meaningful graphical objects and interactive boundaries against adjacent colors.

Always test actual foreground/background pairs.

Do not assume a named palette token automatically works on every surface.

## Cultural and localization considerations

Color meanings vary between regions and cultures.

Never make critical meaning depend only on a culturally specific color association.

Localization may also change text length and therefore the visual balance of colored components.

## Failure modes

### Brand flooding

Everything uses the accent color.

Fix: return most UI to neutrals and reserve accent for priority/state.

### Rainbow dashboard

Every metric receives a different saturated hue.

Fix: group by meaning and emphasize only what needs differentiation.

### Gray-on-gray hierarchy

Secondary text becomes too faint.

Fix: maintain accessible contrast and use spacing/size/weight to reduce prominence.

### Status conflict

The same color means selected, success, and brand action.

Fix: establish semantic token roles and keep them stable.

### Dark-mode inversion

Light colors are simply reversed.

Fix: design dark surfaces and semantic roles intentionally.

## Evaluation checklist

- Is there a clear dominant color role?
- Is brand color reserved enough to remain meaningful?
- Are semantic colors consistent?
- Can state be understood without color?
- Do all meaningful text and UI boundaries meet contrast requirements?
- Does the palette work in dark and high-contrast modes?
- Are data colors stable and distinguishable?
- Can any colored containers be replaced by spacing or hierarchy?
- Does the palette support localization and cultural variation?

## Source foundations

This skill synthesizes Apple branding and color principles, Fluent design-token/accessibility guidance, Shopify Polaris color guidance, WCAG 2.2 contrast requirements, and Gestalt similarity research.

References:

- https://developer.apple.com/design/human-interface-guidelines/branding
- https://fluent2.microsoft.design/design-tokens
- https://fluent2.microsoft.design/accessibility
- https://polaris.shopify.com/design/colors
- https://www.nngroup.com/articles/gestalt-similarity/
- https://www.w3.org/WAI/WCAG22/Understanding/
