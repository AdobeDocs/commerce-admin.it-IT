---
title: '''[!DNL Inventory Management] note sulla versione'
description: Consulta le note sulla versione per informazioni su tutte [!DNL Inventory Management] versioni.
exl-id: 856b9503-7621-4beb-ac2f-3eb1a240cebc
feature: Inventory, Release Notes
source-git-commit: 7384481d1a4a2a04882d4c99448cca75abc9be31
workflow-type: tm+mt
source-wordcount: '3361'
ht-degree: 0%

---

# [!DNL Inventory Management] note sulla versione

Queste note sulla versione descrivono le versioni di [!DNL Inventory Management] e includono:

![Nuovo](../assets/new.svg) Nuove funzioni
![Problema risolto](../assets/fix.svg) Correzioni e miglioramenti
![Problema noto](../assets/bug.svg) Problemi noti

[!DNL Inventory Management] è un progetto speciale di progettazione della community di Magento Open Source aperto ai collaboratori. Per partecipare e contribuire, consulta la [Progetto GitHub](https://github.com/magento/inventory) archivio e [wiki](https://github.com/magento/inventory/wiki) per iniziare. Per discutere il progetto, partecipa al [Slack](https://magentocommeng.slack.com/?redir=%2Farchives%2FC5FU5E2HY) canale ([iscrizione autonoma](https://opensource.magento.com/slack)).

[Pianificazione della versione](https://experienceleague.adobe.com/docs/commerce-operations/release/planning/schedule.html){target="_blank"} per le versioni supportate e compatibili.

## v1.2.6

[!DNL Inventory Management] 1.2.6 (versione modulo: `magento/inventory-metapackage = 1.2.6`) è supportato con la versione 2.4.6 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce sull’infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) La vetrina ora visualizza i prodotti compositi (configurabili, raggruppati e raggruppati) come in magazzino quando i prodotti secondari che erano stati esauriti vengono restituiti alle scorte. In precedenza, la vetrina indicava che il prodotto composito era esaurito in queste condizioni. <!-- ACP2E-1106-->

![Problema risolto](../assets/fix.svg) Le opzioni di prodotto configurabili vengono ora visualizzate come previsto come esaurite sul vetrina se l’opzione è stata creata con quantità impostata su 0 e **[!UICONTROL Display out-of-stock products]** è abilitato. <!-- ACP2E-1148-->

![Problema risolto](../assets/fix.svg) Le cache delle pagine delle categorie non vengono più invalidate quando cambia la quantità di magazzino e il prodotto è ancora in magazzino. Adobe Commerce ora carica le pagine dalla cache, anziché rigenerarle quando cambia la quantità di prodotto (e nient’altro) nella pagina della categoria di vetrina. <!-- ACP2E-118-->

![Problema risolto](../assets/fix.svg) Il conteggio dei prodotti dell’elenco categorie è ora corretto quando si utilizza Inventory in modalità a origine singola con il **[!UICONTROL Display Out-Of-Stock Products]** impostazione abilitata. Adobe Commerce ora controlla se un prodotto è vendibile al momento del conteggio. <!-- ACP2E-1033-->

![Problema risolto](../assets/fix.svg) Le regole del prezzo del carrello per la consegna in negozio ora funzionano come previsto quando Inventory è abilitato. In precedenza, gli sconti generati dalla regola del prezzo del carrello non venivano applicati in queste condizioni. <!-- ACP2E-1015-->

![Problema risolto](../assets/fix.svg) L’aggiornamento dell’inventario dei prodotti in modalità pianificata non cancella più tutte le cache. In precedenza, l’indicizzatore Inventory cancellava tutte le cache di configurazione. <!-- ACP2E-1003-->

![Problema risolto](../assets/fix.svg) Il valore per **[!UICONTROL Allow Multiple Boxes for Shipping]** L&#39;attributo di un prodotto in Inventario avanzato viene ora salvato come previsto. <!-- ACP2E-992-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora emette una compensazione di prenotazione accurata dopo una nota di credito di rimborso parziale per un ordine effettuato con il ritiro in-store. In precedenza, una prenotazione non corretta veniva salvata in `inventory_reservation` tabella quando un utente amministratore ha creato una nota di credito senza selezionare **[!UICONTROL Return to Stock]** casella di controllo. <!-- ACP2E-979-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più i prodotti configurabili come esauriti nella vetrina quando una delle sue varianti è stata restituita manualmente alle scorte nelle distribuzioni che implementano l’inventario da più origini. <!-- ACP2E-952-->

![Problema risolto](../assets/fix.svg) Posizione colonna sulla griglia prodotti (**[!UICONTROL Catalog]** > **[!UICONTROL Products]**) non ritorna più alla posizione precedente dopo che la pagina viene ricaricata nelle distribuzioni con più origini di inventario configurate. <!-- ACP2E-925-->

![Problema risolto](../assets/fix.svg) La quantità di magazzino è ora corretta dopo l&#39;emissione di una nota di credito per un prodotto virtuale quando **[!UICONTROL Back to stock]** non è selezionata. <!-- ACP2E-908-->

![Problema risolto](../assets/fix.svg) È ora possibile salvare le categorie con l&#39;ordinamento e l&#39;ambito automatici dei prodotti assegnati a scorte non predefinite. In precedenza, Adobe Commerce non salvava la categoria e visualizzava questo errore: `Something went wrong while saving the category`. <!-- ACP2E-859-->

![Problema risolto](../assets/fix.svg) Lo stato delle scorte di prodotto configurabili viene ora aggiornato come previsto quando il prodotto viene creato con tutte le varianti configurabili esaurite. <!-- ACP2E-813-->

![Problema risolto](../assets/fix.svg) Lo strumento Analizzatore incoerenza prenotazioni ora funziona correttamente con gli ordini parzialmente spediti che contengono prodotti configurabili, raggruppati e raggruppati. Vengono ora analizzati i tipi di prodotto compositi. In precedenza, annullamenti e rimborsi venivano salvati solo per i prodotti principali e non per gli articoli di ordini di prodotti secondari di pacchetti configurabili e di spedizione. <!-- ACP2E-924-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non visualizza più un errore quando un utente amministratore tenta di assegnare 200 o più origini magazzino a un magazzino o a un prodotto. <!-- ACP2E-1180-->

![Problema risolto](../assets/fix.svg) Adobe Commerce ora supporta la creazione di una nota di credito per un ordine da cui un prodotto è stato eliminato. In precedenza, i commercianti non potevano creare una nota di credito quando i prodotti erano stati eliminati dall&#39;ordine dopo la creazione di una fattura. L’applicazione ha visualizzato questo errore: `Following products with requested skus were not found: s00001`. t. <!-- ACP2E-1138-->

![Problema risolto](../assets/fix.svg) Gli store vengono ora filtrati in base a ID di store singoli e multipli. Il `event` il codice attributo prodotto è stato aggiunto all’elenco dei codici attributo riservati. In precedenza, il rapporto Stock ridotti generava un’eccezione durante l’installazione del modulo Inventario. <!-- ACP2E-1017-->

![Problema risolto](../assets/fix.svg) I filtri di navigazione su più livelli ora funzionano come previsto e i prodotti esauriti sono ora aggiunti all’elenco dei prodotti della categoria vetrina. Il nuovo `is_out_of_stock` l&#39;attributo sorting utilizza l&#39;Elasticsearch dynamic field mapper per la raccolta di prodotti storefront. <!-- ACP2E-748-->

![Problema risolto](../assets/fix.svg) Lo stato del magazzino del prodotto composito (bundle, raggruppato e configurabile) viene aggiornato come previsto quando lo stato del magazzino del prodotto figlio viene modificato da un REST `POST /rest/V1/inventory/source-items` chiamare. <!-- ACP2E-1209-->

## v1.2.5

[!DNL Inventory Management] 1.2.5 (versione modulo: `magento/inventory-metapackage = 1.2.5`) è supportato con la versione 2.4.5 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce sull’infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) Lo stato predefinito delle scorte di magazzino dei prodotti raggruppati e del bundle ora viene aggiornato come previsto quando un commerciante crea una spedizione dall’amministratore. In precedenza, lo stato di questi prodotti rimaneva invariato dopo la creazione di una spedizione. <!--- ACP2E-418-->

![Problema risolto](../assets/fix.svg) I prodotti configurabili vengono ora ripristinati quando si verifica una delle seguenti condizioni: 1. Il prodotto padre ha almeno un figlio salvato in magazzino. 2. Il prodotto configurabile stesso è stato aggiornato e impostato come **in magazzino** e aveva almeno un figlio in magazzino. <!--- ACP2E-443-->

![Problema risolto](../assets/fix.svg) Le modifiche dell’inventario implementate tramite l’API REST ora vengono riportate come previsto nelle pagine dei dettagli del prodotto. La cache per i prodotti catalogo viene ora pulita dopo il confronto tra lo stato dell’ultimo e quello corrente. In precedenza, l’omissione della funzione di callback causava una valutazione errata delle modifiche di stato delle scorte, che non attivava la necessaria pulizia della cache. Di conseguenza, la vetrina non rifletteva le variazioni di inventario. <!--- ACP2E-161-->

![Problema risolto](../assets/fix.svg) I prodotti assegnati alle scorte predefinite e precedentemente esauriti sono ora visibili sul vetrina dopo l&#39;aggiornamento dell&#39;articolo di origine tramite `/V1/inventory/source-items`. In precedenza, questo endpoint REST API impostava su errato `stock_status`. <!--- ACP2E-562-->

![Problema risolto](../assets/fix.svg) Annullamento dell&#39;assegnazione delle origini di magazzino tramite azione collettiva (**[!UICONTROL Catalog]** > **[!UICONTROL Products]** > **[!UICONTROL Select Products]** > **[!UICONTROL Actions - Unassign Inventory Source]**) ora funziona come previsto quando le origini includono SKU duplicati ad eccezione di uno zero iniziale (ad esempio, `01234` e `1234`). In precedenza, l’applicazione non annullava l’assegnazione delle origini di inventario e generava un errore. <!--- ACP2E-2641-->

![Problema risolto](../assets/fix.svg) Lo stato dello stock del prodotto ora è sempre **in magazzino** sul negozio quando sono abilitati ordini inevasi e il prodotto viene assegnato a un magazzino personalizzato, indipendentemente dalla quantità inevasa. In precedenza, i prodotti esaurivano le scorte anche quando erano abilitati gli ordini inevasi. <!--- ACP2E-664-->

![Problema risolto](../assets/fix.svg) Le scorte di prodotto principali e secondarie configurabili ora vengono aggiornate correttamente dopo l’aggiornamento dell’articolo di origine con `POST /V1/inventory/source-items`. Dopo che il prodotto secondario è stato aggiornato tramite l’API, viene aggiunto un nuovo plug-in Inventory per i controlli di magazzino predefiniti e aggiorna la quantità e lo stato configurabili del prodotto. <!--- ACP2E-442-->

![Problema risolto](../assets/fix.svg) I prodotti raggruppati esauriti non sono più elencati nella pagina delle categorie della vetrina. <!--- ACP2E-2082-->

![Problema risolto](../assets/fix.svg) È stato corretto il nome del pacchetto in `CatalogInventory` `composer.json`. <!--- ACP2E-2914-->

![Problema risolto](../assets/fix.svg) Lo stato dell’ordine arretrato ora viene rappresentato correttamente nell’amministratore dopo aver inserito un ordine con quantità zero in una distribuzione con più origini/scorte. [GitHub-33756](https://github.com/magento/magento2/issues/33756) <!--- ACP2E-713-->

![Problema risolto](../assets/fix.svg) I prodotti del bundle esauriti non vengono più visualizzati nella pagina delle categorie della vetrina quando il prodotto del bundle viene aggiornato dalla sezione delle scorte. <!--- ACP2E-2012-->

![Problema risolto](../assets/fix.svg) Sono stati risolti i problemi di compatibilità con PHP 7.4. <!--- AC-3192-->

![Problema risolto](../assets/fix.svg) Sono state migliorate le prestazioni delle operazioni di salvataggio che includono prodotti bundle contenenti molte opzioni (diverse 100). In precedenza, il salvataggio di questi prodotti in bundle di grandi dimensioni richiedeva diversi minuti e talvolta causava timeout nelle distribuzioni con i servizi di inventario abilitati. [GitHub-34732](https://github.com/magento/magento2/issues/34732) <!--- AC-1901-->

![Problema risolto](../assets/fix.svg) Strumento di azione collettiva per prodotti (**[!UICONTROL Select Products]** > **[!UICONTROL Actions]** > **[!UICONTROL Assign Inventory Source]**) funziona ora come previsto quando si assegna l’origine dell’inventario a più prodotti quando gli SKU vengono duplicati, ad eccezione di una `0` (ad esempio, `01234` e `1234`). In precedenza, a un solo prodotto veniva assegnata un’origine di inventario. [GitHub-35171](https://github.com/magento/magento2/issues/35171) <!--- AC-2584-->

![Problema risolto](../assets/fix.svg) Il `ProductInterface.only_x_left_in_stock` ora restituisce 0 se inventory è 0. In precedenza, restituiva null. [GitHub-29932](https://github.com/magento/magento2/issues/29932) <!--- AC-1806-->

![Problema risolto](../assets/fix.svg) È ora possibile modificare le scorte predefinite dall&#39;amministratore **[!UICONTROL Stores]** > **[!UICONTROL Inventory]** > **[!UICONTROL Stocks]**. In precedenza, nella console veniva visualizzato un errore JavaScript quando si tentava di aggiungere o rimuovere sorgenti dalle scorte predefinite, anche se era possibile assegnare siti web alle scorte predefinite. <!--- ACP2E-545-->

![Problema risolto](../assets/fix.svg) <!--- ACP2E-274--> Il conteggio dei prodotti dell’elenco categorie ora è corretto quando si utilizza la modalità a origine singola di inventario con il **[!UICONTROL Display Out-Of-Stock Products]** impostazione abilitata. Un nuovo plug-in ora utilizza `AreProductsSalableInterface` e `StockConfigurationInterface` per determinare il numero totale di prodotti. In precedenza, l&#39;elenco dei prodotti della categoria restituiva una quantità di prodotto errata.

![Problema risolto](../assets/fix.svg) <!--- ACP2E-322--> I prodotti configurabili vengono ora spostati all’ultima posizione nell’elenco dei prodotti dopo l’aggiornamento delle scorte quando **[!UICONTROL Move out of stock to the bottom]** è attivata. Viene implementata una nuova query di database personalizzata per ignorare l’ordinamento dell’indice Elasticsearch, che ignora quello abilitato dall’amministratore. In precedenza, i prodotti configurabili e i relativi prodotti secondari non venivano spostati in fondo all’elenco quando questa impostazione era abilitata.

## v1.2.4

Inventory management 1.2.4 (versione modulo: `magento/inventory-metapackage = 1.2.4`) è supportato con la versione 2.4.4 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce sull’infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) Commerce ora mostra un valore preciso per la quantità vendibile di tutti i prodotti nella vista Elenco prodotti amministratore. In precedenza veniva visualizzato un valore vuoto per la quantità di prodotti in magazzino con SKU contenenti caratteri speciali. <!--- MC-41936-->

![Problema risolto](../assets/fix.svg) Sono state migliorate le prestazioni per le azioni di carrello e pagamento, ad esempio l’aggiunta di prodotti al carrello in implementazioni con molte (circa 10.000) sorgenti di inventario. <!--- MC-42570-->

![Problema risolto](../assets/fix.svg) Il `bin/magento inventory:reservation:list-inconsistencies` Il comando ora gestisce correttamente gli ordini con spedizioni parziali anche se le prenotazioni non vengono effettuate dal database e la cache è stata cancellata. In precedenza, quando questo comando veniva eseguito con una cache pre-cancellata, Commerce mostrava il seguente errore: `Area code is not set`. <!--- MC-42142-->

![Problema risolto](../assets/fix.svg) L’indicizzazione incrementale di prodotti secondari di prodotti raggruppati non causa più l’indicizzazione errata di altri prodotti raggruppati quando vengono condivisi gli elementi secondari. <!--- MC-41963-->

![Problema risolto](../assets/fix.svg) Nella pagina delle categorie della vetrina ora viene visualizzato il numero corretto di prodotti dopo la rimozione di un prodotto da una categoria tramite API. In precedenza, il conteggio dei prodotti della pagina delle categorie non era corretto fino alla reindicizzazione. <!--- MC-42287-->

![Problema risolto](../assets/fix.svg) I prodotti configurabili possono ora essere rimessi in magazzino durante la creazione di una nota di credito quando **[!UICONTROL Manage Stock]** è disabilitata. In precedenza, Commerce non visualizzava **Torna a magazzino** casella di controllo nella pagina di creazione della nota di credito quando questa opzione è stata disabilitata. <!--- MC-42002-->

![Problema risolto](../assets/fix.svg) È stata migliorata la gestione delle scorte di magazzino che superano i 10.000 articoli. In precedenza, a volte i problemi di prestazioni impedivano ai commercianti di modificare le risorse in Admin prima di avviare il sito web. <!--- MC-42643-->

![Problema risolto](../assets/fix.svg) Il **[!UICONTROL User Roles]** In Admin viene aggiornata per fornire agli amministratori autorizzazioni limitate per l’accesso alla configurazione dei metodi di consegna. Il _Metodi di spedizione_ la sezione è stata rinominata in _[!UICONTROL Delivery methods]_, e_[!UICONTROL In-Store Pickup]_ viene spostato sotto _[!UICONTROL Delivery methods]_sezione. [GitHub-30053](https://github.com/magento/magento2/issues/30053)  <!--- MC-41545-->

![Problema risolto](../assets/fix.svg) Adobe Commerce non crea più una prenotazione di prodotto duplicata dopo che una nota di credito è stata aggiornata dall’API. <!--- MC-41757-->

![Problema risolto](../assets/fix.svg) Passaggio dalla _[!UICONTROL Pick up in Store]_scheda a_[!UICONTROL Shipping]_ Questa scheda nel flusso di lavoro di pagamento non attiva più un errore JavaScript quando è disponibile solo la consegna di ritiro in-store. <!--- MC-42808-->

![Problema risolto](../assets/fix.svg) La quantità di prodotto vendibile e la quantità di prodotto in magazzino ora vengono sincronizzate correttamente. In precedenza, per gli ordini annullati non veniva ricreato il compenso per l&#39;impegno di magazzino. <!--- MC-42485-->

![Problema risolto](../assets/fix.svg) Le prestazioni della convalida sono ottimizzate per impedire l&#39;aggiunta di una nuova origine al prodotto figlio di un prodotto in bundle con il tipo di spedizione `Ship Together`. <!--- MC-43039-->

## 1.2.3

[!DNL Inventory Management] 1.2.3 (versione del modulo: `magento/inventory-metapackage = 1.2.3`) è supportato con la versione 2.4.3 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce sull’infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) Sono stati risolti diversi problemi relativi alla visibilità del prodotto composito sul front-end.

![Problema risolto](../assets/fix.svg) Sono state migliorate le prestazioni di gestione delle pagine del carrello con la quantità minima richiesta.

![Problema risolto](../assets/fix.svg) Diverse correzioni mirate a risolvere i problemi relativi alla creazione dell&#39;origine, agli articoli esauriti, all&#39;approvvigionamento delle scorte, all&#39;ordinamento delle origini allocate, alla consegna in-store e ai comandi di inventario.

![Problema risolto](../assets/fix.svg) [!DNL Commerce] ora supporta codici postali canadesi a tre cifre per la consegna in-store. I codici a sei cifre non sono supportati a causa delle limitazioni impostate da `geonames.org`.

![Problema risolto](../assets/fix.svg) L’amministratore visualizza ora la quantità corretta di scorte predefinite per i prodotti disabilitati sul **Prodotti** griglia e **Modifica prodotto** per le distribuzioni in più store.

![Problema risolto](../assets/fix.svg) [!DNL Commerce] ora aggiorna la cache dei prodotti di categoria quando un prodotto bundle torna disponibile.

## 1.2.2

[!DNL Inventory Management] 1.2.2 (versione del modulo: `magento/inventory-metapackage = 1.2.2`) è supportato con la versione 2.4.2 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce sull’infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) Sono stati risolti diversi problemi relativi alla visibilità del prodotto composito sul front-end.

![Problema risolto](../assets/fix.svg) Sono state migliorate le prestazioni della pagina del carrello durante l’aggiornamento della quantità in B2B.

![Problema risolto](../assets/fix.svg) Diverse correzioni mirate a risolvere i problemi relativi al prelievo in negozio, agli aggiornamenti di massa e alla soglia di inventario.

![Nuovo](../assets/new.svg) **Test funzionali.** Sono stati introdotti nuovi test funzionali e sono state fornite correzioni per i test esistenti al fine di renderli più stabili.

## 1.2.1

[!DNL Inventory Management] 1.2.1 (versione del modulo: `magento/inventory-metapackage = 1.2.1`) è supportato con la versione 2.4.1 e compatibile con la versione 2.4.0 di Adobe Commerce, Adobe Commerce sull’infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) È stato risolto un problema noto relativo al `inventory_cleanup_reservations` cron e ha risolto un problema relativo alla funzionalità di ritiro in-store per i prodotti bundle. Questo aggiornamento include anche miglioramenti generali al calcolo delle scorte, al supporto dei prodotti in bundle e alla funzionalità per ordini arretrati.

![Nuovo](../assets/new.svg) **Test funzionali.** Sono stati introdotti nuovi test funzionali per fornire una copertura aggiuntiva alla funzionalità di ritiro in-store.

## 1.2.0

[!DNL Inventory Management] 1.2.0 (versione modulo: `magento/inventory-metapackage = 1.2.0`) è supportato con la versione 2.4.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) Numerose correzioni per risolvere i problemi relativi all&#39;assegnazione della sorgente, al supporto delle funzioni dell&#39;ambiente scalabile e alla compatibilità con PHP 7.4, MySQL 8 e PHPUNIT 9.

![Nuovo](../assets/new.svg) **Metodo di consegna in-store.** È stata aggiunta un’opzione che consente agli utenti di selezionare un’origine da utilizzare come posizione di prelievo durante il pagamento. Consulta [Consegna in-store](../stores-purchase/shipping-in-store-delivery.md) nel _Guida all’esperienza di vendita e acquisto_.

![Nuovo](../assets/new.svg) **Supporto di prodotti in bundle per la modalità multi-source.** Inventory supporta tutti i tipi di prodotto con più origini.

![Nuovo](../assets/new.svg) **Reindicizzazione azionaria asincrona.** È stata aggiunta la possibilità di reindicizzare in modo asincrono le scorte e di migliorare le prestazioni di diversi scenari critici.

![Nuovo](../assets/new.svg) **Interfacce di massa.** Sono state introdotte nuove interfacce di massa per il controllo della salabilità: `\Magento\InventorySalesApi\Api\AreProductsSalableInterface`, `\Magento\InventorySalesApi\Api\AreProductsSalableForRequestedQtyInterface`.

![Nuovo](../assets/new.svg) **Maggiore copertura dei test.** Le nuove funzionalità vengono coperte con test automatizzati, inclusa la copertura estesa per i problemi rilevati e risolti.

![Problema noto](../assets/bug.svg) **Problema noto.** L&#39;assenza della `object_id` nei metadati delle prenotazioni impedisce la `inventory_cleanup_reservations` funzionamento corretto del processo cron. Questo problema è stato introdotto in [magento/inventory#3046](https://github.com/magento/inventory/pull/3046).

**Soluzione alternativa:** Eseguire le query MySQL seguenti per eliminare manualmente le prenotazioni:

```sql
SELECT GROUP_CONCAT(reservation_id) FROM inventory_reservation GROUP BY stock_id, sku HAVING SUM(quantity) = 0;
DELETE FROM inventory_reservation where reservation_id IN (result_of_the_first_query);
```

## 1.1.6

[!DNL Inventory Management] 1.1.6 (versione modulo: `inventory-composer-metapackage = 1.1.6`) è supportato con la versione 2.3.6 e compatibile con le versioni 2.3.5, 2.3.4, 2.3.3, 2.3.2, 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) Correzioni per la risoluzione di problemi relativi a ordini inevasi, note di credito, griglia di rapporti sulle scorte ridotte, correzioni connesse allo strumento CLI &quot;Risolvi incoerenze&quot; e miglioramenti generali.

![Nuovo](../assets/new.svg) **Reindicizzazione azionaria asincrona.** È stata aggiunta la possibilità di reindicizzare in modo asincrono le scorte e di migliorare le prestazioni di diversi scenari critici.

## 1.1.5

[!DNL Inventory Management] 1.1.5 (versione modulo: `inventory-composer-metapackage = 1.1.5`) è supportato con la versione 2.3.5 e compatibile con le versioni 2.3.4, 2.3.3, 2.3.2, 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice del Magento Open Source.

![Nuovo](../assets/new.svg) **Aggiorna l’inventario dopo aver modificato lo SKU del prodotto.** È stata introdotta una nuova impostazione di configurazione per passare al nuovo comportamento: &quot;Sincronizza con catalogo&quot;.

![Nuovo](../assets/new.svg) **Test funzionali.** Sono stati introdotti nuovi test funzionali per eliminare il gap di copertura dei test. Sono stati risolti diversi problemi per rendere i test più stabili e affidabili).

![Problema noto](../assets/bug.svg) Correzioni per evitare la vendita eccessiva dei prodotti, visibilità dei prodotti &quot;esauriti&quot; sulla vetrina, numerose correzioni per il supporto di ambienti scalabili e miglioramenti all’interfaccia utente.

## 1.1.4

[!DNL Inventory Management] 1.1.4 (versione modulo: `inventory-composer-metapackage = 1.1.4`) è supportato con la versione 2.3.4 e compatibile con le versioni 2.3.3, 2.3.2, 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice del Magento Open Source.

![Problema risolto ](../assets/fix.svg)**Prestazioni migliorate.** È stata introdotta una logica di bunching per il comando CLI delle prenotazioni di inventario per ridurre l’utilizzo della memoria ed evitare casi in cui il processo si blocca senza alcuna risposta.

![Nuovo ](../assets/new.svg)**Maggiore copertura dei test.** Sono stati introdotti molti nuovi test funzionali. Quasi tutti gli scenari di magazzino manuali sono coperti da test automatizzati.

![Problema noto](../assets/bug.svg) Numerose correzioni mirate a risolvere i problemi relativi alle note di credito, ai prodotti raggruppati e alle azioni di massa relative a origini e scorte.

## 1.1.3

[!DNL Inventory Management] 1.1.3 (versione modulo: `inventory-composer-metapackage = 1.1.3`) è supportato con la versione 2.3.3 e compatibile con le versioni 2.3.2, 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce on cloud infrastructure e con il codice di Magento Open Source.

![Problema risolto ](../assets/fix.svg)**Migliore integrazione con le funzioni di Adobe Commerce e B2B.** [!DNL Inventory Management] ora funziona correttamente con le seguenti funzioni per i siti web che utilizzano sorgenti di inventario e scorte non predefinite:

- Ordina per SKU (Adobe Commerce)
- Ordine rapido (B2B)
- Elenchi richieste di acquisto (B2B)

![Nuovo ](../assets/new.svg)**Prestazioni migliorate.** Le prestazioni di esplorazione del catalogo Storefront sono migliorate per i siti Web che eseguono le scorte di magazzino e l&#39;origine predefinite.

![Nuovo ](../assets/new.svg)**Maggiore copertura dei test.** La copertura automatizzata dei test funzionali e di integrazione è aumentata in modo significativo.

## 1.1.2

[!DNL Inventory Management] 1.1.2 (versione del modulo: `inventory-composer-metapackage = 1.1.2`) è supportato con la versione 2.3.2 e compatibile con le versioni 2.3.1 e 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) Aggiunto `source_code` alla risposta per il GET `/V1/shipments` Endpoint REST. <!-- https://github.com/magento/inventory/pull/2142 -->

![Problema risolto](../assets/fix.svg) È stato risolto un problema per cancellare correttamente le prenotazioni e aggiornare le quantità dei prodotti dopo l&#39;emissione di una nota di credito per un ordine non spedito. Quando selezioni l’opzione per <!-- https://github.com/magento/inventory/pull/2179 -->

![Problema risolto](../assets/fix.svg) È stato risolto un problema che impediva il corretto salvataggio della quantità per gli elementi figlio del prodotto configurabili durante l’inserimento delle quantità durante la creazione del prodotto. <!-- https://github.com/magento/inventory/pull/2158 -->

Nuovi moduli per [!DNL Inventory Management] 1.1.2 La beta comprende:

```php
        'Magento_InventoryGraphQl' => 1,
        'Magento_InventoryReservations' => 1,
        'Magento_InventoryReservationsApi' => 1,
        'Magento_InventoryReservationCli' => 1,
        'Magento_InventoryExportStock' => 0,
        'Magento_InventoryExportStockApi' => 0,
```

![Nuovo](../assets/new.svg) **È stato aggiunto un endpoint per trasferimento parziale di scorte** - Gli endpoint di trasferimento in blocco correnti spostano tutta la quantità assegnata da un&#39;origine a un&#39;origine di destinazione. Il nuovo `/rest/V1/inventory/bulk-partial-source-transfer` l’endpoint consente ai commercianti di trasferire le scorte parziali dall’origine all’origine come operazione in blocco. Per trasferire una quantità specifica, inserire una richiesta al punto finale con `sku`, `qty`, `origin_source_code`, e `destination_source_code`. I trasferimenti verificano che l&#39;origine sia assegnata al `sku`, quantità sufficiente da trasferire e così via. Consulta [Azioni di massa magazzino](https://developer.adobe.com/commerce/webapi/rest/inventory/bulk-inventory/){target="_blank"} nella documentazione REST API. <!-- https://github.com/magento/inventory/pull/2117 -->

![Nuovo](../assets/new.svg) **CLI prenotazione aggiunta** : i nuovi comandi consentono di rilevare e risolvere le incoerenze nelle prenotazioni. Quando gli ordini vengono sottomessi e lo stato cambia, [!DNL Inventory Management] genera prenotazioni iniziali e aggiornamenti tramite prenotazioni retribuzione. Questi comandi restituiscono un elenco delle incoerenze rilevate in base all’ID ordine, allo SKU e all’ID stock e creano prenotazioni da risolvere. Consulta la [Riferimento CLI](cli.md) per ulteriori informazioni. <!-- https://github.com/magento/inventory/pull/2199 https://github.com/magento/inventory/pull/2184 https://github.com/magento/inventory/pull/2171 https://github.com/magento/inventory/pull/2148  -->

![Nuovo](../assets/new.svg) **Miglioramenti delle prestazioni per origini e opzioni SSA** - La selezione e la selezione delle fonti durante la spedizione hanno causato un deterioramento delle prestazioni per le scorte con un elevato numero di fonti. Questa versione offre miglioramenti significativi delle prestazioni per elencare e ordinare le origini disponibili durante la revisione e la selezione delle opzioni SSA nelle spedizioni. <!-- https://github.com/magento/inventory/pull/2056 https://github.com/magento/inventory/pull/2090 -->

![Nuovo](../assets/new.svg) **Aggiunto supporto GraphQL per Inventory management** - Questa versione installa una nuova `magento/module-inventory-graph-ql` modulo. GraphQL [Attributi ProductInterface](https://developer.adobe.com/commerce/webapi/graphql/schema/products/interfaces/attributes/){target="_blank"} ora include `only_x_left_in_stock` e `stock_status` attributi per [!DNL Inventory Management] supporto. <!-- https://github.com/magento/inventory/pull/2124 -->

![Nuovo](../assets/new.svg) **Interfaccia utente semplificata per le origini assegnate** : la tabella Origini assegnate nelle pagine dei prodotti presenta contenuti semplificati per semplificare gli aggiornamenti e migliorare le prestazioni durante la visualizzazione di più origini. Elenco di tutte le origini per nome origine (passa il puntatore del mouse su per `source_code`).

![Nuovo](../assets/new.svg) **Esporta servizio magazzino aggregato** - Questa versione offre un nuovo servizio di gestione delle scorte aggregate per l&#39;esportazione (mantenimento delle prenotazioni nel sistema) per supportare Sales Channel esterni, come Amazon, eBay e annunci di acquisto Google.  <!-- https://github.com/magento/inventory/pull/2067 -->

## 1.1.0

[!DNL Inventory Management] 1.1.0 (versione modulo: `inventory-composer-metapackage = 1.1.0`) è supportato e compatibile con la versione 2.3.0 di Adobe Commerce, Adobe Commerce su infrastruttura cloud e con la base di codice del Magento Open Source. [!DNL Inventory Management] La versione 1.1.1 viene rilasciata solo come aggiornamento del nome di un pacchetto, supportato per la versione 2.3.1 e compatibile con la versione 2.3.0 di Adobe Commerce, Adobe Commerce sull’infrastruttura cloud e la base di codice del Magento Open Source.

![Problema risolto](../assets/fix.svg) **È stato aggiunto il supporto di Elasticsearch per le modalità a sorgente singola e multipla** — È ora possibile configurare e utilizzare Elasticsearch con scorte personalizzate. Consulta [Configura servizio Elasticsearch](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/service/elasticsearch.html){target="_blank"} per informazioni sull&#39;installazione. <!-- PR https://github.com/magento/inventory/pull/1943 -->

![Problema risolto](../assets/fix.svg) Sono stati risolti dei problemi di prestazioni con Stock predefiniti per aumentare drasticamente le prestazioni con numerose operazioni. I miglioramenti consentono di migliorare le prestazioni per la modalità a origine singola, le pagine Trasferisci magazzino all&#39;origine, Categoria punto vendita e i calcoli della quantità di vendita.

<!-- All Performance Track issues resolved https://github.com/magento/inventory/issues?q=is%3Aopen+is%3Aissue+label%3APerformance -->

![Problema risolto](../assets/fix.svg) Sono stati risolti i problemi relativi allo stato Non disponibile e al trasferimento in blocco delle scorte alle scorte per i prodotti configurabili e raggruppati. La selezione dei prodotti principali e l’esecuzione di azioni in blocco non influiscono sullo stato del prodotto. Se il prodotto principale era In magazzino, questo rimane in magazzino.

<!-- PR https://github.com/magento/inventory/pull/1972 -->

![Nuovo](../assets/new.svg) **Algoritmo di priorità della distanza** — L&#39;algoritmo Distance Priority è un nuovo algoritmo di selezione della sorgente pronto all&#39;uso per i consigli di spedizione basati sulla distanza. Questo algoritmo confronta l&#39;ubicazione dell&#39;indirizzo della destinazione di spedizione con le ubicazioni di origine per determinare l&#39;origine più vicina per evadere le spedizioni. La distanza può essere determinata in base alla distanza fisica o al tempo impiegato per spostarsi da un luogo all&#39;altro, utilizzando i dati di localizzazione del codice geografico importati o le indicazioni Google (guida, camminata o bicicletta).

![Nuovo](../assets/new.svg) **Elenco quantità di origine espansa** — I commercianti con un elevato numero di sorgenti possono passare facilmente il cursore e visualizzare tutte le sorgenti per prodotto attraverso la griglia di prodotto. Ogni prodotto visualizza un minimo di cinque origini e quantità corrispondenti. Passando il puntatore del mouse sulle origini, è possibile scorrere l&#39;intero elenco delle origini e delle quantità correnti.

![Problema noto](../assets/bug.svg) Problema noto con Magento Open Source e Adobe Commerce v2.3.1 - La migrazione asincrona dei dati tra le origini riscontra problemi dovuti alle modifiche nelle API asincrone con nomi di argomenti che riflettono i nomi di classi e metodi PHP. Utilizzo di operazioni sincrone, impostazione **[!UICONTROL Run asynchronously]** a `No`, è consigliato.
