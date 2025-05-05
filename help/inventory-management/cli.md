---
title: Riferimento CLI [!DNL Inventory Management]
description: Scopri i comandi forniti dal modulo  [!DNL Inventory Management]  per gestire i dati di inventario e le impostazioni di configurazione.
exl-id: d92dffce-94a1-443c-8c72-98fecbbd5320
level: Experienced
feature: Inventory, Configuration
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: b4623ada788d44f4628930dcf5dfcb51dd88ee3a
workflow-type: tm+mt
source-wordcount: '843'
ht-degree: 0%

---

# Riferimento CLI [!DNL Inventory Management]

[!DNL Inventory Management] fornisce comandi per gestire i dati di inventario e le impostazioni di configurazione.

Questi comandi includono:

- Verifica e risoluzione delle incongruenze nelle prenotazioni che influiscono sulla quantità vendibile
- Aggiunta di geocodici per l&#39;algoritmo Distance Priority

## Risolvere le incoerenze nelle prenotazioni

Nelle prenotazioni viene applicata una sospensione per quantità vendibile per SKU prodotto per magazzino. Quando si spediscono, si aggiungono prodotti, si annulla o si rimborsa un ordine, gli impegni di retribuzione vengono inseriti per inserire o cancellare questi blocchi.

[!DNL Inventory Management] fornisce due comandi per verificare e risolvere le incoerenze nelle prenotazioni:

