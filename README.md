# Sci-Fi Empfehlungen für Hendrik 📚🚀

Kuratierte Science-Fiction-Buchempfehlungen — als statische GitHub-Page.

**[Live ansehen →](https://hendr15k.github.io/hendrik-sci-fi-recommendations/)**

---

## Was ist das?

Eine durchsuchbare, interaktive Sci-Fi-Bibliothek mit persönlich kuratierten Empfehlungen. Die Seite kombiniert Klassiker, moderne Highlights, preisgekrönte Neuerscheinungen und bewusst ausgewählte Wildcards.

**Kein Framework, kein Build-Step** — nur HTML, CSS und JavaScript. Die Buchdaten liegen in [`books.csv`](books.csv) und werden clientseitig geladen.

---

## Features

- 📚 **135 Sci-Fi-Titel** — kuratiert und mit Kurzbeschreibungen
- 🎯 **Intelligenter Empfehlungsfinder** — "Empfiehl mir 3 Bücher" oder "Überrasch mich"
- 🔍 **Suche + Filter** — nach Kategorie, Stil, Einstiegshürde und Schlagwort
- 🏷️ **Schlagwort-Tags** — Award-Nähe, Mindfuck, Politisch, KI, Neuerscheinungen, Episch, …
- ⚡ **Blitzschnell** — rein clientseitig, keine Server-Abhängigkeit
- 📱 **Responsive** — funktioniert auf Desktop und Handy

---

## Daten

Alle Buchdaten liegen in **[`books.csv`](books.csv)](135 Einträge)**. Felder:

| Feld | Inhalt |
|------|--------|
| `rank` | Prioritätsrang |
| `title` | Titel |
| `author` | Autor |
| `year` | Erscheinungsjahr |
| `cover` | Cover-URL (Open Library) |
| `category` | Kategorien (pipe-getrennt) |
| `tags` | Schlagworte (pipe-getrennt) |
| `awards` | Auszeichnungen (pipe-getrennt) |
| `desc` | Kurzbeschreibung |
| `why` | Empfehlungsgrund |
| `vibe` | Vibe-Nota |

---

## Selbst etwas beitragen

Neues Buch hinzufügen — Zeile in [`books.csv`](books.csv) ergänzen:

```csv
136,Neuer Titel,Autor Name,2025,https://...,modern|space-opera,accessible|new, Hugo 2025 Finalist, Beschreibung, Warum man's lesen sollte.,Vibe-Beschreibung
```

Dann Commit → Push → Fertig. GitHub Pages aktualisiert automatisch.

---

## Deployment

Push auf `main` → automatisch live auf GitHub Pages.

```
main branch → hendr15k.github.io/hendrik-sci-fi-recommendations/
```
