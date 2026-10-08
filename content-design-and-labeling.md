# Content Design and Labeling

Use this skill for navigation labels, buttons, headings, form instructions, errors, empty states, confirmations, onboarding, settings, and any interface copy.

Words are part of the interface. Clear language improves information scent, scanning, accessibility, and task completion.

## Core objective

Help users understand what is happening, what something means, and what will happen next with the fewest words necessary.

## Start from purpose

For every piece of UI text, identify its job:

- orient;
- label;
- instruct;
- describe;
- warn;
- confirm;
- recover;
- navigate;
- trigger an action.

Do not add copy because an empty region looks unfinished.

## Use familiar language

Prefer words users already use for the concept.

Avoid internal product terminology, engineering names, and unnecessary branded vocabulary.

If a branded term is necessary, explain it at first use when users cannot infer its meaning.

## Information scent

Navigation and link labels should predict the destination.

Prefer:

- Billing history
- Security settings
- Team members
- API documentation
- View pricing

over vague labels such as:

- Explore
- Resources
- Manage
- More
- Learn more

when the surrounding context does not explain them.

## Action labels

Prefer verbs that describe the result.

Examples:

- Save changes
- Create project
- Invite member
- Download report
- Delete workspace

Avoid “Submit” when a specific outcome can be named.

Avoid playful labels that make consequential actions ambiguous.

Apple recommends clear, action-oriented language and descriptive links.

## Sentence case

Use sentence case for most UI text unless the design system has a justified exception.

Sentence case is easier to scan and keeps interface tone natural.

Avoid ALL CAPS for ordinary controls and headings.

## Front-load distinguishing words

When users scan lists or menus, put the meaningful term early.

Weak:

- Manage billing
- Manage members
- Manage notifications

Stronger:

- Billing
- Members
- Notifications

## Headings

A heading should summarize what follows.

Use specific headings rather than decorative phrases.

Heading hierarchy should match semantic structure.

Do not use a giant heading merely because the text is short.

## Helper text

Use helper text only when it prevents confusion or error.

Keep it near the control it explains.

Do not repeat the label in different words.

## Placeholders

Use placeholders for examples or optional hints, not as the only field label.

Placeholder text disappears during input and often has lower visual prominence.

Essential instructions should remain visible.

## Errors

Error messages should explain:

1. what went wrong;
2. where it happened;
3. how to fix it when possible.

Weak:

“Invalid input.”

Stronger:

“Password must contain at least 12 characters.”

Do not blame the user.

Do not erase valid input after an error.

## Destructive actions

Use explicit object/action language.

Prefer:

“Delete project”

over:

“Confirm”

Confirmation dialogs should name the consequence and the object when space permits.

Do not make destructive buttons visually or verbally ambiguous.

## Success and status messages

State what happened.

Good:

“Project created.”

“Changes saved.”

“Invitation sent.”

Avoid congratulatory filler for routine system events.

## Empty states

An empty state should answer:

- What is empty?
- Is this expected?
- What can the user do next?

Keep the primary action specific.

Do not let decorative illustration replace explanation.

## Loading

When wait time is meaningful, explain the operation rather than displaying generic “Loading…” everywhere.

Examples:

- Uploading 3 files…
- Generating report…
- Connecting to workspace…

Do not promise precise completion times unless the system can support them.

## Progressive disclosure copy

Disclosure labels should predict hidden content.

Prefer:

- Show deployment details
- Advanced export options
- View permissions

over:

- More
- Details
- Advanced

when specificity is possible.

## Consistency

Create a product vocabulary.

One concept should have one primary name.

Do not alternate:

workspace / project space / hub

member / user / teammate

archive / disable / deactivate

unless they truly represent different concepts.

## Tone

Voice can be branded; meaning must remain clear.

Adjust tone to context.

A payment failure or security warning should be more direct than a celebratory onboarding moment.

Do not let personality interfere with comprehension.

## Plain language

Prefer short familiar words and direct sentence structures.

Avoid:

- jargon;
- unnecessary acronyms;
- bureaucratic phrasing;
- idioms that do not localize;
- gendered assumptions.

## Localization

Write copy that can expand.

Avoid embedding layout assumptions into text.

Do not concatenate sentence fragments in code when translation may change word order.

Support locale-specific dates, numbers, currency, and plural rules.

## Accessibility

- Link purpose should be understandable in context.
- Visible labels should align with accessible names.
- Headings should be descriptive.
- Instructions should not rely only on position, shape, or color.
- Error identification should be textual/semantic, not only visual.
- Unusual abbreviations should be expanded where users may not know them.

## Failure modes

### Vague button text

Fix: name the action/result.

### Cute copy during serious errors

Fix: prioritize clarity and recovery.

### Heading fluff

Fix: write information-rich headings.

### Label inconsistency

Fix: establish one product vocabulary.

### Placeholder-only forms

Fix: add persistent labels.

### “Learn more” everywhere

Fix: make links specific enough to provide information scent.

## Evaluation checklist

- Can users predict every navigation destination?
- Do action labels describe outcomes?
- Are headings meaningful without body copy?
- Are errors specific and recoverable?
- Are terms consistent across screens?
- Is text understandable without product-internal knowledge?
- Does copy localize without breaking layout assumptions?
- Do visible labels match accessible names?

## Source foundations

References:

- https://developer.apple.com/design/human-interface-guidelines/writing
- https://www.nngroup.com/articles/information-scent/
- https://www.nngroup.com/articles/3-ia-mistakes/
- https://fluent2.microsoft.design/accessibility
- https://www.w3.org/WAI/WCAG22/Understanding/
