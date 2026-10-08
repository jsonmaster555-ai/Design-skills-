# UI Asset and Micro-Visual Generation

Use this skill when a product needs bespoke visual assets that belong inside the interface: custom icons, feature illustrations, AI indicators, empty-state graphics, avatars, product objects, micro-animations, onboarding visuals, or hero-supporting imagery.

This is not a generic image-generation skill. The generated asset must behave like part of the product’s design system.

## Core objective

Generate only visual material that improves recognition, communication, feedback, identity, or product character.

The best asset should feel native to the interface rather than pasted in afterward.

## Decide whether generation is appropriate

Use generated assets when a custom visual provides value that standard UI cannot.

Good candidates:

- product-specific feature icons;
- empty-state illustrations;
- branded abstract objects;
- AI activity indicators;
- onboarding illustrations;
- feature metaphors;
- mascots;
- custom file-type graphics;
- hero product objects;
- integration illustrations;
- micro-animation concepts.

Do not generate an image just because an empty area exists.

## Prefer standard interface symbols for universal actions

Use established icon systems for familiar actions such as:

- search;
- close;
- back/forward;
- add/remove;
- settings;
- share;
- download/upload;
- delete;
- menu;
- chevron;
- play/pause.

Replacing familiar controls with novel generated art reduces recognition and consistency.

Use custom imagery for concepts the standard icon system does not express well.

## Asset brief before generation

Define:

- role;
- placement;
- final display size;
- canvas/aspect ratio;
- background or transparency;
- light/dark context;
- palette;
- visual weight;
- style;
- geometry;
- material;
- perspective;
- lighting;
- level of detail;
- animation state if relevant;
- export format.

Do not generate first and decide usage later.

## Match the interface language

Inspect the existing UI before generating.

Match:

- saturation;
- contrast;
- stroke weight;
- corner language;
- depth/elevation;
- perspective;
- material;
- lighting direction;
- shadow softness;
- detail density;
- icon geometry;
- brand color usage.

A restrained monochrome product should not receive a saturated glossy 3D illustration unless the contrast is intentional.

## Generate for the final size

A 20px indicator and a 500px hero object require different detail.

Possible classes:

- 16–24px: icon/micro-indicator;
- 24–48px: feature/status icon;
- 48–96px: empty-state symbol;
- 120–240px: card/onboarding illustration;
- 300px+: hero/supporting product object.

Evaluate the result at actual display size, not only while zoomed in.

## Small assets require strong silhouettes

At small sizes:

- simplify geometry;
- remove tiny textures;
- avoid embedded text;
- reduce highlights;
- maintain clear negative space;
- keep visual mass consistent with sibling icons;
- avoid muddy semitransparent edges.

If a generated icon looks good at 1024px but becomes unreadable at 24px, it failed.

## Raster versus vector

Prefer vector/icon-system assets when precise geometry, scalability, or state manipulation is required.

Use generated raster imagery for bespoke illustration, texture, rendered objects, or expressive visuals.

Do not pretend a raster-generated image is a real SVG merely because it has flat colors.

If a generated design needs to become a production vector, redraw or trace it deliberately and clean the geometry.

## Transparency

Prefer transparent backgrounds when the asset must work inside native UI surfaces.

Check:

- clean alpha edges;
- no accidental matte/fringe;
- no baked white rectangle;
- readability on light and dark surfaces;
- sufficient internal contrast.

Create separate light/dark variants when one asset cannot maintain quality across both.

## Avoid generated text

Do not bake:

- button labels;
- headings;
- status text;
- prices;
- input fields;
- navigation labels;
- dynamic values

into generated imagery.

Render real text in the interface for sharpness, localization, accessibility, responsiveness, and editability.

## Avoid fake UI inside images

Do not generate screenshots of buttons, fields, cards, tables, or menus when those elements should be native components.

Use image generation for the asset only.

Build actual UI with code/components.

## Icon families

When generating multiple custom icons, establish a family specification:

- canvas size;
- occupied area;
- stroke/fill style;
- stroke width;
- corner radius;
- perspective;
- light source;
- color roles;
- detail level;
- optical weight.

One icon should not be thin outline while another is thick clay 3D unless they intentionally belong to different systems.

## Visual weight

Generated imagery can dominate the UI quickly.

Control:

- saturation;
- contrast;
- brightness;
- scale;
- shadow;
- depth;
- texture;
- detail.

A small status indicator should be quieter than a hero object.

An empty-state illustration should not overpower the primary recovery action.

## Product objects

Useful product metaphors include:

- document;
- key;
- lock;
- server;
- database;
- chip;
- terminal;
- folder;
- node/network;
- cloud;
- cube;
- model;
- connection.

Possible treatments:

- flat geometric;
- minimal 3D;
- soft 3D;
- clay;
- restrained metal;
- monochrome material;
- isometric;
- subtle skeuomorphism.

