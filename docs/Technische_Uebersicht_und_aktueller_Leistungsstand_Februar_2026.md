# PsyFEM Engine – Technische Übersicht und aktueller Leistungsstand

## 1. Was ist PsyFEM

PsyFEM ist eine deterministische, mehrstufige Memory-Engine zur strukturellen Verdichtung und Analyse von Daten über lange Zeiträume.  
Sie ist kein LLM-Wrapper, kein reines Retrieval-System und kein klassisches Knowledge-Graph-Frontend, sondern eine eigenständige, persistente Lern- und Struktur-Engine.

Kernidee

 Daten werden als Episoden (L0) gespeichert und über mehrere Ebenen (L1–L4) strukturell verdichtet.  
 Das System erzeugt keine „Wahrheiten“, sondern stabile Muster, Hypothesen und Strukturbeziehungen.

Die Engine ist vollständig offline lauffähig, modular erweiterbar und API-fähig.

---

## 2. Systemklassifikation

PsyFEM vereint Eigenschaften aus mehreren Klassen

- Deterministisches Langzeit-Memory-System
- Mehrschichtige Graph-Engine
- Inkrementelle Strukturverdichtungs-Engine
- Edge-fähige Analyseplattform
- Auditierbare Lernarchitektur

Es ersetzt keine bestehenden Systeme (ERP, FEM, BI, LLM), sondern erweitert sie als persistente Erfahrungsinstanz.

---

## 3. Architekturüberblick

### 3.1 Layer-Modell

- L0 – Episoden (Rohdaten)
- L1 – Lokale Verdichtung
- L2 – Konzepte  Cluster
- L3 – Kontextverdichtung
- L4 – Meta-Gesamtstruktur

Diese Ebenen sind implementiert und persistent im Workspace gespeichert.

---

### 3.2 Komponenten-Trennung

Core (Engine)  
- Graph-Verwaltung  
- Layer-Build-Logik  
- Aktivierungsdynamik  
- Persistenz (NodesEdges)  

API-Schicht  
- Query-Endpunkte  
- Read-only-Modus  
- Parametrisierbare Abfragen  

Orchestrator  
- Laufsteuerung  
- Profile  Etappenlernen  
- Chunk-Verarbeitung  
- Layer-Trigger  

Knowledge UI  
- Layer-Visualisierung  
- Struktur-Exploration  
- Observatory-Zugriff  

Observatory  Analytics  
- NodesEdges-Statistik  
- Layer-Verteilung  
- Strukturmetriken  
- Retrieval-Benchmarks  
- Drift-Indikatoren  

---

## 4. Nachweisbare Stabilität

- 174 Tests erfolgreich
- ~52 % Testabdeckung
- Reproduzierbare Runs
- Persistente Workspace-Struktur
- Deterministische Update-Logik

---

## 5. Effizienz- und Skalierungsmechanismen

### 5.1 Dirty-Mechanismus (Lazy Recompute)

- Markierung betroffener Strukturen als „dirty“
- Aggregationen werden nur bei Bedarf neu berechnet
- Vermeidung vollständiger Rebuilds

→ Reduzierte Rechenzeit bei inkrementellen Updates

---

### 5.2 Active-Set Beschleunigung

- Update-Schritte nur über aktive KnotenKanten
- Parametrisierbare Aktivitätsschwellen

→ Komplexität pro Schritt reduziert von O(E) auf O(E_active)

---

### 5.3 Delay-Etappenlernen

- Chunk-Verarbeitung großer Datenmengen
- Steuerbare Layer-Trigger
- Warmup-Phasen

→ Kontrollierte CPU-Last  
→ Unterbrechbare Lernprozesse

---

### 5.4 Vermeidung von 1-Step-Delay

- Synchrones Aktivierungsupdate bei externen Inputs
- Kein Qualitätsverlust durch propagationsbedingte Verzögerung

---

### 5.5 Workspace-Austauschbarkeit

- Lernen extern möglich
- Nutzung lokal möglich
- Reiner Datenaustausch

→ Trennung von Trainings- und Nutzungskosten

---

### 5.6 Replay  Auditierbarkeit

- Reproduzierbare Runs
- Replay-Backfill-Pfade
- Observatory-Reports
- Integritätsmarker (Config-Hash, Checksums)

→ Vergleichbarkeit und Nachvollziehbarkeit

---

### 5.7 Pruning

- Begrenzung von Episoden nach AnzahlAlter

→ Speicher- und Laufzeitkontrolle

---

## 6. Nachweisbare Leistungsfähigkeit

### 6.1 Skalierung

- 80.000 Nodes
- 600.000 Edges
- Mehrjährige Datenräume verarbeitet

---

### 6.2 Retrieval-Benchmark (intern)

Graph-basierter Retrieval-Ansatz outperformt BM25 im Testset

- Höhere MRR@k
- Höhere nDCG@k
- Niedrige Latenzen

---

### 6.3 Layer-Entstehung in realen Runs

In mehrstündigen Läufen entstehen

- L1-Struktur
- L2-Cluster
- L3-Kontext
- L4-Metaknoten

Persistente Nachweisbarkeit im Workspace.

---

## 7. Edge-Fähigkeit

- Lauffähig auf SurfaceARM
- Lernprozess auslagerbar
- Analyse auch auf schwacher Hardware

---

## 8. Reifegrad

### Aktueller Status

- Funktionsfähiger Technologie-Prototyp
- Stabiler Kern
- Skalierbar
- Nachweisbare Strukturleistung

### Noch nicht

- Vollständig industrialisiert
- Vollständig benchmark-validiert für Enterprise
- Zertifiziert für Produktionsumgebungen

---

## 9. Zusammenfassung

PsyFEM ist eine deterministische, mehrschichtige Memory-Engine mit

- sauberer Grundarchitektur
- modularer Erweiterbarkeit
- integrierter Analysefähigkeit
- nachweisbarer Skalierung
- Effizienzmechanismen (Dirty, Active-Set, Pruning)
- reproduzierbarer Auditierbarkeit

Es handelt sich um eine real implementierte Struktur-Engine mit messbarer Leistung, nicht um ein theoretisches Konzept.