# Wayfinder

Wayfinder is Apache_Pine's private, personal-use Obsidian theme. It is not
prepared for marketplace submission, package publication, external support, or
broad distribution. The repository is organized only for local development and
gradual customization while preserving a stable, known-good build.

## Development

```sh
npm ci
npm run build
```

Use `npm run dev` to rebuild when files under `src/` change. When `HOME` and
`OBSIDIAN_PATH` are set in `.env`, each build also copies `theme.css` into the
configured vault.

`theme.css` is generated. Make changes in `src/`, then rebuild; do not edit the
generated file directly.

## Repository map

- `src/scss/index.scss` — ordered Sass entry point.
- `src/scss/` — theme implementation grouped by responsibility.
- `src/fragments/` — plain CSS appended to the compiled Sass output.
- `theme.css` — generated theme file loaded by Obsidian.
- `build.js` — build and watch script.
- `manifest.json` — Obsidian theme metadata.
- `docs/ARCHITECTURE.md` — build flow and source-folder responsibilities.
- `docs/DESIGN-NOTES.md` — future design decisions and constraints.
- `ROADMAP.md` — maintenance and customization backlog.
- `DEVELOPMENT-LOG.md` — private repository change notes.

## Working agreement

- Keep source changes in `src/`.
- Keep `src/scss/index.scss` explicit so source order remains reviewable.
- Rebuild and compare `theme.css` after structural refactors.
- Record deliberate visual decisions in `docs/DESIGN-NOTES.md`.
- Preserve license notices when moving or adapting existing code.

## Legal note

Upstream MIT copyright notices and third-party palette attribution remain in
the source and generated theme because Wayfinder derives from licensed work.
They identify the relevant code's copyright holders; they are not Wayfinder
authorship, sponsorship, support, or promotional material. Current Wayfinder
authorship is Apache_Pine.
