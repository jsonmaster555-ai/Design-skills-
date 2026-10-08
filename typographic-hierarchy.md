# Typography and Typographic Hierarchy

Use this skill whenever text appears in an interface.

Typography is not decoration applied after layout. Text establishes hierarchy, density, rhythm, scanning behavior, tone, accessibility, and component geometry.

## Core objective

Make text communicate role and importance without requiring excessive size, weight, color, or styling.

## Define semantic text roles

Build a small role system before choosing arbitrary sizes.

Typical product roles:

- display / marketing statement;
- page title;
- section heading;
- subsection heading;
- item title;
- body;
- UI body;
- control label;
- input label;
- caption;
- metadata;
- code/technical value.

Repeated roles should reuse the same typography tokens.

Do not create a new font size for each component.

## Use a restrained type ramp

A compact product interface might begin near:

- 12: caption / metadata;
- 13–14: compact labels and dense UI;
- 14–16: standard body/UI;
- 18–20: small headings;
- 24–32: major product headings;
- larger: intentional marketing/display use.

These are starting ranges, not universal values.

Typeface x-height, platform, reading distance, density, and content type can change the correct size.

Fluent’s web type ramp similarly uses named semantic levels rather than arbitrary styling.

Material’s type systems also separate display/headline/title/body/label roles.

## Fewer weights

Prefer a small weight vocabulary.

For many product interfaces:

- Regular: body and supporting text;
- Medium: controls and moderate emphasis;
- Semibold: headings and strong labels.

Use Bold only when the typeface and context require it.

Avoid ExtraBold/Black as routine UI hierarchy tools.

## Large text already has weight

As type grows, its physical area creates prominence.

A large heading often needs less font weight than a small label.

Do not combine huge size + Black weight + strong contrast unless the design intentionally calls for extreme display typography.

## Improve weak hierarchy in this order

Before increasing font weight:

1. check position;
2. increase size modestly;
3. improve contrast;
4. increase surrounding whitespace;
5. reduce competing text emphasis;
6. then consider weight.

This prevents interfaces where every label becomes bold.

## Line height

Line height depends on role and line length.

Large display headings can use relatively tight line height.

Body copy needs more breathing room.

Multiline labels need enough height to avoid collisions when text wraps.

Do not lock containers to one-line heights when localization or accessibility may create wrapping.

## Letter spacing

Use tracking carefully.

General rules:

- normal body text: use the typeface’s intended spacing;
- large headings: sometimes slightly tighter tracking improves cohesion;
- very small uppercase labels: may require increased tracking;
- heavy large type: modest negative tracking may improve balance;
- normal headings: avoid loose positive tracking unless the typeface/style requires it.

Do not apply wide letter spacing to ordinary UI labels to make the product look “premium.”

Do not use extreme negative tracking that causes collisions.

## Casing

Prefer sentence case for most UI text.

All caps reduces word-shape differentiation and can be slower to scan in longer labels.

Reserve uppercase for very short labels when the design system explicitly uses it.

Fluent recommends sentence case for most interface writing.

## Alignment

For sustained left-to-right reading, use leading/left alignment.

For right-to-left languages, mirror to leading/right alignment.

Center text only for short, isolated content where symmetry or emphasis helps.

Avoid center-aligning long paragraphs.

Avoid justified web/UI text because inconsistent word spacing harms scanning.

## Text width

Do not stretch prose across very wide screens.

Use a comfortable reading measure for paragraphs and documentation.

Tables, code, timelines, and data visualizations are different content types and may use wider regions.

## Contrast hierarchy

Use semantic text colors such as:

- primary text;
- secondary text;
- tertiary text;
- disabled text;
- link/accent;
- danger/status.

Secondary does not mean barely visible.

WCAG AA commonly requires 4.5:1 contrast for normal text and 3:1 for qualifying large text.

Always test the actual foreground/background pair.

## Headings

A heading must do two jobs:

1. explain the content that follows;
2. provide a visible scan anchor.

Keep headings closer to their own content than to the previous section.

Use semantic heading levels in code; do not pick an `<h*>` level only because of default browser styling.

## Body text

Prioritize:

- legibility;
- stable line height;
- appropriate measure;
- clear paragraph separation;
- sufficient contrast;
- natural font weight.

Avoid long blocks of bold or italic text.

## Labels

Labels should be concise and specific.

The typography should match component density.

Do not use oversized labels that force buttons or inputs to become unnecessarily tall.

## Buttons

Button text should remain easy to scan at a glance.

Use Medium/Semibold only as needed.

The label’s typography should not determine an oversized button height.

Prefer verb-first action labels where appropriate:

- Save changes
- Create project
- Invite member

Avoid vague labels such as “Proceed” when a specific action can be named.

## Metadata

Metadata should be quiet but readable.

Use smaller size, lower emphasis, or position—usually not all three aggressively at once.

Do not make timestamps and status details so faint that users cannot read them.

## Monospace

Use monospace for content where fixed-width glyphs carry meaning or improve readability:

- code;
- terminal output;
- technical identifiers when helpful;
- tabular technical data where alignment matters.

Do not use monospace for ordinary navigation, badges, POST/GET labels by default, or regular UI text merely to make the interface look technical.

## Numerals

For dashboards and tables, consider whether the typeface supports:

- tabular numerals;
- lining numerals;
- clear zero/O distinction;
- readable punctuation;
- currency symbols.

Use tabular numerals when columns of changing values need stable width.

