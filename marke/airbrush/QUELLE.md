# Airbrush-Bilder im Fluz-Stil (eigene Motive)

Erzeugt am 2026-10-31 mit Higgsfield (GPT Image 2.5; Objekte medium mit transparentem Grund, Flächen high) auf Marvins
Auftrag: „genau in diesem Stil … auch dieses echte, körnige … nur auf uns umgepasst". Als Stilreferenz dienten Standbilder
aus seinen Bildschirmaufnahmen der Fluz-App/-Kampagne — nur der Stil (Airbrush, Korn, Farben). Kein Fluz-Motiv, -Logo,
-Text oder -Mensch ist übernommen; alle Motive sind eigene aus der Place-Welt.

- `objekte/` (768 px, freigestellt — scharf bis ~380 CSS-px): tuer, muenze, muenze-kante, gem, scheine, schluessel, klingel, haus, herz, ballonhund,
  megafon, pokal, pin, papierflieger, kompass, heissluftballon, sonne, solarpanel, waermepumpe, blitz, krone, geschenk,
  schmetterling, kaffee
- `hintergrund/`: himmel, nacht, wueste (1920 breit, 16:9); nacht-hoch, weltall (1080 breit, 9:16)
- `challenge/` (1200 × 900): strasse, tuer, duell, team
- `ausweis-karte.webp` (1600 × 900): Kartenbild für den Dienstausweis
- `hand-handy.webp` (900 × 1200): Hand mit Telefon für den Wallet-Ablauf — kein Gesicht, keine Person

Keine Menschen als Place-Mitglieder, keine Marken.

