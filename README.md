# Sito NeoGauge

Landing page statica di NeoGauge, pensata per una futura pubblicazione tramite GitHub Pages.

## Anteprima locale

Aprire un terminale nella cartella `Website` e avviare:

```sh
python3 -m http.server 8080
```

Visitare poi `http://localhost:8080`.

## Prima della pubblicazione

- Sostituire il riquadro “Prossimamente su App Store” con il collegamento pubblico reale.
- Inserire eventuali schermate reali definitive dell'app.
- Configurare dominio e immagine social definitiva.

## Pubblicazione con GitHub Pages

Il sito vive nel repository pubblico separato `DjConny/NeoGauge-Site`. Il repository privato `DjConny/NeoGauge` continua a contenere soltanto il progetto dell'app e non viene esposto dalla pubblicazione.

Il workflow `.github/workflows/deploy.yml` pubblica automaticamente il contenuto del repository del sito.

1. Salvare le modifiche in un commit e inviarle al repository GitHub.
2. Aprire `Settings > Pages` nel repository `DjConny/NeoGauge-Site`.
3. In `Build and deployment`, scegliere `GitHub Actions` come origine.
4. Aprire la scheda `Actions` e attendere il completamento di `Pubblica sito NeoGauge`.
5. Il sito sarà disponibile all'indirizzo `https://djconny.github.io/NeoGauge-Site/`.

Un dominio personale potrà essere collegato in seguito senza rifare il sito.

## Visualizzazioni

La soluzione consigliata è Cloudflare Web Analytics: mostra visualizzazioni, visitatori, provenienza e prestazioni in un pannello privato, senza inserire un contatore pubblico nella pagina.

Per attivarla servono:

1. un account Cloudflare;
2. la registrazione dell'indirizzo pubblico del sito in Web Analytics;
3. il token contenuto nel beacon JavaScript generato da Cloudflare;
4. l'inserimento del beacon in `index.html`;
5. l'aggiornamento dell'informativa privacy del sito prima della pubblicazione del beacon.

Non inserire un token di esempio: fino alla configurazione reale il sito non invia dati a servizi di analisi.

Il sito non presenta NeoGauge come navigatore: esclude esplicitamente mappe, pianificazione di itinerari, GPX e ricostruzione del tragitto.
