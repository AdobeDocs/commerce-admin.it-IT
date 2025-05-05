---
title: Note sulla versione di [!DNL Inventory Management]
description: Consulta le note sulla versione per informazioni su tutte le  [!DNL Inventory Management]  versioni.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: fdc14758788fa5cd0391371ebfafb478dadec8a4
workflow-type: tm+mt
source-wordcount: '3462'
ht-degree: 0%

---

# Note sulla versione di [!DNL Inventory Management]

Queste note sulla versione descrivono le versioni di [!DNL Inventory Management] e includono:

![Nuove](../assets/new.svg) nuove funzionalità
![Problema risolto](../assets/fix.svg) correzioni e miglioramenti
![Problema noto](../assets/bug.svg) Problemi noti

[!DNL Inventory Management] è un progetto speciale di progettazione della community Magento Open Source aperto ai collaboratori. Per partecipare e contribuire, consulta l&#39;archivio del progetto [GitHub](https://github.com/magento/inventory) e [wiki](https://github.com/magento/inventory/wiki) per iniziare. Per discutere il progetto, partecipa al canale [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) ([auto-abbonamento](https://opensource.magento.com/slack)).

[Pianificazione del rilascio](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} per le versioni supportate e compatibili.

## v1.2.7

Le note sulla versione di [!DNL Inventory Management] 1.2.7 sono incluse nelle [note sulla versione di core 2.4.7](https://experienceleague.adobe.com/en/docs/commerce-operations/release/notes/adobe-commerce/2-4-7#inventory-management-1).

## v1.2.6

[!DNL Inventory Management] 1.2.6 (versione modulo: `magento/inventory-metapackage = 1.2.6`) è supportato con la versione 2.4.6 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice Magento Open Source.

![Problema risolto](../assets/fix.svg) La vetrina ora visualizza i prodotti compositi (configurabili, raggruppati e raggruppati) come in magazzino quando i prodotti secondari esauriti vengono restituiti alle scorte. In precedenza, la vetrina indicava che il prodotto composito era esaurito in queste condizioni. <!-- ACP2E-1106-->

![Problema risolto](../assets/fix.svg) Le opzioni di prodotto configurabili vengono ora visualizzate come previsto come esaurite nella vetrina se l&#39;opzione è stata creata con quantità impostata su 0 e **[!UICONTROL Display out-of-stock products]** è abilitata. <!-- ACP2E-1148-->

![Problema risolto](../assets/fix.svg) Le cache delle pagine delle categorie non vengono più invalidate quando cambia la quantità di magazzino e il prodotto è ancora in magazzino. Adobe Commerce ora carica le pagine dalla cache, anziché rigenerarle quando cambia la quantità di prodotto (e nient’altro) nella pagina della categoria di vetrina. <!-- ACP2E-118-->

![Problema risolto](../assets/fix.svg) Il conteggio dei prodotti dell&#39;elenco categorie è ora corretto quando si utilizza Inventory in modalità a origine singola con l&#39;impostazione **[!UICONTROL Display Out-Of-Stock Products]** abilitata. Adobe Commerce ora controlla se un prodotto è vendibile al momento del conteggio. <!-- ACP2E-1033-->

![Problema risolto](../assets/fix.svg) Le regole del prezzo del carrello per la consegna in-store ora funzionano come previsto quando Inventory è abilitato. In precedenza, gli sconti generati dalla regola del prezzo del carrello non venivano applicati in queste condizioni. <!-- ACP2E-1015-->

![Problema risolto](../assets/fix.svg) L&#39;aggiornamento dell&#39;inventario dei prodotti in modalità pianificata non cancella più tutte le cache. In precedenza, l’indicizzatore Inventory cancellava tutte le cache di configurazione. <!-- ACP2E-1003-->

![Problema risolto](../assets/fix.svg) Il valore per l&#39;attributo **[!UICONTROL Allow Multiple Boxes for Shipping]** di un prodotto in Inventario avanzato è ora salvato come previsto. <!-- ACP2E-992-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora emette una compensazione di prenotazione accurata dopo una nota di credito di rimborso parziale per un ordine effettuato con il ritiro in-store. In precedenza, una prenotazione non corretta veniva salvata nella tabella `inventory_reservation` quando un utente amministratore creava una nota di credito senza selezionare la casella di controllo **[!UICONTROL Return to Stock]**. <!-- ACP2E-979-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più i prodotti configurabili come esauriti nella vetrina quando una delle relative varianti è stata restituita manualmente alle scorte nelle distribuzioni che implementano l&#39;inventario multiorigine. <!-- ACP2E-952-->

![Problema risolto](../assets/fix.svg) La posizione della colonna nella griglia prodotti (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) non viene più ripristinata alla posizione precedente dopo il ricaricamento della pagina nelle distribuzioni con più origini inventario configurate. <!-- ACP2E-925-->

![Emissione fissa](../assets/fix.svg) La quantità di scorte è ora corretta dopo l&#39;emissione di una nota di credito per un prodotto virtuale quando la casella di controllo **[!UICONTROL Back to stock]** non è selezionata. <!-- ACP2E-908-->

![Problema risolto](../assets/fix.svg) È ora possibile salvare le categorie con l&#39;ordinamento e l&#39;ambito dei prodotti automatici assegnati a scorte non predefinite. In precedenza, Adobe Commerce non salvava la categoria e visualizzava questo errore: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problema risolto](../assets/fix.svg) Lo stato delle scorte di prodotto configurabili ora viene aggiornato come previsto quando il prodotto viene creato con tutte le varianti configurabili esaurite. <!-- ACP2E-813-->

![Problema risolto](../assets/fix.svg) Lo strumento Analizzatore incoerenza prenotazioni ora funziona correttamente con gli ordini parzialmente spediti che contengono prodotti configurabili, raggruppati e raggruppati. Vengono ora analizzati i tipi di prodotto compositi. In precedenza, annullamenti e rimborsi venivano salvati solo per i prodotti principali e non per gli articoli di ordini di prodotti secondari di pacchetti configurabili e di spedizione. <!-- ACP2E-924-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più un errore quando un utente amministratore tenta di assegnare 200 o più origini inventario a un magazzino o a un prodotto. <!-- ACP2E-1180-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora supporta la creazione di una nota di credito per un ordine da cui è stato eliminato un prodotto. In precedenza, i commercianti non potevano creare una nota di credito quando i prodotti erano stati eliminati dall&#39;ordine dopo la creazione di una fattura. L&#39;applicazione ha visualizzato questo errore: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problema risolto](../assets/fix.svg) Gli archivi ora vengono filtrati in base a ID di archivio singoli e multipli. Il codice attributo prodotto `event` è stato aggiunto all&#39;elenco dei codici attributo riservati. In precedenza, il rapporto Stock ridotti generava un’eccezione durante l’installazione del modulo Inventario. <!-- ACP2E-1017-->

![Problema risolto](../assets/fix.svg) I filtri di navigazione a livelli ora funzionano come previsto e i prodotti esauriti sono ora aggiunti all&#39;elenco dei prodotti della categoria vetrina. Il nuovo attributo di ordinamento `is_out_of_stock` utilizza Elasticsearch Dynamic Field Mapper per la raccolta di prodotti storefront. <!-- ACP2E-748-->

![Problema risolto](../assets/fix.svg) Lo stato delle scorte del prodotto composito (bundle, raggruppato e configurabile) viene aggiornato come previsto quando lo stato delle scorte del prodotto secondario viene modificato da una chiamata REST `POST /rest/V1/inventory/source-items`. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (versione modulo: `magento/inventory-metapackage = 1.2.5`) è supportato con la versione 2.4.5 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice Magento Open Source.

![Problema risolto](../assets/fix.svg) Lo stato predefinito delle scorte di magazzino dei prodotti raggruppati e del bundle viene ora aggiornato come previsto quando un commerciante crea una spedizione dall&#39;amministratore. In precedenza, lo stato di questi prodotti rimaneva invariato dopo la creazione di una spedizione. <!--- ACP2E-418-->

![Problema risolto](../assets/fix.svg) I prodotti configurabili ora vengono ripristinati quando viene soddisfatta una delle seguenti condizioni: 1. Il prodotto padre ha almeno un figlio salvato in magazzino. 2. Il prodotto configurabile stesso è stato aggiornato e impostato come **in magazzino** e ha almeno un figlio in magazzino. <!--- ACP2E-443-->

![Problema risolto](../assets/fix.svg) Le modifiche di inventario implementate tramite l&#39;API REST ora vengono riportate come previsto nelle pagine dei dettagli del prodotto. La cache per i prodotti catalogo viene ora pulita dopo il confronto tra lo stato dell’ultimo e quello corrente. In precedenza, l’omissione della funzione di callback causava una valutazione errata delle modifiche di stato delle scorte, che non attivava la necessaria pulizia della cache. Di conseguenza, la vetrina non rifletteva le variazioni di inventario. <!--- ACP2E-161-->

![Problema risolto](../assets/fix.svg) I prodotti assegnati alle scorte predefinite e precedentemente esauriti sono ora visibili nella vetrina dopo l&#39;aggiornamento dell&#39;elemento di origine tramite `/V1/inventory/source-items`. In precedenza, questo endpoint REST API impostava `stock_status` errato. <!--- ACP2E-562-->

![Problema risolto](../assets/fix.svg) L&#39;annullamento dell&#39;assegnazione delle origini inventario tramite l&#39;azione collettiva (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) ora funziona come previsto quando le origini includono SKU duplicati ad eccezione di uno zero iniziale (ad esempio, `01234` e `1234`). In precedenza, l’applicazione non annullava l’assegnazione delle origini di inventario e generava un errore. <!--- ACP2E-2641-->

![Problema risolto](../assets/fix.svg) Lo stato delle scorte del prodotto è sempre **disponibile** nella vetrina quando sono abilitati infiniti ordini arretrati e il prodotto viene assegnato a una scorta personalizzata, indipendentemente dalla quantità inevasa. In precedenza, i prodotti esaurivano le scorte anche quando erano abilitati gli ordini inevasi. <!--- ACP2E-664-->

![È stato risolto il problema](../assets/fix.svg). Le scorte di prodotti padre e figlio configurabili ora vengono aggiornate correttamente dopo l&#39;aggiornamento dell&#39;elemento di origine con `POST /V1/inventory/source-items`. Dopo che il prodotto secondario è stato aggiornato tramite l’API, viene aggiunto un nuovo plug-in Inventory per i controlli di magazzino predefiniti e aggiorna la quantità e lo stato configurabili del prodotto. <!--- ACP2E-442-->

![Problema risolto](../assets/fix.svg) I prodotti raggruppati esauriti non sono più elencati nella pagina delle categorie della vetrina. <!--- ACP2E-2082-->

![È stato corretto il problema](../assets/fix.svg). Il nome del pacchetto in `CatalogInventory` `composer.json` è stato corretto. <!--- ACP2E-2914-->

![Problema risolto](../assets/fix.svg) Lo stato dell&#39;ordine arretrato è ora correttamente rappresentato nell&#39;amministratore dopo aver effettuato un ordine con una quantità zero di prodotto in una distribuzione con più origini/scorte. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problema risolto](../assets/fix.svg) I prodotti del bundle esauriti non vengono più visualizzati nella pagina Categoria di vetrina quando il prodotto del bundle viene aggiornato dalla sezione Stock. <!--- ACP2E-2012-->

![È stato corretto il problema](../assets/fix.svg). I problemi di compatibilità con PHP 7.4 sono stati risolti. <!--- AC-3192-->

![Problema risolto](../assets/fix.svg) Le prestazioni delle operazioni di salvataggio che includono prodotti bundle contenenti numerose opzioni (diverse 100) sono state migliorate. In precedenza, il salvataggio di questi prodotti in bundle di grandi dimensioni richiedeva diversi minuti e talvolta causava timeout nelle distribuzioni con i servizi di inventario abilitati. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Problema risolto](../assets/fix.svg) Lo strumento per azioni in blocco del prodotto (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) ora funziona come previsto quando si assegna l&#39;origine inventario a più prodotti quando gli SKU vengono duplicati, ad eccezione di un `0` iniziale (ad esempio, `01234` e `1234`). In precedenza, a un solo prodotto veniva assegnata un’origine di inventario. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problema risolto](../assets/fix.svg) Il campo `ProductInterface.only_x_left_in_stock` ora restituisce 0 se l&#39;inventario è 0. In precedenza, restituiva null. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problema risolto](../assets/fix.svg) È ora possibile modificare le scorte predefinite dall&#39;amministratore **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. In precedenza, nella console veniva visualizzato un errore di JavaScript quando si tentava di aggiungere o rimuovere sorgenti dalle scorte predefinite, anche se era possibile assegnare siti web alle scorte predefinite. <!--- ACP2E-545-->

