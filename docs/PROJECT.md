# FlyLife Freebies — Technische Projektdokumentation

## Zweck

Dieses Repository enthält statische, interaktive Web-Freebies für FlyLife. Aktuell ist der zentrale Inhalt der **Ausstiegs-Check**, ein deutschsprachiges interaktives Entscheidungs-Tool rund um die Frage „Bleiben oder gehen?“.

## Source-of-Truth-Regeln

- Dieses Dokument beschreibt die dauerhafte technische Struktur und Regeln.
- Notion ist Product Source of Truth für Ideen, Bugs, Wünsche, offene Entscheidungen und aktuellen Produktstatus.
- Der aktuelle Code bestimmt, was tatsächlich implementiert ist.
- Alte Notion-Historie nur lesen, wenn sie für eine konkrete Aufgabe relevant ist.

## Architektur

- Statische Single-File-Web-App.
- Hauptdatei: `ausstiegs-check.html`.
- HTML, CSS, JavaScript und eingebettete Assets sind weitgehend in dieser Datei gebündelt.
- Kein Framework und kein Build-System erforderlich.
- Deployment über GitHub Pages.

## Produkt-/UX-Regeln

- Mobile-first und deutschsprachig.
- Der Check soll verständlich und emotional zugänglich bleiben, nicht wie ein technisches Formular wirken.
- Änderungen an Bewertungslogik, Fragen, Gewichtungen oder Ergebnistexten gelten als Produktlogik und müssen gegen die Product Decisions in Notion geprüft werden.
- Bestehende Nutzerführung, Barrierefreiheit und mobile Touch-Bedienung bei Änderungen erhalten.
- Keine medizinischen, rechtlichen oder finanziellen Garantien aus Ergebnissen ableiten.

## Tests und Prüfung

Vor Abschluss relevanter Änderungen mindestens prüfen:

1. Seite lädt ohne Konsolenfehler.
2. Fragen lassen sich mobil bedienen.
3. Fortschritt funktioniert.
4. Ergebnisberechnung und Ergebnisanzeige funktionieren.
5. Neustart/Reset funktioniert, sofern betroffen.
6. CTA-/externe Links funktionieren, sofern betroffen.
7. Layout auf typischer iPhone-Breite kontrollieren.

Für neue komplexere Bewertungslogik möglichst kleine reproduzierbare Regressionstests oder dokumentierte Testfälle ergänzen.

## Deployment

GitHub Pages dient als Hosting. Bei Änderungen keine unnötige Architektur einführen, solange die statische Single-File-Struktur den Produktbedarf erfüllt.

## Sicherheit

Keine API-Keys, Tokens, Passwörter oder sonstige Secrets in GitHub oder Notion speichern.

## Notion Sync

Bei `Notion Sync durchführen`:

1. `AGENTS.md` bzw. `CLAUDE.md` und dieses Dokument lesen.
2. In Notion nur `CURRENT STATE`, `INBOX`, `OPEN` und relevante `PRODUCT DECISIONS` lesen.
3. Neue Punkte gegen den aktuellen Code prüfen.
4. Als Bug, Feature, Verbesserung, Frage oder Entscheidung klassifizieren.
5. Änderungen minimal umsetzen.
6. Relevante mobile/Browser-Prüfungen durchführen.
7. Dieses Dokument nur aktualisieren, wenn sich dauerhafte technische Wahrheit ändert.
8. Notion aktualisieren: Status, Open/Waiting/Changelog.
9. Verarbeitete Inbox-Punkte entfernen oder verschieben.
10. Ergebnis kurz auf Deutsch berichten.
