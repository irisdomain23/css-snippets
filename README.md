# css-snippets

Three CSS files' worth of things I stopped re-deriving. No build step, no framework, no
class-name system to buy into — copy the block you need and delete the rest.

Each snippet carries a comment about *why* it is written that way, because the reason is
usually the part I forget: why `min()` is inside the `minmax()`, why fading to `transparent`
produces a grey ghost, why a dark-mode shadow cannot be the light-mode one.

## Files

| File | Contents |
| --- | --- |
| `layout.css` | Stack, auto-grid, sidebar, prose column with full-bleed escapes, sticky footer, cluster, aspect-ratio frame, contained scroll area |
| `gradients.css` | Oklab interpolation, scrims without the grey ghost, gradient text and borders, mesh backgrounds, a banding fix, animated `@property` angle |
| `dark-mode.css` | `color-scheme` tokens, system default with an explicit override, elevation that inverts, image dimming, forced-colors handling |

## Usage

Copy the block, or import the file:

```css
@import url("layout.css");
```

Most snippets are tuned through custom properties, so you can adjust them without editing the
rule:

```css
.auto-grid {
  --grid-min: 22rem;
  --grid-gap: 2rem;
}
```

## Browser support

Written against baseline features as of 2025: `:has()`, `aspect-ratio`, `svh`,
`scrollbar-gutter`, `@property`, and `in oklab` interpolation. Two snippets ship an explicit
fallback (`.gradient-clean`, `.gradient-text`); the rest degrade to something plain rather
than something broken. If you support older browsers, check the comments before copying —
they say what breaks first.

## Licence

MIT.