![Problema risolto](../assets/fix.svg) <!--- ACP2E-274--> Il conteggio dei prodotti dell&#39;elenco delle categorie è ora corretto quando si utilizza la modalità a origine singola dell&#39;inventario con l&#39;impostazione **[!UICONTROL Display Out-Of-Stock Products]** abilitata. Un nuovo plug-in ora utilizza `AreProductsSalableInterface` e `StockConfigurationInterface` per determinare il numero totale di prodotti. In precedenza, l&#39;elenco dei prodotti della categoria restituiva una quantità di prodotto errata.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-322--> I prodotti configurabili ora vengono spostati all&#39;ultima posizione nell&#39;elenco dei prodotti dopo l&#39;aggiornamento delle scorte quando l&#39;impostazione **[!UICONTROL Move out of stock to the bottom]** è abilitata. Viene implementata una nuova query di database personalizzata per ignorare l’ordinamento dell’indice Elasticsearch, che ignora quello abilitato dall’amministratore. In precedenza, i prodotti configurabili e i relativi prodotti secondari non venivano spostati in fondo all’elenco quando questa impostazione era abilitata.

## v1.2.4

Inventory management 1.2.4 (versione modulo: `magento/inventory-metapackage = 1.2.4`) è supportato con la versione 2.4.4 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e la base di codice Magento Open Source.

