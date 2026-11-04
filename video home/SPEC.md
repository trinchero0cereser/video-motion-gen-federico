# Vellum Studio — showcase del sito

GOAL:    chi guarda capisce in 40 s che Vellum monta video per creator (progetti, servizi, metodo)
         e chiude sul marchio con "Request a quote".
OUTPUT:  HyperFrames. `index.html` 1920x1080 e `vertical.html` 1080x1920, 30 fps.
TIME:    40 s x 30 = 1200 frame. Nessun file in ./audio → traccia vuota, griglia 120 BPM:
         1 beat = 0,5 s = 15 frame, 1 battuta = 2 s = 60 frame. Ogni taglio cade su un beat.

LOOK
- Fondo #000000 pieno, nessuna texture. Inchiostro #F5F5F2. Grigio #8E8B85 per testo secondario.
  Linee e bordi finestre 1 px #2B2A28. Rosso #F23D3D solo come segnale: il taglio a L, il
  quadratino della sezione attiva, il bordo del tag "Sample project", il bottone del preventivo.
- Silkscreen 400 per titoli enormi e parole in evidenza (16:9: 168 px nel titolo; marquee 300 px).
  Geist 400 per i testi (titolo 168 px, tracking -0,02 em). Geist Mono 400 maiuscolo, tracking
  0,18 em, 22 px (16:9) / 30 px (9:16) per etichette e timecode.
- Il mezzo: gli screenshot reali del sito dentro finestre pulite (bordo 1 px #2B2A28, angoli vivi,
  nessuna ombra, nessuna cornice di browser o dispositivo). Prospettiva 2000 px, inclinazione max 6°.
- Barra in basso (dal secondo 4): linea 1 px #2B2A28, a sinistra ■ + nome sezione, a destra
  "TC 00:00:SS:FF" che avanza col film.

OBJECTS
- Il marchio "Taglio a L": due L #F5F5F2 (path del brief, viewBox 0 0 100 100, evenodd) e il taglio
  rosso M31 -6 V50 H69 V106. 16:9: marchio 520 px al centro; 9:16: 560 px centrato a y 749.
- Il taglio a L a tutto schermo: lo stesso percorso del taglio, allungato fino ai bordi
  (16:9: x 861 → 1059, y 540; 9:16: x 434 → 646, y 749). È la transizione tra le sezioni: la linea
  rossa si disegna (0,35 s), poi la scena nuova si apre come una fessura a L che si allarga
  (clip-path, 0,6 s power3.inOut). Quando escono dal marchio, le due L si spostano con i bordi
  della fessura.
- La finestra pixel del preventivo (09): il video segnaposto è coperto con la nostra ripresa
  (crop del progetto 05 + titolo a pixel che scorre), mascherata con le stesse celle a scalini
  misurate sull'immagine (griglia 10x11).

MOTION
- Arrivi expo.out / power4.out; camera power2.inOut; uscite e zoom attraverso power3.in.
- Molla del logo: back.out(1.5), circa smorzamento 0,6, solo su posizione/scala, mai su opacità.
- Parole: blur 6 px → 0 in 0,13 s, 0,067 s di distanza. Lettere Silkscreen: accese a scalini, 1
  frame l'una.
- Al massimo due cose si muovono insieme. Nessun movimento lineare (il marquee usa sine.inOut).

SHOTS (16:9; la 9:16 ha gli stessi tempi)
- 0,0–4,0   Logo: il taglio si disegna 0,0–1,0; le L arrivano dalla profondità 1,0–1,9 e si chiudono
            con la molla 1,9–2,6; tenuta; 3,0–3,4 il taglio si allunga fino ai bordi.
- 3,5–9,8   Fessura a L → "WE SHAPE / YOUR STORIES" (SHAPE e STORIES in Silkscreen) 4,1–5,2, tenuto
            fino a 6,5. 6,5 cambio con sfocatura → finestra 03, spinta verso la L 3D 6,5–8,5.
            8,5 stacco sul marchio grande; 9,0–9,8 le L si aprono e il progetto riempie lo schermo.
- 9,0–15,0  Progetti: finestra 05 (crop senza il titolo statico) + titolo a pixel "MAREA · BASSA" che
            scorre, tag "SAMPLE PROJECT / LONG-FORM / STORYTELLING".
- 14,5–20,0 Servizi: taglio a L → finestra 06, poi zoom sulle righe e pan verso il basso.
- 19,5–28,0 Metodo (07: pan sui quattro step coi timecode rossi), Domande (08: zoom sulla prima
            domanda, pan in basso), Telefono (10 e 11 affiancati, entrano dalla profondità).
- 27,5–35,0 Preventivo: taglio a L → finestra 09 con la nostra ripresa nella finestra pixel,
            spinta lenta, poi zoom sul dettaglio "TUO ▣ NALE" e sui bottoni.
- 34,5–40,0 Chiusura: taglio a L → marchio, "VELLUM STUDIO", bottone "REQUEST A QUOTE", tenuta 2 s+.

BANNED:  pellicola, fotogrammi di film, glow, luci, particelle, emoji, effetti stock, swipe da
         template, mockup di laptop/telefono, cornici di browser, numeri/clienti/recensioni inventati,
         più di 6 parole per scritta, movimenti lineari, più di due cose in movimento, il logo fisso
         in un angolo, titoli che continuano a muoversi dopo l'arrivo, la macchina segnaposto (04, 09).
QA:      fotogrammi 1,2 / 5,0 / 9,3 / 12,0 / 23,5 / 38,5 in entrambi i formati.