## Nachtrag 31.10.2026, abends (Bento-Runde)
Auf Marvins Auftrag („irgendwie auch nochmal sowas passendes generieren … eins zu eins in diesem Stil … für Bentos") mit GPT Image 2.5 (high)
erzeugt; Stilreferenz: unsere eigenen Objekte (muenze, schmetterling, herz) bzw. seine Fluz-Standbilder — nur Stil, Licht, Korn.
- `objekte/` neu (768 px, freigestellt): taube, globus, rosette, sonnenbrille, turnschuh, blume-blau, blume-rosa, herz-schimmer, klemmbrett
- `fotos/schmuck.webp` (2400 × 1357): Hände mit Ringen halten Kette mit Diamant-Anhänger „place" — kein Gesicht
- `fotos/hoodie.webp` (1792 × 2240): Brust im schwarzen Hoodie, Druck „PLACE" / „FIND YOUR PLACE" vor Lila-Himmel — Bild endet am Kinn, kein Gesicht, keine echte Person, nicht als Mitglied zeigen
- `hintergrund/wiese.webp` (2560 × 1448): gemalte Landschaft, Mitte frei für eine Karte
- `plakatwand.webp` (1792 × 2240): leere Plakatwand frontal; weiße Fläche ≈ links 8,5 %, oben 21,1 %, rechts 92,2 %, unten 60,9 %
- `hand-handy-frei.webp`: `hand-handy.webp` mit herausgerechnetem grünem Grund (per Skript freigestellt, nichts neu erzeugt) — für die Bento-Kachel auf dem Logo-Verlauf
- `objekte/sonnenbrille.webp`: halbdurchsichtiger Schleier ums Objekt entfernt (Alpha unter 90 → 0), sonst stand auf Tinte ein graues Rechteck

## Nachtrag 31.10.2026, nachts (bewegte Heldenobjekte, `film/`)
Auf Marvins Auftrag („diese Animation da wie bei Fluz … noch besser. Unser Stil. Ready.") unsere Standbilder mit Higgsfield
**Kling 3.0** (std, 5 s, 1:1, ohne Ton) bewegt — Anfangs- und Endbild sind dasselbe Standbild, damit die Schleife schließt.
Dafür wurde jedes Objekt auf einfarbiges Blau (#0050FF, kommt in keinem Objekt vor) gelegt und das Blau danach per Skript
ausgestanzt (Farbdifferenz-Schlüssel, Entmischung halbdurchsichtiger Kanten, Kantenfarbe aus dem Inneren gegen den
Magenta-Saum, weicher Rand am Ausschnitt). Keine Hände, keine Menschen, keine Marken; der Ausweis ist ein Ausweis, keine Zahlkarte.

Je Name drei Dateien: `<name>.webp` (animiertes WebP mit Alpha, 400–480 px, 15–16 fps, Schleife),
`<name>.mov` (HEVC mit Alpha, `hvc1`, 24 fps, 508–720 px — Safari/WebKit und iOS/AVPlayer),
`<name>-standbild.webp` (erstes Bild der Schleife, gleiche Größe wie das .mov — Poster und „Bewegung reduzieren").
Einbau im Web: `src/components/shell/AirbrushFilm.jsx`.

| Name | Ausgang | Bewegung | Kling-Job |
|---|---|---|---|
| `muenze-dreht` | `objekte/muenze.webp` | dreht sich einmal um die Hochachse, Funkeln | 43dd294d |
| `ausweis-schwebt` | `objekte/ausweis-muenzen.webp` (neu) | Ausweis schwebt und kippt, Schimmer, vier Münzen kreisen | 152ceb35 |
| `schleuder` | `objekte/schleuder.webp` (neu) | Schlaufe gibt nach, Münze schießt nach oben hinaus und fällt zurück in die Schlaufe | c344f5d7 |
| `rakete` | `objekte/rakete.webp` (neu) | fliegt auf der Stelle, Flamme flackert, Funken ziehen nach | 78023c19 |
| `tuer-auf` | `objekte/tuer.webp` | Tür schwingt auf, warmes Licht, Funken, schwingt zurück | 645ee5e1 |
| `klingel` | `objekte/klingel.webp` | Knopf sinkt zweimal von selbst ein, Schwingungen pulsen | 905bd5a1 |
| `pokal` | `objekte/pokal.webp` | hüpft einmal, Glanz, Gold-/Minz-Konfetti | 55c51b20 |

Neue Standbilder dafür (GPT Image 2.5, high, transparent; Stilreferenz `objekte/muenze` + `objekte/pokal` bzw. `ausweis-karte`):
`objekte/schleuder.webp`, `objekte/rakete.webp`, `objekte/ausweis-muenzen.webp` (Dienstausweis mit Lanyard-Schlitz,
Vorderseite = `ausweis-karte`, vier Münzen) — je 768 px, freigestellt.

## Nachtrag 01.11.2026, nachts (Filme neu gestanzt, Place-Muenze)
Marvin: „nicht richtig ausgeschnitten, die haben diesen blauen Hintergrund". Befund: die `.mov` tragen echtes Alpha
(AVFoundation: `ContainsAlphaChannel`, Grundebene unter Alpha 0 weiss, nicht blau), die WebPs auch — sichtbares Blau
hatten nur die Kling-Rohfilme selbst (Higgsfield-Bibliothek) und kleine Reste in den Stanzungen: blaue Flecken zwischen
Klingelplatte und Strahlen, ein blauer Streifen am Glasrand des Ausweises, graue/schmutzige Konfetti beim Pokal,
Magenta-Saum an der Raketenflamme. Alle sieben Filme sind deshalb aus den Kling-Rohfilmen (Jobs wie oben, `result_url`)
neu gestanzt (Skript: Farbdifferenz-Grobmaske → sicherer Kern → Kernfarbe nach aussen gezogen → Alpha im Saum per
Projektion auf (Vordergrund − Grund) → Entmischen → Restblau/Magenta im Saum begrenzt → vormultipliziert verkleinert,
RGB unter Alpha 0 = Nachbarfarbe; beim Ausweis Inneres gefuellt, echte Loecher wie der Lanyard-Schlitz bleiben frei;
Teilchen laufen am Ausschnitt weich aus). Bildgroesse und Ausschnitt wie bisher, `.mov` HEVC mit Alpha (hvc1, 24 fps,
120 Bilder), WebP 80 Bilder bei 16 fps (Ausweis/Pokal 420 px, sonst 480 px). Die iOS-Kopien
(`relaunch-ios/…/Resources/AirbrushFilm/airbrush-film-*.mov`) sind dieselben Dateien.

- `objekte/place-muenze.webp` (768 px, freigestellt): die Place-Muenze in den Farben des Logos — dicke Muenze, irisierende
  Flaeche Minz → Lila → Himmelblau, das p-Logo schwarz gepraegt. Aus dem App-Icon-Entwurf vom 31.10.2026 (GPT Image 2.5,
  Job dc02a392, auf gruenem Grund) per Apple Vision (Vordergrundmaske) freigestellt, Loecher der Maske in den gruenen
  Muenzpartien ueber die konvexe Huelle geschlossen, Kanten gegen den Grund entmischt. Nichts neu erzeugt.
