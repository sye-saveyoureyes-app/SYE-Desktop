# SYE Desktop Website

Marketing pages for **SYE — Save Your Eyes** desktop app (Mac & Windows), aligned with [getsye.com](https://www.getsye.com).

## Pages

| Path | Description |
|------|-------------|
| `/desktop/` | Main landing — hero, features, presets, FAQ, download |
| `/desktop/mac/` | macOS download + requirements |
| `/desktop/windows/` | Windows download + requirements |

## Local preview

```bash
npx serve .
# or
python3 -m http.server 8080
```

Open [http://localhost:3000/desktop/](http://localhost:3000/desktop/) (serve) or [http://localhost:8080/desktop/](http://localhost:8080/desktop/) (Python).

## Download links

Mac and Windows download buttons on the platform pages use `#` placeholders. Replace with actual DMG / `.exe` URLs when builds are ready:

- `desktop/mac/index.html` — primary download button
- `desktop/windows/index.html` — primary download button

## Deploy

Static files only. Copy the repo contents into your getsye.com hosting (e.g. under `/desktop/`). Ensure `assets/`, `css/`, and `js/` are served at the site root alongside `desktop/`.

## Version

Desktop build: **v3.3.0-notify-presets** · May 2026
