# HAW Initiativen – Übersicht

Dieses Repository enthält eine strukturierte, LaTeX-basierte Übersicht aller Studierendeninitiativen der HAW Hamburg.
---

## 📄 Aktuelle Version

👉 Hier kannst du die automatisch generierte PDF herunterladen:

[![Latest PDF](https://img.shields.io/badge/Download-PDF-blue?style=for-the-badge\&logo=adobeacrobatreader)](./Studierendeninitiativen.pdf)

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
├── Studierendeninitiativen.pdf # Automatisch generierte PDF (GitHub Actions)
│
└── README.md                   # Diese Datei
```

---
## 📨 Initiative einreichen (ohne LaTeX-Kenntnisse)

Du möchtest deine Initiative in diese Übersicht aufnehmen, kannst aber kein LaTeX?

Kein Problem 👍

Dafür gibt es den Ordner:

`initiativen-submissions/`

---

## 📄 So funktioniert es:

- Lade dir eine der Vorlagen aus dem Ordner `initiativen-submissions/` herunter  
- Öffne die Datei (ein einfacher Texteditor reicht, z. B. Notepad, VS Code, etc.)  
- Ersetze die Inhalte mit euren Informationen  
- Du musst dich nicht strikt an die Struktur halten  
- Inhalte können auch angepasst, erweitert oder vereinfacht werden  
- Benenne die Datei passend um (z. B. `ai_club.txt`)  
- Lade die Datei wieder ins Repository hoch
- Die wird später in manuel dann hinzugefügt
  
## 🚀 Neue Initiative hinzufügen (LaTeX-Kenntnisse)

1. Kopiere eine bestehende Datei aus ``initiativen/_VORLAGE.tex`, z. B.:

2. Passe die Felder in der neuen Datei an (Name, Beschreibung, Bild, Zielgruppe etc.)

3. Binde die Datei in `main.tex` ein:

   ```latex
   \input{initiativen/meine_initiative}
   ```

4. Falls ein Bild vorhanden lege das Bild unter `bilder/meine_initiative.jpg` ab (empfohlen: 1200×600 px)

---

## 🛠️ PDF kompilieren (Erstellen der Ausgabe)

Du brauchst eine LaTeX-Distribution wie TeX Live oder MiKTeX.

---

## 💻 Lokale Variante (auf deinem PC)

Einfachste Variante:

```bash
latexmk -pdf main.tex
```

Oder klassisch:

```bash
pdflatex main.tex
pdflatex main.tex
```

## 🤖 Automatische PDF-Erstellung (GitHub Actions)

Dieses Projekt ist so eingerichtet, dass du LaTeX nicht lokal kompilieren musst.

👉 Sobald du etwas änderst in:

- `main.tex`
- dem Ordner `initiativen/`
- dem Ordner `config/` (Design)

wird automatisch eine neue PDF-Version erstellt.

---

## 🔄 Ablauf:

- Du machst einen Push auf GitHub  
- GitHub Actions startet automatisch einen Build  
- Die PDF wird neu generiert (Dauer ca. 5–6 Minuten)  
- Die fertige Datei wird automatisch ins Repository hochgeladen  

---

## 📄 Ergebnis:

Du findest danach immer die aktuelle Version hier im Repo:

**Studierendeninitiativen.pdf**

## 🎨 Design anpassen

Alle Design-Einstellungen (Farben, Schriften, Abstände) befinden sich in `config/design.sty`.
Dort können z. B. die Farben oder das Logo-Placement geändert werden.

---

## 📄 Lizenz

Dieses Template steht allen Studierenden und Fachschaften der HAW Hamburg frei zur Verfügung.
