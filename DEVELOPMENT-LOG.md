# Development log

Internal notes for meaningful changes to this personal theme.

## Current

### Repository changes

- Reoriented project identity around Wayfinder and Apache_Pine.
- Clarified the boundary between Sass sources, plain CSS fragments, and the
  generated Obsidian theme file.
- Added architecture, design-notes, and roadmap documentation.

### Cleanup

- Removed redundant and unreferenced legacy compiled CSS artifacts.
- Marked the npm package as private to prevent accidental publication.
- Removed remaining public support and sponsorship language.

### Design direction

- Established one canonical, predominantly dark Atlas appearance with
  parchment working surfaces.
- Established Windows as the primary platform and iPhone as a supported
  secondary platform.
- Recorded the dated UI mockups as directional references rather than strict
  specifications.
- Defined a CSS-first, optional-enhancement policy for future visual assets.

### Typography

- Replaced the inherited compressed heading sizes with a clear editorial scale.
- Established serif titles, headings, and interface structure alongside
  sans-serif body text and editing.
- Chose a system-font stack that works without bundled fonts on Windows and
  iPhone.

### Synced theme reconciliation

- Recovered the missing Wayfinder identity layer from the theme that had been
  active through Obsidian Sync.
- Moved its Atlas material, semantic color, shape, shadow, and motion tokens
  into maintained Sass sources.
- Preserved the newer enlarged heading scale and reconciled the recovered
  typography with the current serif-structure and sans-serif-writing decision.

### Checklists

- Restored strikethrough as the default treatment for completed tasks.
- Retained an opt-out in Style Settings for workflows that need completed task
  text to remain unmodified.

### Application shell

- Added the first canonical shell pass for the window frame, tabs, sidebars,
  ribbon, file explorer, vault profile, and status bar.
- Strengthened the dark wood and leather hierarchy with fine brass rules,
  quiet gradients, and restrained active states.
- Kept mobile treatments flatter and removed desktop-only framing at phone
  widths.

### Editor and reading surfaces

- Restricted serif typography to display roles and returned functional UI,
  metadata, dates, and navigation to the native sans-serif stack.
- Added tabular numerals to dense interface surfaces for clearer dates,
  counters, and aligned numeric information.
- Refined note titles, properties, tags, links, blockquotes, and list rhythm
  into a quieter catalog-and-annotation language.

### Controls and overlays

- Shifted normal reading text from yellowed parchment toward a more neutral
  warm white while preserving brass display accents.
- Unified fields, buttons, menus, suggestions, prompts, modals, popovers,
  tooltips, search, and supported editor toolbars.
- Kept controls conventional and high-contrast while expressing the Atlas
  through leather surfaces, fine brass borders, and restrained depth.

### Enchanted interactions

- Established hover as spell preparation, press and focus as activation, and
  persistent selection as a settled brass state.
- Added restrained rune-colored wake and activation treatments to tabs,
  navigation, toolbar commands, controls, menus, and links.
- Preserved reduced-motion and touch behavior without relying on hover alone.

### Heading hierarchy

- Increased separation between H1 through H4 and brightened H2 for clearer
  contrast against the dark reading surface.
- Differentiated H5 and H6 as compact label levels through small caps, weight,
  tracking, and restrained color rather than size alone.

### Tables

- Recast Markdown, Live Preview, and Dataview tables as fully framed
  cartographic ledgers with visible row and column rules.
- Added a distinct parchment-and-brass header, subtle alternating rows, and
  rune-lit row inspection.
- Applied magical preparation and activation states to table row, column, and
  drag controls.

### Workspace movement

- Replaced the flat accent-colored resize indicator with a cyan-and-aether
  enchanted seam that appears while a workspace boundary is engaged.
- Added a brighter activation state for dragging and a matching revealed-path
  treatment for docking targets.
- Disabled seam animation under reduced-motion preferences.

### Content artifacts

- Integrated the owner's complete semantic checkbox system as an authoritative
  build fragment.
- Recast callouts, code, progress bars, embeds, tags, and Dataview results as
  coordinated Atlas annotations, technical plates, instruments, mounted pages,
  classification seals, and enchanted indexes.
- Extended rune preparation and activation behavior to artifact controls while
  keeping dense informational surfaces quiet.

### Checkbox asset simplification

- Removed the large embedded ITS icon font from the checkbox system.
- Replaced temporary glyphs with native emoji while preserving every semantic
  task marker and its existing Markdown syntax.
- Centralized mappings so future custom Wayfinder SVG icons can replace emoji
  without rewriting checkbox behavior.
