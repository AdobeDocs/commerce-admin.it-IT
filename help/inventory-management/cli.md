---
title: '[!DNL Inventory Management] Riferimento CLI'
description: Scopri i comandi forniti da [!DNL Inventory Management] per gestire i dati di inventario e le impostazioni di configurazione.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---

# [!DNL Inventory Management] Riferimento CLI

[!DNL Inventory Management] fornisce comandi per gestire i dati di inventario e le impostazioni di configurazione.

Questi comandi includono:

- Verifica e risoluzione delle incongruenze nelle prenotazioni che influiscono sulla quantità vendibile
- Aggiunta di geocodici per l&#39;algoritmo Distance Priority

## Risolvere le incoerenze nelle prenotazioni

Nelle prenotazioni viene applicata una sospensione per quantità vendibile per SKU prodotto per magazzino. Quando si spediscono, si aggiungono prodotti, si annulla o si rimborsa un ordine, gli impegni di retribuzione vengono inseriti per inserire o cancellare questi blocchi.

[!DNL Inventory Management] fornisce due comandi per verificare e risolvere le incoerenze nella prenotazione:

- [&#39;inventory:reservation:list-incoerencies`](#list-inconsistencies-command)
- [&#39;inventory:reservation:create-compensations&quot;](#create-compensations-command)

### Cause delle incongruenze nelle prenotazioni

[!DNL Inventory Management] genera prenotazioni per eventi chiave:

- Posizionamento ordine (prenotazione iniziale)
- Spedizione ordine (prenotazione retribuzione)
- Ordine di rimborso o emissione di una nota di accredito (prenotazione retribuzione)
- Annullamento ordine (prenotazione retribuzione)

È possibile che si verifichino incongruenze nelle prenotazioni quando:

- [!DNL Inventory Management] perde la prenotazione iniziale e inserisce troppe compensazioni per le prenotazioni (sovracompensazione e conseguente incoerenza degli importi)
- [!DNL Inventory Management] inserisce correttamente la prenotazione iniziale, ma perde le prenotazioni compensative.

Puoi rivedere e controllare manualmente gli impegni in `inventory_reservation` tabella.

Le configurazioni e gli eventi seguenti possono causare incongruenze nelle prenotazioni:

- **Esegui l’aggiornamento alla versione 2.3.x con ordini non in stato finale (Completato, Annullato o Chiuso).** [!DNL Inventory Management] crea impegni compensativi per questi ordini, ma non inserisce o non dispone dell&#39;impegno iniziale che deduce dalla quantità vendibile. Si consiglia di utilizzare questi comandi dopo l’aggiornamento ad Adobe Commerce o Magento Open Source v2.3.x da 2.1.x o 2.2.x. Se sono presenti ordini in sospeso, i comandi aggiornano correttamente la quantità e gli impegni di vendita per l&#39;evasione degli ordini e delle vendite.
- **Non si gestisce il materiale e successivamente si modifica questa configurazione.** È possibile iniziare a utilizzare 2.3.x con **[!UICONTROL Manage Stock]** imposta su `No` nella configurazione. [!DNL Commerce] non effettua prenotazioni a eventi di inserimento ordini e spedizione. Se in seguito si abilita **[!UICONTROL Manage Stock]** e alcuni ordini vengono creati, la Qtà vendibile risulterebbe danneggiata con la prenotazione della retribuzione quando si gestisce e si evade l&#39;ordine.
- **Si riassegna il titolo per un sito Web mentre gli ordini vengono inviati a tale sito Web**. La prenotazione iniziale viene inserita per lo stock iniziale e tutte le prenotazioni di retribuzione vengono inserite nel nuovo stock.
- **Il totale di tutte le prenotazioni potrebbe non essere risolto in `0`.** Tutte le prenotazioni nell&#39;ambito di un ordine in uno stato finale (Completato, Annullato, Chiuso) devono essere risolte in `0`, cancellando tutti i blocchi di quantità vendibili.

### comando Elenca incoerenze

Il `list-inconsistencies` Il comando rileva ed elenca tutte le incongruenze relative alle prenotazioni. Utilizza le opzioni del comando per controllare solo gli ordini completati o incompleti o tutti.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Opzioni comando:

- `-c`, `--complete-orders` - Restituisce incoerenze per gli ordini completati. Per gli ordini completati, le prenotazioni non corrette potrebbero essere ancora bloccate.
- `-i`, `--incomplete-orders` - Restituisce incoerenze per ordini incompleti (parzialmente spediti, non spediti). Le prenotazioni non corrette potrebbero contenere quantità eccessive o insufficienti per gli ordini.
- `-b`, `--bunch-size` - Definisce quanti ordini caricare contemporaneamente.
- `-r`, `--raw` - Uscita raw.

Risposte utilizzando `-r` torna in `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` formato:

- L’ID ordine indica l’ambito dell’incoerenza.
- SKU indica il prodotto con l’incoerenza.
- Quantità imposta l&#39;importo da inserire per la retribuzione della prenotazione.
- L&#39;ID magazzino definisce l&#39;ambito per le scorte, che utilizza gli impegni per calcolare la quantità vendibile.

Esempi:

```terminal
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```terminal
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Se non vengono trovati problemi, questo messaggio restituisce: non sono state trovate incongruenze nell’ordine.

### Crea compensazioni, comando

Il `create-compensations` Il comando crea prenotazioni retribuzione. A seconda del problema, vengono create nuove prenotazioni per inserire o rilasciare un blocco sulla quantità vendibile.

Per creare prenotazioni, fornisci le retribuzioni utilizzando il formato `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` come `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Opzione comando:

- `-r`, `--raw` - Restituisce l&#39;output non elaborato.

Se il formato della richiesta non è corretto, viene visualizzato il seguente messaggio:

```terminal
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

Quando il comando crea prenotazioni, visualizza messaggi che indicano gli aggiornamenti per SKU, ordine e stock.

```terminal
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Se lo SKU per una voce di retribuzione include spazi, racchiuderlo tra virgolette.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Rilevare incoerenze e creare compensazioni

Potete rilevare le incongruenze e creare immediatamente compensazioni utilizzando una tubazione per eseguire entrambe le `list-inconsistencies` e `create-compensations`. Utilizza il `-r` opzione di comando per generare e inviare i dati non elaborati `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Esempio di risposta:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```terminal
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Al termine degli aggiornamenti, esegui il comando list per verificare:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```terminal
No order inconsistencies were found.
```

È inoltre possibile reindirizzare i comandi per rilevare incoerenze e creare compensazioni solo per incompleti (`-i`) o completo (`-c`).

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importa geocodici

[!DNL Inventory Management] fornisce [Algoritmo di priorità della distanza](distance-priority-algorithm.md), che consente di determinare l’opzione migliore per la spedizione di un ordine completo o parziale. L&#39;algoritmo utilizza le informazioni GPS o i geocodici per calcolare la distanza tra l&#39;origine (un magazzino o un&#39;altra ubicazione fisica) di ciascun articolo in un ordine e l&#39;indirizzo di spedizione. In base a tali risultati, l’algoritmo consiglia quale origine deve essere utilizzata per spedire ogni articolo nell’ordine.

Il commerciante seleziona il fornitore dei dati GPS o geocode necessari per calcolare le distanze:

- **GOOGLE MAP** utilizza [Piattaforma Google Maps](https://mapsplatform.google.com/) servizi per calcolare la distanza e l&#39;ora tra l&#39;indirizzo della destinazione di spedizione e le ubicazioni di origine. Questa opzione richiede un piano di fatturazione Google e può comportare costi attraverso Google.

- **Calcolo offline** calcola la distanza utilizzando i dati scaricati da [geonames.org](https://www.geonames.org/) e importati in Commerce con un comando. Questa opzione è gratuita.

Per importare i geocodici per il calcolo non in linea:

Immetti il seguente comando con un elenco separato da spazi [Codici paese ISO-3166 alpha2](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Ad esempio:

```bash
bin/magento inventory-geonames:import us ca gb de
```

Il sistema scarica e importa i dati dei geocodici nel database, quindi visualizza il messaggio  `Importing <country code>: OK`.
