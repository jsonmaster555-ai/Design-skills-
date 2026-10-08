# Nested Structural Layouts

Interfaces contain structures inside structures: application → workspace → project → panel → section → component → control. Each level needs a clear relationship without receiving unnecessary visual chrome.

Use indentation, alignment, spacing, grid changes, typography, and subtle surface changes to communicate nesting.

Do not give every nesting level another border, card, background, shadow, and radius. Excessive containers create visual recursion and make hierarchy harder to understand.

## Parent and child relationships

Children should visually belong to their parent through proximity and alignment. Nested content should not accidentally appear equal to the page-level structure.

## Depth

Use the minimum visual signal necessary to explain depth. A small indentation or spacing change may communicate nesting better than another box.

## Repeated structures

Equivalent nesting levels should use consistent geometry and spacing. Avoid changing indentation, padding, or heading treatment arbitrarily between similar sections.

Structural depth should be understandable even when decorative effects are removed.