Choose treatment from the product language, not trend popularity.

## Restrained 3D

For neutral software, prefer:

- low saturation;
- simple geometry;
- controlled lighting;
- soft reflections;
- limited material complexity;
- uncluttered background;
- consistent camera angle.

Avoid glossy neon 3D as an automatic AI aesthetic.

## Empty states

An empty state should visually reinforce the missing concept.

Examples:

- no files → restrained file/folder object;
- no deployments → deployment/server object;
- no messages → conversation object;
- no projects → workspace/project symbol.

Always pair the visual with native text that explains the state and next action.

## Feature illustrations

Use simple metaphors for abstract features such as:

- model routing;
- memory;
- agents;
- tool calling;
- search;
- automation;
- knowledge;
- connections.

Create a consistent family rather than unrelated one-off art for each feature card.

## AI indicators

AI systems may need state visuals for:

- thinking;
- generating;
- searching;
- connecting;
- listening;
- processing;
- completing;
- waiting.

Avoid using the same generic sparkle for every AI function.

Possible restrained systems:

- orbiting points;
- evolving geometric mark;
- pulse;
- changing dot pattern;
- shifting abstract symbol;
- subtle brand mark animation.

Keep the indicator small when the process is background/supporting.

## Micro-animation

Animation should communicate:

- progress;
- state transition;
- completion;
- relationship;
- attention when necessary.

Prefer smooth, short, predictable loops.

Avoid:

- rapid flashing;
- constant distracting motion;
- large movement inside dense UI;
- animation without state meaning.

Respect reduced-motion preferences and provide a static equivalent where needed.

## Frame generation for animation

If the image system cannot output production animation directly:

1. establish a key visual;
2. define start/end state;
3. create consistent frames or a sprite/grid concept;
4. maintain camera, lighting, scale, and geometry;
5. implement motion in code or an animation tool;
6. test loop seams.

Do not generate unrelated frames and hope interpolation creates consistency.

## Asset consistency workflow

For a family of assets:

1. create one strong reference asset;
2. lock style language;
3. use that asset/style board as reference for siblings when the tool supports references;
4. generate siblings with matching composition constraints;
5. evaluate all assets side-by-side;
6. reject outliers;
7. normalize size and transparency in post-processing;
8. test in actual UI.

## Export guidance

Common production formats:

- SVG: true vector icons/illustrations;
- PNG: transparent raster asset;
- WebP/AVIF: compressed raster illustration where supported;
- frame sequence/sprite: animation production pipeline.

Provide suitable pixel density for target displays.

Do not ship unnecessarily huge source-resolution images into tiny UI slots.

## Accessibility

For decorative assets:

- keep them out of the accessibility tree or use empty alt text as appropriate to platform.

For informative assets:

- provide equivalent semantic text or accessible label outside the raster image.

Never require users to interpret color alone.

Avoid flashing content that violates accessibility thresholds.

Generated text is not an accessibility substitute for real text.

## Branding

Apple’s branding guidance emphasizes that brand expression should defer to content and use familiar interaction patterns.

Apply the same principle to generated assets:

- brand the product without taking over the product;
- use accent color judiciously;
- keep controls familiar;
- place expressive identity primarily in content/illustration where appropriate.

## Failure modes

### Random AI art

The asset looks attractive but unrelated to the interface.

Fix: regenerate from a precise asset brief derived from UI style.

### Over-detailed icon

Fix: simplify silhouette and evaluate at target size.

### Style drift

Fix: use reference assets and a shared family specification.

### Baked UI

Fix: regenerate only the illustration/object and build controls natively.

### Baked text

Fix: remove text and render it in the app.

### Hero dominance

Fix: reduce visual weight so the product message/action remains primary.

### Generic sparkle AI

Fix: create a product-specific state system.

## Evaluation checklist

- Does the asset communicate something useful?
- Is custom generation better than a standard icon?
- Does it match the UI’s style and density?
- Is it legible at final size?
- Is text kept native?
- Is UI kept native?
- Does transparency work on actual surfaces?
- Do sibling assets look like one family?
- Is visual weight proportional to importance?
- Is animation purposeful and reduced-motion safe?
- Is meaning available accessibly outside the image?

## Source foundations

This skill applies general design-system principles from Apple HIG, Fluent, Carbon, Material, WCAG, and product-branding guidance to generated UI assets. It also follows the broader Design Skills rules for hierarchy, spacing, typography, component familiarity, semantic color, and accessibility.

References:

- https://developer.apple.com/design/human-interface-guidelines/branding
- https://developer.apple.com/design/human-interface-guidelines/layout
- https://fluent2.microsoft.design/design-tokens
- https://fluent2.microsoft.design/accessibility
- https://m3.material.io/
- https://www.carbondesignsystem.com/
- https://www.w3.org/WAI/WCAG22/Understanding/
