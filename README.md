# ZOOM – 1‑Meter‑Linie · Whirl‑Beam · Scan‑Vektor · C/X/Z‑Matrix

ZOOM ist die erste technische Instanz des Systems.
ZOOM steht direkt nach BEN und liefert alle Roh‑Vektoren,
Achsen, Farben, Masken und Whirl‑Beam‑RUN‑Punkte an ORT und HOME.

ZOOM ist die 1‑Meter‑Linie des gesamten Systems.

---

# 1. Aufgabe von ZOOM

ZOOM führt die ersten drei Schritte aus:

1. Rohdaten aus BEN lesen
2. Achsen, Farben, Masken und Scan‑Vektoren erkennen
3. Whirl‑Beam‑RUN‑Punkte erzeugen (8 / 32 / 128)

ZOOM ist der technische Startpunkt der gesamten Pipeline.

---

# 2. ZOOM‑Input‑Pool (kommt aus BEN)

ZOOM erhält ausschließlich Daten aus BEN:

- BEN.tmp
- BEN.raw
- BEN.scan
- BEN.color
- BEN.axis
- BEN.mask

Wenn eine dieser Dateien fehlt → ZOOM kann nicht starten.

---

# 3. ZOOM‑Datenpool (lokale Dateien im ZOOM‑Repo)

ZOOM verarbeitet folgende Dateien:

- ZOOM.tmp.txt
- zoom.line.txt
- zoom.axis.txt
- zoom.color.txt
- zoom.mask.txt
- zoom.scan.txt
- zoom.vector.txt
- zoom.whirl.txt

Diese Dateien müssen ASCII‑Namen haben,
damit GitHub Pages sie laden kann.

---

# 4. ZOOM‑NC‑Module

ZOOM nutzt drei NC‑Matrizen:

- NC3x3.txt
- NC6e.txt
- NC9x9.txt

Unicode‑Versionen wie `NC3×3` oder `NC9×9` funktionieren NICHT online.

---

# 5. ZOOM‑RESPO‑Module

ZOOM benötigt drei System‑Module:

- ROOT.me
- SOURCE.me
- SYSTEM.me

Diese Dateien müssen im Root des Repos liegen.

---

# 6. Whirl‑Beam‑RUN‑Punkte

ZOOM erzeugt die ersten RUN‑Punkte:

- RUN‑8   → Startpunkt des Wirbels
- RUN‑32  → Verstärkung (RUNC)
- RUN‑128 → Expansion (RUNQ)

Diese Werte werden an ORT und HOME weitergegeben.

---

# 7. ZOOM‑Output‑Pool (geht an ORT und HOME)

ZOOM liefert:

- zoom.line.txt
- zoom.axis.txt
- zoom.color.txt
- zoom.mask.txt
- zoom.scan.txt
- zoom.vector.txt
- zoom.whirl.txt
- NC3x3.txt
- NC6e.txt
- NC9x9.txt
- ROOT.me
- SOURCE.me
- SYSTEM.me

ORT kann ohne diese Daten keine Würfel bilden.  
HOME kann ohne diese Daten keine Weitsicht erzeugen.

---

# 8. ZOOM‑Index (index.html)

Die Datei `index.html` zeigt:

- Tech‑Scan aller ZOOM‑Dateien
- RUN‑Beam‑Punkte
- C/X/Z‑Matrix‑Vergleich
- ZOOM‑Beschreibung

Damit ZOOM online funktioniert, müssen alle Dateien:

- ASCII‑Namen haben
- im Root des Repos liegen
- ohne Unicode sein
- ohne Sonderzeichen sein
- von GitHub Pages ladbar sein

---

# 9. ZOOM‑Verify (ZOOM.verify.html)

Die Datei `ZOOM.verify.html` zeigt:

- ZOOM‑Datenpool
- Input‑Pool
- Output‑Pool
- RUN‑Beam‑Punkte
- NC‑Module
- RESPO‑Module

Wenn verify.html leer bleibt → ZOOM lädt Dateien nicht.

---

# 10. GitHub‑Pages‑Hinweise (wichtig)

Damit ZOOM online funktioniert:

1. `index.html` muss im Root liegen  
2. `.nojekyll` muss im Root liegen  
3. Unicode‑Dateien müssen umbenannt werden  
4. fetch‑Pfad muss ASCII‑Dateien laden  
5. Dateien ohne Endung müssen `.txt` bekommen  

Beispiel:

- `zoom.line` → `zoom.line.txt`
- `NC3×3` → `NC3x3.txt`

---

# 11. ZOOM ist der Startpunkt der gesamten Pipeline

Pipeline:

BEN → **ZOOM** → ORT → HOME → HH → ULTRA

Wenn ZOOM nicht lädt → alles dahinter fällt aus.

ZOOM ist die technische 1‑Meter‑Linie,
die das gesamte System stabil hält.
