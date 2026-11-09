# Cita colors for lsd

An lsd color theme that uses only the 16 terminal colors. It follows the Cita iTerm themes in light and dark mode.

The default lsd theme uses fixed 256-color codes, like pale yellow for the user and size, and bright green for recent dates. They ignore the terminal palette, so they are hard to read on Cita Light.

## Files

- `config.yaml` turns on the custom theme.
- `colors.yaml` maps each lsd part to a terminal color from 0 to 15.

## Install

```sh
mkdir -p ~/.config/lsd
cp config.yaml colors.yaml ~/.config/lsd/
```

If you already have `~/.config/lsd/config.yaml`, add this to it instead of copying the file:

```yaml
color:
  theme: custom
```

## Colors

| Part | Color |
| --- | --- |
| User | 3, yellow |
| Group | 8, gray |
| Sizes | 6 small, 3 medium, 1 large |
| Dates | 10 last hour, 2 last day, 6 older |
| Inode and links | 13, bright magenta |
| Read, write, exec | 2, 3, 1 |
| Empty and invalid | 8, gray |

## Test

```sh
lsd -alhliS
```

Every color in the output should come from the iTerm preset.
