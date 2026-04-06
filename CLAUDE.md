# delightful-iterm2

iTerm2 color profiles using the Delightful OKLCH palette.

## Source of Truth

Token hex values come from [delightful-design-system](https://github.com/kylesnav/delightful-design-system). The generator has its own hardcoded hex palette — no monorepo imports.

## Build

```sh
node scripts/generate-profiles.mjs
```

Reads hex palette from the script itself, outputs `.itermcolors` XML files to `colors/`. Never edit the `.itermcolors` files directly — regenerate from the script.

## Key Files

- `scripts/generate-profiles.mjs` — Generator with embedded hex palette
- `colors/Delightful-Light.itermcolors`, `colors/Delightful-Dark.itermcolors` — Generated output

## Conventions

- Blue slots use cyan (no dedicated blue in Delightful).
- Palette values should match `delightful-ghostty` themes exactly — same OKLCH→hex mapping.
