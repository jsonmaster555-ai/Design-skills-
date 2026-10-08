# Spatial Hierarchy and Prospacing

Use this skill to design spacing as a structural system rather than a collection of random margins and padding values.

Spatial hierarchy communicates relationship, scope, importance, grouping, and density through distance and alignment.

“Prospacing” in this skill means professional, intentional spacing: every gap should communicate something.

## Core objective

Create layouts where users can understand relationships from space before reading labels or borders.

## Relationship-first spacing

Do not choose spacing values in isolation.

Classify the relationship first:

- micro relationship;
- component relationship;
- group relationship;
- section relationship;
- page relationship.

Then choose a value from the system.

## A restrained scale

Use a small spacing vocabulary.

A practical example:

- 2: optical/fine adjustment;
- 4: micro;
- 8: tight relation;
- 12: compact component;
- 16: standard component/group;
- 24: group separation;
- 32: strong group separation;
- 48: section separation;
- 64: major section;
- 96+: expressive/marketing macro spacing.

Do not treat this exact scale as universal. Preserve the principle of a constrained scale.

Fluent’s spacing ramp is largely based around a four-pixel cadence while including small exceptions for icon alignment. Carbon provides both fine spacing tokens and larger layout values.

## Internal space is not external space

Internal padding shapes the component itself.

External margin/gap communicates the component’s relationship to neighbors.

Do not increase button padding because the page feels cramped.

Do not increase card padding because sections need more separation.

Fix the correct layer.

## Component density

Choose component density from task context.

### Compact

Use for:

- dashboards;
- data tables;
- editors;
- developer tools;
- file managers;
- command-heavy desktop software.

### Standard

Use for:

- general SaaS;
- settings;
- consumer productivity;
- account management.

### Spacious

Use for:

- onboarding;
- marketing;
- editorial introductions;
- focused single-task screens.

Do not use spacious marketing controls inside high-density software.

## Buttons

Button spacing should create a compact, optically centered control.

Evaluate:

- label size;
- icon size;
- icon-label gap;
- vertical padding;
- horizontal padding;
- visible height;
- hit target;
- neighboring button gap.

Avoid making every button extremely wide or 48–56px tall on desktop without a usability reason.

A large hit target can exist around a visually compact element when implementation allows.

## Inputs

Keep:

label → input → help/error

as one tight relationship.

Use a larger gap before the next field.

Do not place error text closer to the next field than to the field it describes.

## Cards and panels

Padding depends on information density.

Do not blindly use 24–32px for every card.

Compact product cards may need less.

A large editorial card may need more.

Inside nested surfaces, reduce padding carefully so usable content width is not consumed by multiple layers.

## Lists and navigation

Rows should be large enough to scan and interact with but not inflated.

Use stable vertical rhythm.

Keep icon-to-label gaps consistent.

Separate navigation groups with larger group gaps rather than making every row taller.

## Toolbars

Use tight internal grouping for related commands.

Create larger gaps or subtle separators between command groups.

Do not give each icon button huge standalone margins.

## Section rhythm

A page should have repeated spacing relationships.

For example:

- heading → description = small;
- description → content = medium;
- content group → next content group = medium/large;
- section → next section = large.

Equivalent relationships should usually reuse equivalent spacing.

Consistency creates rhythm; identical spacing everywhere destroys hierarchy.

## Negative space as emphasis

More space around an item can increase perceived importance.

Use this for important headings, summaries, decisions, or central objects.

Do not isolate random decorative content more strongly than task content.

## Proximity versus common region

Proximity is often enough to form a group.

Use a container only when:

- the group acts as one object;
- the region has independent state;
- it needs a surface/elevation role;
- it is selectable/draggable;
- containment must persist when moved or resized.

Avoid substituting cards for weak spacing.

## Vertical rhythm

Maintain predictable vertical intervals across repeated sections.

Text boxes should fit their content rather than use arbitrary fixed heights.

Spacing should attach to the real content box so changes in localization or wrapping do not break rhythm.

## Horizontal rhythm

Share leading edges across related content.

Common horizontal anchors reduce visual effort more than perfectly symmetrical container sizes.

In forms and tables, content alignment often matters more than card-edge alignment.

## Optical correction

Spacing systems are geometric; perception is optical.

After applying the system, inspect:

- circular icons;
- chevrons;
- asymmetric glyphs;
- uppercase text;
- mixed font sizes;
- baseline alignment.

Small corrections are acceptable when they improve perceived balance.

Document repeated corrections so they become component rules rather than one-off magic numbers.

## Responsive spacing

Spacing tokens do not have to scale proportionally.

At smaller widths:

- page margins may shrink;
- major section gaps may reduce;
- micro gaps may remain unchanged;
- touch targets may increase;
- side-by-side groups may stack.

Preserve the hierarchy of relationships.

## Text expansion

Fixed heights can break when users enlarge text or override text spacing.

Allow rows and controls containing text to grow where necessary.

WCAG 2.2 requires content to remain usable when users override line, paragraph, letter, and word spacing.

## Accessibility and targets

Visual compactness does not justify unusably small targets.

WCAG 2.2 includes a minimum target-size criterion of 24×24 CSS pixels with exceptions; platform systems often recommend larger touch targets.

Use enough spacing between adjacent targets to reduce accidental activation.

## Failure modes

### Giant component syndrome

Fix: separate component padding from section whitespace.

### Random-value syndrome

Fix: map relationships to a token scale.

### Equal-gap syndrome

Fix: distinguish internal, group, and section spacing.

### Nested-padding loss

Fix: reduce redundant padding in nested containers and preserve content width.

### Pretty but low-density

Fix: match density to user task, not current UI trends.

### Cramped but “compact”

Fix: maintain readable grouping and usable targets; compact is not compressed.

## Evaluation checklist

- Does each gap correspond to a relationship?
- Are internal gaps smaller than external group gaps?
- Are components compact enough for their task?
- Is the spacing scale constrained?
- Is white space used for hierarchy rather than decoration?
- Can cards/borders be removed without losing grouping?
- Does the rhythm survive localization and text enlargement?
- Are interactive targets still usable?
- Are optical adjustments intentional and repeatable?

## Source foundations

This skill synthesizes Carbon spacing/2x Grid, Fluent layout spacing, Apple layout guidance, Nielsen Norman Group proximity research, and WCAG text-spacing and target-size requirements.

References:

- https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview
- https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/overview
- https://fluent2.microsoft.design/layout
- https://developer.apple.com/design/human-interface-guidelines/layout
- https://www.nngroup.com/articles/gestalt-proximity/
- https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html
- https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum
