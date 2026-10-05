# Valutatore affitti Copenaghen

Uno strumento per confrontare le case in affitto a Copenaghen. Apri `index.html` in un browser moderno (insieme alla cartella `data/`): non serve installare nulla e i tuoi dati restano nel browser.

Si parte dal presupposto che ogni opzione inserita rispetti **già i tuoi requisiti irrinunciabili**. Lo strumento confronta ciò che resta su costi, quartiere e qualità della vita, e riassume tutto in un punteggio a stelle.

## Cosa inserisci

- **Una volta:** stipendio netto mensile, altre spese mensili (facoltativo) e permanenza prevista.
- **Per ogni casa:** via e civico (il quartiere e la posizione sulla mappa si ricavano da soli), affitto, utenze, deposito, durata del contratto, arredata o no, tragitto casa-lavoro, costo dei trasporti, servizi inclusi (palestra, internet, lavanderia) e una valutazione a stelle della qualità dell'alloggio.
- **Per ogni quartiere:** da 1 a 5 stelle su sicurezza, servizi e vita sociale, cioè ciò che i dati aperti non coprono a livello di quartiere. La valutazione è condivisa da tutte le case nello stesso quartiere.
- **Priorità (facoltativo):** il peso di ogni criterio. Affitto e costi partono con peso alto come fattore chiave, insieme alla sicurezza.

## Dati integrati per indirizzo

Dall'indirizzo il modello calcola da solo tre criteri con dati reali:

- **Metro e treno:** distanza dalla stazione di metro o S-tog più vicina.
- **Verde:** distanza dal parco più vicino di almeno 1 ettaro.
- **Tranquillità:** rumore stradale Lden all'indirizzo (abitazione più esposta, mappatura 2022). Il valore guida danese per le abitazioni è 58 dB.

Fonti: Københavns Kommune, dati aperti (rumore stradale per abitazione, quartieri, stazioni, parchi) e © OpenStreetMap contributors per indirizzi e confini di Frederiksberg, dove il rumore non è disponibile. La criminalità è pubblicata solo per comune, quindi la sicurezza resta un voto tuo.

Per aggiornare i dati: `pip install shapely pyproj && python3 tools/build_data.py`, che scarica le fonti e rigenera `data/cph-data.js`.

## Cosa ottieni

- **Verdetto:** la casa con il punteggio più alto e il suo costo mensile tutto incluso.
- **Mappa:** quartieri, parchi, stazioni e le case della shortlist numerate per classifica. Una via sconosciuta si può posizionare cliccando sulla mappa.
- **Valutazione a stelle:** totale e stelle per affitto e costi, quartiere, tragitto e alloggio, con il dettaglio dei quartieri.
- **Costi a confronto:** costo mensile tutto incluso, quota del netto con indicatore di sostenibilità, quanto resta ogni mese, contanti iniziali e contratto.
- **Da ricontrollare:** pochi avvisi mirati, ad esempio un deposito oltre tre mesi di affitto o un quartiere non ancora valutato.

## Come viene calcolato

- **Affitto e costi:** 5 stelle se il costo mensile tutto incluso è al massimo il 25% del netto, 0 stelle dal 55% in su.
- **Tragitto:** 5 stelle fino a 10 minuti, 0 stelle da 60 minuti in su.
- **Metro e treno:** 5 stelle entro 300 m, una in meno ogni 300 m. **Verde:** 5 stelle entro 200 m, una in meno ogni 250 m. **Tranquillità:** 5 stelle a 50 dB, una in meno ogni 5 dB.
- **Sicurezza, servizi, vita sociale e alloggio:** le stelle che assegni tu.
- **Totale:** media pesata secondo le priorità. Le opzioni non sostenibili finiscono in fondo.

Importi in corone danesi (kr). I dati di esempio sono illustrativi: verifica sempre il contratto reale.
