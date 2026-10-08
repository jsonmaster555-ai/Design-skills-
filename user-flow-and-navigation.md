# User Flow and Navigation

Use this skill when designing, reviewing, or repairing how a person moves through a product to complete a goal.

This skill covers task flow, navigation, orientation, progressive disclosure, feedback, recovery, focus order, and friction. It should be used alongside visual design skills rather than treated as a replacement for them.

## Core objective

Make the path from intent to outcome obvious, predictable, recoverable, and proportionate to the consequence of the action.

The shortest flow is not always the best flow. The best flow removes unnecessary decisions while preserving context, safety, agency, and understanding.

## Start with the user goal

Never begin with `What screens should the app have?`

Begin with:

- What is the user trying to accomplish?
- What information do they already have?
- What information must the product ask for?
- What can be inferred or deferred?
- What could go wrong?
- What should happen after success?

Write the goal in plain language.

Example:

`Upload a file and share it with the team.`

Then map the shortest understandable path to that outcome.

## Task flow model

For each important task, define:

1. entry point;
2. orientation;
3. primary action;
4. required input;
5. validation;
6. system response;
7. success state;
8. recovery path;
9. exit/cancel path;
10. return path if the user leaves and comes back.

Do not design only the happy path.

## One screen, one main job

Every screen should have a clear answer to:

`Why am I here?`

A screen can contain multiple controls, but its dominant purpose should remain clear.

Examples:

- dashboard: understand current state and reach frequent work;
- project page: inspect and act on one project;
- settings: configure behavior;
- checkout: complete purchase;
- editor: create or modify content.

If one screen tries to perform several unrelated jobs, separate or progressively disclose them.

## Navigation hierarchy

Organize navigation by level.

A common structure is:

- product;
- major destination;
- object/workspace/project;
- subsection;
- local view/action.

Example:

`Projects → Relay → Webhooks → Production`

Do not flatten every destination, setting, object, and action into one sidebar.

Primary navigation should represent major places, not every feature.

## Navigation is not an action dump

Distinguish destinations from commands.

Destinations:

- Home;
- Projects;
- Inbox;
- Activity.

Actions:

- Create project;
- Upload file;
- Invite member;
- Export.

Do not turn every action into a permanent top-level navigation item.

## Preserve orientation

Users should understand:

- where they are;
- what object they are acting on;
- where they came from when relevant;
- what level of the product they are in.

Use whichever combination fits the product:

- selected nav state;
- page title;
- object name;
- tabs;
- breadcrumb;
- sidebar nesting;
- contextual header.

Do not add breadcrumbs automatically when existing structure already makes location obvious.

## Predictability

Repeated interactions should behave consistently.

If the logo navigates home, keep that behavior stable.

If Back appears in one location, do not move it randomly between screens.

If Settings lives under the account menu, do not place the same destination in unrelated locations without reason.

Consistency lets users form a mental model and spend less attention on the interface itself.

W3C's predictable-interface criteria also reinforce consistent navigation and identification.

## Make the next step obvious

At each stage, the interface should communicate:

- what the user can do;
- which action is primary;
- what information is required;
- what will happen next.

Do not present four equally styled actions when only one advances the task.

Use primary, secondary, and tertiary action hierarchy.

## Progressive disclosure

Show the information and controls needed for the current decision.

Defer advanced configuration until it becomes relevant.

Example:

Initial export UI:

- format;
- size;
- Export;
- `Advanced options` disclosure.

Do not force every user to confront compression algorithms, metadata rules, color profiles, and cache settings before basic export.

Do not hide frequently needed controls behind repeated disclosure either. Frequency matters.

## Decision cost

Every visible choice creates cognitive work.

Before adding a choice, ask:

- Is the decision required now?
- Can the system provide a good default?
- Can it be changed later?
- Does asking now improve the result enough to justify interruption?

Onboarding should not become a questionnaire for settings that can be configured after the user reaches the product.

## Preserve context

Prefer local editing when the task is small and tightly scoped.

Examples:

- rename inline instead of opening three settings pages;
- edit metadata in a side panel when the object should remain visible;
- use a focused dialog for a short blocking decision;
- use a full page when the task genuinely needs space, navigation, or deep configuration.

Do not open a new page merely because every action was implemented as a route.

## Agency and escape routes

Users should normally be able to:

- go back;
- cancel;
- close;
- undo;
- edit before submitting;
- recover after an error.

Do not create accidental traps in multi-step flows.

For reversible low-risk actions, Undo can be better than repeated confirmation dialogs.

For destructive, irreversible, financial, legal, or high-consequence actions, deliberate confirmation and review may be necessary.

Friction should match consequence.

## Confirmation rules

Do not ask `Are you sure?` for routine reversible actions.

Use confirmation when at least one is true:

- action is destructive and hard to reverse;
- action affects many people/items;
- action has financial/legal consequence;
- action changes permissions/security;
- action destroys unsaved work;
- user intent could reasonably be ambiguous.

A confirmation should name the consequence rather than merely repeat the action.

## Feedback

Every meaningful action needs an observable system response.

Examples:

- Saving… → Saved;
- Uploading 42%;
- Message sent;
- File deleted + Undo;
- Validation error beside the field;
- Retry after network failure.

Feedback intensity should match event importance.

Do not use giant toast notifications for trivial events or nearly invisible feedback for destructive actions.

## Loading and latency

When work takes noticeable time:

- acknowledge the action immediately;
- show progress when progress is meaningful;
- preserve context;
- prevent duplicate submissions when required;
- explain long operations when useful;
- allow cancellation when technically and conceptually appropriate.

Do not display a spinner without explaining what is happening when the delay is long or unusual.

## Error recovery

An error state should answer:

1. what happened;
2. what was affected;
3. what the user can do next.

Weak:

`Error 482`

Stronger:

`Upload failed. Your connection was interrupted. Try again.`

Preserve valid user input whenever possible.

Do not wipe a form because one field failed validation.

## Empty states

Empty states should explain the state and offer the appropriate next action when one exists.

Do not turn every empty state into a giant illustration + marketing paragraph + oversized CTA.

Keep empty states proportional to the importance and frequency of the situation.

## Frequency-based placement

High-frequency actions should be easier to reach than rare administrative actions.

Example webhook tool:

Frequent:

- inspect requests;
- copy endpoint;
- create webhook;
- retry delivery.

Rare:

- edit billing address;
- delete workspace;
- rotate organization ownership.

Do not give rare settings equal placement and visual weight to daily work.

## Recognition over recall

Prefer visible, understandable options when users would otherwise have to remember commands, paths, or hidden behavior.

Examples:

- visible recent projects instead of requiring exact search terms;
- labeled controls instead of mystery icons for uncommon actions;
- remembered selections where safe;
- inline guidance for unfamiliar concepts.

Do not expose every option merely to satisfy recognition. Use progressive disclosure where the option set becomes too large.

## Familiar patterns

Use familiar controls and interaction models for common tasks.

Examples:

- magnifying glass for search;
- trash for delete;
- left arrow for back;
- checkbox for multiple independent selections;
- radio group for one choice among several;
- switch for immediate binary settings.

Custom appearance is fine. Custom behavior requires stronger justification.

Apple's design principles emphasize familiar, direct, logically organized experiences while preserving user agency.

## Gestures and shortcuts

Gestures and keyboard shortcuts can accelerate expert use, but essential actions should generally retain discoverable alternatives.

Do not make an invisible gesture the only way to reach a core function.

## Keyboard and focus flow

Sequential focus should preserve meaning and operability.

The focus order should normally support the same mental structure communicated visually.

Do not allow focus to jump randomly between columns, hidden controls, footers, and main form fields.

W3C WCAG 2.2 SC 2.4.3 requires focus order to preserve meaning and operability.

## Focus should not trigger surprise navigation

Merely focusing a control should not unexpectedly:

- submit a form;
- navigate away;
- open a major window;
- erase work;
- change context.

Make consequential changes happen on deliberate user action.

## Target sizing

Interactive targets must remain realistically operable.

WCAG 2.2 SC 2.5.8 establishes a 24 by 24 CSS pixel minimum target size or sufficient spacing under its defined exceptions.

Do not shrink controls simply to achieve a dense aesthetic.

Density should come from hierarchy, spacing discipline, and information design rather than impossible click targets.

## Mobile adaptation

Do not simply stack a desktop flow vertically.

Reconsider:

- navigation mechanism;
- persistent vs temporary controls;
- bottom-reachable frequent actions;
- modal size;
- step count;
- table representation;
- keyboard obstruction;
- touch target spacing.

Preserve the task model even when the layout changes.

## Multi-step flows

Use explicit steps when:

- the task is genuinely sequential;
- later decisions depend on earlier choices;
- the amount of information would overwhelm one screen;
- progress matters.

Do not create a wizard for a task that can be completed clearly in one view.

When steps are used:

- show progress when useful;
- allow Back when safe;
- preserve entered data;
- make final commitment obvious;
- distinguish review from submission.

## The minimum-friction rule

Good UX does not mean zero friction.

Use the minimum friction necessary for:

- understanding;
- correctness;
- safety;
- trust;
- recoverability.

Examples:

Opening a project should be nearly immediate.

Deleting an entire workspace should not be equally immediate.

## Anti-slop flow rules

- Do not add onboarding steps just to showcase features.
- Do not create fake complexity so the product feels powerful.
- Do not hide basic actions inside command palettes only.
- Do not make every action open a modal.
- Do not make every setting auto-save without clear feedback.
- Do not add confirmations to every click.
- Do not use decorative progress indicators with no real progress.
- Do not create navigation categories with vague labels like `Discover`, `Magic`, or `More` when concrete labels exist.
- Do not place rarely used actions in the primary action slot.
- Do not make a flow visually impressive at the cost of predictability.

## Flow review procedure

For each major task:

1. Write the user's goal in one sentence.
2. Identify every step required to reach it.
3. Mark each step as necessary, inferable, deferrable, or removable.
4. Remove unnecessary steps.
5. Check orientation at each remaining step.
6. Check primary action hierarchy.
7. Check Back, Cancel, Undo, and recovery paths.
8. Add loading, error, empty, and success states.
9. Test keyboard/focus order.
10. Test mobile adaptation.
11. Check whether friction matches consequence.
12. Run the task without explanatory narration. If the interface needs the designer to explain it, revise it.

## Review checklist

- Is the primary user goal explicit?
- Is every step necessary?
- Does every screen have a dominant purpose?
- Is top-level navigation limited to real destinations?
- Can users tell where they are?
- Is the next action obvious?
- Are advanced decisions deferred appropriately?
- Can users recover from mistakes?
- Does every meaningful action provide feedback?
- Are error states actionable?
- Does keyboard focus preserve meaning?
- Are targets realistically operable?
- Does mobile preserve the task rather than merely shrink the layout?
- Is friction proportional to consequence?

## Companion skills

Use with:

- `information-architecture.md`;
- `progressive-disclosure.md`;
- `functional-grouping.md`;
- `visual-hierarchy.md`;
- `content-design-and-labeling.md`;
- `accessibility-and-interaction.md`;
- `motion-and-feedback.md`;
- `component-craft.md`.

## Source foundations

- Apple Human Interface Guidelines — Design Principles and Layout
  - https://developer.apple.com/design/human-interface-guidelines/design-principles
  - https://developer.apple.com/design/human-interface-guidelines/layout
- W3C WCAG 2.2 — Focus Order, Predictable behavior, Target Size
  - https://www.w3.org/WAI/WCAG22/Understanding/focus-order.html
  - https://www.w3.org/WAI/WCAG22/Understanding/
  - https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum.html
- Material Design 3 — navigation and interaction foundations
  - https://m3.material.io/
