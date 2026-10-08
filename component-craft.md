# Component Craft — Production-Quality UI Components

Use this skill whenever designing buttons, inputs, cards, badges, menus, sidebars, tabs, tables, dialogs, tooltips, toggles, checkboxes, radio controls, icon buttons, toolbars, navigation, or repeated UI primitives.

The purpose of this skill is to prevent generic AI-generated components: oversized controls, excessive rounding, giant padding, random shadows, heavy text, unclear states, and inconsistent geometry.

## Core objective

Every component must feel intentionally engineered for its role, density, platform, and surrounding system.

Component quality comes from:

anatomy → geometry → typography → spacing → state → interaction → accessibility → optical correction → consistency.

## 1. Start with role and anatomy

Before styling a component, define what parts it actually contains.

Example button anatomy:

- container;
- label;
- optional leading icon;
- optional trailing icon;
- focus ring;
- interaction state layer.

Example input anatomy:

- label;
- field container;
- value/placeholder;
- optional leading/trailing affordance;
- help text;
- error text;
- focus state.

Do not add decorative layers without a functional purpose.

## 2. Design components as a family

Components should share a system for:

- height/density;
- border radius;
- typography;
- icon scale;
- color roles;
- focus treatment;
- spacing tokens;
- stroke width;
- state transitions.

Do not make each component look independently “cool.”

## 3. Density comes from context

Choose a density mode before assigning geometry.

### Compact product UI

Suitable for:

- desktop productivity;
- developer tools;
- tables;
- admin systems;
- editors;
- high-frequency workflows.

Use compact visible controls, restrained padding, and efficient row heights.

### Standard product UI

Suitable for:

- general SaaS;
- settings;
- collaboration tools;
- consumer productivity.

### Touch-first / spacious

Use larger interactive regions when finger input dominates.

Visible geometry can remain restrained while hit areas satisfy interaction requirements.

Do not use touch-first component sizes as the default for mouse-first desktop software.

## 4. Sizing system

Use a small number of component sizes.

Example conceptual tiers:

- small / compact;
- medium / default;
- large / touch-emphasis.

Keep height, icon scale, text role, and padding coordinated within each tier.

Do not allow every screen to invent a unique button height.

## 5. Border radius

Radius is a system property, not decoration.

Use a restrained radius scale.

Possible product pattern:

- tiny controls/badges: 3–4px;
- buttons/inputs: 4–8px;
- cards/panels/dialogs: 6–12px;
- pill/circular: only when role requires it.

The exact values depend on brand and platform.

Do not make every rectangle pill-shaped.

Do not use 16–24px radii on every small software component unless the design language explicitly calls for it.

Nested radii should remain visually coherent: inner radius generally should not exceed the containing radius in a way that looks accidental.

## 6. Shadows and elevation

Structure should come primarily from spacing, surface value, and containment.

Use shadow when it communicates elevation or temporary layering:

- menus;
- popovers;
- dialogs;
- floating panels;
- dragged objects.

Avoid shadows on every card or button.

Flat interfaces can remain clear through borders, neutral surfaces, and spacing.

## 7. Borders

Use borders to clarify a real boundary.

Good uses:

- input boundary;
- table separation;
- selected/active state;
- contained surface;
- focus state.

Avoid dark outlines around every component.

Border contrast should be quieter than primary content unless the boundary is itself important.

## Buttons

### Button hierarchy

Define roles such as:

- primary;
- secondary;
- tertiary/ghost;
- destructive;
- icon-only.

Usually only one action in a local group should appear primary.

Do not use multiple saturated filled buttons side by side unless they truly have equal priority.

### Button width

Buttons should normally hug their content with consistent padding.

Do not stretch a hero button to arbitrary wide dimensions merely to occupy space.

Full-width buttons make sense when:

- the layout is narrow/mobile;
- the flow has one dominant action;
- the container convention calls for it.

### Button padding

Keep icon-label gaps tight enough to read as one control.

Horizontal padding should be proportional to label size and component height.

Avoid tiny labels inside huge horizontal padding.

### Button typography

Use clear, compact text.

Medium or Semibold often works; avoid ExtraBold.

Prefer action-oriented labels.

### Button icons

Use icons only when they clarify or speed recognition.

Universal icon actions may be icon-only if accessible labels/tooltips exist.

Ambiguous actions should include visible text.

### Button states

Design:

- default;
- hover where applicable;
- pressed;
- focus-visible;
- disabled when appropriate;
- loading;
- destructive confirmation when necessary.

Do not indicate hover only by moving the button or dramatically changing layout.

## Inputs

### Input anatomy

Keep label, field, help/error message as one relationship.

The label should be closer to its own field than to the previous field.

### Input height

Match density and input modality.

Do not default to very tall fields on desktop.

Allow height to expand for multiline input and accessibility.

### Placeholder

Placeholder text is not a replacement for a persistent label when users need to remember the field purpose after typing.

Use placeholders for examples or hints, not essential instructions.

### Validation

Show error state with more than color:

- clear message;
- semantic state;
- icon where useful;
- focus/announcement behavior.

Preserve entered input after errors.

### Disabled versus read-only

Use disabled when the control cannot be interacted with.

Use read-only when the value remains readable/selectable but cannot be edited.

Do not make disabled content so faint it becomes illegible.

## Selects, comboboxes, and autocomplete

Choose the control from the task.

- small fixed set: select/radio may work;
- large searchable set: combobox/autocomplete;
- multiple independent choices: checkboxes;
- one choice among few visible options: radio group.

Do not use a dropdown when users benefit from seeing all 3–4 choices at once.

Do not create custom select behavior that breaks keyboard expectations.

## Checkboxes

Use for independent boolean choices or multi-selection.

Label the checkbox with the choice itself.

The entire label area should generally be clickable/tappable.

Design checked, unchecked, indeterminate, focus, hover, disabled states.

Do not use a checkbox for mutually exclusive choices.

## Radio buttons

Use for one choice among a small visible set.

Present options together as a semantic group.

Do not hide the rest of the choices behind separate screens when direct comparison matters.

## Toggles / switches

Use when a change can reasonably take effect immediately and represents an on/off state.

Avoid switches for actions that require a separate Save/Submit step unless the product convention makes state clear.

Pair the switch with a clear label; “On/Off” alone may not explain what is being controlled.

## Badges and status labels

Badges should be compact.

Use them for:

- status;
- category;
- count;
- small metadata.

Avoid oversized pills with excessive horizontal padding.

Do not use monospace for ordinary status/method badges unless the content is technically code-like and the design system explicitly benefits from it.

Status must not depend solely on badge color.

## Cards

A card should represent an independent object, destination, selectable unit, or meaningful surface.

Avoid cards around every section.

Card anatomy may include:

- title/identity;
- supporting information;
- status;
- media;
- actions.

Keep padding appropriate to density.

Do not use a big shadow and huge radius as the primary evidence that something is a card.

## Menus

Menus contain contextual or secondary actions.

Keep rows compact and scannable.

Use:

- clear labels;
- consistent icon column when icons are present;
- shortcut region when useful;
- separators only between meaningful groups;
- destructive actions separated appropriately.

Do not place the main task action in a menu merely to make the toolbar cleaner.

Keyboard navigation, escape behavior, and focus restoration are required considerations.

## Tooltips

Use tooltips for short supplementary clarification, especially ambiguous icon-only controls.

Do not put essential workflow information only in a tooltip.

Tooltips must not be hover-only in a way that excludes keyboard/touch users.

Do not make a tooltip a miniature documentation page.

## Tabs

Tabs represent peer sections inside one context.

Use a clearly selected state.

Keep labels short and specific.

Avoid too many tabs; use alternate IA when the row becomes crowded.

Do not use tabs for a sequential wizard unless the user can genuinely move between peer steps.

## Sidebars

Sidebars should prioritize navigation and context, not become dumping grounds.

Use:

- compact row height;
- stable icon/label alignment;
- clear selected state;
- meaningful section grouping;
- account/workspace switchers separated from core navigation when appropriate.

Avoid excessive row padding and giant icons.

Expandable groups should preserve hierarchy and keyboard access.

## Tables

Tables are for comparable structured data.

Design:

- strong identifying column;
- meaningful column headers;
- consistent alignment by data type;
- compact row density;
- selected/hover/focus states;
- sortable headers when applicable;
- filters separate from column identity;
- stable row action placement.

Right-align or align numerical values consistently when comparison benefits.

Do not center-align every cell.

Do not put every cell in an individual rounded container.

Use horizontal scrolling only when the data cannot be responsively reorganized without losing meaning.

## Dialogs and modals

Use dialogs for focused decisions or short tasks that interrupt the current context.

A dialog needs:

- clear title;
- concise supporting content;
- primary action;
- secondary/cancel action as needed;
- close behavior;
- keyboard focus management.

Avoid giant modal widths for small decisions.

Avoid tiny dialogs containing complex multistep applications.

Do not stack modals when a nested flow or page is clearer.

## Popovers and panels

Use popovers for transient contextual content.

Use panels/inspectors for richer content users may reference alongside the main view.

Keep placement anchored to the invoking object when possible.

Ensure content stays within viewport bounds.

## Navigation bars

Navigation height should match platform and product density.

Do not create an oversized 80–100px product navbar by default.

Marketing nav can be more spacious; desktop software should generally be compact.

Primary actions in nav should remain visually balanced with the rest of the bar.

## Icon buttons

The visible icon can be small while the interactive target is larger.

Maintain a consistent icon canvas/size family.

Optically center asymmetric glyphs.

Provide accessible name and tooltip when meaning is not universally obvious.

Do not draw icons with inconsistent stroke weights or visual mass.

## Loading states

Loading should preserve layout when possible.

Avoid random skeleton shapes that do not reflect actual content geometry.

Use progress indicators when progress is indeterminate or determinate as appropriate.

