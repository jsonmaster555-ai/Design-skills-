# Component Craft

Generate components as precise pieces of a system, not generic rounded rectangles.

Before creating a component, determine its purpose, density, hierarchy, interaction states, anatomy, and relationship to neighboring components.

## Buttons

Keep button geometry proportional to context. Product UI often benefits from compact controls. Avoid defaulting to 48–56px heights, huge horizontal padding, pill shapes, heavy labels, gradients, or dramatic shadows.

Use restrained typography, usually Medium or Semibold. Keep icon-label gaps tight. Distinguish primary, secondary, ghost, and destructive actions through controlled emphasis.

## Inputs

Keep labels visually connected to their fields. Use clear focus states. Placeholder text is not a replacement for a persistent label when the label is necessary for understanding. Avoid giant input heights and excessive rounding.

## Cards

Do not automatically put content in cards. Use a card when containment communicates a real object, grouping, interaction region, or surface distinction. Keep padding proportional to density. Avoid unnecessary shadows and nested cards.

## Badges

Badges should generally be compact. Use tight padding and restrained text. Do not use monospace by default. Do not make every badge a large pill. Status styling should not overpower the content it describes.

## Menus and Dropdowns

Keep menus scannable and compact. Group related commands. Separate destructive or structurally different actions. Align icons and labels consistently. Do not create huge floating panels for a small number of commands.

## Tabs

Tabs represent peer views within the same context. Keep them visually connected to the content they control. Avoid oversized segmented pills unless the product language specifically calls for them.

## Tables

Prioritize scanning, column alignment, row density, and value comparison. Do not turn every row into an isolated card. Numeric values should align consistently where comparison matters.

## Modals and Dialogs

Use dialogs for focused interruptions or decisions, not as a default container for complex application pages. Establish a clear title, content region, and action area. Avoid excessive width, padding, and decorative chrome.

## Sidebars

Keep navigation rows compact and predictable. Use selected states with controlled emphasis. Group sections through spacing and labels rather than large decorative containers.

## Icon Buttons

Maintain clear hit targets while keeping the visible glyph optically balanced. The visual button does not need to appear as large as its interaction target.

## States

Components should account for default, hover, active, focus, selected, disabled, loading, error, and success states when relevant. States should change enough to communicate meaning without making the component jump in size or layout.

## Optical Correction

Mathematical centering is not always visual centering. Correct icons, text, asymmetric glyphs, and mixed shapes by small amounts when necessary. Preserve the token system as the baseline and make optical adjustments deliberately.

The component should look intentional at its actual rendered size, not merely impressive when enlarged in a design canvas.
