# Futuristic

Liquid-glass Discord theme for Vencord, Equicord, Vesktop, and BetterDiscord. Deep dark tones, frosted glass, and a full restyle of the [Vencord AI plugin](https://github.com/TheRealMagyar/Vencord-ai-plugin) (`vc-grokai-*`).

Source: [https://github.com/TheRealMagyar/Futuristic](https://github.com/TheRealMagyar/Futuristic)

The engine CSS is loaded from this repository (`engine/main.css`, `engine/vencord.css`, `engine/betterdiscord.css`).

## Install

1. Copy `Futuristic.theme.css` into your themes folder:

   | Client | Folder |
   | --- | --- |
   | Vencord (Windows) | `%appdata%\Vencord\themes` |
   | Equicord (Windows) | `%appdata%\Equicord\themes` |
   | Vesktop (Windows) | `%appdata%\vesktop\themes` |
   | Vencord / Equicord (macOS) | `~/Library/Application Support/Vencord/themes` |
   | Vesktop (macOS) | `~/Library/Application Support/vesktop/themes` |
   | BetterDiscord | `%appdata%\BetterDiscord\themes` or `~/Library/Application Support/BetterDiscord/themes` |

2. Discord → **Settings → Themes → Local Themes** → enable **Futuristic**.
3. Disable any other full theme so they do not clash.

Online import:

```css
@import url("https://raw.githubusercontent.com/TheRealMagyar/Futuristic/main/Futuristic.theme.css");
```

## Background

The default is an accent-tinted void gradient.

To use a photo, set this in the `:root` block:

```css
--background-image: url(https://example.com/your-image.jpg);
```

Repo wallpaper:

```css
--background-image: url(https://raw.githubusercontent.com/TheRealMagyar/Futuristic/main/assets/futuristic-void.jpg);
```

`--background-shading-percent` (default `64%`): a lower value shows more of the wallpaper through the glass.

## Color variants

In `Futuristic.theme.css`, uncomment **one** block after `:root`:

| Variant | Accent |
| --- | --- |
| Violet (default) | `#7c5cff` |
| Cyan | `#22d3ee` |
| Emerald | `#34d399` |
| Rose | `#fb7185` |
| Amber | `#f59e0b` |
| Pure black | light gray accent, flatter void |

Or edit `--main-color` and `--hover-color` directly.

## AI plugin only

If you want to keep another theme and only restyle the AI plugin, paste [`overrides/Futuristic-AI.override.css`](overrides/Futuristic-AI.override.css) into Vencord → Settings → **QuickCSS**.

## Notes

- The first load needs internet (the engine is fetched from GitHub).
- Intended Discord appearance: **Dark / Darker / Midnight**.
- Do not enable another full theme at the same time.
