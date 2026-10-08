# Information Architecture

Use this skill before styling navigation, pages, menus, settings, dashboards, or content-heavy products.

Information architecture (IA) is the conceptual structure of information, functionality, objects, and destinations. Navigation is one visible mechanism for moving through that structure; a sitemap is only one representation of it.

## Core objective

Organize the product so users can predict where information and actions belong.

A strong IA reduces searching, backtracking, duplicate destinations, ambiguous labels, and “where did they put this?” moments.

## Start from user goals

Before drawing a sidebar, list:

- primary user goals;
- recurring tasks;
- core objects;
- important states;
- major destinations;
- common actions;
- settings/preferences;
- administrative tasks;
- content categories;
- relationships among objects.

Do not begin with a menu and then force features into it.

## Build around mental models

Organize categories according to how users think about the domain, not according to engineering modules or database tables.

Examples:

Workspace → Projects → Project → Files → File

Settings → Billing → Invoices

Organization → Members → Roles

Users should not need to understand backend terminology to navigate the interface.

## Category quality

Good categories are:

- distinct;
- understandable;
- collectively useful;
- stable enough to learn;
- specific enough to predict content;
- flexible enough for product growth.

Avoid categories that overlap heavily.

Avoid one huge “General” category that contains unrelated settings.

Avoid tiny categories containing one item unless that item truly deserves top-level status.

## Information scent

Navigation labels should help users predict what they will find.

Nielsen Norman Group describes information scent as the cues users use to estimate whether a destination will satisfy their goal.

Prefer:

- Billing history
- Team members
- API keys
- Security settings
- Deployment logs

over:

- Manage
- Explore
- Resources
- More
- Tools

unless surrounding context makes the meaning unambiguous.

## Labels

Use familiar user language.

Good labels are:

- concise;
- specific;
- consistent;
- action-oriented when representing actions;
- noun-oriented when representing destinations or objects.

Do not switch between synonyms such as Workspace, Space, Project Area, and Hub for the same concept.

Apple’s writing guidance emphasizes consistent language and clear action-oriented labels.

## Primary navigation

Primary navigation should represent a small set of high-level destinations users return to frequently.

A destination belongs in primary navigation when it is:

- central to the product;
- frequently visited;
- conceptually broad enough to contain meaningful substructure;
- useful across many sessions.

Do not promote every feature to the primary sidebar.

## Secondary navigation

Use secondary navigation for structure inside a high-level destination.

Examples:

Project
- Overview
- Activity
- Files
- Members
- Settings

Keep primary and secondary navigation visually distinct so scope is clear.

## Contextual navigation and actions

Contextual controls should appear near the object they affect.

Examples:

- row actions on a file;
- filters for the current table;
- settings for the current project;
- inspector for the selected layer.

Do not mix contextual controls with global product navigation if their scope is local.

## Hierarchy depth

Use enough depth to create meaningful categories, but avoid unnecessary layers.

Deep hierarchy increases navigation cost and memory burden.

Flat hierarchy creates long undifferentiated lists.

Balance breadth and depth according to content complexity.

Do not optimize for arbitrary rules like “everything must be within three clicks.”

Optimize for confidence: users should know they are moving toward the correct destination.

## Progressive disclosure

Do not expose every subdestination at once.

Use:

- expandable navigation groups;
- nested views;
- contextual menus;
- settings subsections;
- drill-down pages.

Keep the most important destinations visible.

Do not hide frequently used destinations behind repeated overflow interactions.

## Search

Search complements IA; it does not replace IA.

A search box is useful when:

- the content set is large;
- users know what they want;
- labels can be indexed clearly;
- direct navigation would be inefficient.

Search should not be the only way to locate ordinary settings or main product areas.

## Filters and facets

Filters refine a known content set.

Design filters around meaningful properties users understand.

Keep active filters visible and removable.

Do not create multiple filter controls that represent the same concept differently.

## Taxonomy

For large content systems, define a stable taxonomy.

Document:

- category names;
- definitions;
- allowed values;
- parent-child relationships;
- synonyms;
- metadata rules.

Consistency improves navigation, filtering, search, and analytics.

## Cross-linking

Cross-links can help when an item reasonably belongs to multiple mental models.

Use them to support discovery without duplicating the underlying destination.

Avoid creating two separate settings pages that modify the same value.

## Orientation

Users should know:

- where they are;
- what parent context they are in;
- how they arrived;
- how to move up or back;
- what object is currently selected.

Use selected navigation states, page titles, breadcrumbs where appropriate, object names, and consistent page structure.

## Design for growth

Ask how the IA behaves when:

- 10 projects become 1,000;
- 4 settings categories become 20;
- one user becomes a multi-team organization;
- new object types are introduced;
- permissions create hidden destinations.

Do not create architecture that only works for the demo data.

## Permissions and roles

IA should adapt to permissions without creating confusing gaps.

If users cannot access a destination:

- remove it when it is irrelevant;
- disable/explain it when awareness is useful;
- do not leave dead links.

Avoid changing the entire navigation order unpredictably between roles unless necessary.

## Responsive navigation

The IA should remain stable even when the navigation mechanism changes.

A desktop sidebar may become a mobile drawer or nested route.

Do not change category meaning just because the viewport changes.

## Localization

Labels must survive translation.

Allow expansion and avoid wordplay that cannot be translated.

Support right-to-left navigation direction where appropriate.

Do not encode hierarchy using only left indentation; use semantic relationships as well.

## Accessibility

- Navigation regions should be semantically identifiable.
- Repeated navigation should remain consistent.
- Focus order should follow logical sequence.
- Page titles and headings should identify location.
- Links should have meaningful purpose in context.
- Multiple ways to find important pages may be required for larger sites.

## Testing IA

Use methods such as:

### Card sorting

Learn how users naturally group concepts and what labels they expect.

### Tree testing

Test whether users can locate items in the hierarchy without visual styling distracting from structure.

### First-click or navigation testing

Observe where users expect to begin a task.

### Search-log and support analysis

Look for repeated searches, failed terms, and “where is…” support questions.

## Failure modes

### Feature dump sidebar

Every feature receives top-level navigation.

Fix: group around stable product concepts.

### Vague labels

Fix: increase information scent with specific language.

### Duplicate destinations

Fix: create one source of truth and cross-link where necessary.

### Architecture mirrors codebase

Fix: reorganize around user goals and domain concepts.

### Search as a bandage

Fix: repair categories and labels before adding more search dependency.

## Evaluation checklist

- Can users predict where common tasks belong?
- Are top-level categories mutually understandable?
- Are navigation labels specific?
- Is depth appropriate to complexity?
- Are global, local, and contextual navigation separated?
- Can the model grow without becoming a feature dump?
- Does responsive UI preserve the same conceptual structure?
- Can important destinations be found with keyboard/screen reader navigation?
- Has the hierarchy been tested without visual styling?

## Source foundations

This skill synthesizes Nielsen Norman Group information-scent and IA research, Apple layout and writing guidance, Fluent accessibility principles, and WCAG guidance for consistent navigation, headings, labels, location, and multiple ways to locate content.

References:

- https://www.nngroup.com/articles/information-scent/
- https://www.nngroup.com/articles/3-ia-mistakes/
- https://developer.apple.com/design/human-interface-guidelines/layout
- https://developer.apple.com/design/human-interface-guidelines/writing
- https://fluent2.microsoft.design/accessibility
- https://www.w3.org/WAI/WCAG22/Understanding/
