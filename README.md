# NK-Prüfagent CH GREM

Ein deutschsprachiger Prüfagent für Nebenkostenabrechnungen im Schweizer Kontext. Der Agent unterstützt die prüfungsgerechte Belegkontrolle gemäss OR und Mietrecht.

## Projektstatus

> **Proof of Concept / Testphase**

Dieses Projekt befindet sich in der Entwicklungs- und Testphase. Die Prüfungsergebnisse müssen fachlich und manuell validiert werden.

Der Agent soll gezielt mit **Garaio REM** getestet werden:

- mit anonymisierten oder synthetischen Abrechnungsdaten
- mit realistischen Detailjournalen und Mehrjahresvergleichen
- mit Verteiljournalen und Leerstandslisten
- mit vollständigen Abrechnungsperioden
- mit anschliessender manueller Fachprüfung

Die Kompatibilität mit spezifischen Garaio-REM-Exporteinstellungen ist noch nicht abschliessend validiert.

## Zweck

Der Agent analysiert Excel-Unterlagen wie Detailjournal, Mehrjahresvergleich, Verteiljournal und Leerstandsliste.

Er prüft insbesondere:

- vollständige Abrechnungsperioden
- Verteilschlüssel
- Mengen und Einheitspreise
- Brutto-Beträge in CHF
- Mehrjahresvergleich
- Buchungslogik
- Rückstellungen
- Umbuchungen
- Rundungsdifferenzen

## Inhalt

- [`NK-Agent.md`](NK-Agent.md) – vollständige Prüf- und Ausgaberegeln
- [`LICENSE`](LICENSE) – MIT-Lizenz

## Quellen

- [Portal Mietrecht des Bundesamts für Wohnungswesen](https://www.bwo.admin.ch/de/portal-mietrecht)
- [Fedlex – Amtliche Sammlung des Schweizer Rechts](https://www.fedlex.admin.ch/)
- [Schweizerischer Verband der Immobilienwirtschaft SVIT](https://www.svit.ch/)

## Verwendung

1. `NK-Agent.md` als Agent-Anweisung oder eigene KI-Anweisung bereitstellen.
2. Die Excel-Unterlagen zur Abrechnung hochladen.
3. Detailjournal, Mehrjahresvergleich, Verteiljournal und Leerstände bereitstellen.
4. Verfügbare Rechnungen, Verträge und Objektunterlagen als Prüfgrundlagen ergänzen.

## Prüfbericht

Der Bericht enthält:

1. Zusammenfassung
2. Score je Konto
3. Auffällige Zeilenkommentare
4. Fehlerkatalog
5. Risikobeurteilung
6. Massnahmenplan
7. Freigabeentscheid

## Bewertung

- 🟢 OK
- 🟡 Prüfen
- 🔴 Kritisch

Freigabe erfolgt ab Score 85 und ohne kritische Fehler. Zwischen 65 und 84 ist eine Freigabe mit Vorbehalt möglich. Unter 65 oder bei mehreren kritischen Fehlern erfolgt keine Freigabe.

## Bekannte Grenzen

- Die Verarbeitung hängt von der Struktur und Qualität der bereitgestellten Excel-Exporte ab.
- Die Fachprüfung ersetzt keine Erfahrung, Objektkenntnis oder ergänzende Belegprüfung.
- Das Ergebnis ist keine rechtlich verbindliche Feststellung.
- Die Zuverlässigkeit in der Praxis wird erst durch Tests mit realen oder synthetischen Garaio-REM-Daten bestätigt.
- Keine Behauptung darf ohne Zeile, Konto, Betrag, Zeitraum und geeignete Datengrundlage erfolgen.

## Datenschutz und Tests

Für öffentliche Tests dürfen keine personenbezogenen oder vertraulichen Informationen verwendet werden.

Empfohlene Testdaten:

- vollständig anonymisiert
- ohne Mieternamen und Adressen
- ohne Bank- oder Rechnungsdaten
- synthetische Konten und Beträge
- dokumentierte Abweichungen für Wiederholbarkeit

## Mitwirken

Beiträge sind willkommen, insbesondere:

- anonymisierte Testfälle für Garaio REM
- Beispiele für korrekte und fehlerhafte Nebenkostenbuchungen
- Verbesserungsvorschläge für bekannte Excel-Strukturen
- Tests mit Mehrjahresvergleichen
- Dokumentation von Ergebnissen und Abweichungen

Bitte keine Daten aus laufenden Liegenschaften, Mieterverhältnissen oder vertraulichen Rechnungen veröffentlichen.

## Haftung und fachliche Grenze

Der Agent ist ein Prüf- und Assistenzwerkzeug. Er ersetzt keine rechtliche, steuerliche, revisionsrechtliche oder andere professionelle Fachberatung. Nutzerinnen und Nutzer tragen die Verantwortung für die fachliche Validierung und Weiterverwendung der Ergebnisse.

## Lizenz

Dieses Projekt steht unter der [MIT-Lizenz](LICENSE).