![Problema risolto](../assets/fix.svg) Commerce ora visualizza un valore preciso per la quantità vendibile per tutti i prodotti nella visualizzazione elenco prodotti amministratore. In precedenza veniva visualizzato un valore vuoto per la quantità di prodotti in magazzino con SKU contenenti caratteri speciali. <!--- MC-41936-->

![Problema risolto](../assets/fix.svg) Sono state migliorate le prestazioni per le azioni di carrello e pagamento, ad esempio l&#39;aggiunta di prodotti al carrello in implementazioni con molte (circa 10.000) origini inventario. <!--- MC-42570-->

![Problema risolto](../assets/fix.svg) [!BADGE Solo PaaS]{type=Informative url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."} Il comando `bin/magento inventory:reservation:list-inconsistencies` ora gestisce correttamente gli ordini con spedizioni parziali anche se le prenotazioni non vengono effettuate dal database e la cache è stata cancellata. In precedenza, quando il comando veniva eseguito con una cache già cancellata, Commerce mostrava il seguente errore: `Area code is not set`. <!--- MC-42142-->


![È stato risolto il problema](../assets/fix.svg) L&#39;indicizzazione incrementale di prodotti secondari di prodotti raggruppati non causa più l&#39;indicizzazione errata di altri prodotti raggruppati quando vengono condivisi gli elementi secondari. <!--- MC-41963-->

![Problema risolto](../assets/fix.svg) Nella pagina delle categorie della vetrina ora viene visualizzato il numero di prodotti corretto dopo la rimozione di un prodotto da una categoria tramite API. In precedenza, il conteggio dei prodotti della pagina delle categorie non era corretto fino alla reindicizzazione. <!--- MC-42287-->

![Problema risolto](../assets/fix.svg) I prodotti configurabili ora possono essere restituiti alle scorte durante la creazione di una nota di credito quando l&#39;opzione **[!UICONTROL Manage Stock]** è disabilitata. In precedenza, Commerce non visualizzava la casella di controllo **Torna a magazzino** nella pagina di creazione della nota di credito quando questa opzione era disabilitata. <!--- MC-42002-->

![Problema risolto](../assets/fix.svg) È stata migliorata la gestione delle scorte di magazzino che superano i 10.000 elementi. In precedenza, a volte i problemi di prestazioni impedivano ai commercianti di modificare le risorse in Admin prima di avviare il sito web. <!--- MC-42643-->

![Problema risolto](../assets/fix.svg) La pagina **[!UICONTROL User Roles]** nell&#39;amministratore è stata aggiornata per fornire agli amministratori autorizzazioni limitate di accesso alla configurazione dei metodi di consegna. La sezione _Metodi di spedizione_ è stata rinominata in _[!UICONTROL Delivery methods]_e_[!UICONTROL In-Store Pickup]_ è stata spostata nella sezione _[!UICONTROL Delivery methods]_. [GitHub-30053](https://github.com/magento/magento2/issues/30053) <!--- MC-41545-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non crea più una prenotazione di prodotto duplicata dopo che una nota di credito è stata aggiornata dall&#39;API. <!--- MC-41757-->

![È stato risolto il problema](../assets/fix.svg) Il passaggio dalla scheda _[!UICONTROL Pick up in Store]_alla scheda_[!UICONTROL Shipping]_ nel flusso di lavoro di estrazione non attiva più un errore JavaScript quando è disponibile solo la consegna di ritiro nello store. <!--- MC-42808-->

![Problema risolto](../assets/fix.svg) La quantità di prodotto vendibile e la quantità di prodotto in magazzino ora sono sincronizzate correttamente. In precedenza, per gli ordini annullati non veniva ricreato il compenso per l&#39;impegno di magazzino. <!--- MC-42485-->

![Problema risolto](../assets/fix.svg) Le prestazioni della convalida sono ottimizzate per impedire l&#39;aggiunta di una nuova origine al prodotto figlio di un prodotto in bundle con tipo di spedizione `Ship Together`. <!--- MC-43039-->

## 1.2.3.

[!DNL Inventory Management] 1.2.3 (versione modulo: `magento/inventory-metapackage = 1.2.3`) è supportato con la versione 2.4.3 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice Magento Open Source.

![È stato risolto il problema](../assets/fix.svg) relativo alla visibilità del prodotto composito sul front-end.

![Problema risolto](../assets/fix.svg) Sono state migliorate le prestazioni di gestione delle pagine del carrello con la quantità minima richiesta.

![Problema risolto](../assets/fix.svg) Diverse correzioni mirate per risolvere problemi relativi alla creazione di origini, articoli esauriti, origini di magazzino, ordinamento delle origini allocate, consegna in-store e comandi di inventario.

![Problema risolto](../assets/fix.svg) [!DNL Commerce] ora supporta i codici postali canadesi a tre cifre per la consegna in-store. I codici a sei cifre non sono supportati a causa delle limitazioni impostate da `geonames.org`.

![Problema risolto](../assets/fix.svg) L&#39;amministratore visualizza ora la quantità corretta di scorte predefinite per i prodotti disabilitati nella griglia **Prodotti** e nella pagina **Modifica prodotto** per le distribuzioni multi-store.

![Problema risolto](../assets/fix.svg) [!DNL Commerce] ora aggiorna la cache dei prodotti di categoria quando un prodotto bundle torna disponibile.

## 1.2.2.

[!DNL Inventory Management] 1.2.2 (versione modulo: `magento/inventory-metapackage = 1.2.2`) è supportato con la versione 2.4.2 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice Magento Open Source.

![È stato risolto il problema](../assets/fix.svg) relativo alla visibilità del prodotto composito sul front-end.

![Problema risolto](../assets/fix.svg) Miglioramento delle prestazioni della pagina del carrello durante l&#39;aggiornamento della quantità in B2B.

![Problema risolto](../assets/fix.svg) Diverse correzioni mirate per risolvere i problemi relativi al prelievo in-store, agli aggiornamenti di massa e alla soglia di inventario.

![Nuovi](../assets/new.svg) **Test funzionali.** Sono stati introdotti nuovi test funzionali e sono state fornite correzioni per i test esistenti per renderli più stabili.

## 1.2.1.

[!DNL Inventory Management] 1.2.1 (versione modulo: `magento/inventory-metapackage = 1.2.1`) è supportato con la versione 2.4.1 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice Magento Open Source.

![È stato risolto un problema](../assets/fix.svg) È stato risolto un problema noto relativo al processo cron `inventory_cleanup_reservations` ed è stato risolto un problema relativo alla funzionalità di prelievo in-store per i prodotti bundle. Questo aggiornamento include anche miglioramenti generali al calcolo delle scorte, al supporto dei prodotti in bundle e alla funzionalità per ordini arretrati.

![Nuovi](../assets/new.svg) **Test funzionali.** Sono stati introdotti nuovi test funzionali per fornire una copertura aggiuntiva per la funzionalità di prelievo in-store.

## 1.2.0.

[!DNL Inventory Management] 1.2.0 (versione modulo: `magento/inventory-metapackage = 1.2.0`) è supportato con la versione 2.4.0 di Adobe Commerce, Adobe Commerce sull&#39;infrastruttura cloud e la base di codice Magento Open Source.

![Problema risolto](../assets/fix.svg) Numerose correzioni per risolvere i problemi relativi all&#39;assegnazione di origine, al supporto delle funzionalità dell&#39;ambiente scalabile e alla compatibilità con PHP 7.4, MySQL 8 e PHPUNIT 9.

![Nuovo](../assets/new.svg) **Metodo di consegna in-store.** È stata aggiunta un&#39;opzione per consentire agli utenti di selezionare un&#39;origine da utilizzare come percorso di prelievo durante l&#39;estrazione. Consulta [Consegna in negozio](../stores-purchase/shipping-in-store-delivery.md) nella _Guida alle vendite e all&#39;acquisto_.

![Nuovo](../assets/new.svg) **Supporto del prodotto per la modalità multi-source.** Inventory supporta tutti i tipi di prodotto con più origini.

![Nuovo](../assets/new.svg) **Reindicizzazione azionaria asincrona.** È stata aggiunta la possibilità di reindicizzare in modo asincrono le scorte e di migliorare le prestazioni di diversi scenari critici.

![Nuove](../assets/new.svg) **Interfacce in blocco.** Sono state introdotte nuove interfacce bulk per il controllo della salabilità: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nuovo](../assets/new.svg) **Maggiore copertura dei test.** Le nuove funzionalità sono coperte da test automatizzati, inclusa la copertura estesa per i problemi rilevati e risolti.

![Problema noto](../assets/bug.svg) **Problema noto.** L&#39;assenza del campo `object_id` nei metadati delle prenotazioni impedisce il corretto funzionamento del processo cron `inventory_cleanup_reservations`. Questo problema è stato introdotto in [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Soluzione alternativa:** eseguire le query MySQL seguenti per eliminare manualmente le prenotazioni:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6.

[!DNL Inventory Management] 1.1.6 (versione modulo: `inventory-composer-metapackage = 1.1.6`) è supportato con la versione 2.3.6 e compatibile con le versioni 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e la base di codice Magento Open Source.

![Correzione di problemi](../assets/fix.svg) Correzioni per la risoluzione di problemi relativi a ordini inevasi, note di credito, griglia dei report sulle scorte ridotte, correzioni connesse allo strumento CLI &quot;Risolvi incoerenze&quot; e miglioramenti generali.

![Nuovo](../assets/new.svg) **Reindicizzazione azionaria asincrona.** È stata aggiunta la possibilità di reindicizzare in modo asincrono le scorte e di migliorare le prestazioni di diversi scenari critici.

## 1.1.5.

[!DNL Inventory Management] 1.1.5 (versione modulo: `inventory-composer-metapackage = 1.1.5`) è supportato con la versione 2.3.5 e compatibile con le versioni 2.3.4, 2.3.3, 2.3.2, 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e la base di codice Magento Open Source.

![Nuovo](../assets/new.svg) **Aggiorna l&#39;inventario dopo aver modificato lo SKU del prodotto.** È stata introdotta una nuova impostazione di configurazione per passare al nuovo comportamento: &quot;Sincronizza con catalogo&quot;.

![Nuovi](../assets/new.svg) **Test funzionali.** Sono stati introdotti nuovi test funzionali per eliminare il gap di copertura dei test. Sono stati risolti diversi problemi per rendere i test più stabili e affidabili).

![Problema noto](../assets/bug.svg) Correzioni per impedire la vendita eccessiva di prodotti, visibilità &quot;esaurita&quot; dei prodotti nella vetrina, numerose correzioni per il supporto di ambienti scalabili e miglioramenti all&#39;interfaccia utente.

## 1.1.4.

[!DNL Inventory Management] 1.1.4 (versione modulo: `inventory-composer-metapackage = 1.1.4`) è supportato con la versione 2.3.4 e compatibile con le versioni 2.3.3, 2.3.2, 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e la base di codice Magento Open Source.

![È stato risolto il problema ](../assets/fix.svg)**Sono state migliorate le prestazioni.** È stata introdotta una logica di bunching per il comando CLI delle prenotazioni di magazzino per ridurre l&#39;utilizzo di memoria ed evitare casi in cui il processo è bloccato senza alcuna risposta.

![Nuovo ](../assets/new.svg)**Maggiore copertura dei test.** ha introdotto molti nuovi test funzionali. Quasi tutti gli scenari di magazzino manuali sono coperti da test automatizzati.

![Problema noto](../assets/bug.svg) Numerose correzioni mirate a risolvere problemi relativi a note di credito, prodotti raggruppati e azioni di massa per scorte e origini.

## 1.1.3.

[!DNL Inventory Management] 1.1.3 (versione modulo: `inventory-composer-metapackage = 1.1.3`) è supportato con la versione 2.3.3 e compatibile con le versioni 2.3.2, 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e la base di codice Magento Open Source.

![È stato risolto il problema ](../assets/fix.svg)**Migliore integrazione con le funzionalità di Adobe Commerce e B2B.** [!DNL Inventory Management] ora funziona correttamente con le seguenti funzionalità per i siti Web che utilizzano origini e scorte di inventario non predefinite:

- Ordina per SKU (Adobe Commerce)
- Ordine rapido (B2B)
- Elenchi richieste di acquisto (B2B)

![Nuovo ](../assets/new.svg)**Prestazioni migliorate.Le prestazioni di esplorazione del catalogo di** Storefront sono migliorate per i siti Web che eseguono le scorte e l&#39;origine di magazzino predefinite.

![Nuovo ](../assets/new.svg)**Maggiore copertura dei test.** La copertura dei test di integrazione e funzionalità automatizzata è aumentata in modo significativo.

## 1.1.2.

[!DNL Inventory Management] 1.1.2 (versione modulo: `inventory-composer-metapackage = 1.1.2`) è supportato con la versione 2.3.2 e compatibile con le versioni 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce sull&#39;infrastruttura cloud e la base di codice Magento Open Source.

![È stato risolto il problema](../assets/fix.svg). Aggiunta di `source_code` alla risposta per l&#39;endpoint REST `/V1/shipments` di GET. <!-- https://github.com/magento/inventory/pull/2142 -->

![Problema risolto](../assets/fix.svg) È stato risolto un problema per cancellare correttamente le prenotazioni e aggiornare le quantità dei prodotti dopo l&#39;emissione di una nota di credito per un ordine non spedito. Quando si seleziona l&#39;opzione per <!-- https://github.com/magento/inventory/pull/2179 -->

![Problema risolto](../assets/fix.svg) problema risolto per salvare correttamente la quantità per i figli di prodotto configurabili quando si immettono quantità durante la creazione del prodotto. <!-- https://github.com/magento/inventory/pull/2158 -->

I nuovi moduli per [!DNL Inventory Management] 1.1.2 Beta includono:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nuovo](../assets/new.svg) **Aggiunto un endpoint per il trasferimento di scorte parziali in blocco** - Gli endpoint per il trasferimento in blocco correnti spostano tutta la quantità assegnata da un&#39;origine a un&#39;origine di destinazione. Il nuovo endpoint `/rest/V1/inventory/bulk-partial-source-transfer` consente ai commercianti di trasferire le scorte parziali dall&#39;origine all&#39;origine come operazione in blocco. Per trasferire una quantità specifica, immettere una richiesta all&#39;endpoint con `sku`, `qty`, `origin_source_code` e `destination_source_code`. I trasferimenti verificano che l&#39;origine sia assegnata a `sku`, che esista una quantità sufficiente per il trasferimento e così via. Consulta [Azioni di massa inventario](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} nella documentazione REST API. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nuovo](../assets/new.svg) **CLI prenotazione aggiunta** - I nuovi comandi consentono di rilevare e risolvere le incoerenze delle prenotazioni. Quando gli ordini vengono inviati e cambiano stato, [!DNL Inventory Management] genera prenotazioni iniziali e aggiornamenti tramite prenotazioni retribuzione. Questi comandi restituiscono un elenco delle incoerenze rilevate in base all’ID ordine, allo SKU e all’ID stock e creano prenotazioni da risolvere. Per ulteriori informazioni, vedere [CLI reference](cli.md). <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nuovo](../assets/new.svg) **Miglioramenti delle prestazioni per le origini e le opzioni SSA** - L&#39;ordinamento e la selezione delle origini durante la spedizione ha causato un peggioramento delle prestazioni per gli stock con un numero elevato di origini. Questa versione offre miglioramenti significativi delle prestazioni per elencare e ordinare le origini disponibili durante la revisione e la selezione delle opzioni SSA nelle spedizioni. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nuovo](../assets/new.svg) **Aggiunto supporto GraphQL per Inventory management** - Questa versione installa un nuovo modulo `magento/module-inventory-graph-ql`. Gli attributi [ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} di GraphQL ora includono gli attributi `only_x_left_in_stock` e `stock_status` per il supporto di [!DNL Inventory Management]. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nuovo](../assets/new.svg) **Interfaccia utente semplificata per le origini assegnate** - La tabella Origini assegnate nelle pagine dei prodotti presenta contenuti semplificati per semplificare gli aggiornamenti e migliorare le prestazioni durante la visualizzazione di più origini. Tutte le origini sono elencate per nome di origine (passaggio del mouse su `source_code`).

