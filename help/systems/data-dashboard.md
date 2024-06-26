---
title: Dashboard di gestione dati
description: Scopri come accedere alle informazioni sui flussi di dati per [!DNL Catalog Service], [!DNL Live Search], e [!DNL Product Recommendation]s.
feature: Products, Customers, Data Import/Export
exl-id: 63c261c1-1a52-46f7-93f8-81055edf1f7b
source-git-commit: 4495a27b57c04c6f9c37b2c5237b5f2233cc8532
workflow-type: tm+mt
source-wordcount: '682'
ht-degree: 0%

---

# Dashboard di gestione dati

Data Management Dashboard offre una panoramica dello stato di sincronizzazione dei dati di prodotto trasferiti dal database di Commerce ai servizi SaaS di Commerce. Gli utenti possono monitorare comodamente gli stati di sincronizzazione dei prodotti e avviare la risincronizzazione dei dati da un dashboard unificato. Questa funzione fornisce informazioni utili sulla disponibilità dei dati dei prodotti per la vetrina, garantendone la rapida visualizzazione agli acquirenti.

## Pubblico

Il dashboard di gestione dati è disponibile senza costi aggiuntivi per tutti i commercianti Commerce che utilizzano [[!DNL Product Recommendations v6.0.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/product-recommendations/guide-overview), [[!DNL Live Search v4.1.0]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/guide-overview), o [[!DNL Catalog Service v1.17]](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/catalog-service/guide-overview) con una licenza attiva.

Il dashboard di gestione dati si trova in *Sistema* > Trasferimento dati > *Dashboard di gestione dati*.

![Dashboard di gestione dati](assets/data-management-dashboard.png)

Il dashboard contiene i campi seguenti:

| Campo | Descrizione |
|--- |--- |
| Ambito | Sito Web specifico per i dati sincronizzati. |
| [!DNL Product Recommendations] | Visualizza lo stato di sincronizzazione, il numero di prodotti sincronizzati e una tabella del [visualizzabile](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) prodotti sincronizzati per [!DNL Product Recommendations]. |
| [!DNL Live Search] | Visualizza lo stato di sincronizzazione, il numero di prodotti sincronizzati e una tabella del [visualizzabile](https://experienceleague.adobe.com/en/docs/commerce-admin/config/catalog/inventory#stock-options) prodotti sincronizzati per [!DNL Live Search]. |
| [!DNL Catalog Service] | Visualizza lo stato di sincronizzazione, il numero di prodotti sincronizzati e una tabella dei prodotti sincronizzati per [!DNL Catalog Service]. |
| Impostazioni | Apre una finestra di dialogo in cui è possibile [risincronizzare manualmente i dati del catalogo](#resync-catalog-data). |
| Stato sincronizzazione | Visualizza il numero di prodotti trasferiti dal database di Commerce a uno qualsiasi dei servizi SaaS nelle ultime tre ore. Se apporti aggiornamenti non frequenti al catalogo, questo valore è spesso zero. Se è in corso una sincronizzazione, fare clic su **[!UICONTROL Refresh]** per ottenere un conteggio aggiornato. |
| Numero di prodotti | Riflette il numero totale di prodotti catalogo disponibili per il servizio. Il [!DNL Product Recommendations] e [!DNL Live Search] le dashboard visualizzano il numero totale di _visualizzabile_ prodotti. [!DNL Catalog Service] non filtra i prodotti in base alla visualizzabilità, quindi se disponi di entrambi [!DNL Catalog Service] e [!DNL Live Search] o [!DNL Product Recommendations] installato, i due dashboard possono mostrare due valori diversi per il conteggio dei prodotti. |
| Prodotti sincronizzati | Fornisce dettagli sui prodotti nell’indice Commerce di base. Per impostazione predefinita, questa tabella è ordinata per &#39;Ultimo aggiornamento&#39;. Per trovare un prodotto specifico, utilizza **[!UICONTROL Search by SKU]** campo. Per controllare le colonne visualizzate, fare clic su **[!UICONTROL Customize Table]** sulla destra del tavolo. |

## Utilizzo del dashboard Gestione dati

Quando si aggiornano i prodotti nel database di Commerce, i dati dei prodotti vengono trasferiti ai servizi SaaS in base alla configurazione del sistema. All&#39;avvio del processo di sincronizzazione **Numero di prodotti** indica il numero di prodotti inviati ai servizi SaaS.

>[!IMPORTANT]
>
>Il tempo necessario per completare la sincronizzazione varia in base alle dimensioni del catalogo e al volume di dati aggiornati.

Quando il numero di prodotti elaborati corrisponde al numero di prodotti aggiornati, indica che la sincronizzazione è completa.

>[!NOTE]
>
>Adobe fornisce anche un’interfaccia della riga di comando e registri di sistema che gli sviluppatori e gli integratori di sistemi possono utilizzare per gestire e tenere traccia delle operazioni di sincronizzazione e risolvere gli errori per i servizi SaaS di Commerce. Per ulteriori informazioni, vedere [Guida all’esportazione dei dati SaaS](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/saas-data-export/overview).

### Elenco dei prodotti sincronizzati

Per visualizzare i dettagli di un prodotto sincronizzato, fai clic sul prodotto dalla tabella.

![Dettagli prodotto Syncd](assets/sync-product-detail.png)

### Risincronizza dati catalogo

Per essere certi che i servizi Commerce SaaS siano sempre aggiornati con le informazioni più recenti sui prodotti, è necessario [implementare una pianificazione](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/cli/manage-indexers#reindex) per la sincronizzazione dei dati del catalogo.

Mentre puoi [avvia manualmente](#manually-resync-catalog) una risincronizzazione dei dati del catalogo dal database di Commerce ai servizi SaaS, non è consigliata in quanto può aumentare il carico sulle risorse hardware. Tuttavia, potrebbe essere necessario risincronizzare manualmente il catalogo nei seguenti scenari:

- Ogni volta che vengono apportate modifiche significative al catalogo dei prodotti, ad esempio aggiungendo nuovi prodotti, aggiornando i dettagli dei prodotti o modificando le categorie

- Se noti eventuali discrepanze o problemi di prestazioni nella visualizzazione dei dati di prodotto nei negozi

- A seguito di eventuali aggiornamenti o modifiche alle integrazioni tra il database di Commerce e i servizi SaaS

- Durante l’implementazione di personalizzazioni o configurazioni che influiscono sulla gestione dei dati dei prodotti o sui processi di sincronizzazione

Attenendoti a queste linee guida e risincronizzando in modo proattivo i dati del catalogo in base alle esigenze, puoi mantenere la coerenza, l’accuratezza e l’affidabilità dei dati nell’ecosistema Adobe Commerce.

#### Risincronizza catalogo manualmente

Se devi risincronizzare i dati del catalogo, fai clic su **[!UICONTROL Settings]** sul lato destro della pagina per visualizzare una finestra di dialogo in cui avviare una risincronizzazione. La risincronizzazione dei dati del catalogo forza il servizio a recuperare i dati dal database di Commerce ai servizi SaaS.

![Sincronizza manualmente prodotti](assets/resync-data.png)