## Open and freely usable font choices

When a product needs a font that can be bundled or embedded without proprietary platform licensing, prefer well-maintained open-source families with explicit licenses.

### Inter

- Designed for interfaces and small-size readability.
- Variable family available.
- Licensed under SIL Open Font License 1.1.
- Good default for neutral product UI.
- Repository: https://github.com/rsms/inter

### IBM Plex

- Sans, Serif, Mono, and Condensed families.
- Designed to work in UI and broader brand/editorial environments.
- Open-source under the Open Font License.
- Broad script support across family variants.
- Repository: https://github.com/IBM/plex

### Noto Sans

- Broad language/script coverage through the Noto project.
- Google Fonts metadata lists Noto Sans under OFL.
- Useful when internationalization coverage is a major requirement.
- Metadata/source: https://github.com/google/fonts/tree/main/ofl/notosans

Always keep the license file and comply with the font’s actual license terms when distributing font files. Verify the current license for any additional font before embedding it in an app.

## System fonts

System fonts can be an excellent choice because they:

- avoid webfont loading;
- match platform conventions;
- receive platform accessibility optimization;
- often provide broad native script support.

Fluent recommends native platform stacks where appropriate.

Apple likewise recommends system fonts for many interface contexts because of small-size legibility and accessibility behavior.

Do not assume a proprietary platform font can be redistributed as a webfont. Use it through the platform/system stack unless its license explicitly permits redistribution.

## Font pairing

Most product interfaces do not need several families.

A reliable system may use:

- one sans family for UI;
- one mono family for code;
- optional serif/display family only for editorial or branded contexts.

If pairing families, match their visual color, x-height, and personality.

Avoid mixing fonts merely to create hierarchy that the type scale should provide.

## Variable fonts

Variable fonts can reduce the number of font files and expose axes such as weight or optical size.

Use only the axes the design needs.

Do not generate dozens of near-identical weights that destroy system consistency.

## Font loading and performance

For web UI:

- use WOFF2 where appropriate;
- subset only when language requirements are understood;
- preload critical font files carefully;
- define robust fallback stacks;
- avoid invisible text for long periods;
- minimize unnecessary weights/styles.

A beautiful font that delays or destabilizes the UI is not a successful typography system.

## Responsive typography

Do not scale every type role by the same percentage.

Preserve role relationships.

Display text may reduce substantially on small screens while body text remains near a stable readable size.

Allow headings to wrap naturally.

Avoid viewport-based font sizing without sensible minimums and maximums.

## Accessibility and user preferences

- Use relative units such as `rem` for web typography when appropriate.
- Allow browser/user text-size changes.
- Support Dynamic Type or equivalent native scaling.
- Do not clip text at larger sizes.
- Do not encode semantic meaning only through bold/italic appearance.
- Maintain correct semantic headings.
- Ensure custom fonts remain legible at small sizes.
- Test at 200% zoom and with text-spacing overrides.

WCAG’s text-spacing criterion requires content to remain functional when users increase line, paragraph, letter, and word spacing.

## Localization

Typography must support:

- longer translations;
- right-to-left scripts;
- non-Latin scripts;
- different word-breaking rules;
- different font metrics.

Do not force a Latin-only brand font into languages it does not support. Provide appropriate fallback families.

## Optical balance

Two typefaces at 14px can look very different because of x-height and proportions.

Evaluate perceived size, not only CSS size.

Likewise, icons should align to the perceived cap/x-height, not merely the text bounding box.

## Failure modes

### Giant headings in software

Fix: reduce display scale and strengthen hierarchy using position/spacing.

### Bold everything

Fix: return body/labels to Regular/Medium and reserve Semibold.

### Too many sizes

Fix: create named semantic roles and tokens.

### Loose tracking everywhere

Fix: use natural spacing except for justified display/small-uppercase cases.

### Low-contrast metadata

Fix: preserve readability and reduce prominence with multiple gentle cues.

### Decorative monospace

Fix: use mono only when the content benefits from it.

### Font-license assumptions

Fix: use explicit open-source/system-font rules and verify licenses.

## Evaluation checklist

- Can every text style be named by role?
- Are there only a few font weights?
- Are headings visually and semantically hierarchical?
- Is body copy comfortable to read?
- Are labels compact enough for component density?
- Is metadata quiet but accessible?
- Does typography survive zoom, localization, and RTL?
- Are bundled fonts explicitly licensed for the intended use?
- Could a system font reduce complexity without harming the design?
- Are code/technical values the only places using monospace without a specific exception?

## Source foundations

This skill synthesizes Fluent typography/accessibility, Apple typography/branding/writing guidance, Atlassian typography accessibility guidance, Material type-role conventions, WCAG text contrast/resize/text-spacing requirements, and official license sources for Inter, IBM Plex, and Noto Sans.

References:

- https://fluent2.microsoft.design/typography
- https://fluent2.microsoft.design/accessibility
- https://developer.apple.com/design/human-interface-guidelines/typography
- https://developer.apple.com/design/human-interface-guidelines/branding
- https://developer.apple.com/design/human-interface-guidelines/writing
- https://atlassian.design/foundations/typography-beta/applying-typography/
- https://m3.material.io/styles/typography/overview
- https://www.w3.org/WAI/WCAG22/Understanding/
- https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html
- https://github.com/rsms/inter
- https://github.com/IBM/plex
- https://github.com/google/fonts/tree/main/ofl/notosans
