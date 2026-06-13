# Deploy derhupo.at

Statische Seite, kein Build-Schritt nötig. Deployment via Plesk Dateimanager.

## Dateien auf Server hochladen

1. **Plesk öffnen** → Websites & Domains → derhupo.at → **Dateimanager**

2. **Zu `httpdocs/` navigieren**

3. **Hosttech-Placeholder entfernen:**
   - `index.html` (Inhalt: "Hier entsteht eine neue Website") löschen
   - Alle anderen Placeholder-Dateien löschen

4. **Dateien hochladen** (Upload-Button oder Drag & Drop):
   - `index.html`
   - Ordner `assets/` mit `tokens.css`

5. **HTTPS prüfen:**
   `https://derhupo.at` im Browser öffnen → sollte SSL-Zertifikat von Hosttech/Let's Encrypt haben

## Spätere Änderungen

Einfach die geänderten Dateien via Dateimanager ersetzen. Kein git pull, kein Build.

## Optionale GitHub Pages Alternative

Das Repo enthält eine `CNAME`-Datei mit `derhupo.at`. Falls Hosttech-Hosting
wegfällt, kann die Seite direkt über GitHub Pages deployed werden:
- Repo auf GitHub: Settings → Pages → Branch: main, Folder: / (root)
- DNS: CNAME-Record `derhupo.at` → `hubertpeer-svg.github.io`
