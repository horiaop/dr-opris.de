# dr-opris.de · Vorab-Seite („Website im Aufbau“)

Stand 09.10.2026. Platzhalter, bis die vollständige Website aus `Persoenliche-Website-Opris/` fertig ist.

## Hosting: GitHub Pages

- Repository: https://github.com/horiaop/dr-opris.de (Branch `main`, Wurzelverzeichnis). Dieser Ordner ist das lokale Git-Repository.
- GitHub Pages ist aktiv, Custom Domain `dr-opris.de` (Datei `CNAME`). Nach jedem `git push` baut GitHub die Seite in etwa einer Minute neu.
- Domain und DNS liegen bei IONOS (Vertrag „IONOS Domain (Zusatz-Domain)“, kein IONOS-Webspace). Die MX-/TXT-Records für Google Workspace nicht anfassen.
- HTTPS: Sobald die DNS-Records stimmen, stellt GitHub automatisch ein Let's-Encrypt-Zertifikat aus. Danach im Repository unter Settings → Pages „Enforce HTTPS“ einschalten (oder `gh api -X PUT repos/horiaop/dr-opris.de/pages -F https_enforced=true`).

### DNS-Records bei IONOS (Domains & SSL → dr-opris.de → DNS)

| Typ | Hostname | Wert |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |
| CNAME | www | horiaop.github.io |

Die IONOS-Standardrecords A `217.160.0.144` und AAAA `2001:8d8:100f:f000::200` („Default Site“) ersetzen oder deaktivieren. Prüfen mit `dig +short dr-opris.de` (muss die vier 185.199.x.153 liefern).

## Aktualisieren

Dateien ändern, dann im Ordner:

```
git add -A && git commit -m "Beschreibung" && git push
```

## Inhalt

Eine Seite, alles inline (CSS im HTML, Schriften in `fonts/`). `404.html` ist eine Kopie der Startseite. Impressum und Datenschutz als aufklappbare Abschnitte; als Hoster ist GitHub, Inc. eingetragen.

## Livegang der vollständigen Website

Inhalt von `Persoenliche-Website-Opris/` (ohne `docs/`, `assets/`, `LIESMICH.md`, `.htaccess`) in dieses Repository kopieren, `CNAME` behalten, committen und pushen. Anschließend die Sitemap `https://dr-opris.de/sitemap.xml` in der Google Search Console und bei Bing Webmaster Tools anmelden.
