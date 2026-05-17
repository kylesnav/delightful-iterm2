# delightful-iterm2

iTerm2 color profiles using the Delightful terminal palette.

## Source of Truth

`scripts/generate-profiles.mjs` is the source for this repo. It embeds hex values derived from [delightful.build](https://delightful.build/) and emits `.itermcolors` files.

## Validate

```sh
node scripts/generate-profiles.mjs
git diff -- colors/
```

The generated files must match committed output unless the palette intentionally changed.

## Editing Rules

- Do not hand-edit `colors/*.itermcolors`; update `scripts/generate-profiles.mjs` and regenerate.
- Keep the palette aligned with `delightful-ghostty` for ANSI slots and special colors.
- Blue terminal slots use Delightful cyan because the design system has no separate blue family.
- README color tables must match the generator exactly.

## Screenshots

Screenshots should show real iTerm2 light and dark profiles. Refresh them when the generated profiles or recommended appearance settings visibly change.
