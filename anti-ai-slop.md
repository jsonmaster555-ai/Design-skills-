# Anti-AI-Slop UI Enforcement

Use this skill whenever generating, reviewing, or refining a UI where the result must feel intentionally art-directed rather than like a generic AI-generated SaaS template.

This is an enforcement skill, not a mood board. It should actively reject weak defaults, remove decorative filler, and force every visual choice to have a product-specific reason.

## Core rule

If removing the logo would make the interface indistinguishable from hundreds of unrelated AI startups, the design does not have enough identity.

A UI is not improved by adding more fashionable patterns. It is improved by making fewer, stronger, better-justified decisions.

## Mandatory behavior

Before adding any decorative or expressive element, answer:

1. What product-specific purpose does it serve?
2. Does it improve hierarchy, comprehension, state, navigation, trust, or brand recognition?
3. Is there a simpler mechanism that communicates the same thing?
4. Is this pattern being used because the product needs it or because it is a common generated-UI default?
5. Would the design become clearer if the element were removed?

If the answer to 2 is no and the answer to 5 is yes, remove it.

## Hard blacklist

Reject these unless the user explicitly requests them, they already belong to the established brand, or they are functionally necessary:

- fabricated social proof, user counts, ratings, logos, testimonials, or uptime claims;
- fake live-status indicators;
- fake notifications, fake activity feeds, fake command output, or fake product data used only as decoration;
- decorative pulsing green dots with no real live state;
- decorative `AI powered`, `Now live`, `New`, or `Available now` hero pills with no information value;
- random purple/blue gradient identity used as a default for AI products;
- sparkles used as a default symbol for AI or intelligence;
- card-inside-card-inside-card structure with no real hierarchy;
- unreadable low-contrast gray used to imitate minimalism;
- controls whose visual styling hides or weakens their actual function.

## Restricted patterns

The following are not banned, but require a specific justification tied to brand, hierarchy, behavior, accessibility, or supplied reference:

- glassmorphism;
- gradients;
- large blur fields;
- bento grids;
- pill-shaped controls;
- extra-large radii;
- floating UI fragments;
- 3D objects;
- decorative noise or grid backgrounds;
- glow effects;
- large hero dashboards;
- excessive dark-mode neon accents;
- oversized type;
- animated status indicators;
- asymmetrical layouts;
- unusual navigation patterns.

If the justification is only “it looks modern,” do not use it.

## The 100 rules

### Decorative restraint

1. Never add a blinking green dot unless something is actually live.
2. Never add a hero pill merely because the hero feels empty.
3. Avoid generic `Now available` badges unless they carry useful release information.
4. Avoid `AI powered` badges unless AI itself is important to the user's decision.
5. Do not use sparkles as the automatic visual shorthand for AI.
6. Do not use gradient text by default.
7. Do not use purple-blue gradients as a substitute for brand identity.
8. Do not place a giant blurred glow behind every hero.
9. Do not add floating glass cards only to make a composition feel busier.
10. Do not fabricate floating UI fragments the real product does not contain.
11. Do not make every button pill-shaped.
12. Do not make every label a pill.
13. Do not use 24-32px radii everywhere without a shape-system reason.
14. Do not round every container to the same exaggerated degree.
15. Avoid card-inside-card-inside-card structure.
16. Do not place every section inside a bordered rectangle.
17. Use whitespace and alignment before adding another container.
18. Do not add shadows unless elevation or layering needs to be communicated.
19. Do not give every card a shadow.
20. Avoid giant diffuse SaaS shadows by default.
21. Do not use glassmorphism without a product-specific reason.
22. Avoid translucent panels over random gradients.
23. Do not blur backgrounds merely because backdrop blur is available.
24. Do not use a bento grid when a simpler layout communicates the content better.
25. Do not force every feature section into three equal cards.

### Components and iconography

26. Avoid the generic icon + heading + paragraph feature-card formula unless the content genuinely fits it.
27. Do not use a pile of unrelated library icons to manufacture personality.
28. Do not mix icon families without a deliberate contrast strategy.
29. Do not add decorative icons where typography already communicates the idea.
30. Do not make icons visually louder than the information they support.
31. Do not turn ordinary labels into badges simply to add color.
32. Do not turn every metadata value into a chip.
33. Do not use badges as decoration when plain text would scan better.
34. Do not use giant icon tiles as filler.
35. Do not make ordinary controls look like promotional objects.

### Copy and messaging

36. Avoid generic copy such as `Supercharge your workflow`.
37. Avoid `Built for modern teams` unless followed by concrete meaning.
38. Avoid `Move faster` as a standalone value proposition.
39. Avoid `Unlock your potential` and similar empty claims.
40. Avoid `The future of...` unless the statement is genuinely defensible.
41. Avoid `Everything you need in one place` unless the scope is actually explained.
42. Avoid adjective piles such as `Powerful. Simple. Fast.` without evidence.
43. Write what the product actually does using concrete verbs and nouns.
44. Prefer specific outcomes over vague emotional promises.
45. Remove words that add hype but no information.

### Truth and proof

