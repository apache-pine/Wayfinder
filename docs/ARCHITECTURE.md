# Theme architecture

## Build flow

```text
src/scss/index.scss
        |
        v
    Sass compiler
        |
        +-- src/fragments/license.css
        +-- src/fragments/plugin-compatibility.css
        +-- src/fragments/style-settings.css
        |
        v
theme.css
```

`theme.css` remains at the repository root because that is the filename
Obsidian expects for an installed theme. It is generated output even though it
cannot live in a conventional `dist/` directory.

The build produces expanded CSS. This is intentional for the current private
development workflow and should not be changed as part of unrelated work.

## Sass source groups

- `variables/` defines shared tokens and theme-level custom properties.
- `app/` styles Obsidian workspace and editor surfaces.
- `components/` styles reusable interface controls.
- `content/` styles rendered and edited note content.
- `features/` contains optional or cross-cutting theme capabilities.
- `mobile/` contains mobile-platform adjustments.
- `plugins-core/` contains Obsidian core-plugin compatibility.
- `plugins/` contains community-plugin compatibility.
- `color-schemes/` contains selectable palette implementations.
- `wayfinder/` contains the canonical Atlas identity and material treatments.
  It is loaded last so inherited palettes cannot override Wayfinder tokens.
- `dev/` contains inactive development helpers.

## Ordering

Sass modules are loaded explicitly by `src/scss/index.scss`. Preserve its broad
ordering unless a tested change requires otherwise:

1. Variables
2. Obsidian application surfaces
3. Components
4. Note content
5. Theme features
6. Mobile rules
7. Core plugins
8. Community plugins
9. Inherited color schemes
10. Canonical Wayfinder identity

CSS cascade order is behavior. Reordering imports is not a cosmetic cleanup and
must be tested as a functional change.

The files `plugins-core/publish.scss` and
`plugins-core/release-notes.scss` style built-in Obsidian interfaces. They are
not Wayfinder publishing scripts, release automation, or public-release
materials. They remain to avoid changing theme behavior.

## Plain CSS fragments

The files in `src/fragments/` are concatenated around the compiled Sass:

- `license.css` supplies the required license header.
- `plugin-compatibility.css` contains compatibility rules kept outside Sass.
- `checkboxes.css` contains the lightweight semantic checkbox map and temporary
  emoji symbols that will eventually be replaced by custom Wayfinder SVGs.
- `style-settings.css` contains Style Settings metadata and associated rules.

These are source inputs despite their `.css` extension.
