# Tic Tac Toe Two

PWA-Version für iPhone/Safari und GitHub Pages.

## Neu in dieser Version

### 5 KI-Schwierigkeitsgrade
1. **Anfänger** – überwiegend zufällige Züge.
2. **Leicht** – erkennt einfache Chancen und blockiert häufiger.
3. **Mittel** – taktische Heuristik mit guten Angriff-/Abwehrzügen.
4. **Schwer** – begrenzte Vorausberechnung über mehrere Züge.
5. **Meister** – auf 3×3 vollständige Minimax-Suche; auf größeren Boards tiefere, begrenzte Vorausberechnung.

### Zufälliger Startspieler
Bei jeder Partie wird X oder O zufällig als Startspieler bestimmt.

### Bonus-Runden
- Ab dem **5. normalen Zug** wird nach jedem regulären Zug geprüft, ob eine Bonus-Runde startet.
- Wahrscheinlichkeit: **15 %**.
- Nach einer Bonus-Runde folgen **mindestens zwei normale Züge ohne Bonus-Runde**.
- Danach kann wieder zufällig eine Bonus-Runde erscheinen.
- Eine Münze wählt zufällig Spieler X oder O.
- Der gewählte Spieler zieht anschließend eine von **12 Karten**.
- Gegen die KI zieht und spielt Computer O seine Bonuskarte automatisch.

#### 12 Bonuskarten
1. Lösche 1 Feld
2. Lösche 2 Felder
3. Lösche 3 Felder
4. Setze 1 Feld
5. Setze 2 Felder
6. Setze 3 Felder
7. Niete
8. Übernahme – ein gegnerisches Feld wird zum eigenen
9. Versetzen – ein eigenes Symbol wird auf ein freies Feld verschoben
10. +1 Punkt
11. Punktedieb – ein Punkt wird vom Gegner übertragen, sofern vorhanden
12. Doppel-Triplet – das nächste neu gebildete Triplet bringt einen Extrapunkt

Bei Löschkarten können beliebige belegte Felder gewählt werden. Wenn weniger gültige Felder als auf der Karte angegeben vorhanden sind, werden nur die vorhandenen Felder verwendet.

## Projektdateien

- `index.html` – komplette Oberfläche, Spiellogik, KI und Animationen
- `manifest.webmanifest` – PWA-Manifest
- `sw.js` – Offline-Service-Worker
- `apple-touch-icon.png` – iOS-App-Icon
- `icon-192.png` / `icon-512.png` – PWA-Icons
- `.nojekyll` – verhindert unnötige Jekyll-Verarbeitung auf GitHub Pages

## GitHub Pages – vorhandenes Repository aktualisieren

Für dein bestehendes Repository `frogo96/tictactwo`:

1. Dieses ZIP entpacken.
2. Im GitHub-Repository auf **Add file → Upload files** gehen.
3. Alle Dateien aus diesem Projekt in das Stammverzeichnis des Repositories ziehen.
4. Vorhandene Dateien wie `index.html`, `sw.js` und `manifest.webmanifest` ersetzen.
5. Unten **Commit changes** wählen und direkt nach `main` committen.
6. Unter **Settings → Pages** muss weiterhin stehen:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/(root)**
7. Warten, bis der Pages-Deploy abgeschlossen ist.
8. Danach in Safari öffnen:
   `https://frogo96.github.io/tictactwo/`

## iPhone / PWA aktualisieren

Wenn die Web-App schon auf dem Home-Bildschirm installiert ist:

1. Die GitHub-Pages-URL einmal direkt in Safari öffnen.
2. Seite neu laden.
3. Danach die Home-Bildschirm-App erneut öffnen.

Der Cache-Name des Service Workers wurde für diese Version geändert, damit die neue Version übernommen wird.
