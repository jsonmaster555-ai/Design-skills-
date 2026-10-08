# Design Orchestrator

Use this skill as the single entry point for the entire Design Skills repository.

This is the master controller. Its job is to inspect the design task, load the relevant specialist skills, apply them in the correct order, resolve conflicts between them, and run the final quality gate before returning a design, implementation, critique, or design-system decision.

If an agent is allowed to load only one file from this repository first, load this file.

## Core directive

Do not design from generic visual instinct alone.

Route every meaningful UI task through the repository's specialist skills.

The orchestrator must:

1. understand the product and task;
2. identify which design systems are relevant;
3. load the required skills;
4. establish structural rules before visual decoration;
5. establish art direction before polishing components;
6. enforce anti-AI-slop rules throughout;
7. validate accessibility and responsive behavior;
8. run the final quality gate;
9. revise failed areas before returning the result.

The orchestrator coordinates the skills. It does not replace them.

---

# Skill registry

The repository currently contains the following specialist skills.

## Structure, hierarchy, and flow

### `visual-hierarchy.md`
Use for:

- reading order;
- focal priority;
- primary/secondary/tertiary emphasis;
- action hierarchy;
- visual dominance;
- density hierarchy.

### `information-architecture.md`
Use for:

- product structure;
- navigation categories;
- taxonomy;
- information scent;
- labels;
- object hierarchy;
- wayfinding.

### `user-flow-and-navigation.md`
Use for:

- task flows;
- navigation paths;
- onboarding;
- checkout;
- multi-step processes;
- feedback and recovery;
- user agency;
- friction;
- keyboard/focus flow.

### `progressive-disclosure.md`
Use for:

- advanced settings;
- complex forms;
- staged configuration;
- hiding low-frequency complexity;
- deciding what is visible now vs later.

### `content-chunking.md`
Use for:

- breaking information into understandable groups;
- forms;
- dashboards;
- settings;
- documentation-like screens;
- reducing walls of content.

### `functional-grouping.md`
Use for:

- grouping controls by task;
- grouping data by meaning;
- Gestalt relationships;
- separating unrelated actions;
- deciding whether controls belong together.

### `nested-structural-layouts.md`
Use for:

- app shells;
- workspace → page → panel hierarchy;
- nested navigation;
- nested content regions;
- preventing card-inside-card layouts.

---

# Space, alignment, scale, and attention

### `spatial-hierarchy-prospacing.md`
Use for:

- spacing scales;
- internal vs external spacing;
- component density;
- layout rhythm;
- optical spacing corrections.

### `proximity-and-whitespace-distribution.md`
Use for:

- deciding what belongs together;
- section spacing;
- whitespace balance;
- dense vs spacious layouts;
- reducing unnecessary dividers and cards.

### `alignment-and-grid-structures.md`
Use for:

- columns;
- gutters;
- page margins;
- key alignment lines;
- grids;
- baseline relationships;
- cross-screen alignment consistency.

### `contrast-and-scale.md`
Use for:

- visual emphasis;
- size relationships;
- luminance differences;
- target sizing;
- restrained prominence;
- preventing everything from becoming large and loud.

### `focus-and-attention-mapping.md`
Use for:

- focal points;
- attention competition;
- motion salience;
- error prominence;
- imagery dominance;
- keyboard focus visibility.

### `scannability-fields.md`
Use for:

- tables;
- dashboards;
- long forms;
- lists;
- navigation;
- search results;
- repeated content structures.

### `reading-patterns.md`
Use for:

- content-heavy pages;
- landing pages;
- marketing layouts;
- dashboards;
- scanning behavior;
- F-pattern, layer-cake, spotted, and Z-flow reasoning.

---

# Color

### `color-theory-and-palette.md`
Use for:

- choosing hues;
- saturation/chroma;
- lightness/value;
- palette generation;
- monochromatic/analogous/complementary relationships;
- semantic color roles;
- dark mode;
- accessibility;
- palette refinement.

### `color-weight-and-dominance.md`
Use for:

- deciding how much color to use;
- accent dominance;
- brand-color restraint;
- semantic state colors;
- surfaces;
- charts and data;
- dark/light theme balance.

---

# Typography and language

### `typographic-hierarchy.md`
Use for:

- type scales;
- font selection;
- display/body roles;
- weights;
- line height;
- tracking;
- numeric typography;
- localization;
- open-source font guidance.

