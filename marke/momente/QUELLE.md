# Quelle: Place-Momente (Website → Video)

Aufgenommen am 01.11.2026 aus dem Demo-Portal (`http://localhost:5331/?demo=gast`, Worktree `portal-cash`).
Marvin wollte die besten Bild-/Animations-Momente der Website auch in der iPhone-App — als fertige Videos statt
nachgebauter Code-Animationen.

Kein neues Bildmaterial: jede Datei ist eine Aufnahme einer bestehenden Kachel oder eines bestehenden Bildes.
Darsteller (Mega-Menü-Fotos, „Leg los") sind KI-generierte bzw. gestellte Personen — nie mit Namen, nie als
Mitglied, Kundin oder Vertriebler ausgeben. Der Betrag in `provision-ansehen` trägt sichtbar „Beispiel".

## Dateien je Moment

| Datei | Inhalt |
|---|---|
| `<name>.mp4` | H.264 High, yuv420p, BT.709, 864 × 1080 (4:5), 30 fps, stumm, `+faststart` |
| `<name>-hevc.mp4` | HEVC (`hvc1`, Safari/iOS), sonst gleich |
| `<name>.webm` | VP9, sonst gleich |
| `<name>-poster.webp` | Standbild aus der Schleife (für `poster=` und „Bewegung reduzieren") |

Alle Schleifen sind nahtlos (Anfang = Ende) und < 3 MB je Datei.

| Name | Quelle | Länge | Schleife |
|---|---|---|---|
| `make-your-move` | Mega-Menü „Make your move." — `welt-bilder/kampagne-mantel.webp` | 6,0 s | Ken-Burns-Zoom 1 → 1,08 und zurück |
| `waehl-dein-gebiet` | Mega-Menü „Wähl dein Gebiet." — `kampagne/kulisse-strasse.webp` | 6,0 s | Ken-Burns-Zoom 1 → 1,08 und zurück |
| `raus-baby-raus` | `KachelTrichter` („RAUS, BABY, RAUS.") | 6,0 s | Strom läuft, 1 s Überblendung Ende → Anfang |
| `provision-ansehen` | `KachelTelefon` („Provision ansehen · 240,00 €", Beispiel) | 6,4 s | Telefon steigt, Karte und Knopf ploppen auf (Pop-up), Telefon sinkt |
| `kette` | `KachelSchmuck` („Jede Tür ist ein Move.") | 6,4 s | Pille kommt und geht, Funkeln, 1 s Überblendung |
| `pullover` | `KachelHoodie` („Find your place.") | 6,4 s | wie `kette` |
| `rausgehen-mit-place` | `KachelPlakat` („Rausgehen? Mit Place.") | 6,0 s | 24 Objekte ploppen auf, wippen, ploppen weg |
| `dein-tag-hand` | `KachelHand` („Dein Tag passt in eine Hand.") | 6,0 s | Herzen/Münzen ploppen auf und weg, Hand steht |
| `dein-tag-wortmarke` | `KachelWortmarke` | 5,2 s | Ruhe → Aufkleber-Verlauf (wie beim Zeigen) → Ruhe |
| `leg-los` | `start3/Vertrauen.jsx` `LegLos` | 6,0 s | Karte im Hochformat, beide 3D-Zeichen schweben |
| `place-tauben` | `KachelRiese` (Wortmarke auf Flieder, Taube, Schmetterlinge) | 6,0 s | Flug, 1,2 s Überblendung |

## Was für die Aufnahme anders ist als auf der Seite

- Jede Kachel bildfüllend auf 340 × 425 CSS-px gezwungen (Gerätefaktor 2,54 → 864 × 1080), ohne Rundung — die
  Ecken rundet die App. Innen rechnen die Kacheln in cqw/cqh, das Layout bleibt ihres.
- `provision-ansehen`: Telefon kleiner (76 cqw × 87 cqh) mit Dynamic-Island-Strich, damit es im Hochformat ganz
  steht; „Provision freigegeben" und der Knopf ploppen nacheinander auf (`mo-pop`), statt einfach dazustehen.
- `rausgehen-mit-place` / `dein-tag-hand`: Ausploppen (`mo-weg`) am Ende, damit die Schleife leer beginnt und endet;
  die Hand bleibt oben stehen.
- `leg-los`: nur „Leg los.", der Darsteller und die beiden 3D-Zeichen — Absatz, Knöpfe, QR-Code und Store-Abzeichen
  sind ausgeblendet (in der App gibt es eigene Knöpfe; ein QR-Code zum Laden der App wäre in der App sinnlos).
  Die Zeichen schweben (3 s hin und her), auf der Seite stehen sie.
- Ken Burns gibt es auf der Website nicht; das Mega-Menü zeigt die Fotos still.

## Wie aufgenommen

Werkzeug im Scratchpad: `portal/mo-momente/aufnahme.mjs` (Headless Chrome über CDP, eine Zeit-Attrappe für
`setTimeout`/`requestAnimationFrame`/`performance.now`, jede Web-/CSS-Animation pro Bild auf ihre virtuelle Zeit
gesetzt → 30 fps ohne Ruckeln), `plan.mjs` (die Liste oben), `kodieren.mjs` (ffmpeg: FFV1-Meister mit `xfade` für
die Überblendung → libx264 / libx265 / libvpx-vp9, `cwebp` fürs Poster), `bogen.mjs` (Kontaktbogen und Nahtprüfung).
