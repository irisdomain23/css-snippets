<div align="center">

# css-snippets

**Layout primitives that still work when the content does not cooperate.**

[![license](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)

</div>

## About

Each snippet is a few rules of modern CSS (grid / flex / `:has()`) with
`clamp()`-based spacing and no class names that clash. They are written for
content that is longer, shorter, or in another language than the mockup —
the layout rules are what holds up rather than a fixed pixel grid.

## Quick start

```bash
git clone https://github.com/irisdomain23/css-snippets
# link the file you need:
# @import url("./snippets/cluster.css");
```

## Configuration

| Key | Description |
| --- | --- |
| `--space` | stack/cluster gap, defaults to `1rem` |
| `--measure` | line length cap for prose, defaults to `65ch` |
| `--breakout` | full-bleed width for images inside prose |
## Roadmap

- [ ] RTL verification pass
- [ ] Container-query variants
- [ ] Visual regression snapshots

## Contributing

Issues and pull requests are welcome. Please keep changes small and focused,
and add a test for any behaviour change — every repository here ships with a
runnable test suite and no third-party dependencies, so CI is just
`python3 -m unittest` / `bash test_*.sh`.

## License

[MIT](LICENSE)