### `content-design-and-labeling.md`
Use for:

- button labels;
- navigation labels;
- headings;
- errors;
- empty states;
- helper copy;
- plain language;
- tone;
- localization.

---

# Components and system construction

### `component-craft.md`
Use for:

- buttons;
- inputs;
- selects;
- checkboxes;
- switches;
- badges;
- menus;
- tabs;
- sidebars;
- tables;
- dialogs;
- popovers;
- states;
- micro-details.

### `design-tokens-and-theming.md`
Use for:

- design tokens;
- semantic variables;
- spacing tokens;
- color tokens;
- component tokens;
- dark mode;
- high-contrast mode;
- designer/developer parity.

### `responsive-adaptation.md`
Use for:

- breakpoints;
- reflow;
- mobile adaptation;
- responsive tables;
- navigation transformations;
- touch layouts;
- zoom;
- localization stress.

### `accessibility-and-interaction.md`
Use for:

- keyboard behavior;
- focus;
- target size;
- contrast;
- reflow;
- semantic structure;
- form errors;
- status messages;
- reduced motion;
- high-contrast behavior.

### `motion-and-feedback.md`
Use for:

- hover/press transitions;
- loading;
- skeletons;
- progress;
- optimistic UI;
- state transitions;
- drag feedback;
- AI activity indicators;
- reduced motion.

---

# Personality, art direction, and visual quality

### `visual-art-direction.md`
Use for:

- visual personality;
- product character;
- art direction;
- density character;
- geometry;
- shape language;
- imagery direction;
- signature visual decisions;
- making the interface recognizable without relying on decoration.

### `anti-ai-slop.md`
Use for:

- rejecting generic generated-UI patterns;
- excessive pills;
- fake green status dots;
- gradient-text defaults;
- random glows;
- card soup;
- fake metrics;
- fake testimonials;
- generic startup copy;
- trend imitation;
- unnecessary bento grids;
- template-like heroes.

This skill contains 100 explicit anti-slop rules and should be active for every new interface unless the user explicitly requests an intentionally trend-heavy style.

### `ui-asset-generation.md`
Use for:

- illustrations;
- 3D objects;
- custom icons;
- product visuals;
- empty-state art;
- AI indicators;
- coherent asset families;
- raster/vector decisions.

### `interface-quality-gate.md`
Use as the mandatory final review.

It checks:

- truth;
- user flow;
- IA;
- hierarchy;
- accessibility;
- spacing;
- typography;
- color;
- components;
- art direction;
- responsiveness;
- motion;
- anti-slop restraint;
- cross-screen consistency.

---

# Default orchestration sequence

For a full UI generation task, run the skills in this order.

## Phase 1 — Understand

Read the request and establish:

- product type;
- audience;
- platform;
- primary task;
- secondary tasks;
- expected content density;
- brand/reference constraints;
- accessibility constraints;
- responsive targets;
- implementation environment if supplied.

Do not invent missing product facts unless necessary to make progress. When assumptions are required, make conservative assumptions that preserve flexibility.

## Phase 2 — Structure

Load:

1. `information-architecture.md`
2. `user-flow-and-navigation.md`
3. `progressive-disclosure.md`
4. `functional-grouping.md`
5. `content-chunking.md`
6. `nested-structural-layouts.md`

Decide:

- screen purpose;
- navigation model;
- content groups;
- primary actions;
- object relationships;
- what must be visible immediately;
- what can be deferred;
- success/error/recovery states.

Do not begin decorative styling before this phase is coherent.

## Phase 3 — Hierarchy and composition

Load:

1. `visual-hierarchy.md`
2. `alignment-and-grid-structures.md`
3. `spatial-hierarchy-prospacing.md`
4. `proximity-and-whitespace-distribution.md`
5. `contrast-and-scale.md`
6. `focus-and-attention-mapping.md`
7. `scannability-fields.md`
8. `reading-patterns.md` when relevant.

Decide:

- first/second/third focal points;
- grid;
- margins;
- content widths;
- spacing rhythm;
- density;
- major alignment anchors;
- scan path;
- visual dominance.

The interface should already work in grayscale before expressive color is applied.

## Phase 4 — Art direction

Load:

1. `visual-art-direction.md`
2. `anti-ai-slop.md`

