# Interface Quality Gate

Use this skill as the final review pass after an interface has been designed or implemented.

This is not another style guide. It is an enforcement layer that checks whether hierarchy, usability, art direction, typography, spacing, color, components, accessibility, responsiveness, and anti-slop rules form one coherent product.

## Core objective

Reject interfaces that are merely functional or superficially polished.

A production-quality interface must be:

- understandable;
- usable;
- visually coherent;
- product-specific;
- accessible;
- responsive;
- truthful;
- consistent under real states;
- maintainable as a system.

Do not pass a design because the hero screenshot looks good.

## Pass / fail model

A review should produce one of three outcomes:

### PASS

No critical problems remain. The system is coherent and the design can scale beyond the current screenshot.

### PASS WITH FIXES

The core system is strong but specific non-critical issues should be corrected before shipping.

### FAIL

One or more critical issues undermine usability, accessibility, truthfulness, hierarchy, or system coherence.

Do not soften a fail into vague feedback such as `could be improved`.

## Critical fail conditions

Fail the design immediately when any of these are present:

- fabricated testimonials, logos, usage numbers, ratings, uptime, activity, or other proof presented as real;
- inaccessible critical text or controls;
- missing keyboard access for core functionality on keyboard-relevant platforms;
- destructive action with no reasonable prevention or recovery when consequences are serious;
- primary navigation that makes the product's structure unintelligible;
- status communicated only through inaccessible color distinctions where the meaning is important;
- interaction state that hides whether an action succeeded or failed;
- mobile layout that prevents completion of the primary task;
- visual styling that makes standard controls ambiguous or misleading;
- user input being discarded unnecessarily after validation/error;
- fake live indicators or fake urgency used to manipulate attention.

## Review order

Always review in this order because later visual polish cannot rescue earlier structural failures.

1. truth;
2. task and user flow;
3. information architecture;
4. hierarchy;
5. accessibility;
6. layout and spacing;
7. typography;
8. color;
9. components and states;
10. art direction and personality;
11. responsiveness;
12. motion and feedback;
13. anti-slop cleanup;
14. consistency across screens.

## 1. Truth audit

Check all visible claims and simulated content.

Ask:

- Is this real product data?
- Is this clearly labeled demo/sample content?
- Are testimonials real?
- Are company logos authorized and real?
- Are metrics measured?
- Is `live`, `online`, `secure`, `verified`, or similar status actually backed by product state?

Remove decorative fake proof.

Do not approve a visually polished lie.

## 2. Task audit

For the screen being reviewed, state the main user goal in one sentence.

Then verify:

- entry point is understandable;
- primary action is visible;
- unnecessary decisions are removed or deferred;
- progress/feedback exists;
- error and recovery paths exist;
- cancellation/back behavior is reasonable;
- friction matches consequence.

If the reviewer cannot state the main task, the screen likely lacks focus.

## 3. Information architecture audit

Check:

- destinations are grouped by user mental model;
- actions are not mixed randomly with destinations;
- labels use concrete language;
- nested levels make sense;
- users can tell where they are;
- high-frequency destinations are easy to reach;
- rare administration does not dominate primary navigation.

Reject `More`, `Magic`, `Explore`, or similarly vague labels when a concrete label would provide better information scent.

## 4. Hierarchy audit

Identify what the eye should notice first, second, and third.

If this cannot be answered consistently, revise.

Check:

- one dominant screen purpose;
- clear primary action;
- supporting content visibly secondary;
- metadata visibly tertiary;
- color does not outrank more important content accidentally;
- large type is earned by importance;
- strong contrast is reserved for meaningful elements.

Use fewer emphasis techniques before adding more.

## 5. Accessibility audit

Check at minimum:

- text contrast;
- non-text control contrast where applicable;
- visible keyboard focus;
- logical focus order;
- keyboard operation;
- target size/spacing;
- zoom/reflow;
- labels and instructions;
- error identification;
- non-color state cues;
- reduced motion behavior where relevant;
- semantic structure.

Treat accessibility as a design constraint, not a cleanup stage.

## 6. Layout and spacing audit

Inspect the page without focusing on colors or decoration.

Check:

- strong alignment anchors;
- coherent grid;
- consistent outer margins;
- consistent gutters;
- related items use tighter proximity;
- unrelated sections have stronger separation;
- internal padding follows a system;
- whitespace communicates structure;
- large empty areas have a compositional reason;
- containers are not being used where spacing alone would work.

Look for accidental one-off values.

If 14px, 17px, 19px, 23px, 27px, and 31px gaps appear with no reason, normalize the system.

## 7. Typography audit

Check:

- a small semantic role system exists;
- sizes are not arbitrary;
- weights are not all heavy;
- line-height suits text size and use;
- body copy has comfortable measure;
- labels remain readable;
- secondary text is not excessively faint;
- numerals align appropriately in tables/data;
- font choice matches product character and license constraints;
- productive UI does not accidentally use giant marketing typography everywhere.

Reject hierarchy that depends only on boldness.

## 8. Color audit

Check:

- neutral scale is coherent;
- accent color has a clear role;
- semantic colors are consistent;
- large surfaces are not unnecessarily saturated;
- brand color is not sprayed across the interface;
- dark mode is intentionally designed rather than inverted;
- colors preserve meaning in real context;
- contrast is adequate;
- critical distinctions do not rely on color alone.

Remove colors that have no role.

## 9. Component audit

For each interactive component, inspect:

- default;
- hover where relevant;
- pressed/active;
- focus;
- selected;
- disabled;
- loading;
- error;
- empty if applicable.

Check component anatomy:

- label alignment;
- icon size;
- icon/text gap;
- padding;
- height;
- border;
- radius;
- state transition.

Do not approve a component based only on its default state.

