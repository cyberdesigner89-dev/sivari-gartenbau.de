# Sivari Gartenbau – Website (Premium-Remaster)

Statische Website für **Sivari Gartenbau**, Garten- und Landschaftsbau in Langenfeld.
HTML, CSS und JavaScript ohne Framework, ohne Build-Schritt, ohne externe Anfragen.

- Live (GitHub Pages): https://cyberdesigner89-dev.github.io/sivari-gartenbau.de/
- Repository: https://github.com/cyberdesigner89-dev/sivari-gartenbau.de

## Inhalt des Repositorys

```
/                          index.html, impressum.html, datenschutz.html, 404.html,
                           sitemap.xml, robots.txt, manifest.webmanifest, .nojekyll,
                           favicon.ico, apple-touch-icon.png, icon-192.png, icon-512.png,
                           social-preview.jpg, README.md
assets/css/                style.css
assets/js/                 main.js
assets/fonts/              Fraunces (variabel, normal + kursiv) und Manrope (variabel) als woff2
assets/img/original/       Originalbilder und Logos von sivari-gartenbau.de (AVIF + WebP, 480/800/1280 px)
assets/img/generated/      digital erzeugte Hintergründe (AVIF + WebP, Quer- und Hochformat, SVG-Höhenlinien, Papierstruktur)
```

Ordner, die beim Hochladen per Browser angelegt werden müssen (jeweils über die Upload-URL
`…/upload/main/<ordner>`): `assets/css`, `assets/js`, `assets/fonts`, `assets/img/original`, `assets/img/generated`.

## GitHub Pages aktivieren

1. Repository → **Settings → Pages**
2. *Source*: **Deploy from a branch**, Branch **main**, Ordner **/ (root)** → *Save*
3. Nach 1–2 Minuten ist die Seite unter https://cyberdesigner89-dev.github.io/sivari-gartenbau.de/ erreichbar.

Die leere Datei `.nojekyll` sorgt dafür, dass GitHub die Dateien unverändert ausliefert.

## Später: Umstellung auf die eigene Domain sivari-gartenbau.de (CNAME)

1. Im Repository unter **Settings → Pages → Custom domain** `sivari-gartenbau.de` eintragen und speichern.
   GitHub legt dabei automatisch eine Datei `CNAME` mit dem Inhalt `sivari-gartenbau.de` im Repository an.
2. Beim Domain-Anbieter (DNS) einrichten:
   - für `sivari-gartenbau.de` vier **A-Records**: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - optional **AAAA-Records**: `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`, `2606:50c0:8003::153`
   - für `www.sivari-gartenbau.de` einen **CNAME** auf `cyberdesigner89-dev.github.io`
   - Bestehende A-/CNAME-Einträge des alten Hostings vorher entfernen. E-Mail (MX-Einträge) **nicht** ändern.
3. Sobald die Domain geprüft ist: **Enforce HTTPS** aktivieren.
4. Absolute Adressen auf die neue Domain umstellen – überall `https://cyberdesigner89-dev.github.io/sivari-gartenbau.de/`
   durch `https://sivari-gartenbau.de/` ersetzen in:
   - `index.html`, `impressum.html`, `datenschutz.html`, `404.html` (canonical, `og:url`, `og:image`, JSON-LD)
   - `sitemap.xml` und `robots.txt`
5. Alle internen Links und Pfade sind relativ – sie funktionieren unter beiden Adressen ohne Änderung.
6. Optional: In der Google Search Console die neue Domain hinterlegen und `sitemap.xml` einreichen.

## Hinweise zum Inhalt

- Alle Firmendaten, Leistungen und Texte stammen von der bisherigen Website sivari-gartenbau.de.
  Es wurden keine Kundenstimmen, Bewertungen, Jahreszahlen, Preise oder Team-Namen ergänzt.
- „Seit über 20 Jahren“ und „mehr als 3.000 Anlagen“ beziehen sich ausdrücklich auf den **TeichMeister-Verbund**.
- Die generierten Hintergründe sind Stimmungsbilder und zeigen keine Projekte von Sivari Gartenbau.
- Das Anfrageformular sendet nichts an einen Server, sondern öffnet `https://wa.me/491773286283?text=…`.
- Impressum und Datenschutzerklärung wurden übernommen bzw. angepasst und sind **vom Inhaber rechtlich zu prüfen**.

## Lokal ansehen

```
python3 -m http.server 8000
# dann http://localhost:8000/ öffnen
```
