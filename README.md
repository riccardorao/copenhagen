# Valutatore affitti Copenaghen

Confronta le case in affitto a Copenaghen che rispettano già i tuoi requisiti irrinunciabili. Apri `index.html` in un browser moderno, insieme alla cartella `data/`: non serve installare nulla e i tuoi dati restano nel browser.

## Come si usa

1. **Tu:** netto mensile, altre spese, permanenza.
2. **Shortlist:** per ogni casa via e civico (quartiere e posizione sulla mappa si ricavano da soli), affitto, utenze, deposito, contratto, arredamento, tragitto, trasporti, servizi inclusi e il tuo voto all'alloggio. Una via sconosciuta si posiziona cliccando sulla mappa.
3. **Quartieri:** il tuo voto a servizi e vita sociale.

Tutti i voti a stelle vanno da 0,5 a 5 a passi di mezza stella: un clic sulla metà di una stella, lo stesso clic di nuovo per azzerare, oppure le frecce della tastiera.

## Cosa mostra

- **Migliore:** la casa col punteggio più alto, con le sue stelle e il costo mensile tutto incluso.
- **Mappa:** quartieri, parchi, stazioni e le case numerate per classifica.
- **Stelle:** totale, costi, zona, tragitto e alloggio. "Dettaglio" apre sicurezza, metro, verde, quiete, servizi e vita sociale; passando il cursore su una stella compare il dato sottostante.
- **Costi:** kr al mese tutto incluso, quota dell'affitto sul netto con indicatore (✓ fino al 30%, ! fino al 40%, ✕ oltre), quanto resta ogni mese, contanti all'ingresso e contratto.
- **Attenzione:** etichette brevi solo quando serve: rumore alto, sera poco sicura, deposito oltre tre mesi, vincolo più lungo della permanenza, voti mancanti.

## Dati integrati per indirizzo

- **Sicurezza:** [Tryghedsundersøgelse 2025](https://www.kk.dk/sites/default/files/2025-06/Tryghedsunders%C3%B8gelsen%202025.pdf) del Comune di Copenaghen, nei suoi 13 quartieri: media tra residenti che si sentono sicuri nel quartiere e la sera. 70% = 1 stella, 90% = 5. I reati per 1.000 abitanti restano nel dettaglio come contesto.
- **Metro e treno:** distanza dalla stazione più vicina. 5 stelle entro 300 m, una in meno ogni 300 m.
- **Verde:** distanza dal parco di almeno 1 ettaro più vicino. 5 stelle entro 200 m, una in meno ogni 250 m.
- **Quiete:** rumore stradale Lden all'indirizzo (mappatura 2022). 5 stelle a 50 dB, una in meno ogni 5 dB.

Fonti: Københavns Kommune (dati aperti) e © OpenStreetMap contributors per indirizzi e confini di Frederiksberg, dove rumore e indagine sulla sicurezza non sono disponibili. Per aggiornare i dati: `pip install shapely pyproj && python3 tools/build_data.py`.

Importi in corone danesi (kr). I dati di esempio sono illustrativi.
