# Design Skills — Source Index

Design Skills is a synthesis of established interface-design systems, usability research, accessibility standards, and open-source typography resources.

The skill files paraphrase and operationalize principles rather than copying source documentation. When a platform has a specific convention, prefer that platform’s current official documentation over generic advice in this repository.

## Primary design systems and guidelines

### Apple Human Interface Guidelines

Used for platform familiarity, layout, hierarchy, accessibility, inclusion, writing, branding, typography, motion, and component behavior.

- HIG home: https://developer.apple.com/design/human-interface-guidelines/
- Layout: https://developer.apple.com/design/human-interface-guidelines/layout
- Accessibility: https://developer.apple.com/design/human-interface-guidelines/accessibility
- Inclusion: https://developer.apple.com/design/human-interface-guidelines/inclusion
- Typography: https://developer.apple.com/design/human-interface-guidelines/typography
- Writing: https://developer.apple.com/design/human-interface-guidelines/writing
- Branding: https://developer.apple.com/design/human-interface-guidelines/branding
- Motion: https://developer.apple.com/design/human-interface-guidelines/motion

### Google Material Design 3

Used as a reference for component systems, semantic design roles, typography, color, motion, adaptive layout, and platform-neutral UI patterns.

- Material 3: https://m3.material.io/
- Components: https://m3.material.io/components
- Typography: https://m3.material.io/styles/typography/overview
- Color: https://m3.material.io/styles/color/overview
- Motion: https://m3.material.io/styles/motion/overview

### Microsoft Fluent 2

Used heavily for spacing, layout, grids, typography, tokens, accessibility, component anatomy, and cross-platform behavior.

- Fluent 2: https://fluent2.microsoft.design/
- Layout: https://fluent2.microsoft.design/layout
- Typography: https://fluent2.microsoft.design/typography
- Accessibility: https://fluent2.microsoft.design/accessibility
- Design tokens: https://fluent2.microsoft.design/design-tokens
- Design resources: https://fluent2.microsoft.design/get-started/design

### IBM Carbon Design System

Used heavily for spacing systems, geometric rhythm, grids, density, product layouts, hierarchy, and repeatable design foundations.

- Carbon: https://www.carbondesignsystem.com/
- Spacing: https://www.carbondesignsystem.com/building-blocks/foundations/spacing/overview
- 2x Grid overview: https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/overview
- 2x Grid guidelines: https://www.carbondesignsystem.com/building-blocks/foundations/2x-grid/guidelines

### Atlassian Design System

Used for scalable product typography, accessibility-aware foundation rules, tokens, and enterprise-product design patterns.

- Atlassian Design: https://atlassian.design/
- Typography: https://atlassian.design/foundations/typography-beta/applying-typography/
- Accessibility: https://atlassian.design/foundations/accessibility/

### Shopify Polaris

Used for semantic color, status communication, accessibility, data-heavy product UI, and merchant/productivity patterns.

- Polaris: https://polaris.shopify.com/
- Color: https://polaris.shopify.com/design/colors

## Usability and human-behavior research

### Nielsen Norman Group

Used for information architecture, information scent, progressive disclosure, visual scanning, Gestalt grouping, proximity, similarity, and web usability research.

- Information scent: https://www.nngroup.com/articles/information-scent/
- IA mistakes / labeling: https://www.nngroup.com/articles/3-ia-mistakes/
- Progressive disclosure: https://www.nngroup.com/articles/progressive-disclosure/
- Proximity principle: https://www.nngroup.com/articles/gestalt-proximity/
- Similarity principle: https://www.nngroup.com/articles/gestalt-similarity/
- Text scanning patterns: https://www.nngroup.com/articles/text-scanning-patterns-eyetracking/
- F-shaped scanning: https://www.nngroup.com/articles/f-shaped-pattern-reading-web-content/
- Visual design: https://www.nngroup.com/articles/good-visual-design/

## Accessibility standard

### W3C WCAG 2.2

Used as the accessibility baseline for semantic relationships, meaningful sequence, contrast, text resizing, reflow, text spacing, keyboard access, focus, target size, dragging, motion, labels, errors, status messages, and predictable navigation.

- Understanding WCAG 2.2: https://www.w3.org/WAI/WCAG22/Understanding/
- Text spacing: https://www.w3.org/WAI/WCAG22/Understanding/text-spacing.html
- Target size minimum: https://www.w3.org/WAI/WCAG22/Understanding/target-size-minimum
- Focus appearance: https://www.w3.org/WAI/WCAG22/Understanding/focus-appearance

## Open-source typography references

### Inter

Interface-focused type family licensed under SIL Open Font License 1.1.

- https://github.com/rsms/inter

### IBM Plex

Open-source family with Sans, Serif, Mono, and Condensed variants, distributed under the Open Font License.

- https://github.com/IBM/plex

### Noto Sans

Broad-language family. Google Fonts metadata identifies Noto Sans as OFL licensed.

- https://github.com/google/fonts/tree/main/ofl/notosans

## How to use these sources

When guidance conflicts:

1. Accessibility and user safety requirements come first.
2. Follow the target platform’s native conventions for platform-specific behavior.
3. Follow the product’s established design system when it is coherent and accessible.
4. Use usability research to evaluate whether the pattern supports the task.
5. Treat numeric values from another design system as references, not universal constants.
6. Preserve semantic intent when adapting a pattern to another platform.

## Research principle

Do not cargo-cult any design system.

Apple, Material, Fluent, Carbon, Atlassian, and Polaris solve different product and platform problems. The goal of Design Skills is to extract durable reasoning patterns—hierarchy, grouping, predictability, accessibility, density, semantic tokens, familiar behavior, and content clarity—then apply them according to the current product’s context.