## 10. Art-direction audit

Hide the logo mentally or literally.

Ask:

- Does this still feel like a specific product?
- Can its character be described with precise words?
- Are 1-3 signature ideas visible?
- Do type, density, shape, color, imagery, and motion support the same character?
- Is personality coming from a system rather than decorative filler?

If the answer is no, use `visual-art-direction.md`.

If the design only becomes recognizable through generic gradient/glass/card patterns, fail the identity review.

## 11. Responsive audit

Test at representative widths rather than one desktop frame.

Check:

- layout recomposes rather than merely shrinks;
- navigation adapts appropriately;
- important actions remain reachable;
- text measure remains sensible;
- tables and dense data have an adaptation strategy;
- dialogs fit small viewports;
- touch targets remain operable;
- keyboard and virtual keyboard do not block critical controls;
- orientation/context is preserved.

## 12. Motion and feedback audit

Check:

- motion has a purpose;
- timing matches task character;
- hover motion is restrained;
- loading state accurately represents activity;
- success/failure feedback is visible;
- animation does not hide delays;
- reduced-motion preferences are respected where relevant.

Reject decorative motion that competes with the primary task.

## 13. Anti-slop audit

Run `anti-ai-slop.md` explicitly.

Search for:

- decorative hero pills;
- blinking green dots;
- generic gradient text;
- purple/blue AI gradients;
- unnecessary glassmorphism;
- random glows;
- fake floating product cards;
- excessive pills;
- giant radii;
- card soup;
- giant padding;
- fake proof;
- generic startup copy;
- equal-weight feature grids;
- random icon tiles;
- decorative terminal windows;
- unnecessary bento layouts.

Each surviving expressive pattern must have a reason.

## 14. Cross-screen consistency audit

A design system is proven across different states and screen types.

Compare at least:

- dense screen;
- simple screen;
- settings/form screen;
- empty state;
- error state;
- modal/dialog;
- mobile layout if applicable.

Check whether the same:

- spacing logic;
- type roles;
- color roles;
- radii;
- icon family;
- control behavior;
- tone;
- motion language

survive across all of them.

Do not approve a system that only works for the hero or dashboard.

## Severity levels

### Critical

Blocks completion, accessibility, truth, safety, or comprehension.

Must fix.

### Major

Damages hierarchy, navigation, consistency, responsiveness, or product identity.

Should fix before shipping.

### Minor

Polish issue that does not significantly impair use.

Fix when practical.

Do not mark systematic spacing or typography problems as minor just because each individual mismatch is small.

## Numeric consistency check

Look for uncontrolled values in:

- spacing;
- radii;
- font sizes;
- line heights;
- control heights;
- icon sizes;
- border widths;
- shadow recipes;
- motion durations.

A design does not need one universal scale, but repeated values should come from deliberate systems.

## Screenshot test

At a glance, verify:

- focal point appears quickly;
- primary action is identifiable;
- page does not look equally loud everywhere;
- section boundaries are understandable;
- text does not look like a wall;
- accent color appears intentional;
- no decorative pattern dominates without meaning.

## Grayscale test

Temporarily remove color mentally or in tooling.

The interface should retain meaningful hierarchy through:

- scale;
- spacing;
- typography;
- alignment;
- shape;
- luminance.

If hierarchy collapses without hue, the design may depend too heavily on color.

## Blur test

Blur or squint at the interface.

Large visual masses should still reveal:

- primary focal area;
- major grouping;
- navigation region;
- content region;
- major action emphasis.

This is a heuristic, not an accessibility test.

## Content stress test

Replace ideal content with:

- long names;
- long translations;
- zero data;
- very large data;
- errors;
- multiple notifications;
- long table values;
- wrapped labels.

A strong system should degrade gracefully.

## Final scorecard

Score each category 0-2:

- truth;
- flow;
- IA;
- hierarchy;
- accessibility;
- spacing/layout;
- typography;
- color;
- components/states;
- art direction;
- responsiveness;
- motion/feedback;
- anti-slop restraint;
- cross-screen consistency.

`0` = failing
`1` = acceptable but weak/incomplete
`2` = strong

Maximum: 28.

Suggested interpretation:

- 25-28: strong pass;
- 21-24: pass with targeted fixes;
- 16-20: substantial revision required;
- below 16: redesign the system rather than polishing symptoms.

A critical fail condition overrides the numeric score.

## Required review output

When an AI uses this skill, return findings in this order:

1. verdict: PASS / PASS WITH FIXES / FAIL;
2. top 3 issues by severity;
3. exact reason each issue matters;
4. concrete correction;
5. systems affected;
6. final short scorecard.

Do not return vague comments like `make it cleaner`, `add more personality`, or `improve spacing` without identifying the specific relationship and correction.

## Companion skills

This gate is strongest when the relevant underlying skills are available:

- `anti-ai-slop.md`;
- `visual-art-direction.md`;
- `user-flow-and-navigation.md`;
- `visual-hierarchy.md`;
- `information-architecture.md`;
- `typographic-hierarchy.md`;
- `spatial-hierarchy-prospacing.md`;
- `alignment-and-grid-structures.md`;
- `color-theory-and-palette.md`;
- `component-craft.md`;
- `accessibility-and-interaction.md`;
- `responsive-adaptation.md`;
- `motion-and-feedback.md`.

## Source foundations

This quality gate combines the repository's source-backed skills. Primary foundations include:

- Apple Human Interface Guidelines
  - https://developer.apple.com/design/human-interface-guidelines/
- Material Design 3
  - https://m3.material.io/
- IBM Carbon Design System
  - https://www.carbondesignsystem.com/
- Atlassian Design System
  - https://atlassian.design/
- W3C WCAG 2.2
  - https://www.w3.org/WAI/WCAG22/Understanding/
