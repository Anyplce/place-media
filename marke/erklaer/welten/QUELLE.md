# Gemalte Welten der Erklär-Storys

Erzeugt am 2026-10-31 mit Higgsfield (GPT Image 2.5, quality high, 1k, 9:16 → 752 × 1344) auf Marvins Freigabe
im Chat („aber welt bilder angepasst … bei einem in haustür rein oder so"). Stilvorlage nur als Beschreibung im
Prompt (gemalt, körnig, sanfte Hügel, leuchtende Band-Wege, Kapsel-Fenster, Licht von hinten, kühle Töne) nach dem
OpenAI-Markenfilm, den Marvin geliefert hat — kein Motiv, keine Figur, kein Logo daraus übernommen; keine
Bildreferenz hochgeladen. Kosten: 5 Bilder × 1,5 Credits = 7,5 Credits.

Die Welten erzählen den Weg durch eine Haustür (Kurzfilm in `src/components/erklaer/Kurzfilm.jsx`):

| Datei | Rolle | Motiv |
|---|---|---|
| strasse-9x16.webp | Außen | Wohnstraße am Abend auf Hügeln, mintgrüne Haustür mit Messingklingel, leuchtender Band-Weg zur Tür; zwei kleine Figuren von hinten |
| tuer-9x16.webp | Übergang | die offene mintgrüne Tür, warmes Licht, durch die Tür die gemalte Welt |
| kapseln-9x16.webp | Innen/Traumwelt | Hügel mit Band-Wegen, Kapsel-Fenster mit Tür, Klingel, Karte, Münze; kleine Figuren von hinten |
| huegel-9x16.webp | Innen, ruhig | Hügel, zwei Band-Wege zum hellen Horizont, Mitte frei (für das Telefon) |
| weitblick-9x16.webp | Abschluss | Weitblick vom Hügel über ein kleines Viertel bei Morgenlicht; eine Figur von hinten |

Keine erkennbaren Gesichter, keine echten Personen, keine Marken, keine Schrift. Figuren nie als Place-Mitglieder ausgeben.
Eingebunden über `WELTEN_DA` in `src/components/erklaer/welten.js`.
