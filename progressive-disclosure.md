# Progressive Disclosure

Use this skill when an interface contains more information, controls, settings, or capabilities than users need at one time.

Progressive disclosure is not “hide things to make the screen cleaner.” It is the deliberate staging of complexity so that the most important and most frequently needed choices are available first, while specialized, advanced, contextual, or infrequent choices remain reachable when they become relevant.

## Core objective

Reduce cognitive load without reducing capability.

A good disclosure system should make the first interaction easier while preserving a clear path to advanced functionality.

## Primary rules

1. Show the minimum information required to understand the current task.
2. Keep high-frequency and high-importance actions visible.
3. Defer advanced, rare, or conditional options until users request them or until context makes them relevant.
4. Do not hide a required step behind an ambiguous control.
5. Do not hide safety-critical, destructive, billing, permission, or irreversible consequences.
6. Prefer one clear path over several competing paths that all lead to the same outcome.
7. Make the existence of additional options discoverable.
8. Preserve user context when revealing more information.
9. Let users reverse or collapse disclosure when doing so helps them recover space or focus.
10. Keep the disclosure mechanism consistent throughout the product.

## What belongs at the first level

Keep an item visible when it is:

- required to finish the main task;
- used frequently by the target user;
- a primary navigation destination;
- needed to understand the current state;
- time-sensitive;
- destructive or consequential enough that hiding it would cause surprise;
- a status users must notice before acting;
- the obvious next step in a workflow.

## What can move to a secondary level

Good candidates include:

- advanced configuration;
- low-frequency customization;
- debugging or developer controls;
- optional metadata;
- historical detail;
- rarely changed preferences;
- contextual actions that apply only after selection;
- secondary filters;
- long explanatory material;
- additional statistics;
- alternate export formats;
- power-user features.

## Disclosure mechanisms

Choose the mechanism based on the relationship between the hidden information and the current task.

### Inline expansion

Use when the secondary content is directly related to the item above it and users benefit from seeing both at once.

Examples: “Show details,” advanced filter criteria, expandable error explanations.

### Accordion or disclosure group

Use when several peer sections exist and each section contains secondary information.

Do not use accordions merely to make a page look shorter. If most users need every section, show the content.

### Menu

Use for compact sets of secondary actions, especially actions that operate on the current object.

Do not put the primary action in an overflow menu just to keep a toolbar visually minimal.

### Nested view or drill-down

Use when the secondary information has enough complexity to deserve its own navigational context.

Preserve clear back-navigation and location cues.

### Inspector or side panel

Use when users need secondary properties while still referencing the main content.

Do not cover the object they are trying to inspect if resizing or reflowing the main content is feasible.

### Modal or dialog

Use when attention must temporarily narrow to a decision or short task.

Do not use a modal as a dumping ground for an entire sub-application.

### Tabs

Use for peer categories that users may switch between repeatedly.

Tabs are not progressive disclosure when one tab simply hides essential sequential steps.

## Information scent

A disclosure control must predict what it reveals.

Prefer specific labels such as:

- Advanced export options
- View permissions
- Show deployment logs
- More billing details

Avoid vague labels such as:

- More
- Extras
- Misc
- Other

unless the surrounding context already makes the destination obvious.

## Layer depth

Avoid deep chains such as:

Settings → More → Advanced → Additional → Configure

Every additional layer increases memory burden and makes features harder to discover.

When a feature requires repeated access, promote it to a higher level.

## State and persistence

Decide whether disclosure state should persist.

Persist it when:

- users repeatedly work in the same expanded mode;
- expansion expresses a user preference;
- collapsing it on every visit would create repetitive work.

Reset it when:

- the content is transient;
- persistence could expose sensitive information;
- the state depends on an object that no longer exists;
- preserving the state would make the next task confusing.

## Responsive behavior

Do not assume desktop disclosure patterns should simply shrink on mobile.

A desktop inspector may become a full-screen nested view on a narrow viewport.

A toolbar with visible secondary actions may become an overflow menu.

Preserve action priority and information relationships across breakpoints even if the mechanism changes.

## Accessibility

- Every disclosure control must be keyboard reachable.
- Focus order must follow the visual and logical order.
- Expanded/collapsed state must be programmatically exposed.
- When opening a dialog or temporary surface, move focus intentionally and restore it when the surface closes.
- Do not make hidden information available only on hover.
- Do not use color alone to indicate that a section is expanded.
- Ensure revealed content remains usable at large text sizes and high zoom.

## Common failure modes

### Hiding too much

Symptoms: users repeatedly open the same overflow menu, advanced section, or panel.

Fix: promote frequently used items.

### Hiding too little

Symptoms: dense screens, long settings forms, many low-priority buttons competing with the main action.

Fix: stage complexity based on frequency and task relevance.

### Surprise disclosure

Symptoms: clicking a harmless-looking label opens a complex workflow or changes state.

Fix: strengthen the label and separate navigation from destructive actions.

### Lost context

Symptoms: opening details removes the object users were comparing against.

Fix: prefer inline expansion, split view, or reversible navigation.

### Decorative minimalism

Symptoms: important features are hidden only so the page can look empty.

Fix: optimize for comprehension and task completion, not screenshot cleanliness.

## Evaluation checklist

Before finalizing a disclosure pattern, ask:

- Can a new user complete the main task without opening secondary UI?
- Can an expert still reach advanced capability quickly?
- Are common actions visible?
- Is the label specific enough to predict what appears?
- Is the number of layers reasonable?
- Does revealing content preserve context?
- Can users return to the previous state?
- Does keyboard focus remain logical?
- Does the pattern still work at narrow widths and enlarged text?
- Are consequential options visible enough to avoid surprise?

## Source foundations

This skill synthesizes guidance from Apple Human Interface Guidelines on layout and progressive disclosure, Nielsen Norman Group research on progressive disclosure and information scent, Microsoft Fluent accessibility and layout guidance, and WCAG 2.2 requirements for focus, keyboard interaction, meaningful sequence, and content on hover/focus.

References:

- https://developer.apple.com/design/human-interface-guidelines/layout
- https://www.nngroup.com/articles/progressive-disclosure/
- https://www.nngroup.com/articles/information-scent/
- https://fluent2.microsoft.design/accessibility
- https://www.w3.org/WAI/WCAG22/Understanding/
