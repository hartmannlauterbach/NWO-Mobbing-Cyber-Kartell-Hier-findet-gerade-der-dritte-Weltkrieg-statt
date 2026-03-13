# KI-Agenten und Tools Dokumentation

## Übersicht

Dieses Dokument beschreibt die KI-Agenten und MCP (Model Context Protocol) Tools, die im Skepsiz NWO Cybermobbing Musiker GRU Influence Forschungprojekt verwendet werden. Die Agenten sind darauf ausgelegt, automatisierte Forschung, Datensammlung und -analyse durchzuführen, unter Verwendung verschiedener Web-Scraping- und Browsing-Funktionen.

## Primärer Agent: Cascade

### Rolle
- **Funktion**: Leistungsstarker agentischer KI-Coding-Assistent
- **Fähigkeiten**:
  - Code-Generierung und Debugging
  - Dateisystemoperationen
  - Terminalbefehl-Ausführung
  - Web-Forschung und Datensammlung
  - Aufgabenmanagement und Planung

### Verwendete Tools
- **browsermcp**: MCP-Server für Webbrowsing und Interaktion
  - Seitennavigation und Snapshot-Erfassung
  - Elementinteraktion (Klicken, Tippen)
  - Screenshot-Erfassung
  - Console-Log-Abfrage

- **Code-Suche-Tools**:
  - `code_search`: Schnelle Kontextsuche zur Erkundung des Codebases
  - `grep_search`: Leistungsstarke ripgrep-basierte Textsuche
  - `find_by_name`: Datei- und Verzeichnissuche

- **Dateioperationen**:
  - `read_file`: Dateilesung mit Zeilenversatz-Unterstützung
  - `edit`: Exakte Zeichenkettenersetzungen in Dateien
  - `multi_edit`: Mehrere Bearbeitungen in einer einzelnen Datei
  - `write_to_file`: Neue Dateien erstellen

- **Aufgabenmanagement**:
  - `todo_list`: Todo-Listen mit Prioritäten und Status erstellen und verwalten

## MCP-Server

### browsermcp
- **Zweck**: Automatisiertes Webbrowsing und Datenextraktion
- **Fähigkeiten**:
  - Navigation zu URLs
  - Erfassung von Seitensnapshots
  - Screenshot-Erstellung
  - Interaktion mit Seitenelementen (klicken, hovern, tippen)
  - Abruf von Console-Logs
  - Behandlung der Browsernavigation (zurück, vorwärts)

### Verwendung in der Forschung
- Spotify-Künstlerseiten-Scraping
- Social-Media-Profil-Analyse
- Nachrichtenartikel-Sammlung
- Foren- und Community-Forschung

## Agenten-Workflow

### Forschungsinitiierung
1. **Planung**: Todo-Liste für Forschungstasks erstellen
2. **Navigation**: browsermcp verwenden, um zu Zielwebsites zu navigieren
3. **Datenerfassung**: Snapshots und Screenshots von relevanten Seiten aufnehmen
4. **Interaktion**: Elemente anklicken, um zusätzliche Inhalte zuzugreifen (Tabs, "mehr anzeigen"-Buttons)
5. **Extraktion**: Seiteninhalt nach Schlüsselinformationen parsen
6. **Analyse**: Funde in Berichte zusammenstellen

### Fehlerbehandlung
- Automatische Wiederholungsmechanismen für fehlgeschlagene Operationen
- Fallback-Strategien für unzugängliche Inhalte
- Timeout-Management für langlaufende Operationen

## Sicherheitsüberlegungen

- Alle Operationen respektieren die Nutzungsbedingungen der Websites
- Keine Authentifizierung oder Anmeldeversuche
- Nur öffentlich verfügbare Daten
- Rate-Limiting und respektvolles Crawling

## Zukünftige Agenten-Erweiterungen

Potenzielle Ergänzungen:
- NLP-Agenten für Sentiment-Analyse
- Bilderkennungsagenten für visuelle Inhaltsanalyse
- Social-Media-API-Integrationen
- Datenbank-Speicheragenten für Forschungspersistenz
