# Focus and Attention Mapping

Use this skill to predict where attention is likely to go, decide where attention should go, and remove visual competition that prevents users from seeing the next useful thing.

Attention mapping is not a literal eye-tracking simulation. It is a design method for reasoning about visual priority from hierarchy, task, layout, content, contrast, motion, and learned patterns.

## Core objective

Create a deliberate attention path:

context → important information → decision → action

The page should not demand equal attention everywhere.

## Start from the task

Before styling, define:

- What is the user trying to accomplish?
- What must they notice before acting?
- What is the primary object?
- What is the main action?
- What information is supporting context?
- What can remain peripheral until needed?

Attention hierarchy should follow task hierarchy.

## Attention drivers

Elements can attract attention through:

- size;
- high contrast;
- saturated color;
- position;
- surrounding whitespace;
- faces or recognizable imagery;
- motion;
- unusual shape;
- bold/heavy type;
- novelty;
- selection or focus state.

Every attention cue has a cost. If many cues compete, users must perform more filtering.

## Primary focal point

Most screens benefit from one dominant focal region.

Examples:

- editor: the document/canvas;
- dashboard: the most relevant summary or task area;
- checkout: the current step and action;
- settings: the selected settings group;
- landing page: the main proposition and primary CTA.

Do not create three “primary” focal points using equally saturated buttons, giant headings, and strong imagery.

## Attention budget

Treat strong visual emphasis as limited.

A useful rule:

- one dominant emphasis;
- a few secondary anchors;
- most UI remains neutral.

The fewer elements that shout, the easier it is for important elements to be noticed.

## Reduce competitors before amplifying the target

When something is hard to notice, do not immediately make it larger, bolder, brighter, and more colorful.

First inspect:

- nearby buttons;
- saturated icons;
- unnecessary badges;
- repeated cards;
- high-contrast borders;
- decorative imagery;
- oversized headings;
- motion.

Often the correct fix is to quiet competing elements.

## Reading order

Apple notes that people often begin in natural reading order, generally from top/leading toward bottom/trailing depending on language direction.

Place high-priority orientation information where users are likely to encounter it early.

Do not assume this pattern overrides every other cue; strong imagery, motion, or contrast can pull attention elsewhere.

## Scanning behavior

Nielsen Norman Group research shows multiple scanning patterns, including F-pattern, spotted, layer-cake, and commitment patterns.

Use strong headings and recognizable anchors to encourage efficient scanning rather than forcing users through undifferentiated text.

Do not design a literal F or Z shape and assume eyes will follow it.

## Visual entry points

Give users obvious places to begin:

- page title;
- current object name;
- selected navigation item;
- primary metric;
- hero message;
- form heading;
- active step.

Avoid starting a screen with several similarly weighted labels and controls.

## Action attention

Primary actions should be visible near the information that motivates them.

Context → value/state → action

Do not isolate the CTA so far from its explanation that the relationship becomes unclear.

Do not use a sticky primary action if it constantly steals attention from the content needed to make the decision.

## Error and warning attention

Errors require enough salience to be discovered quickly.

Place messages near the source of the problem.

For forms:

- identify the field;
- describe the problem;
- preserve entered data;
- move or announce focus appropriately when submission fails.

Do not rely on a distant toast as the only indication that an input failed.

## Motion

Motion is a powerful attention magnet.

Use it for:

- state changes;
- transitions that preserve spatial understanding;
- progress;
- meaningful feedback;
- temporary attention when required.

Avoid continuous animation in peripheral areas.

Respect reduced-motion preferences.

Do not use rapid flashing.

## Images and generated assets

A strong image can overpower typography and actions.

Evaluate:

- contrast;
- saturation;
- subject placement;
- gaze or object direction;
- background detail;
- visual mass;
- relationship to CTA.

Generated assets should reinforce the intended focal path rather than become the focal point by accident.

## Navigation attention

Persistent navigation should remain discoverable without dominating the work area.

Selected state requires stronger emphasis than unselected states.

Do not use saturated icons for every navigation item if only one is active.

## Focus versus visual attention

Keyboard focus is not the same as visual hierarchy.

A keyboard user needs an unmistakable focus indicator even when the focused element is visually secondary.

Never remove focus outlines without replacing them with an accessible alternative.

WCAG 2.2 includes focus visibility, focus-not-obscured, and focus-appearance criteria.

## Temporary UI and focus restoration

When dialogs, menus, popovers, or sheets open:

- send focus to an appropriate element;
- keep focus within modal contexts when required;
- restore focus to the invoking control after dismissal;
- prevent sticky UI from obscuring focus.

Fluent explicitly calls out focus management as a core accessibility practice.

## Responsive attention

The focal hierarchy should survive layout changes.

On mobile:

- content may stack;
- the image may move below text;
- secondary actions may enter overflow;
- the primary action may need to remain near its context.

Do not let DOM reordering accidentally place tertiary content before the main task.

## Failure modes

### Everything competes

Too many filled buttons, badges, colors, and cards.

Fix: reduce emphasis levels.

### Main action is visually loud but contextless

Fix: place it near the information that explains why it matters.

### Motion steals attention

Fix: remove continuous decorative animation.

### Important status is outside the attention field

Fix: move it near the object/action it affects.

### Focus indicator is subtle

Fix: make keyboard focus clearly visible against adjacent colors.

## Evaluation checklist

Perform a blur test or squint test and ask:

- What is noticed first?
- What is noticed second?
- Is that order useful for the task?
- Are there accidental hotspots?
- Does the main action compete with other actions?
- Can warnings/errors be found immediately?
- Is keyboard focus obvious and unobscured?
- Does the attention order still work on mobile and at zoom?
- Does motion have a functional reason?

## Source foundations

This skill synthesizes Apple layout guidance, Nielsen Norman Group eyetracking/scanning research, Fluent accessibility guidance on focus, WCAG 2.2 focus and motion requirements, and established hierarchy/spacing principles from Carbon and Fluent.

References:

- https://developer.apple.com/design/human-interface-guidelines/layout
- https://www.nngroup.com/articles/text-scanning-patterns-eyetracking/
- https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/
- https://fluent2.microsoft.design/accessibility
- https://www.w3.org/WAI/WCAG22/Understanding/
- https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview
