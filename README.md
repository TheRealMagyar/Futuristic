<p align="center">
  <img src="assets/nebula.jpg" alt="Futuristic nebula wallpaper" width="100%">
</p>

<h1 align="center">Futuristic</h1>

<p align="center">
  Liquid-glass Discord theme — deep void, frosted chrome,<br>
  and a full restyle of the <a href="https://github.com/TheRealMagyar/Vencord-ai-plugin">Vencord AI plugin</a>.
</p>

<p align="center">
  <img alt="version" src="https://img.shields.io/badge/version-2.2.7-7c5cff?style=flat-square">
  <img alt="license" src="https://img.shields.io/badge/license-Apache%202.0-6b7280?style=flat-square">
  <img alt="clients" src="https://img.shields.io/badge/Vencord%20·%20Equicord%20·%20Vesktop%20·%20BetterDiscord-0c0c12?style=flat-square">
</p>

<p align="center">
  <a href="#install">Install</a> ·
  <a href="#wallpapers">Wallpapers</a> ·
  <a href="#colors">Colors</a> ·
  <a href="#settings">Settings</a>
</p>

`Futuristic.theme.css` is **settings only** — colors, wallpaper, fonts. Glass, AI chrome, and motion live in `engine/` and load from this repo.

Intended appearance: **Dark / Darker / Midnight**. Enable only this theme.

---

## Wallpapers

Default is an accent-tinted void gradient. Uncomment **one** wallpaper block at the bottom of `Futuristic.theme.css`.

<p align="center">
  <img src="assets/futuristic-void.jpg" alt="Void" width="49%">
  <img src="assets/nebula.jpg" alt="Nebula" width="49%">
</p>
<p align="center"><sub>Void · Nebula</sub></p>

<p align="center">
  <img src="assets/ice.jpg" alt="Ice" width="32%">
  <img src="assets/orbit.jpg" alt="Orbit" width="32%">
  <img src="assets/aurora.jpg" alt="Aurora" width="32%">
</p>
<p align="center"><sub>Ice · Orbit · Aurora</sub></p>

| Name | File | Look |
| --- | --- | --- |
| Void | [`assets/futuristic-void.jpg`](assets/futuristic-void.jpg) | Abstract purple bokeh |
| Nebula | [`assets/nebula.jpg`](assets/nebula.jpg) | Violet dust, dark center |
| Ice | [`assets/ice.jpg`](assets/ice.jpg) | Cyan / teal nebula |
| Orbit | [`assets/orbit.jpg`](assets/orbit.jpg) | Ringed planet and moon |
| Aurora | [`assets/aurora.jpg`](assets/aurora.jpg) | Glass shards and light ribbons |

Wallpaper and icon `url()`s go through jsDelivr. Discord blocks `raw.githubusercontent.com` in CSS images; the files are still the ones in this repo.

Or any HTTPS photo:

```css
--background-image: url("https://example.com/your-image.jpg");
```

`--background-shading-percent` (default `64%`): lower shows more of the photo through the glass. Wallpaper blocks already drop this to ~40%.

---

## Icons

Discord's own icons stay on by default (nothing extra is fetched).

A geometric set lives in [`assets/icons/`](assets/icons/). Uncomment the **Icons** block at the bottom of `Futuristic.theme.css` to swap home, discover, add, settings, inbox, help, nitro, shop, gift, emoji, gif, sticker, search, pins, threads, members, call, video, mute, and deaf.

Or turn on a single icon, for example:

```css
:root {
  --home-native: none;
  --home-icon: url("https://cdn.jsdelivr.net/gh/TheRealMagyar/Futuristic@main/assets/icons/home.svg");
}
```

---

## Install

1. Copy [`Futuristic.theme.css`](Futuristic.theme.css) into your themes folder:

   | Client | Folder |
   | --- | --- |
   | Vencord (Windows) | `%appdata%\Vencord\themes` |
   | Equicord (Windows) | `%appdata%\Equicord\themes` |
   | Vesktop (Windows) | `%appdata%\vesktop\themes` |
   | Vencord / Equicord (macOS) | `~/Library/Application Support/Vencord/themes` |
   | Vesktop (macOS) | `~/Library/Application Support/vesktop/themes` |
   | BetterDiscord | `%appdata%\BetterDiscord\themes` |

2. Discord → **Settings → Themes → Local Themes** → enable **Futuristic**.
3. Turn off any other full theme so they do not clash.

Online import:

```css
@import url("https://github.com/TheRealMagyar/Futuristic/raw/main/Futuristic.theme.css");
```

First load needs internet. The engine is fetched from GitHub.

---

## Colors

Uncomment **one** accent block in `Futuristic.theme.css`, or edit `--main-color` / `--hover-color`.

| Variant | Accent | Hover |
| --- | --- | --- |
| Violet (default) | `#7c5cff` | `#9b82ff` |
| Cyan | `#22d3ee` | `#67e8f9` |
| Emerald | `#34d399` | `#6ee7b7` |
| Rose | `#fb7185` | `#fda4af` |
| Amber | `#f59e0b` | `#fbbf24` |
| Pure black | `#e5e7eb` | `#ffffff` |

Status colors (`--online-color`, `--idle-color`, `--dnd-color`, …) sit in the same `:root` block.

---

## Settings

Everything users change is in [`Futuristic.theme.css`](Futuristic.theme.css).

| Token | What it does |
| --- | --- |
| `--main-color` / `--hover-color` | Accent |
| `--background-image` | Gradient or `url(...)` |
| `--background-shading-percent` | How much glass sits on the wallpaper |
| `--background-filter` | Saturate / brightness on photo wallpapers |
| `--user-popout-filter` / `--user-modal-filter` | Frost on profile popout / modal |
| `--main-font` / `--code-font` | UI and code (must be installed, except Orbitron) |
| `--futuristic-overlay-filter` | Menu frost — set to `none` if Discord stutters |

---

## AI plugin only

Keep another theme and only restyle the AI windows: paste [`overrides/Futuristic-AI.override.css`](overrides/Futuristic-AI.override.css) into Vencord → Settings → **QuickCSS**.

---

## Performance

Live blur is off by default (chat, menus, profiles). The wallpaper paints on one layer only.

To turn frost back on:

```css
--futuristic-overlay-filter: blur(14px) saturate(1.18);
--user-popout-filter: blur(16px) saturate(1.2) brightness(0.82);
--user-modal-filter: blur(18px) saturate(1.15) brightness(0.8);
```

---

## License

Apache 2.0. See [LICENSE](LICENSE) and [NOTICE](NOTICE).
