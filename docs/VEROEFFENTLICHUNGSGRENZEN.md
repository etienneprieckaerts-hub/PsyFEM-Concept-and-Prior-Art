# PsyFEM - Veroeffentlichungsgrenzen

**Stand:** 2. Juni 2026

## 1. Ziel

Dieses Repository soll PsyFEM sichtbar und fachlich einordenbar machen, ohne eine
technische Blaupause des proprietaeren Systems zu veroeffentlichen. Die richtige
Detailtiefe liegt zwischen einer reinen Werbeaussage und einer nachbaubaren
Implementierungsbeschreibung.

## 2. Was oeffentlich sinnvoll ist

Oeffentlich geeignet sind:

- Zweck und fachliche Einordnung des Systems;
- abstrakte Architektur auf Systemebene;
- qualitative Beschreibung des Verarbeitungsflusses;
- ehrlicher Reifegrad;
- datierte, konservative Statusaussagen;
- klar bezeichnete Grenzen der Validierung;
- nicht technische Anwendungsfelder;
- Kontakt- und Lizenzhinweise.

## 3. Was privat bleiben soll

Nicht in dieses Repository gehoeren:

- Source Code, Pseudocode oder ausfuehrbare Beispiele;
- interne Datei-, Paket-, Klassen- oder Funktionsnamen;
- exakte Algorithmen, Formeln oder Verarbeitungsschritte;
- Schwellenwerte, Gewichte, Defaultwerte und Profilparameter;
- Datenbankschemata, JSON-Strukturen oder interne Artefaktformate;
- vollstaendige API-Routen und betriebliche Startbefehle;
- interne Audit-Berichte, Coverage-Matrizen und Risikokarten;
- reale Datenbestaende, Logs, Screenshots oder lokale Pfade;
- detaillierte Benchmark-Datensaetze, Messreihen oder Optimierungsrezepte;
- Zugangsdaten, Tokens, Schluessel oder Konfigurationsdateien.

## 4. Drei Freigabestufen

### Stufe A - Oeffentlich

Konzept, Einordnung, Vision, ausgewaehlte qualitative Statusaussagen und bewusst
begrenzte technische Uebersichten.

### Stufe B - Vertraulich teilbar

Vertiefte technische Berichte, Demonstrationen oder ausgewaehlte Messwerte nur nach
bewusster Einzelfallpruefung und gegebenenfalls unter einer geeigneten
Vertraulichkeitsvereinbarung.

### Stufe C - Intern

Quellcode, vollstaendige Audits, Architekturkarten, Testmatrizen, Datenformate,
Parameter, Laufartefakte und operative Dokumentation.

## 5. Prueffragen vor jeder Veroeffentlichung

Vor einer neuen Datei oder Aenderung sind mindestens diese Fragen zu beantworten:

1. Ermoeglicht der Text eine konkrete Rekonstruktion eines internen Mechanismus?
2. Werden Parameter, Formeln, Datenformate oder interne Namen genannt?
3. Werden Werte behauptet, deren Messgrundlage nicht oeffentlich erklaert werden kann?
4. Verraet ein Screenshot lokale Pfade, Daten, Tokens oder interne Oberflaechen?
5. Ist die Aussage durch eine interne Primaerquelle belegt?
6. Ist klar erkennbar, ob eine Aussage intern validiert oder extern nachpruefbar ist?

Wenn eine der ersten vier Fragen mit Ja beantwortet wird, gehoert der Inhalt
grundsaetzlich nicht in den oeffentlichen Bereich.

## 6. Hinweis zur Git-Historie

Eine einmal veroeffentlichte Datei kann auch nach ihrer Entfernung aus dem aktuellen
Stand in der Git-Historie, in Caches, Forks oder lokalen Kopien erhalten bleiben.
Deshalb muss die Freigabepruefung vor dem ersten Commit erfolgen.

## 7. Rechtlicher Hinweis

Diese Ablage ist keine Rechtsberatung und ersetzt keine professionelle
IP-, Patent- oder Lizenzpruefung. Eine oeffentliche Dokumentation kann Sichtbarkeit und
Datierung schaffen. Sie verhindert technisch jedoch keine Kopie und sollte bei
patentrelevanten Entscheidungen vorab mit fachkundiger Beratung abgestimmt werden.

Eine oeffentliche Fassung ist nicht automatisch eine rechtlich hinreichende
Prior-Art-Offenbarung. Umgekehrt kann eine zu detaillierte eigene Veroeffentlichung
spaetere Patentoptionen beeintraechtigen. Die sachliche Einordnung ist im
[Publication and IP Notice](PUBLICATION_AND_IP_NOTICE.md) zusammengefasst.
