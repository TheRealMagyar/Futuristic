# Futuristic

Liquid-glass Discord téma Vencord / Equicord / Vesktop / BetterDiscord-hoz. Mély sötét tónusok, frosted glass, és a [Vencord AI plugin](https://github.com/TheRealMagyar/Vencord-ai-plugin) (`vc-grokai-*`) teljesen a témához van igazítva.

A motor CSS ebből a repóból töltődik (`engine/main.css`, `engine/vencord.css`, `engine/betterdiscord.css`).

## Telepítés

1. Másold a `Futuristic.theme.css` fájlt a themes mappába:

   | Kliens | mappa |
   | --- | --- |
   | Vencord (Windows) | `%appdata%\Vencord\themes` |
   | Equicord (Windows) | `%appdata%\Equicord\themes` |
   | Vesktop (Windows) | `%appdata%\vesktop\themes` |
   | Vencord / Equicord (macOS) | `~/Library/Application Support/Vencord/themes` |
   | Vesktop (macOS) | `~/Library/Application Support/vesktop/themes` |
   | BetterDiscord | `%appdata%\BetterDiscord\themes` vagy `~/Library/Application Support/BetterDiscord/themes` |

2. Discord → **Settings → Themes → Local Themes** → kapcsold be a **Futuristic**-et.
3. Kapcsold ki a többi teljes témát, hogy ne ütközzenek.

Online import:

```css
@import url("https://raw.githubusercontent.com/TheRealMagyar/Futuristic/main/Futuristic.theme.css");
```

## Háttérkép

Alapból egy accent-tinted void gradient.

Fotóhoz írd át a `:root` blokkban:

```css
--background-image: url(https://example.com/your-image.jpg);
```

Repo wallpaper:

```css
--background-image: url(https://raw.githubusercontent.com/TheRealMagyar/Futuristic/main/assets/futuristic-void.jpg);
```

`--background-shading-percent` (alap `64%`): kisebb szám = több háttér látszik a glass mögött.

## Színvariánsok

A témafájl tetején, a `:root` után, kommentezd ki **egyet**:

| Variáns | accent |
| --- | --- |
| Violet (alap) | `#7c5cff` |
| Cyan | `#22d3ee` |
| Emerald | `#34d399` |
| Rose | `#fb7185` |
| Amber | `#f59e0b` |
| Pure black | világos szürke accent, laposabb void |

Vagy írd át a `--main-color` / `--hover-color` sorokat.

## Csak az AI plugin

Ha meg akarod tartani egy másik témádat, és csak a plugin kinézetét akarod:

másold be: [`overrides/Futuristic-AI.override.css`](overrides/Futuristic-AI.override.css)

Vencord → Settings → **QuickCSS**.

## Fontos

- Internet kell az első betöltéshez (a motor a GitHubról jön).
- Discord Appearance-ben **Dark / Darker / Midnight** a szándékolt.
- Ne kapcsold be egyszerre egy másik teljes témát.
