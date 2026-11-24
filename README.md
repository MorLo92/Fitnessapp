# Fit in 15

Kleine Fitness-Web-App für kurze Workouts (10–15 Minuten) mit dem eigenen Körpergewicht – ohne Geräte.

## Funktionen

- **Workout-Generator**: Dauer (10/12/15 Min), Niveau (Einsteiger/Fortgeschritten/Profi), Fokus (Ganzkörper, Beine & Po, Rumpf, Oberkörper, Cardio) und Intervall (z. B. 40 s Übung / 20 s Pause)
- **Intervall-Timer** mit Fortschrittsring, Signaltönen, optionalen deutschen Sprachansagen und Seitenwechsel-Hinweis
- **Stretching danach**: 2–8 Minuten, passend zum Fokus, sortiert vom Stehen bis zum Liegen
- **Übungsbibliothek**: 71 Trainingsübungen + 31 Dehnungen, jeweils mit animierter Strichfigur, Anleitung in drei Schritten und Tipp
- **Favoriten** (♥): gelikte Übungen werden beim Mischen bevorzugt

## Aufbau

Alles steckt in einer einzigen Datei: `index.html` (HTML, CSS und JavaScript, keine Abhängigkeiten).

- `EX` – Datenbank der Trainingsübungen
- `STR` – Datenbank der Dehnungen
- Posen der Figuren: 11 Gelenkpunkte `x,y` (Kopf, Hals, Ellbogen1, Hand1, Ellbogen2, Hand2, Hüfte, Knie1, Fuß1, Knie2, Fuß2), Boden bei `y=92`. Mehrere Posen pro Übung werden flüssig ineinander animiert.

## Starten

`index.html` im Browser öffnen – fertig. Einstellungen, Favoriten und Zähler werden im `localStorage` des Browsers gespeichert.

## Veröffentlichen über GitHub Pages

Repository → **Settings → Pages** → Source: *Deploy from a branch* → Branch `main`, Ordner `/ (root)` → Save.

## Als App installieren (PWA)

Die App ist eine Progressive Web App: Nach dem ersten Öffnen funktioniert sie auch **offline**.

- **iPhone (Safari):** Teilen-Symbol → „Zum Home-Bildschirm“
- **Android (Chrome):** Menü ⋮ → „App installieren“ bzw. „Zum Startbildschirm hinzufügen“

Dateien:
- `manifest.webmanifest` – Name, Farben, Icons
- `sw.js` – Service Worker für den Offline-Betrieb. **Bei jeder Änderung an der App `VERSION` in `sw.js` hochzählen**, damit installierte Apps das Update bekommen.
- `icons/` – App-Icons
