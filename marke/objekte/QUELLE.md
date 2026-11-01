# Quelle: Place-Markenobjekte (D2D)

Generiert am 2026-10-31 mit Higgsfield (GPT Image 2.5, Ultra-Konto von Marvin). Referenzen: das gewählte Logo
(Konzept 01 „Tür im p", Runde 3, Variante 4 Torbogen 720) und Fotostil-Vorlagen aus den Koto-Fallstudien Fluz/Bolt
(nur Licht und Bildsprache). Freigegeben von Marvin: Ausweis am Lanyard, Türhänger + Fußmatte, Schlüssel + Sticker, Merch.

Hinweis: Das Logo ist vom Modell nachgebildet, nicht exakt platziert (auf der Fußmatte leicht verzogen). Für Druck und
echte Produktion gelten die SVGs, nicht diese Bilder. merch-person zeigt eine KI-generierte Person — nie als Teammitglied ausgeben.

## Exaktes Logo (2026-10-31, Relaunch 2c)

Auf den ebenen Flächen ist das nachgebildete Logo durch das exakte aus `public/marke/logo/` ersetzt; die unveränderten
Bilder liegen als `*-original.webp` daneben. Weg: Masken aus den SVG-Pfaden (Wortmarke, Kachel, „p") mit headless
Chrome gerendert, Ecken der Fläche bzw. Rahmen des alten Zeichens aus den Pixeln gemessen (Kantengeraden, Drehung),
das alte Zeichen getilgt (gewichtetes Mittel der umgebenden Fläche, 16 Bit, ein Hauch Korn), die exakte Maske mit
ffmpeg `perspective=…:sense=destination` eingepasst, in der gemessenen Farbe der Fläche eingefärbt und mit
`maskedmerge` überblendet.

| Datei | ersetzt |
|---|---|
| ausweis-lanyard | Wortmarke auf dem Ausweis (gleiche Höhe, linksbündig) und die Mint-Kachel mit „p" |
| tuerhaenger-fussmatte | das „p" auf dem Türhänger |
| schluessel-anhaenger | das „p" auf dem Anhänger |
| sticker-klemmbrett | der „place"-Aufkleber (neu aus der Wortmarke, weiße Kontur ≈ 26 px) und die „p"-Kachel |

Nicht ersetzt: die Fußmatte (Kokosfasern, das Logo ist eingewebt und verzogen — sauber nicht machbar) und die Merch-Bilder.
