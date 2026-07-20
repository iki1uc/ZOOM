# ZOOM – 1‑Meter‑Linie · Whirl‑Beam · Scan‑Vektor · C/X/Z‑Matrix
ZOOM ist die erste technische Instanz des Systems.
ZOOM steht direkt nach BEN und liefert alle Roh‑Vektoren,
Achsen, Farben, Masken und Whirl‑Beam‑RUN‑Punkte an ORT und HOME.

ZOOM ist die 1‑Meter‑Linie des gesamten Systems.

Dieses README beschreibt **jede Datei** im Repository
und erklärt **ihren technischen Zweck**.

---

# 1. Haupt‑HTML‑Dateien

## index.html
Startseite des ZOOM‑Systems.
Zeigt:
- Tech‑Scan aller ZOOM‑Dateien
- RUN‑Beam‑Punkte (8 / 32 / 128)
- C/X/Z‑Matrix‑Vergleich
- ZOOM‑Beschreibung

Lädt alle `.txt`‑Dateien per `fetch()`.

## verify.html
Basis‑Analyse‑Seite.
Zeigt:
- ZOOM‑Datenpool
- Input‑Pool
- Output‑Pool
- RUN‑Beam‑Punkte
- NC‑Module
- RESPO‑Module

## ZOOM.verify.html
Erweiterte Analyse‑Seite.
Zeigt:
- vollständige ZOOM‑Pipeline
- alle Module
- alle Vektoren
- alle RUN‑Punkte
- alle NC‑Matrizen

---

# 2. ZOOM‑Datenpool (lokale Dateien)

Diese Dateien werden von index.html und verify.html geladen.

## ZOOM.tmp.txt
Haupt‑Rohdaten des ZOOM‑Systems.
Erster Input für:
- zoom.line
- zoom.axis
- zoom.color
- zoom.mask
- zoom.scan
- zoom.vector
- zoom.whirl

## zoom.line.txt
Erste 1‑Meter‑Linie.
Enthält:
- horizontale Achsen
- lineare Scan‑Daten

## zoom.axis.txt
Achsen‑Definitionen:
- X
- Y
- Z
- U
- V
- W

## zoom.color.txt
Farberkennung:
- RGB‑Werte
- Maskenfarben
- Scan‑Farben

## zoom.mask.txt
Masken‑Definitionen:
- Filter
- Blocker
- Sicht‑Masken

## zoom.scan.txt
Scan‑Vektor:
- Roh‑Scan
- Linien‑Scan
- Achsen‑Scan

## zoom.vector.txt
Vektor‑Berechnung:
- LEN
- LINES
- WORDS
- RUN‑Punkte

## zoom.whirl.txt
Whirl‑Beam‑Daten:
- RUN‑8
- RUN‑32
- RUN‑128
- Whirl‑Startpunkt

---

# 3. NC‑Module (Matrix‑System)

Diese Dateien definieren die ZOOM‑Matrix.

## NC3x3.txt
Grundmatrix (3×3).
Basis für:
- C‑Matrix
- X‑Matrix
- Z‑Matrix

## NC6e.txt
Erweiterte Matrix (6‑Elemente).
Für:
- Achsen‑Erweiterung
- Scan‑Erweiterung

## NC9x9.txt
Vollmatrix (9×9).
Für:
- Würfel‑Bildung in ORT
- Weitsicht in HOME

---

# 4. RESPO‑Module (System‑Kontext)

Diese Dateien definieren den System‑Kontext.

## ROOT.me
Ursprung des Systems.
Basis‑Nullpunkt.

## SOURCE.me
Quelle der Daten.
Verbindet:
- BEN → ZOOM → ORT → HOME

## SYSTEM.me
System‑Kontext.
Definiert:
- globale Parameter
- System‑Achsen
- System‑Masken

---

# 5. RUN‑Beam‑Punkte (Whirl‑Physik)

ZOOM erzeugt die ersten drei RUN‑Punkte:

- RUN‑8   → Startpunkt des Wirbels
- RUN‑32  → Verstärkung (RUNC)
- RUN‑128 → Expansion (RUNQ)

Diese Werte werden an ORT und HOME weitergegeben.

---

# 6. Pipeline

BEN → **ZOOM** → ORT → HOME → HH → ULTRA

ZOOM ist der technische Startpunkt.
Wenn ZOOM nicht lädt → alles dahinter fällt aus.

---

# 7. GitHub‑Pages‑Hinweise

Damit ZOOM online funktioniert:

1. Alle Dateien müssen ASCII‑Namen haben  
2. `.nojekyll` muss im Root liegen  
3. Unicode‑Dateien dürfen NICHT existieren  
4. fetch() muss `.txt`‑Dateien laden  
5. index.html muss im Root liegen  

Beispiel:
- `zoom.line` → `zoom.line.txt`
- `NC3×3` → `NC3x3.txt`

---

# 8. ZOOM ist die technische 1‑Meter‑Linie

ZOOM stabilisiert:
- Achsen
- Farben
- Masken
- Scan‑Vektoren
- RUN‑Punkte
- NC‑Matrizen
- RESPO‑Module

ZOOM ist die Grundlage für ORT‑Würfel und HOME‑Weitsicht.

