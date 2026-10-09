# dr-opris.de · Vorab-Seite („Website im Aufbau“)

Stand 09.10.2026. Platzhalter, bis die vollständige Website aus `Persoenliche-Website-Opris/` fertig ist.

## Hochladen (IONOS)

Domain `dr-opris.de` liegt bei IONOS (registriert 04.08.2026, zeigt derzeit die IONOS-Standardseite).

1. IONOS-Kundencenter → **Hosting** → **SFTP & SSH**: Zugangsdaten (Server `access…webspace-host.com` oder `home…1and1-data.host`, Benutzer `u…`, Passwort) anzeigen bzw. setzen.
2. Mit Cyberduck, FileZilla oder `sftp` verbinden und **alle Dateien dieses Ordners außer LIESMICH.md** in das Verzeichnis laden, auf das die Domain zeigt (Standard: Hauptverzeichnis `/`; prüfen unter **Domains & SSL** → dr-opris.de → **Ziel/Verwendung**). Die versteckte `.htaccess` nicht vergessen.
3. **Domains & SSL** → dr-opris.de → SSL-Zertifikat aktivieren (IONOS-Standard, kostenlos), sonst schlägt die HTTPS-Umleitung fehl.
4. Prüfen: https://dr-opris.de, http://www.dr-opris.de (muss auf https://dr-opris.de umleiten).

Alternativ ohne SFTP: **Hosting** → **Webspace** → Dateimanager (WebspaceExplorer) im Browser, dort die Dateien hochladen.

## Inhalt

Eine Seite, alles inline (CSS im HTML, Schriften in `fonts/`). Impressum und Datenschutz als aufklappbare Abschnitte, Hoster IONOS SE ist eingetragen. Keine Cookies, keine Skripte.

## Livegang der vollständigen Website

Ordner `Persoenliche-Website-Opris/` komplett hochladen (überschreibt `index.html`, `.htaccess`, `robots.txt`, `favicon.svg`, `fonts/`). Anschließend die Sitemap `https://dr-opris.de/sitemap.xml` in der Google Search Console und bei Bing Webmaster Tools anmelden.
