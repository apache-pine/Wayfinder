# Wayfinder roadmap

## Established direction

- [x] Define Wayfinder's core design philosophy.
- [x] Establish one canonical, predominantly dark appearance.
- [x] Establish Windows as the primary platform and iPhone as secondary.
- [x] Preserve generated `theme.css` and explicit Sass source ordering.
- [x] Restore the locked local development dependencies.

## Foundation

- [ ] Confirm which color schemes are actively used.
- [ ] Confirm which community-plugin compatibility modules are still needed.
- [ ] Review Style Settings controls against the owner's actual configuration.
- [ ] Decide whether to keep expanded CSS or restore a separate minified build.
- [ ] Establish a repeatable Obsidian smoke-test checklist.
- [ ] Review inactive files in `src/scss/dev/`.
- [ ] Define semantic Wayfinder color and material tokens.
- [ ] Define typography, spacing, shape, elevation, and motion tokens.
- [ ] Decide how the canonical appearance should supersede Obsidian's light and
      dark mode selectors.
- [ ] Define an asset directory, naming convention, licensing record, and
      mobile fallback policy before adding bundled visual assets.

## Visual implementation

- [x] Build the first dark workspace shell and parchment surface hierarchy.
- [ ] Refine shell spacing and contrast from in-app Windows and iPhone review.
- [ ] Customize one subsystem at a time with Windows and iPhone checks.
- [ ] Establish controlled global ornament before high-expression dashboards.
- [x] Complete the first editor and reading-view typography and hierarchy pass.
- [ ] Refine editor spacing and content contrast from real-note review.
- [x] Complete the first navigation, tabs, ribbon, status bar, controls, menus,
      prompts, and modal pass.
- [x] Complete the first callout, code, checkbox, progress, embed, tag, and
      Dataview artifact pass.
- [ ] Refine artifact density and semantic colors from specimen-note review.
- [x] Complete the first Markdown and Dataview table treatment.
- [ ] Add CSS-native material details and ornament.
- [ ] Add authored assets only where they materially outperform CSS.
- [ ] Add reduced mobile treatments for expensive or crowded decoration.
- [ ] Record meaningful personal-theme changes in `DEVELOPMENT-LOG.md`.

## Later

- [ ] Review inherited alternate palettes after the canonical theme is stable.
- [ ] Build map, settlement, and landmark asset systems.
- [ ] Complete the design-system component and token references from the
      implemented theme.