Define:

- 3-4 character words;
- density character;
- geometry character;
- typography personality;
- color intensity;
- imagery direction;
- motion character;
- 1-3 signature visual decisions.

Reject decorative ideas that do not support the product identity.

Do not copy the visual language of a fashionable product unless the user explicitly asks for it or the product context strongly supports similar conventions.

## Phase 5 — Typography and content

Load:

1. `typographic-hierarchy.md`
2. `content-design-and-labeling.md`

Set:

- font family/families;
- semantic type roles;
- type scale;
- line heights;
- text measure;
- label tone;
- heading tone;
- action labels;
- error language;
- empty-state language.

Avoid filler copy.

## Phase 6 — Color system

Load:

1. `color-theory-and-palette.md`
2. `color-weight-and-dominance.md`
3. `design-tokens-and-theming.md`

Set:

- neutral temperature;
- primary accent;
- accent scale;
- semantic success/warning/danger/info colors;
- background and surface roles;
- border roles;
- text roles;
- light/dark/high-contrast mapping where relevant.

Do not add colors without roles.

## Phase 7 — Components

Load:

1. `component-craft.md`
2. `design-tokens-and-theming.md`
3. `accessibility-and-interaction.md`

Define component anatomy and states.

For interactive components include applicable:

- default;
- hover;
- pressed;
- focused;
- selected;
- disabled;
- loading;
- error.

Do not judge components only in the default state.

## Phase 8 — Motion and assets

Load when relevant:

1. `motion-and-feedback.md`
2. `ui-asset-generation.md`

Motion must communicate state, causality, continuity, or brand character.

Assets must belong to one coherent visual family.

Do not generate decorative assets because a blank area feels empty.

## Phase 9 — Responsive adaptation

Load:

1. `responsive-adaptation.md`
2. `accessibility-and-interaction.md`
3. `user-flow-and-navigation.md`

Verify the task at:

- narrow mobile;
- typical mobile;
- tablet when relevant;
- desktop;
- wide desktop when relevant.

Do not simply stack desktop components vertically.

## Phase 10 — Anti-slop enforcement

Run `anti-ai-slop.md` again after the interface appears visually complete.

Remove or justify:

- decorative hero pills;
- blinking green dots;
- random gradients;
- glow fields;
- unnecessary bento grids;
- glassmorphism;
- giant radii;
- pill overload;
- floating UI fragments;
- fake social proof;
- generic marketing copy;
- random icon tiles;
- card soup;
- giant whitespace used as fake luxury;
- shadows without elevation meaning;
- animations without a job.

If the design becomes clearer after removing an element, remove it.

## Phase 11 — Final quality gate

Load `interface-quality-gate.md`.

Run the complete review.

If verdict is:

### PASS
Return the result.

### PASS WITH FIXES
Apply the important fixes before returning whenever possible.

### FAIL
Do not return the failed design as complete. Route each failure back to its specialist skill, revise, then run the gate again.

Example:

- weak hierarchy → `visual-hierarchy.md`;
- random spacing → `spatial-hierarchy-prospacing.md`;
- generic personality → `visual-art-direction.md`;
- excessive pills/glows → `anti-ai-slop.md`;
- confusing navigation → `information-architecture.md` + `user-flow-and-navigation.md`;
- weak palette → `color-theory-and-palette.md`;
- inaccessible focus → `accessibility-and-interaction.md`;
- poor mobile behavior → `responsive-adaptation.md`.

---

# Routing by task type

The orchestrator may use targeted mode when a full-system pass would add no value.

## Landing page / hero

Load at minimum:

- `visual-art-direction.md`;
- `visual-hierarchy.md`;
- `alignment-and-grid-structures.md`;
- `spatial-hierarchy-prospacing.md`;
- `typographic-hierarchy.md`;
- `color-theory-and-palette.md`;
- `focus-and-attention-mapping.md`;
- `reading-patterns.md`;
- `content-design-and-labeling.md`;
- `anti-ai-slop.md`;
- `responsive-adaptation.md`;
- `accessibility-and-interaction.md`;
- `interface-quality-gate.md`.

## Dashboard

Load at minimum:

