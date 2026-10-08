# Proximity and Whitespace Distribution

Use this skill to communicate relationships through distance, create focus through empty space, and control density without inflating components.

Whitespace is not leftover space. It is an active structural tool.

## Core principle

Distance communicates relationship.

Closer = more strongly related.

Farther apart = more separate.

Nielsen Norman Group notes that proximity can overpower competing cues such as color or shape. This makes spacing one of the strongest grouping tools in interface design.

## Design relationships before values

Before choosing 8px, 16px, or 24px, identify the relationship:

- icon ↔ label;
- heading ↔ description;
- label ↔ input;
- input ↔ helper text;
- row ↔ row;
- group ↔ group;
- section ↔ section;
- page ↔ viewport.

Then choose a spacing value appropriate to that relationship.

Do not ask “what gap looks nice?”

Ask “how related should these things feel?”

## Internal versus external space

Internal space belongs inside a component or semantic group.

External space separates that group from other groups.

Internal spacing should generally be tighter than external spacing.

Example:

heading → description: 8

description → actions: 16

section → next section: 48

The exact values may differ, but the ratios should communicate the hierarchy.

## Use a spacing scale

Prefer a limited set of reusable values.

A practical compact scale:

4, 8, 12, 16, 24, 32, 48, 64, 96

Fluent uses a mostly 4px spacing cadence with additional values for optical alignment.

Carbon’s scale uses multiples of two, four, and eight to cover detailed component relationships and larger layout separation.

Consistency is the goal; blindly forcing every relationship to the same spacer is not.

## Micro spacing

Micro spacing controls tiny relationships such as:

- icon to button label;
- status dot to text;
- checkbox to label;
- shortcut key to menu label;
- badge edge to badge text;
- field icon to input text.

These gaps should feel tight enough that the pieces read as one component.

Do not use page-level spacing values inside small controls.

## Component padding

Padding should be proportional to component role and density.

Avoid defaulting to:

- 20–32px horizontal padding on every small button;
- tall 48–56px desktop controls without reason;
- 24–32px padding inside every card;
- huge navbar row heights.

Compact productivity UI can use tight visible geometry while maintaining adequate hit targets.

## Section spacing

Major sections require stronger separation than internal groups.

Section spacing can create hierarchy without borders or background blocks.

Use larger whitespace to signal:

- a new topic;
- a new workflow stage;
- a major content region;
- a shift from summary to detail.

## White space and importance

Elements with more surrounding whitespace often receive greater attention.

Use this to emphasize:

- key headings;
- major values;
- primary actions;
- important warnings;
- central content objects.

Do not give extra empty space to low-priority decorative elements while compressing important content.

## Density modes

Choose density from context.

### High-density

Examples:

- code editors;
- admin panels;
- data tables;
- file managers;
- IDE-like products;
- professional tools.

Use compact components, stable row rhythm, smaller group gaps, and restrained container padding.

### Medium-density

Examples:

- general SaaS apps;
- settings;
- project management;
- consumer productivity.

Balance scanability with efficient workspace use.

### Low-density / expressive

Examples:

- marketing;
- onboarding;
- editorial introductions;
- simple single-task pages.

Use more whitespace around major content but do not inflate every control.

## Whitespace before dividers

Try spacing before adding:

- border;
- divider;
- colored background;
- card;
- shadow.

If spacing already communicates the group boundary, additional decoration may be unnecessary.

## Forms

Use proximity to attach labels and messages to fields.

A form field should read as:

label
field
helper/error

with relatively tight internal gaps.

Then use a larger gap before the next field.

For long forms, use larger section gaps and descriptive section headings.

## Lists

Repeated list rows should have consistent internal spacing.

Do not increase row height just to make a list feel “premium.”

Choose a row density appropriate to the scanning task.

Use more space only when each list item contains more information or requires a larger touch target.

## Tables

Dense tables need enough row/column separation to track data without wasting screen space.

Use alignment, row rhythm, subtle borders where useful, and whitespace around major table regions.

Avoid large card padding around a table that reduces usable data width.

## Responsive spacing

Do not mechanically halve every desktop value on mobile.

Preserve relational hierarchy.

A 64px section gap might become 40px, while an 8px label-to-field gap may remain 8px.

Component hit areas may need to become larger even while page margins become smaller.

## Optical spacing

Mathematical equality can look unequal.

Examples:

- triangular icons appear offset inside square boxes;
- uppercase labels may need different vertical centering;
- text with tall ascenders may look visually high;
- icon-label pairs may need a 1–2px correction.

Apply optical correction after the spacing system is established.

Do not use optical correction as an excuse for random values everywhere.

## Text spacing accessibility

WCAG 2.2 requires content to remain functional when users override text spacing, including increased line, paragraph, letter, and word spacing.

Do not build fixed-height containers that clip when text expands.

## Failure modes

### Equal-gap disease

Every relationship uses 16px.

Fix: create clear micro, component, group, and section levels.

### Giant-padding UI

Components are inflated to create an illusion of quality.

Fix: use page/section whitespace instead of fattening controls.

### Cramped hierarchy

Major sections are separated by the same gap as rows.

Fix: increase macro separation.

### Empty dead zones

Large gaps do not communicate hierarchy or focus.

Fix: redistribute space around meaningful content.

### Border dependence

Every group needs a line to be understood.

Fix: strengthen proximity and spacing first.

## Evaluation checklist

- Are related items closer than unrelated items?
- Is internal spacing tighter than external spacing?
- Are controls appropriately dense for the product?
- Is a limited spacing scale used consistently?
- Can borders/cards be removed while preserving grouping?
- Does whitespace emphasize the right content?
- Does responsive spacing preserve relationships?
- Does enlarged text remain unclipped?
- Are optical exceptions small and intentional?

## Source foundations

This skill synthesizes Nielsen Norman Group proximity research, Carbon spacing guidance, Fluent layout/spacing guidance, Apple layout guidance, and WCAG text-spacing/reflow requirements.

References:

- https://www.nngroup.com/articles/gestalt-proximity/
- https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview
- https://fluent2.microsoft.design/layout
- https://developer.apple.com/design/human-interface-guidelines/layout
- https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html
- https://www.w3.org/WAI/WCAG22/Understanding/
