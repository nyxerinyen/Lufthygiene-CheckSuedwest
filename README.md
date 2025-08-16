# Lufthygiene Südwest – Static Site (GitHub Pages ready)

## Dateien
- `index.html` – Startseite
- `Colors.css`, `Fonts.css`, `Styles.css` – Stylesheets
- `CNAME.sample` – Vorlage für eigene Domain (optional)

## Veröffentlichen auf GitHub Pages
1. Neues Repo anlegen (z. B. `lufthygiene-suedwest`), diese 4–5 Dateien hochladen.
2. **Settings → Pages**: Source = `main`/`master`, Folder = `/ (root)` → Save.
3. Seite erscheint unter `https://<username>.github.io/<repo>/`.

## Eigene Domain verbinden (United Domains)
### Variante A – Subdomain (www.deine-domain.de)
- In GitHub Pages unter **Custom Domain**: `www.deine-domain.de` eintragen.
- Bei United Domains **CNAME** erstellen:
  - Name/Host: `www`
  - Ziel/Value: `<username>.github.io`
- Optional Weiterleitung (301) von `deine-domain.de` → `www.deine-domain.de` aktivieren.

### Variante B – Apex-Domain (deine-domain.de)
- In GitHub Pages **Custom Domain**: `deine-domain.de` eintragen.
- Bei United Domains **A-Records** setzen (4 Einträge):
  - 185.199.108.153
  - 185.199.109.153
  - 185.199.110.153
  - 185.199.111.153
- Optional zusätzlich: `www` als CNAME → `<username>.github.io`

> Nach DNS-Änderungen kann es 1–24h dauern. Danach `Enforce HTTPS` aktivieren.

## CNAME-Datei (optional im Repo)
Wenn die Domain feststeht, erstelle eine Datei `CNAME` **ohne Endung**, die NUR diese Zeile enthält:
```
deine-domain.de
```
GitHub setzt dann automatisch die Domain & Zertifikate.