![Nuovo](../assets/new.svg) **Esporta Aggregated Stock Service** - Questa versione fornisce un nuovo servizio di aggregazione delle scorte per l&#39;esportazione (mantenendo le prenotazioni nel sistema) per supportare i canali di vendita esterni, come Amazon, eBay e gli annunci Google Shopping.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0.

[!DNL Inventory Management] 1.1.0 (versione modulo: `inventory-composer-metapackage = 1.1.0`) è supportato e compatibile con la versione 2.3.0 di Adobe Commerce, Adobe Commerce sull&#39;infrastruttura cloud e la base di codice Magento Open Source. [!DNL Inventory Management] 1.1.1 viene rilasciato solo come aggiornamento del nome di un pacchetto, supportato per la versione 2.3.1 e compatibile con la versione 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice Magento Open Source.

![È stato risolto il problema](../assets/fix.svg) **È stato aggiunto il supporto di Elasticsearch per le modalità a origine singola e multipla**. È ora possibile configurare e utilizzare Elasticsearch con scorte personalizzate. Per informazioni sull&#39;installazione, vedere [Configurazione del servizio Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"}. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![È stato risolto il problema](../assets/fix.svg). Sono stati risolti i problemi di prestazioni con Stock predefinito per aumentare drasticamente le prestazioni con numerose operazioni. I miglioramenti consentono di migliorare le prestazioni per la modalità a origine singola, il trasferimento delle scorte in Source, le pagine delle categorie di vetrina e i calcoli della quantità di vendita.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Problema risolto](../assets/fix.svg) Problemi risolti relativi allo stato esaurito e al trasferimento in blocco delle scorte in magazzino per prodotti configurabili e raggruppati. La selezione dei prodotti principali e l’esecuzione di azioni in blocco non influiscono sullo stato del prodotto. Se il prodotto principale era In magazzino, questo rimane in magazzino.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nuovo](../assets/new.svg) **Algoritmo di priorità della distanza**. L&#39;algoritmo di priorità della distanza è un nuovo algoritmo di selezione Source predefinito per i consigli di spedizione basati sulla distanza. Questo algoritmo confronta l&#39;ubicazione dell&#39;indirizzo della destinazione di spedizione con le ubicazioni di origine per determinare l&#39;origine più vicina per evadere le spedizioni. La distanza può essere determinata in base alla distanza fisica o al tempo impiegato per spostarsi da un luogo all&#39;altro, utilizzando i dati di localizzazione del codice geografico importati o le indicazioni Google (guida, camminata o bicicletta).

![Nuovo](../assets/new.svg) **Elenco di quantità di origine espanso** — I commercianti con un numero elevato di origini possono passare facilmente il puntatore del mouse e visualizzare tutte le origini per prodotto tramite la griglia prodotti. Ogni prodotto visualizza un minimo di cinque origini e quantità corrispondenti. Passando il puntatore del mouse sulle origini, è possibile scorrere l&#39;intero elenco delle origini e delle quantità correnti.

![Problema noto](../assets/bug.svg) Problema noto con Magento Open Source e Adobe Commerce v2.3.1 - La migrazione asincrona dei dati tra origini ha problemi a causa delle modifiche nelle API asincrone con nomi di argomenti che riflettono i nomi di classi e metodi PHP. Si consiglia di utilizzare operazioni sincrone, impostando **[!UICONTROL Run asynchronously]** su `No`.
