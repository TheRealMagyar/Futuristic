# Futuristic

Modern liquid-glass **ClearVision v7 preset** Vencord / Equicord / Vesktop / BetterDiscord-hoz. A cél: **jobb, mint a sima ClearVision** — mélyebb sötét, olvashatóbb kontraszt, frosted glass, és a [Vencord AI plugin](https://github.com/TheRealMagyar/Vencord-ai-plugin) (`vc-grokai-*`) teljesen a témához van igazítva.

Ez ugyanaz a forma, mint a hivatalos Sapphire / Amethyst preset: `main.css` + `vencord.css` import, majd a ClearVision `:root` változó-API.

Motor: [ClearVision v7.0.1 @ `8182251`](https://github.com/ClearVision/ClearVision-v7/tree/81822515a91db4b821e2573f635e80fec3e763a0) (Apache-2.0). Az extra CSS a `src/backend/_classes.scss` hash-eit használja ebből a commitból.

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
3. **Kapcsold ki** a hivatalos ClearVision témát. Ha mindkettő megy, duplán töltődik a motor.

Online import (ha a kliensed tud remote CSS-t):

```css
@import url("https://raw.githubusercontent.com/TheRealMagyar/Futuristic/main/Futuristic.theme.css");
```

(Cseréld a usernamet/repót, ha máshova pusholod.)

## Háttérkép

Alapból egy accent-tinted void gradient — nincs külső kép, azonnal üveges.

Fotóhoz írd át a `:root` blokkban:

```css
--background-image: url(https://example.com/your-image.jpg);
```

A repo `assets/futuristic-void.jpg` fájlja egy hozzá illő wallpaper. GitHubra push után:

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

Vagy írd át kézzel a `--main-color` / `--hover-color` sorokat.

## Csak az AI plugin

Ha meg akarod tartani a saját ClearVision / más témádat, és csak a plugin kinézetét akarod:

másold be: [`overrides/Futuristic-AI.override.css`](overrides/Futuristic-AI.override.css)

Vencord → Settings → **QuickCSS**.

Ez a fájl a `--main-color` értéket használja, ha a másik témád már beállítja (ClearVision igen).

## Mit ír felül a pluginból

A [styles.css](https://github.com/TheRealMagyar/Vencord-ai-plugin/blob/main/styles.css) összes felülete:

chat ablak (sidebar, thread, toolbar, bubbles, composer, send/stop, thinking/tools), chat-bar ikon, server-list harang, notification center, settings kártya, spinner / pulse.

## Miért jobb, mint a sima ClearVision

- Mélyebb onyx / midnight tónusok, nem a 2018-as kék sapphire.
- Kiválasztott channel: üveges tint + bal accent sáv, nem tömör kék téglalap.
- Popout / modal / input: backdrop-blur + vékony highlight border.
- Brand tokenek (`--brand-500`, mention, scrollbar) az accentre mennek.
- Az AI ablak nem „Discord default modal + idegen plugin”, hanem ugyanaz a glass nyelv.

## Fontos

- Internet kell az első betöltéshez (ClearVision CDN: `clearvision.github.io`).
- Discord Appearance-ben **Dark / Darker / Midnight** a szándékolt. Light működik, de a glass sötétre van hangolva.
- Ne kapcsold be egyszerre a hivatalos ClearVision-t.

## Kredit

- Skin + AI override: TheReal + Grok
- Coverage engine: [ClearVision v7](https://github.com/ClearVision/ClearVision-v7/tree/81822515a91db4b821e2573f635e80fec3e763a0) (Apache-2.0, lásd `NOTICE`)
- AI plugin: [TheRealMagyar/Vencord-ai-plugin](https://github.com/TheRealMagyar/Vencord-ai-plugin)