- `information-architecture.md`;
- `visual-hierarchy.md`;
- `scannability-fields.md`;
- `alignment-and-grid-structures.md`;
- `spatial-hierarchy-prospacing.md`;
- `functional-grouping.md`;
- `component-craft.md`;
- `color-weight-and-dominance.md`;
- `typographic-hierarchy.md`;
- `accessibility-and-interaction.md`;
- `responsive-adaptation.md`;
- `anti-ai-slop.md`;
- `interface-quality-gate.md`.

## Settings / forms

Load at minimum:

- `information-architecture.md`;
- `functional-grouping.md`;
- `progressive-disclosure.md`;
- `content-chunking.md`;
- `user-flow-and-navigation.md`;
- `component-craft.md`;
- `content-design-and-labeling.md`;
- `accessibility-and-interaction.md`;
- `spatial-hierarchy-prospacing.md`;
- `interface-quality-gate.md`.

## Component library

Load at minimum:

- `component-craft.md`;
- `design-tokens-and-theming.md`;
- `typographic-hierarchy.md`;
- `spatial-hierarchy-prospacing.md`;
- `color-theory-and-palette.md`;
- `accessibility-and-interaction.md`;
- `motion-and-feedback.md`;
- `responsive-adaptation.md`;
- `anti-ai-slop.md`;
- `interface-quality-gate.md`.

## Design critique

Load:

- `interface-quality-gate.md` first;
- then every specialist skill corresponding to a failed category;
- `anti-ai-slop.md` for generated/template-like patterns;
- `visual-art-direction.md` if the product lacks identity.

## Brand / visual refresh

Load:

- `visual-art-direction.md`;
- `typographic-hierarchy.md`;
- `color-theory-and-palette.md`;
- `color-weight-and-dominance.md`;
- `ui-asset-generation.md` when imagery is included;
- `component-craft.md`;
- `anti-ai-slop.md`;
- `accessibility-and-interaction.md`;
- `interface-quality-gate.md`.

## Onboarding / checkout / wizard

Load:

- `user-flow-and-navigation.md`;
- `progressive-disclosure.md`;
- `information-architecture.md`;
- `content-design-and-labeling.md`;
- `functional-grouping.md`;
- `motion-and-feedback.md`;
- `component-craft.md`;
- `accessibility-and-interaction.md`;
- `interface-quality-gate.md`.

## Mobile adaptation

Load:

- `responsive-adaptation.md`;
- `user-flow-and-navigation.md`;
- `component-craft.md`;
- `accessibility-and-interaction.md`;
- `visual-hierarchy.md`;
- `spatial-hierarchy-prospacing.md`;
- `interface-quality-gate.md`.

## Color / palette task

Load:

- `color-theory-and-palette.md`;
- `color-weight-and-dominance.md`;
- `design-tokens-and-theming.md`;
- `accessibility-and-interaction.md`;
- `visual-art-direction.md`;
- `interface-quality-gate.md` when reviewing a finished system.

---

# Conflict resolution

Specialist skills may occasionally pull in different directions.

Resolve conflicts using this priority:

1. user safety and accessibility;
2. explicit user requirements;
3. target-platform conventions;
4. core task usability;
5. established product design system;
6. product-specific art direction;
7. general cross-platform heuristics;
8. visual novelty.

Never sacrifice accessibility or task comprehension merely to preserve a decorative style rule.

Do not use a numeric guideline from another design system as an absolute law when the product context clearly requires adaptation.

Preserve the reason behind the guideline.

---

# Full-system mode

When the user asks for the strongest possible design pass, a complete redesign, a full product UI, or explicitly asks to use all design skills, activate full-system mode.

In full-system mode:

1. reference every specialist skill in this repository;
2. apply each skill where it materially affects the task;
3. do not force irrelevant patterns into the design merely to say every skill was used;
4. maintain one shared design model across all skills;
5. run `anti-ai-slop.md` continuously;
6. run `interface-quality-gate.md` last;
7. revise failures before completion.

`Use all skills` means every skill participates in the review model, not that every skill must produce visible decoration or additional UI.

---

# Targeted mode

For a narrow task such as `fix this button`, `choose a palette`, or `review this navbar`, load only the specialist skills needed plus:

- `anti-ai-slop.md` when visual styling is involved;
- `accessibility-and-interaction.md` when interaction is involved;
- `interface-quality-gate.md` when the user requests a final-quality review.

Do not create unnecessary complexity by invoking unrelated skills.

---

