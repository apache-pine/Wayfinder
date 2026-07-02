# Design notes

This file records implementation-level decisions for Wayfinder. The broader
intent lives in `design and philosophy/`; these notes translate that intent
into constraints that can be applied and tested in the theme.

## Current direction

- Wayfinder has one canonical appearance rather than separate light and dark
  themes.
- The canonical appearance is predominantly dark, with lighter parchment
  surfaces used where they improve reading, hierarchy, or the artifact
  metaphor.
- Windows desktop is the primary platform. iPhone is a supported secondary
  platform and should retain a coherent, usable experience even when expensive
  ornament or optional assets are reduced.
- The two dated UI mockups are directional references, not pixel-perfect
  specifications. The June mockup is a useful restraint and layout reference;
  the July mockup explores richer materials and component detail.
- Ornament is allowed throughout the interface, but its intensity should
  respond to frequency and information density. Frequently used controls and
  long-form work surfaces remain quieter than maps and dashboards.
- Wayfinder is a personal theme. Maintainability and the owner's workflow take
  precedence over marketplace conventions or broad configuration support.

## Visual hierarchy

1. Dark wood, charcoal, iron, or leather establish the surrounding workspace.
2. Parchment and aged paper establish reading and working surfaces.
3. Ink establishes content and hierarchy.
4. Brass, bronze, copper, and wax identify structure, emphasis, and status.
5. Luminous magical colors identify dynamic, revealed, connected, or otherwise
   impossible behavior.

Magic is a semantic layer, not a general accent treatment. Static controls
should not glow merely to appear fantastical.

## Typography

- Sustained writing and body copy use a clean sans serif.
- Interface labels, note titles, and headings use a restrained serif. This
  gives structural text an atlas character while keeping prose comfortable.
- The default cross-platform pairing uses system fonts: Georgia for structure
  and the native Windows/iOS sans-serif stack for writing.
- Note titles must be visually dominant, and heading levels must form a real
  descending scale. No heading level should be smaller than body text by
  default.
- Decorative or runic fonts remain reserved for rare labels and authored
  artifacts; they are not appropriate for ordinary navigation or prose.

## Implementation direction

- Introduce semantic Wayfinder tokens before substantial component restyling.
  Map those tokens to Obsidian variables rather than embedding material colors
  independently in each component.
- Prefer CSS for borders, rules, gradients, shadows, simple grain, geometric
  ornament, and interaction states.
- Use image assets when CSS cannot reproduce the needed authored detail
  economically, such as illustrations, maps, seals, complex engravings, or
  convincing irregular material textures.
- Treat assets as optional enhancement where practical. Core navigation,
  focus, status, and content meaning must survive a failed or omitted asset.
- Keep asset dimensions and file sizes conservative, and provide reduced or
  omitted decoration for mobile where it improves performance or clarity.
- Preserve inherited features and compatibility modules until they are
  reviewed deliberately; do not assume every inherited option belongs in the
  final canonical theme.

## Accessibility and usability

- Long-form text, code, tables, and task lists take priority over texture and
  ornament.
- Focus and selection must remain visible without relying only on color.
- Meaning must not depend on background images.
- Respect reduced-motion preferences.
- Avoid fixed-size ornament that clips controls at narrow mobile widths.
- Texture must not materially reduce text contrast.

## Interaction state language

- Hover represents magical preparation: the Atlas senses intent and a dormant
  path, tool, or rune begins to wake.
- Press and keyboard focus represent activation, using a brighter but brief
  rune-colored response.
- Persistent selection represents settled state and returns to physical brass
  rather than remaining luminous.
- Dense informational content does not glow merely because the pointer crosses
  it. Magic is reserved for actionable controls, paths, and focus.
- Reduced-motion mode preserves state color and contrast without animated
  transitions. Touch interfaces emphasize press and focus because hover is not
  available.

## Decision template

For each future decision, record:

- Date and scope
- Goal
- Chosen approach
- Alternatives considered
- Affected tokens or source modules
- Light, dark, desktop, and mobile verification
- Accessibility considerations

## Open questions

- Which inherited color schemes and optional features are actually used?
- Which community plugins are part of the owner's real compatibility baseline?
- Which fonts and decorative assets will be bundled, and under what licenses?
- Which surfaces should use actual parchment assets rather than CSS treatment?
- What repeatable Windows and iPhone smoke-test vault should be used after
  larger changes?
