---
title: Dashboard di gestione dati
description: Scopri come accedere alle informazioni sui flussi di dati per Catalog Service, Live Search, Product Recommendations.
feature: Products, Customers, Data Import/Export
source-git-commit: eed80afd8755d416d979c362f8c21fe97ce2d2ba
workflow-type: tm+mt
source-wordcount: '258'
ht-degree: 0%

---


# Dashboard di gestione dati

Il dashboard di gestione dati fornisce informazioni approfondite sui flussi di dati per i prodotti SaaS di Adobe Commerce. Utenti di [!DNL Live Search], [!DNL Product Recommendations], e [!DNL Catalog Service] può visualizzare gli stati di sincronizzazione dei prodotti e risincronizzare i dati da un singolo dashboard.

Il dashboard di gestione dati si trova in *Sistema* > Trasferimento dati > *Dashboard di gestione dati*.

![Dashboard di gestione dati](assets/data-management-dashboard.png)

## Impostazioni

Il **[!UICONTROL Settings]** sul lato destro della pagina apre la finestra di dialogo in cui puoi risincronizzare i dati del catalogo.

La risincronizzazione dei dati del catalogo forza il servizio a recuperare i dati dal database di Commerce. Questa azione viene in genere utilizzata durante il primo onboarding quando la sincronizzazione del catalogo non viene eseguita per un paio d’ore.

## Stato sincronizzazione

Il _[!UICONTROL Sync]_il pannello di stato riporta il numero di prodotti sincronizzati nelle ultime tre ore. Se apporti aggiornamenti non frequenti al catalogo, questo valore è spesso zero. Clic **[!UICONTROL Refresh]**per aggiornare il conteggio.

## Numero di prodotti

Il pannello di conteggio dei prodotti riflette il numero totale di prodotti catalogo disponibili per il servizio.

Il [!DNL Product Recommendations] e [!DNL Live Search] le dashboard visualizzano il numero totale di _visualizzabile_ prodotti. [!DNL Catalog Service] non filtra i prodotti in base alla visualizzabilità, quindi se disponi di entrambi [!DNL Catalog Service] e [!DNL Live Search] o [!DNL Product Recommendations] installato, i due dashboard possono mostrare due valori diversi per il conteggio dei prodotti.

## Prodotti sincronizzati

La tabella Prodotti sincronizzati fornisce dettagli sui prodotti nell&#39;indice. Per impostazione predefinita, questa tabella è ordinata per &#39;Ultimo aggiornamento&#39;.

Per trovare un prodotto specifico, utilizza **[!UICONTROL Search by SKU]** campo .
Per controllare le colonne visualizzate, fare clic su **[!UICONTROL Customize Table]** sulla destra del tavolo.