- [&quot;inventory:reservation:list-incoerencies&quot;](#list-inconsistencies-command)
- [`inventory:reservation:create-compensations`](#create-compensations-command)

### Cause delle incongruenze nelle prenotazioni

[!DNL Inventory Management] genera prenotazioni per eventi chiave:

- Posizionamento ordine (prenotazione iniziale)
- Spedizione ordine (prenotazione retribuzione)
- Ordine di rimborso o emissione di una nota di accredito (prenotazione retribuzione)
- Annullamento ordine (prenotazione retribuzione)

È possibile che si verifichino incongruenze nelle prenotazioni quando:

- [!DNL Inventory Management] perde la prenotazione iniziale e immette troppe compensazioni per la prenotazione (sovracompensazione e conseguente incoerenza degli importi)
- [!DNL Inventory Management] inserisce correttamente la prenotazione iniziale, ma perde le prenotazioni compensative.

È possibile rivedere e controllare manualmente le prenotazioni nella tabella `inventory_reservation`.

Le configurazioni e gli eventi seguenti possono causare incongruenze nelle prenotazioni:

- **Eseguire l&#39;aggiornamento alla versione 2.3.x con ordini non in stato finale (Completato, Annullato o Chiuso).** [!DNL Inventory Management] crea prenotazioni compensative per questi ordini, ma non inserisce o non dispone della prenotazione iniziale che deduce dalla quantità vendibile. Si consiglia di utilizzare questi comandi dopo l’aggiornamento ad Adobe Commerce o Magento Open Source v2.3.x da 2.1.x o 2.2.x. Se sono presenti ordini in sospeso, i comandi aggiornano correttamente la quantità e gli impegni di vendita per l&#39;evasione degli ordini e delle vendite.
- **Non si gestiscono le scorte e successivamente si modifica questa configurazione.** È possibile iniziare a utilizzare 2.3.x con **[!UICONTROL Manage Stock]** impostato su `No` nella configurazione. [!DNL Commerce] non effettua prenotazioni agli eventi di invio e di spedizione dell&#39;ordine. Se in seguito si abilita la configurazione di **[!UICONTROL Manage Stock]** e vengono creati alcuni ordini, la Qtà vendibile verrà danneggiata con la prenotazione della retribuzione quando si gestisce e si esegue l&#39;ordine.
- **È possibile riassegnare le azioni per un sito Web mentre gli ordini vengono inviati a tale sito Web**. La prenotazione iniziale viene inserita per lo stock iniziale e tutte le prenotazioni di retribuzione vengono inserite nel nuovo stock.
- **Il totale di tutte le prenotazioni potrebbe non essere risolto in `0`.** Tutte le prenotazioni nell&#39;ambito di un ordine in uno stato finale (Completato, Annullato, Chiuso) devono essere risolte in `0`, cancellando tutti i blocchi di quantità vendibili.

### comando Elenca incoerenze

Il comando `list-inconsistencies` rileva ed elenca tutte le incoerenze delle prenotazioni. Utilizza le opzioni del comando per controllare solo gli ordini completati o incompleti o tutti.

```bash
bin/magento inventory:reservation:list-inconsistencies
```

Opzioni comando:

- `-c`, `--complete-orders` - Restituisce incoerenze per gli ordini completati. Per gli ordini completati, le prenotazioni non corrette potrebbero essere ancora bloccate.
- `-i`, `--incomplete-orders` - Restituisce incoerenze per ordini incompleti (parzialmente spediti, non spediti). Le prenotazioni non corrette potrebbero contenere quantità eccessive o insufficienti per gli ordini.
- `-b`, `--bunch-size` - Definisce quanti ordini caricare contemporaneamente.
- `-r`, `--raw` - Output non elaborato.

Le risposte che utilizzano `-r` restituiscono in formato `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>`:

- L’ID ordine indica l’ambito dell’incoerenza.
- SKU indica il prodotto con l’incoerenza.
- Quantità imposta l&#39;importo da inserire per la retribuzione della prenotazione.
- L&#39;ID magazzino definisce l&#39;ambito per le scorte, che utilizza gli impegni per calcolare la quantità vendibile.

Esempi:

```bash
bin/magento inventory:reservation:list-inconsistencies

Inconsistencies found on following entries:
Order 172:
- Product bike-123 should be compensated by +2.000000 for stock 1
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r

172:bike-123:+2.000000:1
```

Se non vengono trovati problemi, questo messaggio restituisce: non sono state trovate incongruenze nell’ordine.

### Crea compensazioni, comando

Il comando `create-compensations` crea prenotazioni di retribuzione. A seconda del problema, vengono create nuove prenotazioni per inserire o rilasciare un blocco sulla quantità vendibile.

Per creare prenotazioni, fornire compensi utilizzando il formato `<ORDER_INCREMENT_ID>:<SKU>:<QUANTITY>:<STOCK-ID>` come `172:bike-123:+2.000000:1`.

```bash
bin/magento inventory:reservation:create-compensations
```

Opzione comando:

- `-r`, `--raw` - Restituisce l&#39;output non elaborato.

Se il formato della richiesta non è corretto, viene visualizzato il seguente messaggio:

```
Error while parsing argument "your_incorrect_format_argument". Given argument does not match pattern "/(?P<increment_id>.*):(?P<sku>.*):(?P<quantity>.*):(?P<stock_id>.*)/".
```

Quando il comando crea prenotazioni, visualizza messaggi che indicano gli aggiornamenti per SKU, ordine e stock.

```bash
bin/magento inventory:reservation:create-compensations 172:bike-123:+2.000000:1

Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
```

Se lo SKU per una voce di retribuzione include spazi, racchiuderlo tra virgolette.

```bash
bin/magento inventory:reservation:create-compensations 172:"bike 123":+2.000000:1
```

### Rilevare incoerenze e creare compensazioni

È possibile rilevare incoerenze e creare immediatamente compensazioni utilizzando una pipe per eseguire sia `list-inconsistencies` che `create-compensations`. Utilizzare l&#39;opzione di comando `-r` per generare e inviare i dati non elaborati a `create-compensations`.

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

Esempio di risposta:

```bash
bin/magento inventory:reservation:list-inconsistencies -r | bin/magento inventory:reservation:create-compensations
```

```
Following reservations were created:
- Product bike-123 was compensated by +2.000000 for stock 1
- Product bikehat-456 was compensated by +1.000000 for stock 1
```

Al termine degli aggiornamenti, esegui il comando list per verificare:

```bash
bin/magento inventory:reservation:list-inconsistencies -r
```

```
No order inconsistencies were found.
```

È inoltre possibile reindirizzare i comandi per rilevare incoerenze e creare compensazioni solo per ordini incompleti (`-i`) o completi (`-c`).

```bash
bin/magento inventory:reservation:list-inconsistencies -r -i | bin/magento inventory:reservation:create-compensations
```

```bash
bin/magento inventory:reservation:list-inconsistencies -r -c | bin/magento inventory:reservation:create-compensations
```

## Importa geocodici

[!DNL Inventory Management] fornisce l&#39;[algoritmo di priorità distanza](distance-priority-algorithm.md), che consente di determinare l&#39;opzione migliore per la spedizione di un ordine completo o parziale. L&#39;algoritmo utilizza le informazioni GPS o i geocodici per calcolare la distanza tra l&#39;origine (un magazzino o un&#39;altra ubicazione fisica) di ciascun articolo in un ordine e l&#39;indirizzo di spedizione. In base a tali risultati, l’algoritmo consiglia quale origine deve essere utilizzata per spedire ogni articolo nell’ordine.

Il commerciante seleziona il fornitore dei dati GPS o geocode necessari per calcolare le distanze:

- **Google MAP** utilizza i servizi [Google Maps Platform](https://mapsplatform.google.com/) per calcolare la distanza e l&#39;ora tra l&#39;indirizzo di destinazione di spedizione e i percorsi di origine. Questa opzione richiede un piano di fatturazione Google e può comportare costi attraverso Google.

- **Il calcolo offline** calcola la distanza utilizzando i dati scaricati da [geonames.org](https://www.geonames.org/) e importati in Commerce con un comando. Questa opzione è gratuita.

Per importare i geocodici per il calcolo non in linea:

Immettere il comando seguente con un elenco separato da spazi di [codici paese ISO-3166 alpha2](https://www.geonames.org/countries/):

```bash
bin/magento inventory-geonames:import <country code> <country code> ...
```

Ad esempio:

```bash
bin/magento inventory-geonames:import us ca gb de
```

Il sistema scarica e importa i dati dei geocodici nel database, quindi visualizza il messaggio `Importing <country code>: OK`.
