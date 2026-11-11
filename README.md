# mywald.de

Statische Webseite von [www.mywald.de](https://www.mywald.de): eine kleine Visitenkarte mit Foto
und Links zu meinen Profilen – kein Framework, kein JavaScript, kein Build. Änderungen direkt in
`index.html`.

Das Thema ist ein Wortspiel: Maiwald → „my wald“. Deshalb oben ein Blätterdach aus Efeu, das sich
leicht wiegt (aus bei „Bewegung reduzieren“), Efeublätter als Anstecker am Foto und als Zeichen vor
jedem Link. Hell oder dunkel je nach Systemeinstellung; unten in der Fußzeile lässt es sich
umschalten (ohne JavaScript: eine Checkbox und `:has()`, die Wahl gilt nur bis zum Neuladen).

- `index.html` – Inhalt; oben das Efeublatt als SVG-Symbol `#efeu`, das überall wiederverwendet
  wird. „Kontakt und Datenschutz“ ist ein HTML-`popover`, das der Browser selbst öffnet und
  schließt
- `css/mywald.css` – Layout und Farben (oben die Farbvariablen, je mit `light-dark(hell, dunkel)`)
- `fonts/calligraffiti.woff2` – Schriftzug „my wald“; nur eine Teilmenge (Buchstaben m, y, w, a,
  l, d), erzeugt mit
  `pyftsubset Calligraffiti-webfont.ttf --text="mywaldMYWALD" --flavor=woff2` aus der alten Seite
  ([archive/mywald2020](https://gitlab.mywald.de/archive/mywald2020)). Für andere Buchstaben
  neu erzeugen. Text in Systemschrift
- `img/philip.jpg` – Foto (quadratischer Ausschnitt, 640 px); `img/apple-touch-icon.png`
- `favicon.svg`, `favicon.ico` – das Efeublatt

Eingecheckt ist nur, was die Seite ausliefert (`.gitignore` ist eine Whitelist) – so lässt sich
das Repo direkt in IntelliJ öffnen, ohne `.idea/` oder `*.iml` einzuchecken.

Die bisherige Seite (Onepager von 2017, zuletzt 2023 geändert) steht im ersten Commit nach
„Initial commit“; die ganze Historie seit 2012 in archive/mywald2020, das braune Design von 2012 in
[archive/mywald2012](https://gitlab.mywald.de/archive/mywald2012).

## Vorschau

Im Heimnetz unter https://pages.mywald.de/websites/mywald/ (GitLab Pages, `.gitlab-ci.yml`),
aktualisiert bei jedem Merge auf `main`. `CNAME` ist für GitHub Pages vorbereitet
(`www.mywald.de`); bis zur Umstellung kommt die Seite noch aus S3/CloudFront.

## Rechte

Texte und Fotos: © Philip Maiwald, alle Rechte vorbehalten.
Das Repository ist öffentlich, damit die Seite über GitHub Pages ausgeliefert werden kann;
eine Lizenz zur Weiterverwendung ist damit nicht verbunden.

Die Schrift Calligraffiti steht unter der Apache License 2.0 (`fonts/LICENSE-Apache-2.0.txt`).
