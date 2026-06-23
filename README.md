# HAW Initiativen – Übersicht

Dieses Repository enthält eine strukturierte, LaTeX-basierte Übersicht aller Studierendeninitiativen der HAW Hamburg. Es eignet sich für die **Orientierungseinheit (OE)**, Webseiten, Aushänge oder Broschüren.

---

## 📁 Struktur

```
haw-initiativen/
│
├── main.tex                    # Haupt-Dokument (kompiliert alles zusammen)
├── config/
│   └── design.sty              # Einheitliches Design-Paket (Farben, Schriften, Layout)
│
├── initiativen/
│   ├── coding_club.tex         # Eine Datei pro Initiative
│   ├── nachhaltigkeitsgruppe.tex
│   ├── hochschulradio.tex
│   └── ...                     # Weitere Initiativen hier hinzufügen
│
├── bilder/
│   ├── haw_logo.png            # HAW-Logo (bitte selbst hinzufügen)
│   ├── coding_club.jpg         # Bilder der jeweiligen Initiative
│   └── ...
│
└── README.md                   # Diese Datei
```

---

## 🚀 Neue Initiative hinzufügen

1. Kopiere eine bestehende Datei aus `initiativen/`, z. B.:
   ```
   cp initiativen/coding_club.tex initiativen/meine_initiative.tex
   ```

2. Passe die Felder in der neuen Datei an (Name, Beschreibung, Bild, Zielgruppe etc.)

3. Binde die Datei in `main.tex` ein:
   ```latex
   \input{initiativen/meine_initiative}
   ```

4. Lege ein Bild unter `bilder/meine_initiative.jpg` ab (empfohlen: 1200×600 px)

---

## 🛠️ Kompilieren

Benötigt wird eine LaTeX-Distribution (z. B. [TeX Live](https://tug.org/texlive/) oder [MiKTeX](https://miktex.org/)).

```bash
pdflatex main.tex
pdflatex main.tex   # Zweimal für Inhaltsverzeichnis
```

Oder mit `latexmk`:
```bash
latexmk -pdf main.tex
```

Das fertige PDF heißt dann `main.pdf`.

---

## 🎨 Design anpassen

Alle Design-Einstellungen (Farben, Schriften, Abstände) befinden sich in `config/design.sty`.  
Dort können z. B. die HAW-Farben oder das Logo-Placement geändert werden.

---

## 📋 Felder pro Initiative

Jede Initiative-Datei enthält folgende Informationen:

| Feld | Beschreibung |
|------|-------------|
| `\initiativeName` | Name der Initiative |
| `\initiativeKurz` | Kurzbeschreibung (1–2 Sätze) |
| `\initiativeBeschreibung` | Ausführliche Beschreibung |
| `\initiativeBild` | Pfad zum Bild (relativ zu `bilder/`) |
| `\initiativeZielgruppe` | Für wen ist die Initiative geeignet? |
| `\initiativeSemester` | Empfohlenes Semester (z. B. „ab 1. Semester") |
| `\initiativeStudiengang` | Relevante Studiengänge |
| `\initiativeKontakt` | E-Mail oder Website |
| `\initiativeTreffen` | Wann/Wo treffen sie sich? |

---

## 📄 Lizenz

Dieses Template steht allen Studierenden und Fachschaften der HAW Hamburg frei zur Verfügung.