# Mandatory design principles

Regardless of task type:

- relationships come before decoration;
- hierarchy comes before styling;
- spacing should communicate grouping;
- alignment should create structure;
- typography should use semantic roles;
- color should have defined jobs;
- components need real states;
- interactions should remain familiar unless there is a strong reason otherwise;
- advanced complexity should be progressively disclosed;
- accessibility is part of design quality;
- mobile is adaptation, not shrinking;
- personality should come from coherent decisions, not trend effects;
- fake proof and fake state are forbidden;
- unnecessary pills, glows, cards, gradients, and animations should be removed;
- final output must survive the quality gate.

---

# Anti-AI default behavior

When uncertain, do not fill space with generic startup patterns.

Do not automatically add:

- `Now available` pills;
- blinking green dots;
- sparkle icons;
- purple-to-blue gradients;
- glass cards;
- giant rounded rectangles;
- fake dashboards;
- fake metrics;
- floating badges;
- `Trusted by` logos;
- generic testimonials;
- decorative terminals;
- giant glow backgrounds;
- equal 3-card feature rows;
- vague copy like `Supercharge your workflow`.

Instead improve:

- composition;
- typography;
- spacing;
- alignment;
- product imagery;
- concrete copy;
- content hierarchy;
- one or two product-specific visual ideas.

---

# Required behavior when generating UI

Before generating final UI, establish a compact internal design brief containing:

- product purpose;
- primary audience;
- primary task;
- platform;
- density;
- hierarchy;
- art-direction words;
- typography direction;
- color strategy;
- geometry/radius strategy;
- grid/spacing strategy;
- motion strategy;
- responsive strategy;
- accessibility risks;
- anti-slop risks.

Use that brief as the shared state across all specialist skills.

Do not let later skills silently contradict earlier decisions.

---

# Required behavior when reviewing UI

When critiquing an existing design:

1. identify critical usability/accessibility issues first;
2. identify structural and hierarchy problems second;
3. identify visual system inconsistencies third;
4. identify generic/AI-slop patterns fourth;
5. identify personality opportunities last.

Do not start by changing colors if the information architecture is broken.

Do not start by adding personality if basic hierarchy is unclear.

Do not recommend more decoration as the default fix for boring design.

---

# Required final validation

Before declaring a UI complete, verify all of these:

## Structure

- clear screen purpose;
- understandable navigation;
- logical grouping;
- unnecessary steps removed;
- context preserved.

## Hierarchy

- obvious focal order;
- one clear primary action where appropriate;
- secondary and tertiary content visibly quieter;
- no accidental attention competition.

## Layout

- coherent grid;
- repeated alignment lines;
- controlled text measure;
- intentional density;
- consistent spacing relationships.

## Typography

- semantic role system;
- readable body text;
- controlled weights;
- appropriate line height;
- typography supports product character.

## Color

- every accent has a role;
- semantic states are consistent;
- contrast works;
- large surfaces are not needlessly saturated;
- dark mode is intentionally handled when required.

## Components

- component anatomy is consistent;
- states exist;
- controls remain recognizable;
- targets remain operable.

## Personality

- 3-4 clear character words;
- 1-3 signature ideas;
- recognizable without relying entirely on the logo;
- not dependent on current SaaS trends.

## Anti-slop

- no fake proof;
- no decorative fake status;
- no gratuitous pills;
- no card soup;
- no random glow/gradient filler;
- no vague AI-startup copy;
- no decoration without a reason.

## Accessibility

- focus visible;
- keyboard path logical;
- contrast acceptable;
- important meaning not color-only;
- errors understandable;
- reduced-motion needs considered;
- zoom/reflow supported where applicable.

## Responsive behavior

- task remains possible on smaller screens;
- layout recomposes;
- navigation adapts;
- important controls remain reachable;
- dense data has a mobile strategy.

## Final gate

Run `interface-quality-gate.md`.

Do not call the result finished until critical failures are resolved.

---

# Repository philosophy

The specialist skills are intentionally modular so an AI can reason deeply about each design problem.

This orchestrator exists so those modules behave like one design system instead of isolated checklists.

The goal is not to generate more UI.

The goal is to generate fewer arbitrary decisions.

A strong interface should feel like one designer made hundreds of connected choices for one specific product rather than an AI assembled fashionable components from unrelated templates.
