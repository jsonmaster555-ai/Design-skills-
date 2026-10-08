# Content Chunking

Use this skill when a page, panel, form, article, table, dashboard, or workflow contains enough information that users must scan before they can understand it.

Chunking means dividing information into meaningful, recognizable units so users can process structure before reading every detail.

The goal is not to create more boxes. The goal is to make relationships obvious.

## Core principle

People should be able to answer three questions quickly:

1. What are the major groups?
2. What belongs inside each group?
3. Where should I look for the thing I need?

## Build semantic chunks first

Group content by meaning before styling it.

Useful grouping dimensions include:

- task;
- object;
- subject;
- time;
- status;
- workflow stage;
- ownership;
- frequency of use;
- comparison dimension;
- input purpose.

Do not group items merely because they fit neatly into equal-sized cards.

## Strong chunk boundaries

A boundary can be communicated using:

- whitespace;
- headings;
- alignment changes;
- background or surface changes;
- dividers;
- containers;
- indentation;
- tabs;
- list structure;
- progressive disclosure.

Use the least visually heavy boundary that communicates the relationship.

Spacing should usually be attempted before borders and cards.

## Proximity rule

Related elements should be closer to each other than they are to unrelated elements.

Examples:

- heading to its description: close;
- label to its input: close;
- input to its help or error text: close;
- one field group to the next field group: farther;
- one major section to the next section: much farther.

If the distances are visually equal, the relationships will also feel equal.

## Internal versus external spacing

Treat each chunk as having an inside and an outside.

Internal spacing communicates relationships among items within the chunk.

External spacing separates the chunk from neighboring chunks.

As a rule, external separation should be perceptibly larger than the repeated internal gap.

Do not inflate every component to create page-level whitespace.

## Headings as scan anchors

Use headings to label conceptual groups, not merely to decorate the page.

A useful heading should:

- summarize the section;
- use words users expect;
- differ visibly from body text;
- be closer to the content it introduces than to the previous section;
- follow a logical semantic heading order in code.

Avoid heading styles that are visually impressive but vague, such as “Explore,” “More,” or “Discover,” when a specific label would improve information scent.

## Chunk size

There is no universal number of items per chunk.

Prefer a chunk large enough to represent one concept but small enough to scan as a unit.

Split a chunk when:

- several subtopics are mixed together;
- the heading no longer accurately describes everything inside it;
- users must repeatedly search inside the group;
- different actions apply to different subsets;
- the group becomes visually dense enough that substructure disappears.

Combine chunks when:

- they always appear together;
- they serve the same decision;
- their separation creates unnecessary navigation or containers;
- users need to compare them directly.

## Forms

Chunk forms by user intent rather than implementation schema.

Good groups might be:

- Contact information
- Shipping address
- Billing information
- Team permissions
- Notification preferences

Avoid one uninterrupted stack of unrelated fields.

Keep labels close to controls and support/error text close to the field it describes.

Do not separate a field from its validation message with a large gap or unrelated content.

## Lists and tables

Use chunks to improve row and column scanning.

For tables:

- keep related columns adjacent;
- make the primary identifying column easy to locate;
- avoid decorative column separation that competes with the data;
- use alignment consistently by data type;
- separate sections or groups only when the grouping has meaning.

For lists:

- establish a predictable item anatomy;
- keep repeated metadata in repeated locations;
- use consistent gaps between peer items;
- do not vary card padding randomly between items.

## Dashboards

Do not turn every metric into an isolated card.

Group metrics that answer the same question.

For example, acquisition metrics can form one region, revenue metrics another, and system health another.

If every number has identical visual treatment, users cannot tell which metrics are related or important.

## Long-form content

Support scanning using:

- descriptive subheadings;
- short paragraphs;
- meaningful lists;
- front-loaded sentences;
- selective emphasis;
- restrained line length;
- enough separation between topics.

Nielsen Norman Group eyetracking research shows that users frequently scan rather than read continuously, so a wall of prose should not be the default structure for task-oriented content.

## Cards are not chunks by definition

A card is a visual container. A chunk is a semantic group.

A valid chunk may need no card at all.

Use a card when the content behaves as an independent object, destination, selectable unit, or surface.

Avoid cards when whitespace and headings communicate the grouping more clearly.

## Responsive chunking

When layouts stack, preserve conceptual relationships.

Do not let responsive reordering place a section heading far away from its content.

If side-by-side groups become a vertical stack, make the boundary between the original groups clear.

Do not rely on desktop columns alone to communicate meaning.

## Accessibility

Chunking must exist semantically as well as visually.

Use appropriate headings, lists, fieldsets/groups, tables, and landmarks where applicable.

A screen reader should encounter a meaningful structure even without visual whitespace or borders.

Ensure zoom, larger type, and user-defined text spacing do not cause chunks to overlap or lose their labels.

## Failure modes

### Card soup

Everything is placed in its own rounded rectangle.

Fix: remove containers and restore grouping through spacing, typography, and alignment.

### Uniform gaps

Every vertical distance is identical.

Fix: define stronger internal and external spacing relationships.

### Over-fragmentation

Every sentence or metric is its own chunk.

Fix: recombine elements that support the same concept or decision.

### Under-chunking

A page is one continuous region of content.

Fix: identify semantic groups and give each a clear anchor.

### Decorative headings

Headings exist but do not help users predict content.

Fix: write specific, task-relevant labels.

## Evaluation checklist

- Can the major groups be identified without reading all body copy?
- Are related items closer than unrelated items?
- Is the heading attached to the content it introduces?
- Can unnecessary borders/cards be removed without losing meaning?
- Are repeated items internally consistent?
- Does the grouping still work on a narrow screen?
- Is the structure also represented semantically for assistive technology?
- Does each chunk represent one understandable concept?

## Source foundations

This skill synthesizes Nielsen Norman Group research on Gestalt proximity and scanning, Carbon spacing guidance, Fluent layout guidance, Apple layout guidance, and WCAG guidance on information relationships, meaningful sequence, headings, and text adaptation.

References:

- https://www.nngroup.com/articles/gestalt-proximity/
- https://www.nngroup.com/articles/text-scanning-patterns-eyetracking/
- https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview
- https://fluent2.microsoft.design/layout
- https://developer.apple.com/design/human-interface-guidelines/layout
- https://www.w3.org/WAI/WCAG22/Understanding/
