---
title: '[!UICONTROL Catalog] &gt; [!UICONTROL Inventory]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Catalog] &gt; [!UICONTROL Inventory] pagina dell’amministratore di Commerce.
exl-id: 80113a31-3585-4ee1-95af-31efc09389eb
feature: Configuration, Inventory
source-git-commit: 80630957dbe25d21c45f64d8027a39b7b396619d
workflow-type: tm+mt
source-wordcount: '1223'
ht-degree: 0%

---

# [!UICONTROL Catalog] > [!UICONTROL Inventory]

{{config}}

>[!NOTE]
>
>[!DNL Inventory Management] per Adobe Commerce e Magento Open Source offre gli strumenti per gestire l’inventario dei prodotti. I commercianti con un singolo punto vendita in più magazzini, magazzini, ubicazioni di prelievo, corrieri diretti e altro ancora possono utilizzare queste funzioni per gestire le quantità per le vendite e gestire le spedizioni per completare gli ordini. Per ulteriori informazioni su queste funzioni e su come utilizzarle per gestire le scorte in più posizioni, vedere [_[!DNL Inventory Management] Guida utente _](https://experienceleague.adobe.com/docs/commerce-admin/inventory/introduction.html).

## [!UICONTROL Stock Options]

![Opzioni Stock](./assets/catalog-inventory-stock-options.png)<!-- zoom -->

<!-- [Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Decrease Stock When Order is Placed] | Globale | Se impostato su `Yes`, diminuisce la quantità in magazzino al momento dell&#39;ordine. Con _Gestisci Stock_ abilitato, vengono inserite prenotazioni per i prodotti e le quantità ordinati. Opzioni: `Yes` / `No` |
| [!UICONTROL Set Items' Status to be in Stock When Order is Cancelled] | Visualizzazione store | Se impostato su `Yes`, restituisce l&#39;articolo in magazzino quando l&#39;ordine viene annullato. Con _Gestisci Stock_ abilitata, la prenotazione viene cancellata per i prodotti e le quantità annullati. Opzioni: `Yes` / `No` |
| [!UICONTROL Display Out of Stock Products] | Globale | Se impostato su `Yes`, visualizza i prodotti esauriti. Se sono attivati anche gli avvisi sui prodotti, i clienti possono registrarsi per ricevere una notifica quando il prodotto diventa disponibile. Opzioni: `Yes` / `No` |
| [!UICONTROL Only X left Threshold] | Sito Web | Stabilisce la soglia per il `Only x left` messaggio. Ad esempio, se è impostato su 3, il messaggio viene visualizzato quando un articolo è in stock per un massimo di tre unità. Il messaggio non viene visualizzato se il valore è impostato su `0`. |
| [!UICONTROL Display products availability in Stock on Storefront] | Visualizzazione store | Se impostato su `Yes`, visualizza un `In Stock` o `Out of Stock` sulla pagina del prodotto. Opzioni: `Yes` / `No` |
| [!UICONTROL Enable Inventory Check On Cart Load] | Globale | Determina se viene eseguito un controllo dell&#39;inventario durante il caricamento di un prodotto nel carrello. La disattivazione di questo controllo dell’inventario può migliorare le prestazioni per i passaggi di pagamento, soprattutto quando nel carrello sono presenti molti articoli. Tuttavia, se salti la pre-convalida, i clienti potrebbero vedere _esaurito_ errori più avanti nel processo di pagamento. Opzioni: `Yes` / `No` |
| [!UICONTROL Synchronize with Catalog] | Globale | Se impostato su `Yes`, i dati di inventario vengono regolati in base alle modifiche apportate al catalogo (ad esempio rimozioni di prodotti, modifiche SKU di prodotti e modifiche al tipo di prodotto) e mantiene la coerenza tra inventario e catalogo. Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Product Stock Options]

![Opzioni magazzino prodotto](./assets/catalog-inventory-product-stock-options.png)<!-- zoom -->

<!-- [Product Stock Options](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Manage Stock] | Globale | Determina se si utilizza il controllo completo dell&#39;inventario per gestire gli articoli nel catalogo. Opzioni: <br/>**Sì** - Attiva il controllo completo dell&#39;inventario per tenere traccia del numero di articoli attualmente in magazzino. <br/>**No** - Non tiene traccia del numero di articoli attualmente in magazzino. |
| [!UICONTROL Backorders] | Globale | Determina il modo in cui lo store gestisce gli ordini inevasi. Un ordine inevaso non modifica lo stato di elaborazione dell’ordine. I fondi vengono comunque autorizzati o acquisiti immediatamente al momento dell&#39;ordine, indipendentemente dal fatto che il prodotto sia in magazzino. Quando il prodotto diventa disponibile, viene spedito. Opzioni: <br/>**Nessun ordine arretrato** - Non accetta ordini inevasi quando il prodotto è esaurito. <br/>**Consenti qtà inferiore a 0** - Accetta ordini inevasi quando la quantità scende sotto zero. <br/>**Consenti quantità inferiore a 0 e notifica al cliente** - Accetta ordini inevasi quando la quantità scende al di sotto di zero, ma notifica ai clienti che gli ordini possono ancora essere effettuati. |
| [!UICONTROL Use deferred Stock update] | Globale | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Determina se posticipare l&#39;aggiornamento delle scorte se sono consentiti ordini inevasi (il _Ordini arretrati_ è impostata su qualsiasi elemento oltre a `No backorders` valore predefinito). Funziona per un singolo prodotto o un intero sito Web e utilizza _Coda processi_ meccanismo per consentire l&#39;aggiornamento asincrono degli indicatori di quantità di magazzino dopo l&#39;inserimento degli ordini. Questa opzione funziona anche con [Posizionamento dell’ordine asincrono](https://experienceleague.adobe.com/docs/commerce-operations/performance-best-practices/high-throughput-order-processing.html#asynchronous-order-placement) in combinazione con [Inventory management](../../inventory-management/introduction.md). |
| Quantità massima consentita nel carrello | Globale | Determina il numero massimo di prodotti che possono essere acquistati in un singolo ordine. Per impostazione predefinita, la quantità massima è impostata su 10.000. |
| [!UICONTROL Out-of-Stock Threshold] | Globale | Determina il livello di scorte al quale un prodotto viene considerato esaurito. Opzioni: <br/>**Importo positivo** - Con _Ordini arretrati_ disabilitato, inserisci un importo positivo. Con ordini inevasi abilitati, questo importo viene ignorato. <br/>**Zero** - Con _Ordini arretrati_ abilitato, immissione `0` consente ordini inevasi infiniti. <br/>**Importo negativo** - Con _Ordini arretrati_ attivato, si consiglia di immettere un importo negativo. L&#39;importo viene aggiunto alla quantità di vendita. Ad esempio, immettere -50 per consentire ordini fino a questo importo. |
| [!UICONTROL Minimum Qty Allowed in Shopping Cart] | Globale | Determina l&#39;importo minimo di un articolo disponibile per l&#39;acquisto in base al gruppo di clienti. Per impostazione predefinita, la quantità minima è impostata su 1. Clic **[!UICONTROL Add Minimum Qty]** per inserire un valore diverso per un gruppo di clienti specifico. |
| [!UICONTROL Notify for Quantity Below] | Globale | Determina il livello delle scorte al quale viene inviata la notifica che le scorte sono scese al di sotto della soglia. |
| [!UICONTROL Enable Qty Increments] | Globale | Determina se gli articoli possono essere venduti con incrementi di quantità. Opzioni: `Yes` / `No` |
| [!UICONTROL Qty Increments] | Globale | Stabilisce il numero di prodotti che compongono un incremento di quantità. |
| [!UICONTROL Automatically Return Credit Memo Item to Stock] | Globale | Determina se gli articoli inclusi nelle note di accredito vengono automaticamente restituiti al magazzino. Opzioni: `Yes` / `No` |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Admin Bulk Operations]

![Operazioni di amministrazione in blocco](./assets/catalog-inventory-admin-bulk-operations.png)<!-- zoom -->

<!-- [Admin Bulk Operations](https://docs.magento.com/user-guide/catalog/inventory-options-global.html) -->

>[!NOTE]
>
>Per configurare e supportare **responsabili coda asincroni**, è necessario utilizzare la riga di comando. Questo potrebbe richiedere l’assistenza dello sviluppatore. Consulta [Avvia consumer coda messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) nel _Guida alla configurazione_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Run asynchronously] | Globale | Determina se eseguire operazioni in blocco in modo asincrono per azioni di massa sui prodotti, tra cui [in blocco](../../inventory-management/bulk-assignment.md) assegnare le origini, annullare l&#39;assegnazione delle origini e [trasferisci magazzino all&#39;origine](../../inventory-management/inventory-transfer.md). Raccoglie azioni in blocco fino al _[!UICONTROL Asynchronous batch size]_, quindi esegue tali azioni. Questa funzione è disabilitata per impostazione predefinita. Prima di abilitare questa funzione, è consigliabile rivedere le prestazioni con azioni in blocco. Opzioni:<br/>**`Yes`**- Esegue tutte le operazioni in blocco per [!DNL Inventory Management] in modo asincrono. Per attivare questa funzione, è necessario configurare un sistema di gestione delle code asincrone.<br/>**`No`**- Impostazione predefinita. Non esegue operazioni di massa in modo asincrono. |
| [!UICONTROL Asynchronous batch size] | Globale | Imposta **[!UICONTROL Run asynchronously]** a `Yes` per immettere un valore per _[!UICONTROL Asynchronous batch size]_campo. <br/>La dimensione predefinita del batch è 100. Quando i processi in blocco raggiungono questo importo, vengono eseguiti. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Inventory Indexer Settings]

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Stock/Source reindex strategy] | Globale | Determina la strategia utilizzata per la reindicizzazione stock/sorgente. Opzioni: `Synchronous` / `Asynchronous` (è necessario configurare un gestore di code asincrone per la modalità asincrona) |

>[!NOTE]
>
> A causa delle dipendenze degli aggiornamenti di magazzino per le attività correlate all’ordine, l’indicizzatore magazzino viene attivato anche al salvataggio del prodotto, indipendentemente `Synchronous` o `Asynchronous` impostazione.


{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Distance Provider for Distance Based SSA]

![Fornitori di distanze per SSA basato sulla distanza](./assets/catalog-inventory-distance-provider.png)<!-- zoom -->

<!-- [Distance Providers for Distance Based SSA](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Provider] | Globale | Determina il provider da utilizzare per l&#39;algoritmo di selezione dell&#39;origine di priorità distanza. Questa funzione è attivata per impostazione predefinita. Opzioni: <br/>**`Google MAP`**: utilizza i servizi Google per calcolare la distanza e l’ora tra l’indirizzo della destinazione di spedizione e le posizioni di origine (indirizzo e coordinate GPS). Questa opzione richiede una chiave API Google e può comportare costi aggiuntivi tramite Google.<br/>**`Offline Calculation`** - Calcola la distanza utilizzando un database incorporato per determinare l&#39;origine più vicina all&#39;indirizzo di destinazione della spedizione. Per utilizzare questa opzione, potrebbe essere necessario richiedere l&#39;assistenza dello sviluppatore per scaricare inizialmente il contenuto della posizione del database per tutti i paesi di destinazione mediante una riga di comando. |

{:style=&quot;table-layout:auto&quot;}

## [!UICONTROL Google Distance Provider]

![Provider distanza Google](./assets/catalog-inventory-distance-provider-settings.png)<!-- zoom -->

<!-- [Google Distance Provider](https://docs.magento.com/user-guide/catalog/inventory-configure-distance-priority.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Google API key] | Globale | Immetti la chiave API Google per il provider Google MAP. La chiave proviene da [!DNL Google Maps Platform] e dovrebbero avere [!DNL Geocoding API] e [!DNL Distance Matrix API] abilitato. Per ulteriori informazioni, consulta [Configurare l&#39;algoritmo di priorità della distanza](../../inventory-management/distance-priority-algorithm.md#configure-the-distance-priority-algorithm) nel _Guida di Inventory management_. |
| [!UICONTROL Computation mode] | Globale | Determina le direzioni e i percorsi per calcolare la distanza dall&#39;indirizzo di spedizione e da tutte le origini assegnate al magazzino. Per impostazione predefinita, i calcoli utilizzano la modalità guida. Opzioni: <br/>**`Driving`**- Impostazione predefinita, richiede indicazioni stradali standard utilizzando la rete stradale.<br/>**`Walking`** - Richiede indicazioni stradali utilizzando sentieri pedonali e marciapiedi (se disponibili). <br/>**`Bicycling`**- Richiede indicazioni per il ciclismo utilizzando piste ciclabili e strade preferite (attualmente disponibili solo negli Stati Uniti e in alcune città canadesi). |
| [!UICONTROL Value] | Globale | Indica cosa calcolare e restituire per la distanza e l&#39;ora per le ubicazioni di origine all&#39;indirizzo di destinazione di spedizione. L&#39;algoritmo di priorità distanza consiglia l&#39;origine con la distanza o il tempo più breve all&#39;indirizzo di destinazione della spedizione, che fornisce più velocemente e possibilmente più economico per evadere le spedizioni. Opzioni: <br/>**`Distance`**- Restituisce la distanza tra i punti in metriche (chilometri e metri) o imperiali (miglia e piedi).<br/>**`Time to Destination`** - Restituisce il tempo necessario per spostarsi dalle località di origine all&#39;indirizzo di spedizione in ore e minuti. |

{:style=&quot;table-layout:auto&quot;}
