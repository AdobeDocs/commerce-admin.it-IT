---
title: Dashboard di gestione dati
description: Scopri la dashboard di gestione dati
feature: Products, Customers, Data Import/Export
source-git-commit: 925af4d3841f2972dfffcd52125a41c4a4b28815
workflow-type: tm+mt
source-wordcount: '291'
ht-degree: 0%

---

# Dashboard di gestione dati

Il dashboard di gestione dati fornisce informazioni approfondite sui flussi di dati per i prodotti SaaS di Adobe Commerce. Utenti di [!DNL Live Search], [!DNL Product Recommendations], e [!DNL Catalog Service] può visualizzare gli stati di sincronizzazione dei prodotti e risincronizzare i dati da un singolo dashboard.

Il dashboard di gestione dati si trova in *Sistema* > Trasferimento dati > *Dashboard di gestione dati*.

![Dashboard di gestione dati](assets/data-management-dashboard.png)

## Impostazioni

Il pulsante Settings (Impostazioni) sul lato destro della pagina apre il [[!DNL Catalog Sync]](https://experienceleague.adobe.com/docs/commerce-merchant-services/user-guides/data-services/catalog-sync.html) impostazioni.

Normalmente, il [!DNL Catalog Sync] il processo viene eseguito automaticamente, una volta all&#39;ora.

La risincronizzazione dei dati del catalogo forza il servizio a recuperare i dati dal database di Commerce, garantendo che le modifiche più recenti vengano applicate al servizio e al sito. Utilizzare questo pulsante se sono state apportate diverse modifiche al prodotto e tali modifiche devono essere aggiornate prima del normale processo di sincronizzazione automatica.

## Stato sincronizzazione

Il _[!UICONTROL Sync]_il pannello di stato riporta il numero di prodotti sincronizzati nelle ultime tre ore. Se apporti aggiornamenti non frequenti al catalogo, questo valore è spesso zero. Clic **[!UICONTROL Refresh]**per aggiornare il conteggio.

## Numero di prodotti

Il pannello di conteggio dei prodotti riflette il numero totale di prodotti catalogo disponibili per il servizio.

Il [!DNL Catalog Service] la dashboard riflette il numero totale di prodotti nel catalogo disponibili per il servizio. In genere si tratta di tutti i prodotti nel database Commerce.

Le dashboard di Recommendations e Live Search del prodotto visualizzano il numero totale di [_ricercabile_](https://experienceleague.adobe.com/docs/commerce-admin/catalog/catalog/search/search.html) prodotti. Se alcuni prodotti non sono impostati per essere ricercabili, ciò corrisponderebbe alla differenza nei totali dei prodotti tra [!DNL Product Recommendations] e [!DNL Live Search], e [!DNL Catalog Service].

## Prodotti sincronizzati

La tabella Prodotti catalogo sincronizzati fornisce dettagli sui prodotti nell’indice. Per impostazione predefinita, questa tabella è ordinata per &#39;Ultimo aggiornamento&#39;.

Per trovare un prodotto specifico, utilizza**[!UICONTROL Search by SKU]Campo ** .
Per controllare le colonne visualizzate, fare clic su **[!UICONTROL Customize Table]** sulla destra del tavolo.
