# haakemusic.com – Website

## Was ist das?

Statische Website unter Domain `haakemusic.com` (custom domain).
Hostet Landing-Pages für Drone Pad und (geplant) NoteChart sowie Privacy-Policy.

## Technologie-Stack

- **Statisch**: reines HTML, kein Framework, kein Build-Step
- **Hosting**: GitHub Pages
- **Repo-Name**: `notebynote.github.io` (lokaler Ordner heißt `github-web`)
- **Domain**: `haakemusic.com` via `CNAME`-Datei

## Wichtige Dateien

| Datei | Zweck |
|---|---|
| `CNAME` | Custom-Domain-Verknüpfung (`haakemusic.com`) |
| `index.html` | Startseite |
| `dronepad.html` | Drone-Pad-Landingpage (Marketing) |
| `dronepad-app.html` | Drone-Pad-App-PWA-Variante (iOS-tauglich) |
| `notechart.html` | NoteChart-Landingpage |
| `patchdirector.html` | Patchdirector-Landingpage |
| `privacy.html` | Privacy Policy |
| `favicon.png` | Browser-Icon |
| `images/` | Bildressourcen (z. B. NoteChart-Screenshots) |

## Deploy-Workflow

GitHub Pages publiziert automatisch nach jedem `git push` auf `main`. Kein manueller Build, kein CI/CD-Schritt nötig.

```
git pull
# Änderungen machen
git add -A
git commit -m "Update zu xy"
git push
# → ~1-2 Minuten später ist haakemusic.com aktualisiert
```

## Deployment-Historie

- Aktuell live über `notebynote.github.io`-Repo
- Älteres, inaktives Repo `notebynote/drone-pad` enthält Website-Backup mit V44-Tags (Stand vor Migration)
- Früher gehostet via Netlify, später migriert zu GitHub Pages

## iOS-PWA-Aspekt

`dronepad-app.html` enthält PWA-Optimierungen (Touch-Targets, AudioContext-Unlock, Safe-Area-Insets) – fungiert als mobile Variante von Drone Pad. Vorherige Capacitor-Versuche wurden verworfen.

## Hinweis für Edits

Da Änderungen sofort live gehen, vor `git push` immer:
1. Im Browser lokal testen (Doppelklick auf HTML-Datei)
2. Erst dann pushen
