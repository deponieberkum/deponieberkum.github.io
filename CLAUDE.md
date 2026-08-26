# CLAUDE.md

Diese Datei gibt Claude Code (claude.ai/code) Hinweise zur Arbeit mit diesem Repository.

## Projektübersicht

Statische HTML/CSS/JS-Website der Bürgerinitiative „Keine Deponie in Berkum“, die sich gegen die
Reaktivierung/Erweiterung der ehemaligen Peiner-Träger-Deponie bei Berkum einsetzt. Kein Build-Tool,
kein Paketmanager, keine Tests – reine Dateien, die unverändert ausgeliefert werden.

Gehostet via GitHub Pages unter der in `CNAME` hinterlegten Domain (keine-deponie-berkum.de).

## Arbeiten in diesem Repo

- HTML/CSS direkt bearbeiten; es gibt keinen Compile-/Build-/Lint-/Test-Schritt.
- Für eine lokale Vorschau die HTML-Dateien direkt im Browser öffnen oder das Verzeichnis mit einem
  beliebigen statischen Server ausliefern (z. B. `npx serve` oder Pythons `http.server`) – es ist
  kein Dev-Server konfiguriert.
- `git push` auf `main` deployt automatisch via GitHub Pages. **Nur pushen, wenn der Nutzer es
  ausdrücklich verlangt** – lokale Edits/Commits sind auf Anfrage in Ordnung, aber ohne
  ausdrücklichen Auftrag nicht pushen oder anderweitig deployen.
- Platzhalter im Content sind mit `[…]` markiert und müssen vor öffentlicher Bewerbung ausgefüllt
  werden (siehe README.md).

## Redaktionsregel für die Startseite (Schaufenster-Prinzip)

Nutzer-Feedback (Aug. 2026): Die Seite „erschlägt einen mit Informationen". Deshalb gilt für
`index.html`: **je Abschnitt 2–3 Sätze + eine Kernzahl/ein Bild + Link auf die Unterseite** mit der
Tiefe. Details gehören in native Aufklapper `<details class="disclosure">` (kein JavaScript) oder auf
die Unterseiten. **Pro Absatz höchstens eine `<strong>`-Auszeichnung.** Richtwert: die Startseite
bleibt unter ~1.500 sichtbaren Wörtern (messen mit einem Skript, das `<details>`-Inhalte ausklammert).

## Struktur

- `index.html` – Startseite: Hero, Abschnitte zu Fakten/Risiken/Zeitachse (jeweils
  `<section id="...">` unter `<main id="inhalt">`), Petitions-/Kontakt-/Mitmachen-Blöcke.
  SVG-Icon-Symbole sind am Dateianfang inline definiert und werden per `<use>` referenziert.
- `deponien.html` – Karte der 24 bestehenden DK-II-Deponien in Norddeutschland, erlaubte
  Klasse-II-Abfälle (`#klasse-zwei`) und Hintergrund zu den Betreiber-Konzernen.
- `faktencheck.html` – Faktencheck der Betreiber-Webseite deponie-berkum.de (Zitat-Frage-Blöcke).
- `aktuelles.html` – chronologische Sammlung von Presse, Terminen und Veranstaltungen (Badges
  Presse/Termin/Veranstaltung/Mitteilung). **Neue Meldung:** ein `<li class="news-item">` ganz oben
  in die `<ol class="news-list">` einfügen (Marker-Kommentar dort). Das kompakte „Aktuelles"-Band
  auf der Startseite (`#aktuelles` in `index.html`) zeigt die zwei neuesten Meldungen – bei Bedarf
  dort spiegeln. Fremde Zeitungsartikel nur verlinken/zitieren, keine Artikel-PDFs hosten.
- `geschichte.html` – Zeitleiste der Deponie-Geschichte plus Grundwasser-Abschnitt.
- `vortrag.html` – Dokumentation der Info-Veranstaltung im Forum Peine am 13.05.2026.
- `ortstermin.html` – Protokoll des Ortstermins an der Deponie am 22.07.2026 (Standpunkte + Link zum
  Zeitungsbericht).
- `impressum.html`, `datenschutz.html` – Impressum und Datenschutzerklärung.
- `style.css` – gesamtes Styling der Seite (ein Stylesheet, kein Präprozessor).
- `bilder/` – Bild-Assets (JPEG- und WebP-Varianten).
- `Material/`, `infomaterial/`, `Vortrag Forum 13052026/` – Quelldokumente, Flyer, Presseausschnitte
  und Präsentationsfolien als Referenzmaterial für Inhalte; keine ausgelieferten/verlinkten Assets,
  außer sie werden explizit aus dem HTML referenziert.
- `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png` – Icons der Seite.
