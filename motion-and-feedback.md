# Motion and Feedback

Use this skill for transitions, loading, progress, state changes, hover/press feedback, drag interactions, menus, dialogs, AI activity, success/error confirmation, and micro-animation.

Motion is one of the strongest attention cues in an interface. Use it to explain change, not to decorate empty space.

## Core objective

Help users understand:

- what changed;
- what caused the change;
- where an object went;
- whether an action succeeded;
- whether the system is still working;
- what requires attention next.

## Motion must have a job

Acceptable purposes include:

- continuity between states;
- spatial orientation;
- feedback after interaction;
- communicating progress;
- showing relationship between source and destination;
- drawing temporary attention to a meaningful change.

Avoid animation that exists only because the UI “feels too static.”

## Prefer state continuity

When an element expands, moves, opens, or changes mode, motion can preserve its perceived identity.

Examples:

- a menu originates from its trigger;
- a panel enters from the edge it belongs to;
- an expanding card retains its spatial relationship;
- a selected object transitions into a detail view.

Do not animate unrelated elements across the screen in ways that imply false relationships.

## Duration

Use short motion for small state changes and longer motion for larger spatial transitions.

Keep a small duration scale rather than inventing timings per component.

Micro-feedback should feel immediate.

Large navigation transitions can take slightly longer if the motion helps orientation.

Do not make common actions wait for decorative animation to finish.

## Easing

Use easing that reflects physical/visual intent.

Entering elements can decelerate into place.

Exiting elements can accelerate away.

State changes may use balanced easing.

Avoid bouncy/spring motion unless it fits brand and does not reduce task efficiency.

## Hover

Hover may provide subtle feedback for pointer users.

Do not make hover the only way to discover an action.

Avoid large layout shifts on hover.

Do not animate position so much that pointer targets move away from the cursor.

## Pressed state

Pressed feedback should feel immediate.

Use restrained changes such as:

- surface change;
- slight scale change where appropriate;
- ripple/state layer when the platform language uses it;
- contrast change.

Do not make buttons jump several pixels.

## Focus

Keyboard focus is not an animation opportunity first; it is an accessibility state.

Focus must remain clearly visible even if animation is disabled.

Do not animate focus indicators so subtly that users cannot locate them.

## Loading

Choose feedback according to scope.

### Component loading

Only block or skeleton the affected region.

### Page loading

Preserve stable shell/navigation when possible.

### Determinate progress

Use when real progress can be measured.

### Indeterminate progress

Use when the duration or work units are unknown.

Do not show fake precise percentages.

## Skeletons

Skeletons should approximate the actual content geometry.

Do not use decorative gray blobs unrelated to the final structure.

Avoid skeletons for operations so fast that they create flicker.

## Optimistic feedback

For actions likely to succeed quickly, optimistic UI can make the system feel responsive.

Provide rollback/error handling if the operation fails.

Do not imply success permanently before the system can recover from failure.

## Success

Routine success should be clear but not theatrical.

Examples:

- inline state change;
- short toast/status message;
- checkmark/state icon;
- saved-state label.

Avoid confetti or celebratory animation for ordinary saves unless the product context genuinely benefits from it.

## Errors

Error feedback should remain until users can understand and recover.

Do not flash an error briefly and disappear.

Place errors near the affected object and explain recovery.

Animation can draw attention once, but the persistent state must still communicate the problem.

## Drag and drop

Show:

- what is draggable;
- active drag state;
- valid drop targets;
- insertion point or destination;
- result after drop.

Provide a non-drag alternative where accessibility requirements apply.

Do not rely on motion alone to explain where an item will land.

## Menus and popovers

Transitions should be fast and anchored.

Avoid elaborate scaling/rotation that delays access.

Dismissal should feel immediate.

Focus must be restored correctly when keyboard users close the surface.

## Dialogs

A dialog transition can communicate modal layering, but content and focus behavior matter more than animation.

Do not use slow full-screen cinematic transitions for simple confirmations.

## AI activity

AI interfaces may need feedback for:

- searching;
- reasoning/processing;
- generating;
- listening;
- connecting;
- completing.

Use state-specific indicators when it improves understanding.

Avoid an endlessly pulsing generic sparkle for every AI state.

## Reduced motion

Respect `prefers-reduced-motion` and platform equivalents.

When reduced motion is enabled:

- remove parallax;
- reduce large spatial movement;
- replace animated transitions with opacity/state changes where appropriate;
- keep feedback and meaning intact.

Motion must not be required to understand the interface.

## Flashing and safety

Avoid rapid flashing and high-frequency visual effects.

Follow WCAG flashing/seizure criteria.

## Motion and performance

Animation that drops frames makes the interface feel worse.

Prefer properties and techniques that can animate smoothly on target devices.

Avoid animating huge blurred layers, heavy filters, or unnecessary full-page effects.

Performance is part of perceived quality.

## Layout shift

Do not let asynchronous content unexpectedly push controls away while users are trying to interact.

Reserve space when dimensions are known.

Use stable loading patterns.

## Sound and haptics

When platform-appropriate, sound or haptic feedback can reinforce important interactions.

Never make audio/haptics the only feedback.

Respect system preferences and avoid overuse.

## Failure modes

### Motion everywhere

Fix: reserve animation for state/relationship/feedback.

### Slow “premium” UI

Fix: shorten common transitions and remove blocking decoration.

### Endless pulsing

Fix: show state with stable visual feedback and animate only when useful.

### Layout shift

Fix: reserve geometry and localize loading changes.

### Reduced-motion breakage

Fix: ensure state meaning remains without movement.

### Success theater

Fix: match feedback intensity to consequence.

## Evaluation checklist

- What does each animation explain?
- Could it be removed without losing understanding?
- Is feedback immediate enough?
- Does loading affect only the necessary region?
- Are failures persistent and recoverable?
- Does reduced-motion mode remain understandable?
- Is focus behavior correct after temporary UI closes?
- Does animation perform smoothly on target hardware?
- Is motion intensity proportional to the event?

## Source foundations

References:

- https://www.w3.org/WAI/WCAG22/Understanding/
- https://fluent2.microsoft.design/accessibility
- https://developer.apple.com/design/human-interface-guidelines/motion
- https://m3.material.io/styles/motion/overview
