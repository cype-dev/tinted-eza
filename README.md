# tinted-eza

A [tinted-theming](https://github.com/tinted-theming) template for [eza](https://github.com/eza-community/eza).

Only supports base16 for now.

## Usage
Add the following snippet to your [tinty](https://github.com/tinted-theming/tinty) `config.toml`
```toml
[[items]]
name = "tinted-eza"
path = "https://github.com/cype-dev/tinted-eza"
themes-dir = "themes"
hook = "cp -f %f ~/.config/eza/theme.yml"
supported-systems = ["base16"]
```

Afterwards, run `tinty sync` (or `tinty install`) and apply with `tinty apply <theme>`.

## Troubleshooting
If applying the theme doesn't seem to work, make sure the environment variables `LS_COLORS` and `EXA_COLORS` are unset, as those take precedence.

## Alternatives
As an alternative you can try the excellent [vivid](https://github.com/sharkdp/vivid) and accompanying [base16-vivid](https://github.com/tinted-theming/base16-vivid) to generate `LS_COLORS` with **tinty**.

Just add the following to your **tinty** `config.toml`
```toml
[[items]]
name = "tinted-vivid"
path = "https://github.com/tinted-theming/base16-vivid"
themes-dir = "themes"
hook = "cp -f %f ~/.config/vivid/themes/tinted.yml"
supported-systems = ["base16"]
```

and follow the [instructions](https://github.com/sharkdp/vivid?tab=readme-ov-file#usage) on the **vivid** repo on how to apply the theme.

## Screenshots
| `gruvbox` | `darkmoss` | `ayu` |
| --- | --- | --- |
| ![base16-gruvbox-dark-soft theme](https://i.imgur.com/4Us6MXZ.png) | ![base16-darkmoss theme](https://i.imgur.com/FOd032s.png) | ![base16-ayu-light theme](https://i.imgur.com/r5FjSJw.png) |

## Useful resources
Themes were built with [tinted-builder-rust](https://github.com/tinted-theming/tinted-builder-rust).
