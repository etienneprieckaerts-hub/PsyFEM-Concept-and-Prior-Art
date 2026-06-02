# PsyFEM - Oeffentliche Evidenzbasis

**Veroeffentlichungsstand:** 2. Juni 2026
**Dokumenttyp:** Bewusst begrenzte Einordnung interner Belege

## 1. Zweck

Dieses Dokument erklaert, wie die oeffentlichen Aussagen zum PsyFEM-Prototyp intern
abgesichert wurden. Es veroeffentlicht keine internen Audit-Berichte, Quellpfade,
Testmatrizen oder reproduzierbaren Implementierungsdetails.

## 2. Rangfolge der Belege

Fuer die oeffentliche Einordnung gilt folgende Rangfolge:

1. Massgeblich ist die zentrale codebasierte Audit-Serie mit inhaltlichem Stand vom
   31. Mai 2026 und Abschlusspruefungen vom 1. Juni 2026.
2. Ergaenzend wurde der reale Workspace am 2. Juni 2026 direkt inventarisiert.
3. Aeltere Test-, Validierungs- und Forschungsberichte werden nur als datierte,
   thematisch begrenzte Zusatzbelege verwendet.
4. Aeltere Planungsdokumente oder historische Snapshots ueberschreiben keinen neueren
   Audit-Befund.

Diese Reihenfolge ist wichtig, weil der private Entwicklungsbestand viele historische,
generierte und experimentelle Artefakte enthaelt.

## 3. Aktuelle Inventaraussagen

Die direkte Inventarisierung vom 2. Juni 2026 stuetzt unter anderem folgende
oeffentliche Aussagen:

- Der Prototyp besitzt einen modularen Kern, Orchestrierung, persistente Arbeitsstaende,
  Analysepfade, API-Flaechen, UIs sowie CLI- und Tool-Pfade.
- Die bewusst betrachteten Implementierungs- und Tool-Bereiche umfassen ungefaehr
  `114.400` physische Python-Zeilen. Tests sowie historische Snapshot- und
  Refactor-Baeume sind dabei nicht enthalten.
- Zwei betrachtete API-Flaechen enthalten zusammen `58` deklarierte HTTP-Routen.
- Vier UI-Einstiege sind vorhanden.
- Die primaere aktive Testsuite umfasst `241` Testdateien mit `1.107` entdeckten
  Testfunktionen. Ein separater QA-Baum enthaelt weitere `6` Testdateien mit `17`
  entdeckten Testfunktionen.

Zeilenzahlen und Dateizaehler sind Inventarindikatoren, keine Qualitaetsbewertung.

## 4. Ausgewaehlte datierte Laufbelege

Die folgenden Laufbelege werden bewusst mit ihrem engen Scope genannt:

| Datum | Interner Lauf | Ergebnis | Oeffentliche Einordnung |
|---|---|---:|---|
| 21. Mai 2026 | Silent-Failure- und Kernpfadpruefung | `12 / 12` und `60 / 60` | Fokussierte Pfade; keine Vollstaendigkeitsgarantie fuer das Gesamtsystem |
| 1. Juni 2026 | Abschlusslauf fuer zuvor offene Direktpruefungen | `16 / 16` | Direktpruefungen fuer sechs gezielt geschlossene Pfade |
| 1. Juni 2026 | Live-Integrations-Haertung | Regressionstests ergaenzt | Zusaetzliche operative Erprobung; keine Produktionszertifizierung |

Ein breiterer Validierungs-Harness vom 11. Mai 2026 bleibt intern dokumentiert. Er wird
hier nicht als zusammengefasste Erfolgszahl verwendet, weil sein Umfang mehrere
unterschiedlich belastbare Evidenzklassen umfasst und Teile synthetisch oder
temporaer-workspace-begrenzt sind.

## 5. Bewusst begrenzte Schlussfolgerungen

Aus den internen Belegen folgt:

- Eine reale, funktionsfaehige Prototyp-Implementierung existiert.
- Zentrale Kern-, Persistenz-, Orchestrierungs-, Analyse- und Integrationspfade sind
  vorhanden.
- Tests, Audits und reproduzierbare Teilpruefungen werden aktiv eingesetzt.
- Ein kontrollierter Anpassungspfad und ein Live-Integrationsdemonstrator sind
  vorhanden.

Nicht daraus abgeleitet werden:

- Produktionsreife fuer externe Nutzer;
- vollstaendige Testabdeckung;
- allgemeine Benchmark-Ueberlegenheit;
- wissenschaftlich nachgewiesene Emergenz;
- externe Zertifizierung oder unabhaengige Replikation.

## 6. Schutzgrenze

Die vollstaendigen internen Belege bleiben privat. Das betrifft insbesondere konkrete
Algorithmen, Profile, Parameter, Datenformate, Routenlisten, Modulnamen, Laufartefakte,
Fehleranalysen und Optimierungsrezepte.

Die allgemeine Freigaberegel ist in den
[Veroeffentlichungsgrenzen](VEROEFFENTLICHUNGSGRENZEN.md) dokumentiert.
