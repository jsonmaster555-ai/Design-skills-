# Design Skills

A modular, source-backed UI design reference pack for AI-assisted product design.

Design Skills is built to help an AI produce interfaces that feel deliberately designed rather than generically generated. Each skill focuses on one design problem and gives operational rules, failure modes, accessibility checks, responsive behavior, and source references.

The files stay flat at the repository root so an agent, designer, or developer can load only the guidance relevant to the current task without digging through nested folders.

## What this pack is trying to prevent

Common generated-UI failures include:

- oversized buttons and inputs;
- unnecessary full-width controls;
- excessive pills and corner radii;
- card-inside-card layouts;
- giant padding used as a substitute for hierarchy;
- heavy typography everywhere;
- random shadows and gradients;
- vague navigation labels;
- inaccessible low-contrast secondary text;
- inconsistent spacing values;
- weak keyboard/focus behavior;
- desktop layouts that simply shrink instead of adapting;
- generated illustrations that look pasted onto the product;
- inconsistent component states;
- color used without semantic meaning.

Design Skills treats these as system problems, not isolated styling mistakes.

## Skills

### Structure and hierarchy

- [`visual-hierarchy.md`](visual-hierarchy.md) — priority, emphasis, reading order, action hierarchy, density, and anti-patterns.
- [`information-architecture.md`](information-architecture.md) — mental models, categories, navigation, information scent, search, taxonomy, orientation, and IA testing.
- [`progressive-disclosure.md`](progressive-disclosure.md) — deciding what is visible first, what can be deferred, and which disclosure mechanism fits the task.
- [`content-chunking.md`](content-chunking.md) — semantic chunks, headings, proximity, lists, forms, tables, dashboards, and avoiding card soup.
- [`functional-grouping.md`](functional-grouping.md) — grouping controls and content according to task, scope, Gestalt principles, and user mental models.
- [`nested-structural-layouts.md`](nested-structural-layouts.md) — app → workspace → page → panel → component hierarchy without endless nested containers.

### Space, alignment, scale, and attention

- [`spatial-hierarchy-prospacing.md`](spatial-hierarchy-prospacing.md) — spacing systems, density, internal/external space, component rhythm, and optical correction.
- [`proximity-and-whitespace-distribution.md`](proximity-and-whitespace-distribution.md) — relationship-first spacing, whitespace, density modes, forms, lists, tables, and text expansion.
- [`alignment-and-grid-structures.md`](alignment-and-grid-structures.md) — key lines, columns, gutters, margins, baseline alignment, responsive grids, and cross-screen continuity.
- [`contrast-and-scale.md`](contrast-and-scale.md) — size, weight, luminance, density, action contrast, target sizing, and restrained visual prominence.
- [`color-weight-and-dominance.md`](color-weight-and-dominance.md) — semantic color, brand-color restraint, status colors, surfaces, dark mode, high contrast, and data visualization.
- [`focus-and-attention-mapping.md`](focus-and-attention-mapping.md) — focal points, attention budget, competing cues, motion, imagery, errors, and keyboard focus.
- [`scannability-fields.md`](scannability-fields.md) — scan anchors, leading edges, headings, repeated anatomy, tables, forms, navigation, and search results.
- [`reading-patterns.md`](reading-patterns.md) — F-shaped, layer-cake, spotted, commitment, and Z-flow scanning without treating them as rigid templates.

### Typography and content

- [`typographic-hierarchy.md`](typographic-hierarchy.md) — semantic type roles, restrained type ramps, weights, line height, tracking, numerals, localization, font loading, and open-source font guidance.
- [`content-design-and-labeling.md`](content-design-and-labeling.md) — navigation labels, buttons, headings, errors, empty states, plain language, information scent, tone, and localization.

### Components and product systems

- [`component-craft.md`](component-craft.md) — production-quality buttons, inputs, selects, checkboxes, radios, switches, badges, cards, menus, tabs, sidebars, tables, dialogs, popovers, icon buttons, states, and component anti-patterns.
- [`design-tokens-and-theming.md`](design-tokens-and-theming.md) — raw/global tokens, semantic aliases, component tokens, light/dark/high-contrast themes, naming, and designer/developer parity.
- [`responsive-adaptation.md`](responsive-adaptation.md) — content-driven breakpoints, structural transformations, responsive grids, navigation, tables, forms, dialogs, zoom, and localization.
- [`accessibility-and-interaction.md`](accessibility-and-interaction.md) — semantic structure, keyboard access, focus, contrast, target size, zoom, text spacing, reflow, forms, status messages, reduced motion, and high-contrast modes.
- [`motion-and-feedback.md`](motion-and-feedback.md) — transitions, progress, loading, skeletons, optimistic UI, drag feedback, AI activity, reduced motion, and performance.

### Generated visual assets

- [`ui-asset-generation.md`](ui-asset-generation.md) — custom icons, illustrations, AI indicators, empty states, product objects, raster/vector decisions, transparency, micro-animation, asset families, exports, and accessibility.

## Typography choices

The typography skill includes open-source options that are suitable starting points when a product needs a font it can legally bundle or embed under the font's license:

- Inter — SIL Open Font License 1.1;
- IBM Plex — Open Font License;
- Noto Sans — Open Font License through the Google Fonts distribution.

Always keep the relevant license and verify the current terms before redistributing font files. Proprietary platform fonts should normally be used through the platform/system font stack unless their license explicitly permits redistribution.

## Source foundations

The pack synthesizes guidance from widely used interface-design systems, platform guidelines, usability research, and accessibility standards, including:

- Apple Human Interface Guidelines;
- Google Material Design 3;
- Microsoft Fluent 2;
- IBM Carbon Design System;
- Atlassian Design System;
- Shopify Polaris;
- Nielsen Norman Group usability research;
- W3C WCAG 2.2.

See [`SOURCES.md`](SOURCES.md) for the full source index and links.

The source documentation is not copied into this repository. The skills paraphrase and combine relevant principles into actionable design rules. When a platform-specific convention conflicts with generic advice, prefer the current official guidance for the target platform.

## Design philosophy

Design relationships before decoration.

Use hierarchy, proximity, alignment, typography, spacing, contrast, semantic color, clear language, familiar behavior, and restrained geometry to communicate structure.

Prefer the least visually heavy mechanism that solves the problem:

1. semantic structure;
2. spacing and proximity;
3. alignment;
4. typography;
5. color/contrast;
6. subtle surface or divider;
7. full container/elevation only when the interface actually needs it.

A professional interface should not need every element to be large, bold, rounded, shadowed, saturated, or placed inside a card.

## How an AI should use the pack

Do not load every skill blindly for every task. Select the files that match the design problem.

Examples:

- building a dashboard: visual hierarchy + spacing + grid + scannability + component craft + accessibility;
- designing a settings screen: IA + grouping + progressive disclosure + typography + component craft;
- building a responsive product shell: nested layouts + grid + responsive adaptation + accessibility;
- creating a landing hero: hierarchy + typography + reading patterns + attention mapping + asset generation;
- building a component library: component craft + tokens/theming + typography + spacing + accessibility;
- generating custom product visuals: asset generation + color dominance + hierarchy + motion when animated.

The final design should reconcile the selected skills into one system rather than applying each rule independently.

## Source priority when guidance conflicts

1. Accessibility and user-safety requirements.
2. Current target-platform conventions.
3. The product's established, coherent design system.
4. Task-specific usability evidence and user research.
5. General cross-platform design heuristics.

Numeric values from another design system are references, not universal laws. Preserve the reasoning behind the rule and adapt it to the product's context.
