# Sci-Fi Empfehlungen für Hendrik 📚🚀

Kuratierte Science-Fiction-Buchempfehlungen als schlanke, statische GitHub-Page — schnell, filterbar und mit eingebautem Empfehlungsfinder.

**Live:** https://hendr15k.github.io/hendrik-sci-fi-recommendations/

---

## Überblick

Das Projekt ist eine kleine Sci-Fi-Discovery-Seite für Hendrik:

- **durchsuchbarer Katalog** statt statischer Liste
- **kuratierte Empfehlungen** statt beliebiger Massen-Importe
- **interaktiver Finder** für 3 passende Vorschläge oder einen Zufallstreffer
- **saubere Datentrennung**: Inhalte liegen in `books.csv`, nicht in `index.html`

Die Seite läuft komplett ohne Framework und ohne Build-Step — nur mit `index.html` + `books.csv`.

---

## Aktueller Stand

- **150 Bücher** im Katalog
- Datenquelle: **`books.csv`**
- Frontend: **pures HTML, CSS und JavaScript**
- Deployment: **GitHub Pages**
- Architektur: **clientseitig, ohne Backend**

---

## Features

- 📚 **Kuratiertes Ranking** mit Priorisierung über `rank`
- 🔍 **Suche** nach Titel, Autor und Beschreibung
- 🧭 **Filter** nach Kategorien, Tags und Lesestil
- 🎯 **Empfehlungsfinder** mit „Empfiehl mir 3 Bücher“ und „Überrasch mich“
- 🏷️ **Tag-System** für Stimmungen und Themen wie `mindfuck`, `politisch`, `ki`, `episch`, `award`, `new`
- ⚡ **Schnelles Laden** durch rein statische Auslieferung
- 📱 **Responsive Layout** für Desktop und Handy

---

## Projektstruktur

```text
hendrik-sci-fi-recommendations/
├── index.html   # UI, Styling und Logik
├── books.csv    # Buchdaten
└── README.md
```

---

## Datenformat

Die Seite lädt `books.csv` automatisch beim Öffnen.

Verwendete Spalten:

| Feld | Bedeutung |
|------|-----------|
| `rank` | Sortier- und Prioritätsrang |
| `title` | Buchtitel |
| `author` | Autor |
| `year` | Erscheinungsjahr |
| `cover` | Cover-URL |
| `category` | Kategorien, per `|` getrennt |
| `tags` | Schlagworte, per `|` getrennt |
| `awards` | Preise / Award-Hinweise |
| `desc` | Kurzbeschreibung |
| `why` | Warum das Buch empfohlen wird |
| `vibe` | Ton / Lesestimmung |

Beispielzeile:

```csv
151,Neuer Titel,Autor Name,2025,https://example.com/cover.jpg,modern|space-opera,accessible|new,Hugo Finalist,Längere Kurzbeschreibung,Warum Hendrik das mögen könnte.,energetisch, groß, abenteuerlich
```

Wichtig:
- Mehrfachwerte in `category`, `tags` und `awards` werden mit `|` getrennt.
- UTF-8 verwenden.
- Reihenfolge der Spalten beibehalten.

---

## Bücher hinzufügen oder ändern

Ein neues Buch braucht nur eine neue Zeile in `books.csv`.

Typischer Ablauf:

1. `books.csv` öffnen
2. Zeile ergänzen oder vorhandenen Eintrag verbessern
3. committen und pushen
4. GitHub Pages aktualisiert die Seite automatisch

Das ist bewusst so gebaut, damit der Katalog später leicht auf **200+ Titel**, längere Beschreibungen und gepflegtere Metadaten wachsen kann.

---

## Lokales Testen

Weil `books.csv` per `fetch()` geladen wird, sollte die Seite lokal über einen kleinen HTTP-Server geöffnet werden, nicht per `file://`.

Beispiel:

```bash
cd /home/openclaw/.openclaw/workspace/hendrik-sci-fi-recommendations
python3 -m http.server 8124
```

Dann im Browser öffnen:

```text
http://127.0.0.1:8124/
```

---

## Deployment

Push auf `main` → GitHub Pages baut und veröffentlicht automatisch.

```text
main → https://hendr15k.github.io/hendrik-sci-fi-recommendations/
```

---

## Nächste sinnvolle Ausbaustufen

- längere und bessere Buchbeschreibungen
- mehr Bücher im Katalog
- stärkere Gewichtung nach Geschmack/Vibe
- zusätzliche Felder wie Reihe, Seitenzahl, Härtegrad oder deutsche Verfügbarkeit
- Import-/Pflege-Workflows für größere Kataloge

---

## Ziel des Projekts

Nicht einfach „viele Sci-Fi-Bücher auflisten“, sondern **schnell die richtigen nächsten Bücher finden**.
