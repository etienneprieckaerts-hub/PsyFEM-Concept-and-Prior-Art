# Pflegehinweise fuer das oeffentliche PsyFEM-Repository

**Stand:** 2. Juni 2026

## 1. Grundregel

Dieses Repository ist ein kuratierter oeffentlicher Schaukasten. Neue Inhalte werden
zuerst intern erstellt und geprueft. Erst danach wird eine bewusst reduzierte
oeffentliche Fassung hier aufgenommen.

## 2. Kleine, verstaendliche Struktur

Die Ablage bleibt absichtlich einfach:

- `README.md`: Startseite und Einordnung;
- `LICENSE.txt`: Nutzungs- und Rechtehinweis;
- `docs/`: freigegebene oeffentliche Dokumente;
- `.gitignore`: Schutz vor versehentlich aufgenommenen lokalen Dateien.

Quellcode, Rohberichte und interne Entwicklungsordner gehoeren nicht hierher.

## 3. Einfacher Ablauf fuer Aenderungen

Vor einer Veroeffentlichung:

1. Neue Datei intern erstellen.
2. Inhalt anhand von [Veroeffentlichungsgrenzen](VEROEFFENTLICHUNGSGRENZEN.md) pruefen.
3. Nur die freigegebene Fassung nach `docs/` uebernehmen.
4. Das [Dokumentenregister](DOKUMENTENREGISTER.md) aktualisieren.
5. Vor dem Hochladen die geaenderten Dateien kontrollieren.

Nuetzliche Git-Befehle fuer die Kontrolle:

```text
git status --short
git diff -- README.md docs .gitignore
git diff --stat
git ls-files --others --exclude-standard
```

Erst wenn die Liste plausibel ist, sollte ein Commit erstellt und zu GitHub
hochgeladen werden.

## 4. Gute Commit-Namen

Ein Commit beschreibt genau eine nachvollziehbare Aenderung. Beispiele:

```text
Add public technical status report for June 2026
Update public disclosure boundaries
Refresh public document register
```

## 5. Was niemals hochgeladen werden soll

- private Audit-Ordner;
- Programmsourcecode;
- lokale Pfade oder Nutzerverzeichnisse;
- Rohdaten, Logs oder Laufartefakte;
- `.env`-Dateien, Tokens, Kennwoerter oder Schluessel;
- unfreigegebene Entwuerfe;
- interne Screenshots.

## 6. Wenn versehentlich zu viel veroeffentlicht wurde

Die Datei nicht nur loeschen und weitermachen. Ein normaler Loesch-Commit entfernt den
Inhalt nicht aus der Git-Historie. Zuerst den betroffenen Inhalt und seine Reichweite
pruefen. Bei Zugangsdaten muessen die Daten sofort ersetzt oder gesperrt werden. Bei
technisch sensiblen Inhalten sollte vor weiteren Schritten eine gezielte Bereinigung
der Historie geplant werden.

Eine Historienbereinigung reduziert die weitere Sichtbarkeit, kann bereits erstellte
Forks, Caches oder lokale Kopien aber nicht rueckwirkend entfernen.

## 7. Umgang mit veralteten Konzeptfassungen

Nicht jede ueberholte Aussage erfordert eine Umschreibung der Git-Historie. Wenn eine
fruehere Fassung keine Zugangsdaten, keinen Quellcode und keine reproduktionskritische
Implementierungsspezifikation enthaelt, kann ihr Erhalt sinnvoll sein. Die Historie
dokumentiert dann transparent die Entwicklung des Projekts.

In diesem Fall wird eine aktuelle, datierte Fassung erstellt und die fruehere Aussage
in der [historischen Einordnung](HISTORISCHE_EINORDNUNG.md) als Konzept- oder
Zwischenstand gekennzeichnet.