Do not block unrelated regions if only one component is loading.

## Empty states

An empty state should explain:

- what is empty;
- why that matters;
- what the user can do next.

Use generated illustration only when it improves comprehension or product character.

The CTA should not be visually subordinate to decorative art.

## Error states

Place errors near the affected component.

Use plain language.

Explain recovery.

Do not erase user input.

For page-level failures, distinguish retryable system errors from user-correctable validation errors.

## Component states are mandatory

Do not design only the “pretty default.”

For every interactive component consider:

- default;
- hover;
- focus-visible;
- pressed;
- selected;
- disabled;
- loading;
- error;
- success;
- empty;
- read-only;
- high-contrast mode;
- dark mode.

Only include states that apply, but never ignore them by default.

## Focus treatment

Keyboard focus must be clearly visible and not obscured.

Do not use the same treatment for hover and focus if keyboard users cannot tell where focus is.

Use semantic focus tokens or system focus behavior where appropriate.

## Touch targets

WCAG 2.2 includes a 24×24 CSS pixel minimum target-size success criterion with exceptions.

Fluent also references larger platform touch targets such as 44×44 for iOS/web touch contexts and 48×48 for Android.

The visible component does not always need to fill the entire hit target.

Maintain spacing between adjacent small targets.

## Color and contrast

Components must remain legible and operable across surfaces.

Normal text commonly needs 4.5:1 contrast; qualifying large text 3:1; meaningful component boundaries/icons commonly need 3:1 against adjacent colors under WCAG AA criteria.

Do not use color as the only cue for selection, error, or state.

## Design tokens

Use semantic tokens for:

- color;
- spacing;
- typography;
- radius;
- stroke;
- elevation;
- motion;
- size.

Avoid raw one-off values embedded in individual components.

Fluent’s global → alias token model is a strong reference: components should consume semantic meaning rather than raw hex/pixel values wherever possible.

## Optical correction

After geometric alignment, inspect visually.

Common corrections:

- chevron appears 1px low;
- icon with asymmetric shape needs a slight shift;
- icon appears smaller than text even at matching numeric size;
- text baseline looks off inside a compact button;
- circular badge feels visually higher/lower than adjacent text.

Make corrections at the component level and reuse them.

## Responsiveness

Components should adapt rather than merely shrink.

Examples:

- button group → stacked full-width actions on narrow mobile;
- sidebar → drawer/nested navigation;
- inspector → separate screen;
- table → horizontal scroll or alternate key-value layout depending on data;
- toolbar → overflow for low-priority commands.

Preserve role hierarchy during transformation.

## Localization and RTL

Use logical leading/trailing placement.

Allow label expansion.

Mirror directional icons when meaning depends on direction.

Do not flip icons whose physical/object meaning should remain unchanged.

Test components with long translated labels.

## Anti-patterns for generated UI

Reject components that exhibit several of these at once:

- huge padding;
- unnecessary full-width buttons;
- excessive pill shapes;
- 16–24px radius everywhere;
- heavy drop shadows;
- bold labels everywhere;
- large icons inside tiny text systems;
- random gradients;
- cards around every group;
- enormous input heights;
- inconsistent row density;
- unstyled focus states;
- placeholder-only form labels;
- low-contrast secondary text;
- icon-only ambiguous actions;
- one-off spacing values.

## Component review procedure

For every component, perform this order:

1. Identify role.
2. List anatomy.
3. Choose density/size tier.
4. Apply semantic typography.
5. Apply spacing tokens.
6. Apply restrained radius/stroke.
7. Define states.
8. Check keyboard/touch behavior.
9. Check contrast.
10. Check responsive behavior.
11. Check localization/RTL.
12. Perform optical correction.
13. Compare against sibling components.
14. Remove unnecessary decoration.

## Final quality test

A professional component should feel inevitable: its size, spacing, labels, states, and interactions should look like parts of one coherent system rather than independent choices.

If a component looks impressive in isolation but awkward beside the rest of the interface, it is not finished.

## Source foundations

This skill synthesizes Apple guidance on familiar components, layout, labels, and platform behavior; Fluent 2 component/layout/accessibility/token systems; Carbon spacing/grid principles; Material component conventions; Shopify Polaris color/accessibility patterns; Nielsen Norman Group Gestalt research; and WCAG 2.2 interaction/contrast/focus/target-size requirements.

References:

- https://developer.apple.com/design/human-interface-guidelines/
- https://developer.apple.com/design/human-interface-guidelines/layout
- https://developer.apple.com/design/human-interface-guidelines/labels
- https://fluent2.microsoft.design/layout
- https://fluent2.microsoft.design/design-tokens
- https://fluent2.microsoft.design/accessibility
- https://m3.material.io/components
- https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview
- https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/guidelines
- https://polaris.shopify.com/design/colors
- https://www.nngroup.com/articles/gestalt-proximity/
- https://www.nngroup.com/articles/gestalt-similarity/
- https://www.w3.org/WAI/WCAG22/Understanding/
