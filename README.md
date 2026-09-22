# DBD-Assistent

Lokaler HTML-Assistent zum schnellen Erzeugen und Kopieren von DBD-Befehlen.

## Version 0.4.0

### Neu

- **Profile & Presets**
  - Eingebautes, unveränderliches Profil `Team C – Standard`
  - Eigene Profile können erstellt, bearbeitet und lokal gespeichert werden
  - Änderungen an einem Standardprofil werden immer als neues eigenes Profil gespeichert
  - Profile können als JSON importiert, exportiert und – wenn vom Browser unterstützt – über die System-Teilen-Funktion weitergegeben werden

- **Bearbeitungsmodus**
  - Spalten hinzufügen, löschen, umbenennen und verschieben
  - Befehle hinzufügen, löschen, umbenennen und verschieben
  - Befehlspräfixe frei bearbeiten
  - Hervorhebungsfarben über eine passende Farbpalette, freie Farbauswahl und – sofern vom Browser unterstützt – Pipette wählen
  - Änderungen können mit `Speichern` übernommen oder mit `Abbrechen` vollständig verworfen werden

- **Schnellbefehle**
  - `Alpha-Abfrage` ist jetzt Teil eines eigenen Schnellbefehle-Arrays
  - Weitere feste Befehle können im Profil hinzugefügt werden
  - Schnellbefehle erscheinen gemeinsam mit `Alle Nummern löschen` oberhalb der Spalten

- **Auto-Clear pro Profil**
  - Automatische Löschzeit kann im Profil zwischen 1 und 60 Minuten eingestellt werden

- **Feedback**
  - Neue Feedback-Schaltfläche öffnet eine E-Mail an `ilia.bolotskikh@dwpservice.de`
  - Betreff wird automatisch mit `DBD-Assistent Feedback` vorbelegt

- **Bedienung**
  - Auch nicht farblich hervorgehobene Befehle geben beim Kopieren jetzt eine dezente visuelle Rückmeldung
  - Statusanzeige wurde als schmale Leiste unter die Schnellbefehle verschoben
  - Profilwahl befindet sich platzsparend direkt unter dem Programmnamen

## Datenschutz / lokale Speicherung

Der Assistent bleibt ein lokales HTML-Tool und sendet selbst keine Kundendaten an einen Server.

`localStorage` wird ab Version 0.4.0 ausschließlich für **Konfigurationsdaten** verwendet, zum Beispiel:

- eigene Profile
- Befehlslisten und Reihenfolge
- Farben
- Auto-Clear-Einstellung
- ausgewähltes Profil
- Darstellungsmodus

**Nicht gespeichert werden:**

- Depotnummern
- PIDs
- temporäre Notizen
- erzeugte kundenbezogene Befehle
- Inhalte der Zwischenablage

Importierte Profile werden validiert. Profilwerte werden als Daten behandelt und nicht als ausführbarer HTML-/JavaScript-Code in die Oberfläche übernommen.

## Nutzung

Die Datei `dbd_assistant.html` lokal speichern und mit Microsoft Edge oder einem anderen modernen Chromium-Browser öffnen. Es ist kein Server, keine Installation und keine externe Bibliothek erforderlich.
