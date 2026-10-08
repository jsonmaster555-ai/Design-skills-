# Functional Grouping

Use this skill to organize controls, content, actions, and data by what they do and what they affect.

Functional grouping answers a simple question: which things belong together because the user thinks about or uses them together?

Visual grouping should reflect task grouping. If the interface looks grouped one way but behaves another way, users will make incorrect assumptions.

## Core objective

Make relationships and scope obvious before interaction.

A user should be able to infer:

- which controls operate on the same object;
- which actions belong to the current task;
- which information is supporting versus primary;
- which controls are global versus local;
- which options are mutually related;
- which items form a repeated set.

## Group by user task, not code structure

Do not expose backend architecture directly.

A database may store fields in one schema, but users may expect them grouped as:

- Profile
- Security
- Notifications
- Billing

Likewise, a project page might group functionality as:

- Overview
- Files
- Members
- Deployments
- Settings

The grouping should follow user intent and vocabulary.

## Gestalt principles

Use proximity and similarity deliberately.

### Proximity

Items placed close together are perceived as related.

Use smaller gaps within a functional group and larger gaps between groups.

### Similarity

Items that share color, shape, size, style, or behavior are perceived as related.

Use similarity to reinforce recurring component roles, but do not make unrelated actions look identical if that suggests the wrong relationship.

### Common region

A container can strongly imply a group.

Use this only when the grouping deserves a surface or boundary. Do not wrap every cluster in a card.

## Action grouping

Separate actions by consequence and scope.

Good groupings:

- Previous / Next
- Undo / Redo
- Save / Cancel
- Sort / Filter / View options
- Edit / Duplicate / Archive

Keep destructive actions visually and spatially distinct when accidental activation would be costly.

Do not place an unrelated “Add” action inside a navigation-action cluster simply because there is empty space.

## Primary versus secondary actions

A group can contain multiple actions without giving them equal emphasis.

Establish:

- primary action;
- secondary action;
- tertiary or overflow actions;
- destructive action when applicable.

Do not create three equally loud buttons when one action clearly advances the task.

Avoid using color to make every button look primary.

## Toolbar grouping

Toolbars should form recognizable clusters.

For example:

[Undo Redo]   [Select Move]   [Zoom]   [Share]

Use separators or larger spacing only where the groups need stronger distinction.

Keep icon behavior consistent inside each group.

If an icon is ambiguous, provide a label or accessible name.

## Form grouping

Group fields according to the question users believe they are answering.

Keep:

label → field → support/error

as one micro-group.

Then separate that micro-group from the next field.

Use section headings for groups such as shipping, payment, team access, or preferences.

Do not use a divider after every field.

## Settings grouping

Settings pages often fail because categories mirror implementation rather than mental models.

Use mutually understandable categories and avoid duplication.

If one setting logically fits in two places, choose the strongest expected location and use cross-references only when necessary.

Do not create vague catch-all groups such as “General,” “Other,” or “Advanced” unless the contents genuinely form a coherent secondary set.

## Data grouping

In dashboards and tables, group values that answer the same question.

Examples:

- revenue, orders, average order value;
- requests, latency, error rate;
- active users, retention, churn;
- storage used, quota, projected usage.

Do not separate related numbers into distant cards merely for visual symmetry.

## Navigation grouping

Navigation sections should represent distinct conceptual areas.

Within a sidebar:

- keep related destinations adjacent;
- use section labels only when they clarify categories;
- do not over-section a list of six items into five titled groups;
- keep account/profile/help items separated from core task navigation if their scope differs.

## Component anatomy grouping

Inside a component, treat sub-elements according to function.

A list item might contain:

leading identity → main label → metadata → status → trailing action

These roles should stay stable across repeated items.

Do not randomly move metadata or actions between rows.

## Visual weight inside groups

Related does not mean equal.

Within one group, establish hierarchy using:

- typography;
- contrast;
- position;
- scale;
- whitespace;
- color;
- emphasis.

The group label may be quieter than the primary value, while secondary metadata may be quieter still.

## Responsive grouping

When groups reflow, preserve relationships.

A horizontal action cluster may stack vertically, but the primary and secondary actions should remain adjacent and ordered logically.

Do not allow responsive wrapping to mix two previously separate groups into one visual row.

When wrapping is possible, use group containers in layout code so each cluster wraps as a unit.

## Accessibility

- Do not rely on visual grouping alone when semantic grouping exists.
- Use fieldsets/legends for related form controls when appropriate.
- Use heading structure for content sections.
- Use lists and tables for actual list/table relationships.
- Ensure focus order follows the functional grouping.
- Do not separate labels from controls in the accessibility tree.
- Do not use color as the only cue distinguishing group type or status.

## Failure modes

### Accidental grouping

Elements are close only because the grid happened to place them there.

Fix: review proximity according to functional relationship.

### False similarity

Destructive and safe actions look identical.

Fix: differentiate role while keeping component family consistency.

### Group overload

A group contains too many unrelated controls.

Fix: split according to task or scope.

### Excessive sectioning

Every two controls receive a heading or card.

Fix: remove unnecessary boundaries and use spacing.

### Scope mismatch

A global action appears inside a local panel.

Fix: move it to a level that matches what it affects.

## Evaluation checklist

- Can users predict which controls operate together?
- Are related elements closer than unrelated ones?
- Are recurring component roles visually consistent?
- Is the primary action obvious within each group?
- Are destructive actions separated appropriately?
- Does navigation grouping match users’ mental models?
- Do groups remain intact when the viewport changes?
- Does semantic markup preserve the same relationships?
- Can unnecessary borders/cards be removed without losing the grouping?

## Source foundations

This skill synthesizes Nielsen Norman Group research on Gestalt proximity and similarity, Apple guidance on grouping related information and functions, Fluent layout guidance on proximity and spacing patterns, Carbon spacing guidance, and WCAG requirements around programmatic relationships and meaningful sequence.

References:

- https://www.nngroup.com/articles/gestalt-proximity/
- https://www.nngroup.com/articles/gestalt-similarity/
- https://developer.apple.com/design/human-interface-guidelines/layout
- https://fluent2.microsoft.design/layout
- https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview
- https://www.w3.org/WAI/WCAG22/Understanding/
