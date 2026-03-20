# PatziLabs Website – GitHub Pages Setup

## Struktur

```
patzilabs-site/
├── index.html              ← Startseite (App-Übersicht)
├── style.css               ← Gemeinsames Design
├── apps/
│   └── plc-dataswap/
│       ├── privacy.html    ← Datenschutzerklärung
│       └── support.html    ← Support & FAQ
│   └── naechste-app/       ← (später: nächste App)
│       ├── privacy.html
│       └── support.html
```

## Einrichtung auf GitHub Pages

### Option A: Eigenes Repo (empfohlen)

1. Neues Repo auf GitHub erstellen: `patzilabs.github.io`
   (EXAKT so benennen – mit deinem GitHub-Usernamen als Prefix!)

   Falls dein GitHub-User `prohrweck-hub` ist:
   → Repo-Name: `prohrweck-hub.github.io`
   → URL wird: `https://prohrweck-hub.github.io/`

2. Alle Dateien aus diesem Ordner in das Repo pushen:
   ```bash
   cd patzilabs-site
   git init
   git add .
   git commit -m "PatziLabs Website"
   git branch -M main
   git remote add origin https://github.com/prohrweck-hub/prohrweck-hub.github.io.git
   git push -u origin main
   ```

3. GitHub Pages ist bei `*.github.io` Repos automatisch aktiv.

4. URLs:
   - Startseite: `https://prohrweck-hub.github.io/`
   - Privacy: `https://prohrweck-hub.github.io/apps/plc-dataswap/privacy.html`
   - Support: `https://prohrweck-hub.github.io/apps/plc-dataswap/support.html`

### Option B: Unterordner im App-Repo

1. Im `plc-dataswap` Repo einen `docs/` Ordner erstellen
2. Alle Dateien dort reinlegen
3. Repo Settings → Pages → Source: "Deploy from branch" → `/docs`
4. URL wird: `https://prohrweck-hub.github.io/plc-dataswap/`

### Option A ist besser weil:
- Die URL sauberer ist (kein App-Name in der Domain)
- Du alle Apps unter einer Domain hast
- Spätere Apps einfach als Unterordner dazukommen

## Im Google Play Store eintragen

Diese URL als Privacy Policy angeben:
```
https://prohrweck-hub.github.io/apps/plc-dataswap/privacy.html
```

Diese URL als Support/Website angeben:
```
https://prohrweck-hub.github.io/apps/plc-dataswap/support.html
```

## Neue App hinzufügen (später)

1. Neuen Ordner erstellen: `apps/neue-app/`
2. `privacy.html` und `support.html` aus plc-dataswap kopieren und anpassen
3. In `index.html` eine neue App-Card hinzufügen (Template ist auskommentiert)
4. Pushen – fertig.