46. Do not invent metrics.
47. Do not add `10,000+ users` unless it is real and verified.
48. Do not add `99.99% uptime` unless it is measured and appropriate to surface.
49. Do not create fake testimonial people.
50. Do not use random stock headshots as fabricated social proof.
51. Do not fabricate customer or partner logos.
52. Do not add a `Trusted by` strip without real organizations.
53. Do not use meaningless five-star graphics.
54. Do not create fake activity feeds to make screenshots feel alive.
55. Do not fabricate notifications, transactions, messages, or analytics only to fill space.

### Layout and composition

56. Do not center every section by default.
57. Avoid repeating centered heading + centered paragraph + centered buttons across the whole page.
58. Use asymmetry only when it creates stronger hierarchy or composition.
59. Create deliberate alignment lines and preserve them across sections.
60. Do not randomly offset elements to simulate visual interest.
61. Use a real grid or coherent alignment system.
62. Keep gutters and margins consistent unless a deliberate break creates emphasis.
63. Keep text measure intentional; do not stretch paragraphs across the viewport.
64. Do not make every section the same height or composition.
65. Do not use huge vertical padding as a substitute for hierarchy.
66. Do not use excessive empty space merely to imitate luxury branding.
67. Do not make dense software unnecessarily spacious.
68. Match density to task frequency, information volume, and target device.
69. Do not make every dashboard behave visually like a marketing page.
70. Do not make every marketing page imitate the same popular productivity app.

### Typography

71. Do not choose Inter automatically for every project.
72. Choose type based on product character, readability, platform, and licensing needs.
73. Do not invent seven or more arbitrary font sizes when a smaller type system works.
74. Do not make every heading 700 weight.
75. Do not use bold text as the only hierarchy mechanism.
76. Use size, weight, spacing, color, measure, and position together.
77. Keep body text comfortably readable at realistic viewport sizes.
78. Do not shrink secondary text until it becomes difficult to read.
79. Do not use extremely faint gray just to look minimal.
80. Do not make all secondary text the same generic gray regardless of role.

### Color

81. Do not use low contrast as a styling technique.
82. Do not use five accent colors with equal visual importance.
83. Assign colors semantic or brand roles.
84. Establish one dominant accent before adding secondary accents.
85. Do not flood the interface with the brand color.
86. Do not use neon colors on large surfaces unless the product identity truly calls for it.
87. Do not use gradients to rescue weak composition.
88. Do not use red or green as the only cue for state.
89. Do not use status colors decoratively when those colors already carry meaning.
90. Do not create a rainbow dashboard when a neutral context would make the important data clearer.

### Motion and behavior

91. Do not use animation to compensate for weak design.
92. Do not animate every hover.
93. Avoid bouncing buttons unless playfulness is an intentional brand behavior.
94. Avoid dramatic card lift on ordinary hover states.
95. Avoid glowing borders on normal controls.
96. Keep motion restrained unless expressive motion is part of the product language.
97. Do not invent experimental controls when familiar controls already solve the problem.
98. Give the product one or two memorable visual ideas instead of twenty competing tricks.
99. Make every decorative element justify its existence.
100. If removing an element makes the interface clearer, more recognizable, or more usable, remove it.

## Exception protocol

A restricted or blacklisted pattern may be used only when at least one of these is true:

- the user explicitly requests it;
- it exists in the supplied reference or established design system;
- it communicates real state or behavior;
- it is essential to the brand language;
- usability testing or product context supports it;
- removing it would reduce comprehension or recognition.

When an exception is used, preserve the underlying reason. Do not let one justified exception become permission to repeat the pattern everywhere.

## Anti-slop review procedure

Review the interface in this order:

1. **Truth** — remove fake proof, fake data, fake status, and fake urgency.
2. **Structure** — remove unnecessary containers and duplicated grouping.
3. **Hierarchy** — ensure there is a clear reading order and action priority.
4. **Typography** — eliminate arbitrary sizes, excessive boldness, and weak text contrast.
5. **Color** — reduce competing accents and restore semantic roles.
6. **Geometry** — normalize radii, borders, shadows, and control shapes.
7. **Decoration** — remove gradients, glows, floating fragments, and effects that have no job.
8. **Identity** — add one or two product-specific visual decisions if the result is now too generic.
9. **Interaction** — verify states, focus, hover, loading, error, empty, and disabled behavior.
10. **Final test** — hide the logo and ask whether the product still has recognizable character.

## Output requirements for AI-generated UI

When this skill is active:

- prefer real product content over placeholder marketing fluff;
- prefer layout, type, spacing, imagery, and product-specific details over decoration;
- explain unusual visual choices through the product's identity or function;
- use the least visually heavy solution that still communicates the relationship;
- reject generic embellishments when the user did not ask for them;
- preserve accessibility and familiar interaction behavior while creating visual personality.

## Source foundations

This skill synthesizes anti-pattern detection with principles from Apple Human Interface Guidelines, Material Design 3, IBM Carbon, Microsoft Fluent, Shopify Polaris, Nielsen Norman Group usability research, and WCAG 2.2.

References:

- https://developer.apple.com/design/human-interface-guidelines/
- https://m3.material.io/
- https://carbondesignsystem.com/
- https://fluent2.microsoft.design/
- https://polaris.shopify.com/
- https://www.nngroup.com/articles/aesthetic-usability-effect/
- https://www.w3.org/WAI/WCAG22/Understanding/
