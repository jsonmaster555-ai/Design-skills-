# Accessibility and Interaction

Use this skill across every interface. Accessibility is not a final checklist applied after visual design; it changes component anatomy, color, focus behavior, layout, motion, content, and interaction from the beginning.

## Core objective

Make the product perceivable, operable, understandable, and robust across different ways of seeing, hearing, reading, moving, and interacting.

This skill uses WCAG 2.2 as a baseline and combines it with platform guidance from Apple and Microsoft Fluent.

## Semantic structure

Visual structure and semantic structure should agree.

Use appropriate:

- headings;
- landmarks;
- lists;
- tables;
- labels;
- form groups;
- buttons;
- links.

Do not build button behavior with a generic clickable div when a native button is appropriate.

## Meaningful sequence

The reading/focus order should remain logical if CSS styling, columns, or visual positioning is removed.

Do not visually reorder content into a sequence that differs from the semantic order in a way that changes meaning.

## Keyboard access

Every essential interactive function must be operable without a pointing device.

Check:

- Tab/Shift+Tab movement;
- Enter/Space activation;
- arrow-key behavior in composite widgets;
- Escape for dismissible temporary UI;
- shortcuts that do not trap or conflict;
- no keyboard traps.

Use established component patterns so keyboard behavior is predictable.

## Focus visibility

Keyboard focus must be obvious.

Do not remove native focus styling without providing an equally clear or stronger replacement.

Focus treatment should:

- contrast against adjacent colors;
- remain visible on different surfaces;
- not be clipped by overflow;
- remain visible while sticky elements are present;
- be distinct from hover where necessary.

WCAG 2.2 includes Focus Visible, Focus Not Obscured, and Focus Appearance guidance.

## Focus management

When temporary UI opens:

- place focus in an appropriate location;
- keep focus within a modal dialog while it is active;
- restore focus to the invoking control on close;
- do not reset focus to the top of the page unnecessarily.

When content updates dynamically, move focus only when doing so helps the task; otherwise announce status changes without hijacking focus.

## Target size

WCAG 2.2 includes a 24×24 CSS pixel minimum target-size criterion with exceptions.

Platform systems often recommend larger touch targets; Fluent cites 44×44 for iOS/web touch contexts and 48×48 for Android contexts.

Visible icon size can be smaller than the hit area.

Keep enough space between adjacent small targets to reduce accidental activation.

## Color contrast

Common WCAG AA contrast thresholds include:

- 4.5:1 for normal text;
- 3:1 for qualifying large text;
- 3:1 for many meaningful UI boundaries and graphical objects against adjacent colors.

Test actual foreground/background pairs.

Do not assume a token works on every surface.

## Do not use color alone

State and meaning should have an additional cue.

Examples:

Error = color + message + semantic state.

Selected = color + indicator/check/background/state.

Success = color + icon/text.

Chart category = color + label/marker/pattern when necessary.

## Text resize and zoom

Design must remain usable when users enlarge text or zoom.

Allow:

- text wrapping;
- row growth;
- vertical stacking;
- responsive reflow;
- dialogs/panels to adapt.

Avoid fixed-height text containers.

## Text spacing

WCAG requires no loss of content or functionality when users override text spacing to specified larger values.

Do not position labels or text with brittle pixel offsets that overlap when line/word/letter spacing changes.

## Reflow

Content should reflow at narrow effective widths without requiring two-dimensional scrolling for ordinary reading/task content, except where two-dimensional layout is essential (for example, some complex data tables, maps, or diagrams).

Do not simply shrink desktop UI until controls become unreadable.

## Labels and instructions

Inputs need persistent, understandable labels.

Do not rely on placeholder text as the only label.

Provide instructions before users make predictable errors.

Use specific error messages and explain recovery.

## Label in name

For controls with visible text, the accessible name should contain the visible label so speech-input users can activate what they see.

Avoid an icon button whose accessible name is unrelated to the visible tooltip or nearby label.

## Links versus buttons

Use a link for navigation.

Use a button for an action/change.

Do not style one as the other without preserving correct semantics and behavior.

## Images and icons

Decorative images should not add noise to assistive technology.

Informative images need meaningful alternatives.

Icon-only controls need accessible names.

Do not put essential text inside raster images.

## Tables

Use real table semantics for tabular data.

Identify headers correctly.

Do not use tables for page layout.

For responsive tables, preserve header/value relationships even if presentation changes.

## Forms

- Associate labels programmatically.
- Group related radios/checkboxes.
- Identify required fields consistently.
- Announce validation errors.
- Preserve entered data.
- Move focus or provide an error summary when submission fails, depending on complexity.
- Do not disable submission without explaining why if the reason is not obvious.

## Status messages

Loading, saving, success, or error messages that appear without moving focus should still be exposed to assistive technology where appropriate.

Do not rely only on a visual toast.

## Hover and focus content

If information appears on hover or focus, ensure it is dismissible, hoverable when needed, and persistent long enough to use.

Do not make essential instructions hover-only.

## Motion

Respect reduced-motion preferences.

Avoid unnecessary large movement, parallax, or continuous animation.

Do not use rapid flashing.

Provide non-motion equivalents where motion is not essential.

## Orientation and input

Do not lock content to one device orientation unless essential.

Support multiple input mechanisms where practical: mouse, touch, keyboard, assistive technology.

Do not require complex path-based gestures when a simpler alternative can exist.

## Dragging

When functionality uses drag-and-drop, provide another method when WCAG requirements apply.

Examples:

- move up/down buttons;
- destination menu;
- keyboard reordering.

## Time limits

Avoid unnecessary time limits.

When time limits are required, provide adjustment, extension, warning, or alternatives according to applicable accessibility requirements.

## Language and localization

Set document/page language correctly.

Identify language changes when required.

Use plain language and avoid unnecessary jargon.

Support RTL layouts and locale-specific formatting.

## Consistency

Keep navigation, help placement, icons, and repeated controls consistent.

Predictability reduces cognitive load and supports users relying on learned patterns.

## High-contrast themes

Test OS/browser high-contrast or forced-color modes.

Ensure:

- focus remains visible;
- selected state survives;
- icons remain perceivable;
- custom backgrounds do not erase controls;
- boundaries remain meaningful.

## Accessibility review checklist

For every interactive screen, test:

- keyboard-only;
- focus visibility;
- focus order;
- 200% zoom or larger where relevant;
- narrow viewport/reflow;
- larger text;
- color contrast;
- color-independent meaning;
- screen-reader semantics;
- light/dark/high-contrast themes;
- reduced motion;
- touch target spacing;
- errors and status announcements;
- localization/RTL.

## Source foundations

Primary references:

- https://www.w3.org/WAI/WCAG22/Understanding/
- https://fluent2.microsoft.design/accessibility
- https://developer.apple.com/design/human-interface-guidelines/accessibility
- https://developer.apple.com/design/human-interface-guidelines/inclusion
- https://atlassian.design/foundations/accessibility/
