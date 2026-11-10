# mywald.de

Statische Webseite von [www.mywald.de](https://www.mywald.de): ein Onepager mit Foto und Links
zu meinen Profilen (Social Media, Software, Making und Grafik), dazu eine Kontaktseite –
jeweils auf Deutsch und Englisch. Kein Build: Dateien ändern, fertig.

- `index.html` – Startseite (Deutsch)
- `en/index.html` – Startseite (Englisch)
- `de/impressum.html`, `en/impressum.html` – Kontakt (E-Mail) und Haftungsausschluss
- `css/boilerplate.css` – Reset und Grundstile aus [HTML5 Boilerplate](https://html5boilerplate.com/) (2012)
- `css/base.css` – eigenes Layout
- `css/fonts/` – Calligraffiti (Schriftzug „my wald“) und Roboto Thin (Text)
- `img/` – Logo (Blätter) und Foto; `favicon.ico` im Hauptverzeichnis
- `js/` – jQuery 1.7.1, Modernizr 2.5.3 und die leeren Vorlagen `plugins.js`/`script.js`
  der Boilerplate

Eingecheckt ist nur, was die Seite ausliefert (`.gitignore` ist eine Whitelist) – so lässt sich
das Repo direkt in IntelliJ öffnen, ohne `.idea/` oder `*.iml` einzuchecken.

## Herkunft

Übernommen aus [archive/mywald2020](https://gitlab.mywald.de/archive/mywald2020) (Stand
`64c2c71`, Ordner `web/`), dort mit der ganzen Historie seit 2012 und allen Altlasten
(App-Engine-Projekt, Thurek-Seite, Profilbild-Seiten, Bildmaterial). Hier ist nur, was die
vier Seiten im Browser wirklich laden (per Netzwerkmitschnitt bei verschiedenen
Fensterbreiten ermittelt), dazu die übrigen Formate der beiden Schriften. Alle Dateien sind
byte-gleich mit dem, was www.mywald.de am 10.11.2026 auslieferte (S3/CloudFront).

`css/base.css` stammt noch vom braunen Design von 2012 (siehe
[archive/mywald2012](https://gitlab.mywald.de/archive/mywald2012)) und enthält Regeln für
Bilder und Schriften, die heute nicht mehr verwendet werden und hier fehlen (Holz, Blatt,
Bearpaw, Santana, vtks, Roboto Light). Der Browser lädt sie nicht, weil keine Seite diese
Regeln nutzt.

## Vorschau

Im Heimnetz unter https://pages.mywald.de/websites/mywald/ (GitLab Pages, `.gitlab-ci.yml`),
aktualisiert bei jedem Merge auf `main`. `CNAME` ist für GitHub Pages vorbereitet
(`www.mywald.de`); heute kommt die Seite noch aus S3/CloudFront.

## Rechte

Texte und Fotos: © Philip Maiwald, alle Rechte vorbehalten.

Calligraffiti und Roboto stehen unter der Apache License 2.0
(`css/fonts/Apache License Version 2.txt`). HTML5 Boilerplate, jQuery und Modernizr stehen
unter der MIT-Lizenz.
