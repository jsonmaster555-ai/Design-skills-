# Reading Patterns — F-Shape, Layer Cake, Spotted, Z-Flow, and Task Scanning

Use this skill to arrange information so scanning behavior helps users discover the next useful thing instead of hiding it.

Reading patterns are tendencies, not rigid templates. The user’s task, language direction, prior expectations, content type, and visual hierarchy all influence where attention moves.

## Core objective

Design for efficient scanning first and sustained reading second, unless the product is explicitly a long-form reading experience.

## Do not treat F and Z as laws

The F-pattern is an observed scanning behavior, not a layout template designers should copy.

The Z-pattern is better understood as a composition heuristic for simple pages with few major elements, not a universal eyetracking law.

Strong hierarchy can alter scanning behavior.

## F-shaped scanning

Nielsen Norman Group research found that users often create an F-like fixation pattern when scanning poorly structured text-heavy pages.

Typical behavior in left-to-right languages:

- more attention near the top;
- more attention near the leading edge;
- shorter horizontal scans farther down the page.

In right-to-left languages, the directional bias can mirror.

## F-pattern implications

Do not hide important words at the end of long lines or paragraphs.

Front-load:

- headings;
- list items;
- notifications;
- search results;
- navigation labels;
- table labels;
- setting names.

Weak:

“To change how your account is billed, open Billing Settings.”

Stronger:

“Billing Settings controls your payment method and invoices.”

## Prevent unproductive F-scanning

The F-pattern often appears when pages lack structure.

Improve the content with:

- descriptive headings;
- short paragraphs;
- bullets for real lists;
- front-loaded sentences;
- meaningful links;
- stable alignment;
- appropriate text width;
- selective emphasis.

Do not respond by simply making every first word bold.

## Layer-cake scanning

Users often scan headings and subheadings horizontally, skipping body content until a heading looks relevant.

This is highly useful behavior.

Support it with:

- informative headings;
- clearly differentiated heading levels;
- sufficient whitespace between sections;
- heading proximity to the content it introduces;
- logical semantic heading order.

A user should understand the outline by reading only the headings.

## Spotted scanning

Users may jump between distinctive visual signals such as:

- links;
- bold terms;
- numbers;
- status labels;
- colored terms;
- icons;
- list bullets.

Use these signals sparingly.

If too much content is visually highlighted, spotted scanning becomes random rather than helpful.

## Commitment reading

When users are strongly interested in the content, they may read more thoroughly.

Support committed reading with:

- comfortable line length;
- readable type;
- sufficient line height;
- stable paragraphs;
- restrained visual interruptions;
- meaningful sectioning.

Do not optimize an article like a dashboard or a dashboard like an article.

## Z-flow composition

For simple layouts with a few dominant elements, a rough Z-like composition can be useful:

1. orientation/brand near the beginning of the top region;
2. navigation or utility at the opposite top region;
3. main proposition/content through the central field;
4. primary action near the concluding focal region.

Do not place controls in strange locations solely to trace a literal Z.

## Hero sections

For a hero:

- establish context quickly;
- use one main heading;
- keep supporting copy close;
- place the primary action close to its explanation;
- use imagery that supports rather than competes with the message.

If the supporting image is visually stronger than the heading, ensure that this is intentional.

## Lists and search results

Users often scan the leading parts of repeated items.

Place distinguishing information early.

Example result anatomy:

Title
Short context/snippet
Metadata/status
Relevant action

Avoid repeated boilerplate prefixes that push unique terms later.

## Tables

Table scanning is not an F-pattern problem.

Users compare columns and rows based on the task.

Support comparison through:

- stable columns;
- meaningful headers;
- consistent numeric alignment;
- visible row identity;
- restrained status styling;
- predictable actions.

## Forms

Users scan forms for labels and expected inputs.

Use:

- consistent label placement;
- clear section headings;
- visible required/optional conventions;
- compact label-field relationships;
- errors adjacent to fields;
- primary action at the end of the relevant task flow.

Do not scatter field instructions across the opposite side of the page.

## Reading patterns and visual hierarchy

Size, color, contrast, imagery, and motion can override natural text scanning.

A huge illustration may become the starting point even when the headline appears first in DOM order.

Use visual dominance intentionally.

## Reading patterns and spatial hierarchy

Spacing can either preserve or break the scan path.

Heading and paragraph should appear as one unit.

Primary action and explanation should appear related.

A large unexplained gap can make users interpret content as belonging to different sections.

## Reading patterns and information architecture

Good scanning cannot repair poor IA.

If users are searching for “Billing” but the destination is labeled “Workspace Operations,” no visual pattern will create sufficient information scent.

Structure and labels come first.

## RTL and localization

Do not hard-code left-biased assumptions.

Reading direction can reverse.

Translations can increase text length, changing line breaks and visual balance.

Use logical leading/trailing alignment and test translated layouts.

## Mobile scanning

Mobile screens narrow the attention field and increase vertical travel.

Keep:

- headings close to content;
- key actions close to context;
- related comparison items near each other;
- important labels early in text;
- sticky UI from obscuring headings or focus.

Do not assume desktop side-by-side relationships remain obvious after stacking.

## Accessibility

- Use semantic headings in logical order.
- Ensure link text explains destination or action in context.
- Maintain meaningful sequence at zoom and reflow.
- Do not encode importance only through visual styling.
- Preserve readable text when spacing or font size changes.

## Failure modes

### Designing a literal F

Fix: structure content for scanning rather than drawing an eye path.

### Designing a literal Z

Fix: use Z-flow only as a loose composition model for simple pages.

### Wall of text

Fix: create layer-cake scanning through descriptive headings.

### Highlight soup

Fix: reduce bold/color/link emphasis to genuinely useful anchors.

### Important words appear late

Fix: front-load distinguishing terms.

### Desktop-only scan logic

Fix: reassess relationships after responsive stacking.

## Evaluation checklist

- Can users understand the page from headings alone?
- Are distinguishing words front-loaded?
- Are important actions close to motivating information?
- Does the design support several possible scan strategies?
- Is any element accidentally hijacking attention?
- Does the layout work for RTL and mobile?
- Does the semantic reading order match the intended information sequence?

## Source foundations

This skill synthesizes Nielsen Norman Group eyetracking research on F-shaped, layer-cake, spotted, and commitment scanning; Apple layout guidance on reading order; Fluent typography guidance; and WCAG requirements for headings, labels, meaningful sequence, and link purpose.

References:

- https://www.nngroup.com/articles/text-scanning-patterns-eyetracking/
- https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/
- https://developer.apple.com/design/human-interface-guidelines/layout
- https://fluent2.microsoft.design/typography
- https://www.w3.org/WAI/WCAG22/Understanding/
