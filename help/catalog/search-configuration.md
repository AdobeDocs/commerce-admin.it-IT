---
title: Configura ricerca catalogo
description: Scopri come configurare la ricerca nel catalogo per il tuo store.
exl-id: b4f22bce-39e2-4269-99a4-eb2d647df939
feature: Catalog Management, Search
source-git-commit: 06673ccb7eb471d3ddea97218ad525dd2cdcf380
workflow-type: tm+mt
source-wordcount: '729'
ht-degree: 0%

---

# Configura ricerca catalogo

Sono disponibili due varianti della configurazione di Ricerca nel catalogo. Il primo metodo descrive le impostazioni disponibili quando è installato [Live Search](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/overview.html). Il secondo metodo descrive le impostazioni di configurazione per Adobe Commerce nativo con [Elasticsearch][1]{:target=&quot;_blank&quot;}.

## Metodo 1: Adobe Commerce con [!DNL Live Search]

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Catalog Search]**.

   ![Ricerca nel catalogo per Live Search](../configuration-reference/catalog/assets/catalog-search-live-search.png){width="600" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni, vedi [Adobe Commerce con Live Search](../configuration-reference/catalog/catalog.md#adobe-commerce-with-live-search) nel _Riferimento configurazione_.

1. Per limitare la lunghezza e il numero di parole del testo della query di ricerca, impostare un valore per **[!UICONTROL Minimal Query Length]** e **[!UICONTROL Maximum Query Length]**.

1. Per limitare la quantità di risultati di ricerca popolari da memorizzare nella cache per ottenere risposte più veloci, impostare una quantità per **[!UICONTROL Number of top search results to cache]**.

   Il valore predefinito è `100`. Se si immette un valore di `0`, vengono memorizzati nella cache tutti i termini e i risultati di ricerca una seconda volta.

1. Per modificare il numero massimo di righe disponibili per i risultati restituiti nello [storefront pop sopra](https://experienceleague.adobe.com/docs/commerce-merchant-services/live-search/live-search-storefront/quick-tour.html), immettere un valore **[!UICONTROL Autocomplete Limit]** diverso.

   La limitazione del numero di righe migliora le prestazioni delle ricerche e riduce le dimensioni dell’elenco restituito. Il valore predefinito è `8` righe.

## Metodo 2: Commerce con Elasticsearch

>[!IMPORTANT]
>
>A causa dell’annuncio di fine del supporto di [!DNL Elasticsearch 7] per agosto 2023, si consiglia a tutti i clienti di Adobe Commerce di migrare al motore di ricerca OpenSearch 2.x. Per informazioni sulla migrazione del motore di ricerca durante l&#39;aggiornamento del prodotto, vedere [Migrazione a OpenSearch](https://experienceleague.adobe.com/docs/commerce-operations/upgrade-guide/prepare/opensearch-migration.html) nella _Guida all&#39;aggiornamento_.

### Passaggio 1: configurare le opzioni di ricerca generali

>[!NOTE]
>
>Ad Elasticsearch, non è disponibile il supporto predefinito per la ricerca in base al suffisso. Ad esempio, la ricerca per SKU potrebbe non restituire il risultato previsto se la parola chiave contiene solo la parte finale dello SKU.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Catalog Search]**.

   ![Impostazioni Elasticsearch](../configuration-reference/catalog/assets/catalog-search-elasticsearch.png){width="600" zoomable="yes"}

   Per ulteriori informazioni su queste opzioni, vedere [Adobe Commerce con Elasticsearch](../configuration-reference/catalog/catalog.md#adobe-commerce-with-elasticsearch) nel _Riferimento configurazione_.

1. Per limitare la lunghezza e il numero di parole del testo della query di ricerca, impostare un valore per **[!UICONTROL Minimal Query Length]** e **[!UICONTROL Maximum Query Length]**.

   >[!IMPORTANT]
   >
   >Il valore impostato per questo intervallo minimo e massimo deve essere compatibile con l’intervallo corrispondente impostato nella configurazione di Elasticsearch del motore di ricerca. Se ad esempio si impostano questi valori su `2` e `300` in Commerce, aggiornare i valori corrispondenti nel motore di ricerca.

1. Per limitare la quantità di risultati di ricerca popolari da memorizzare nella cache per ottenere risposte più veloci, impostare una quantità per **[!UICONTROL Number of top search results to cache]**.

   Il valore predefinito è `100`. Se si immette un valore di `0`, vengono memorizzati nella cache tutti i termini e i risultati di ricerca una seconda volta.

1. Se si desidera abilitare o disabilitare l&#39;indicizzatore Product EAV, impostare **[!UICONTROL Enable EAV Indexer]**.

   Questa funzione migliora la velocità di indicizzazione e impedisce all’indicizzatore di essere utilizzato da estensioni di terze parti.

1. Per limitare il numero massimo di risultati di ricerca da visualizzare per il completamento automatico della ricerca, impostare un valore per **[!UICONTROL Autocomplete Limit]**.

   Limitando questa quantità si aumentano le prestazioni delle ricerche e si riduce la dimensione dell’elenco visualizzato. Il valore predefinito è `8`.

### Passaggio 2: configurare la connessione Elasticsearch

>[!IMPORTANT]
>
>I campi **[!UICONTROL Search Engine]**, **[!UICONTROL Elasticsearch Server Hostname]**, **[!UICONTROL Elasticsearch Server Port]**, **[!UICONTROL Elasticsearch Index Prefix]**, **[!UICONTROL Enable Elasticsearch HTTP Auth]** e **[!UICONTROL Elasticsearch Server Timeout]** sono stati configurati al momento dell&#39;installazione o dell&#39;aggiornamento di Commerce. Questi valori devono essere modificati solo quando si aggiorna o si modifica l’Elasticsearch.

1. Per **[!UICONTROL Search Engine]**, accettare il valore predefinito `Elasticsearch 7`.

   L&#39;Elasticsearch 7.6.x è richiesto per tutte le installazioni di Commerce.

1. Per **[!UICONTROL Elasticsearch Server Hostname]**, accettare il valore predefinito configurato al momento dell&#39;installazione di Commerce.

   In questo esempio, il valore predefinito è `elasticsearch.internal`.

1. Per **[!UICONTROL Elasticsearch Server Port]**, accettare il valore predefinito configurato al momento dell&#39;installazione di Commerce.

   In questo esempio, il valore predefinito è `9200`.

1. Per **[!UICONTROL Elasticsearch Index Prefix]**, immettere un prefisso per identificare l&#39;indice Elasticsearch.

   Il valore predefinito è `magento2`.

1. Per utilizzare l&#39;autenticazione HTTP per richiedere un nome utente e una password per accedere a Elasticsearch Server, impostare **[!UICONTROL Enable Elasticsearch HTTP Auth]** su `Yes`.

1. Per **[!UICONTROL Elasticsearch Server Timeout]**, immettere il numero di secondi prima del timeout del sistema.

   Il valore predefinito è `15`.

1. Per verificare la configurazione, scegliere **[!UICONTROL Test Connection]**.

### Passaggio 3: configurare suggerimenti e consigli

>[!NOTE]
>
>I suggerimenti e i consigli di ricerca possono influire sulle prestazioni del server.

1. Per offrire consigli, impostare **[!UICONTROL Enable Search Recommendations]** su `Yes` ed effettuare le seguenti operazioni:

   - Per **[!UICONTROL Search Recommendation Count]**, immettere il numero di consigli da offrire.

   - Per visualizzare il numero di risultati trovati per ogni consiglio, impostare **[!UICONTROL Show Results Count for Each Recommendation]** su `Yes`.

1. Impostare **[!UICONTROL Enable Search Suggestions]** su `Yes` ed effettuare le seguenti operazioni:

   - Per **[!UICONTROL Search Suggestions Count]**, immettere il numero di suggerimenti di ricerca da offrire.

   - Per visualizzare il numero di risultati trovati per ogni suggerimento, impostare **[!UICONTROL Show Results for Each Suggestion]** su `Yes`.

### Passaggio 4: configurare i termini minimi da abbinare

Per controllare il numero minimo di termini della query che i risultati della ricerca devono corrispondere per la restituzione, specificare un valore per **[!UICONTROL Minimum Terms to Match]**. Specificando questo valore si garantisce la rilevanza dei risultati ottimali per gli acquirenti. Per un elenco dei valori accettati, vedi [parametro minimum_should_match](https://www.elastic.co/guide/en/elasticsearch/reference/current/query-dsl-minimum-should-match.html) nella documentazione di Elasticsearch.

Al termine, fare clic su **[!UICONTROL Save Config]**.

[1]: https://experienceleague.adobe.com/docs/commerce-operations/installation-guide/prerequisites/search-engine/overview.html
[2]: https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/search/overview-search.html
