---
title: Dashboard di amministrazione
description: Scopri la dashboard di amministrazione, in genere la prima pagina visualizzata all’accesso.
exl-id: 56957c0a-1618-444b-a37a-ecf0d7b27eae
source-git-commit: 7b6d70e2f3052af69075790cec1f396e2505bf8b
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 0%

---

# Dashboard di amministrazione

La dashboard è in genere la prima pagina visualizzata quando si accede al _Amministratore_ e può fornire una panoramica in tempo reale delle vendite e dell&#39;attività dei clienti. I dati del dashboard forniscono un’istantanea delle vendite a vita, dell’importo medio dell’ordine, degli ordini recenti e dei termini di ricerca. Il grafico mostra gli ordini completati e gli importi per l’intervallo di date selezionato e può essere generato da dati dinamici, dati in tempo reale o dati aggregati cronologici. Le schede in basso forniscono rapporti rapidi sui prodotti più venduti, sui prodotti più visualizzati, sui nuovi clienti e sui clienti che hanno acquistato di più.

Se si dispone di una quantità significativa di dati da elaborare, è possibile disattivare il grafico per migliorare le prestazioni. La dashboard nell’esempio seguente è configurata per utilizzare dati in tempo reale e mostra gli ordini completati per ora nelle ultime 24 ore. Il grafico viene aggiornato per ogni ordine completato.

![Dashboard](./assets/dashboard-full.png){zoomable=&quot;yes&quot;}

[Reporting avanzato](business-intelligence.md#advanced-reporting) visualizza una dashboard personalizzata in base ai dati di prodotto, ordine e cliente.

![Reporting avanzato](./assets/dashboard-advanced-reporting.png){zoomable=&quot;yes&quot;}

## Configurare il dashboard

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**e completare una delle seguenti impostazioni.

1. Al termine della configurazione, fai clic su **[!UICONTROL Save Config]**.

1. Dopo aver salvato le modifiche, fai clic su **[!UICONTROL Cache Management]** e aggiorna ogni cache non valida.

### Abilita grafici

Se la quantità di dati da elaborare è elevata, è possibile disattivare la visualizzazione del grafico per migliorare le prestazioni. Se non è abilitata, al posto del grafico viene visualizzato il messaggio &quot;Nessun dato trovato&quot;, anche se vengono ancora generati i totali di riepilogo riportati di seguito.

1. Nel pannello di navigazione a sinistra in **[!UICONTROL Advanced]**, scegli **[!UICONTROL Admin]**.

1. Se necessario, espandere **[!UICONTROL Dashboard]** sezione.

   ![Configurazione avanzata - Abilita grafici](./assets/admin-dashboard-config.png){width="600"}

1. Per modificare il valore predefinito, deselezionare **[!UICONTROL Use system value]** casella di controllo.

1. Imposta **Abilita grafici** a `Yes`.

Per ulteriori informazioni sulle opzioni di configurazione dell’amministratore, vedi [Guida di riferimento alla configurazione](../configuration-reference/advanced/admin.md).

### Modificare la pagina di avvio

Il dashboard è quello predefinito [pagina di avvio](../configuration-reference/advanced/admin.md) per l’amministratore, anche se è possibile configurare una pagina di avvio diversa.

1. Se le opzioni di configurazione dell’amministratore non sono già aperte, scegli **[!UICONTROL Admin]** in _[!UICONTROL Advanced]_nel pannello di navigazione a sinistra.

1. Fai clic per espandere **Pagina di avvio** sezione.

   ![Dashboard di amministrazione: impostazione della pagina di avvio](./assets/admin-startup-page.png){width="600"}

1. Cancella **[!UICONTROL Use system value]** e scegli la **Pagina di avvio** che desideri visualizzare quando accedi all’amministratore.

### Scegli le date di inizio

1. Nel pannello di navigazione a sinistra in **[!UICONTROL General]**, scegli **Rapporti**.

1. Nella pagina, espandi il **[!UICONTROL Dashboard]** sezione.

1. Cancella **[!UICONTROL Use system value]** le caselle di controllo per le impostazioni della data ed effettuare le seguenti operazioni:

   - Imposta **Inizio progressivo anno** al **Mese** e **Giorno**.

   - Imposta **Inizio mese corrente** al **Giorno**.

   ![Admin Dashboard - Impostazioni data](./assets/reports-dashboard.png){width="600"}

Per ulteriori informazioni su [!UICONTROL Reports] opzioni di configurazione, vedi [_Guida di riferimento alla configurazione_](../configuration-reference/general/reports.md).

### Configurare l’origine dati

Il grafico del dashboard può essere generato in tempo reale o utilizzando dati storici aggregati. Se le prestazioni rappresentano un problema, è possibile velocizzare le cose utilizzando dati aggregati.

1. Nel pannello di navigazione a sinistra, fai clic su per espandere **Vendite** e scegli **Vendite** sotto.

1. Nella pagina, espandi il **[!UICONTROL Dashboard]** sezione.

   ![Dashboard di amministrazione: impostazione origine dati](./assets/config-sales-dashboard.png){width="600"}

1. Cancella **[!UICONTROL Use system value]** casella di controllo e impostazione **[!UICONTROL Use Aggregated Data]** a uno dei seguenti elementi:

   - Per i dati storici aggregati, scegliere `Yes`.
   - Per i dati in tempo reale, scegli `No`.

## Sezioni del grafico

| Sezione | Descrizione |
|--- |--- |
| [!UICONTROL Orders] | In questa scheda viene visualizzato un grafico in tempo reale di tutti gli ordini completati per la visualizzazione del negozio corrente e per il periodo di tempo specificato. |
| [!UICONTROL Amounts] | In questa scheda viene visualizzato un grafico in tempo reale di tutti gli importi degli ordini completati per la visualizzazione del negozio corrente e per il periodo di tempo specificato. |
| [!UICONTROL Time Range] | Determina i dati rappresentati nel grafico e nei totali di riepilogo riportati di seguito. Opzioni: `Last 7 Days` / `Current Month` / `YTD` / `2YTD` |
| [!UICONTROL Summary Totals] | I totali di ricavi, imposte, spedizione e quantità sotto il grafico si basano sui dati del grafico e sull&#39;impostazione dell&#39;intervallo di tempo corrente. |

{style="table-layout:auto"}

## Dati snapshot

| Sezione | Descrizione |
|--- |--- |
| [!UICONTROL Lifetime Sales] | Totale aggregato delle vendite durante il ciclo di vita del negozio. |
| [!UICONTROL Average Order] | L&#39;importo medio dell&#39;ordine durante la durata del negozio. |
| [!UICONTROL Last Orders] | Riepilogo degli ultimi cinque ordini effettuati. |
| [!UICONTROL Last Search Terms] | Gli ultimi cinque termini di ricerca. |
| [!UICONTROL Top Search Terms] | I cinque termini di ricerca più comunemente utilizzati. |

{style="table-layout:auto"}

## Schede del rapporto

| Sezione | Descrizione |
|--- |--- |
| [!UICONTROL Bestsellers] | I cinque prodotti più venduti nel periodo di tempo specificato. |
| [!UICONTROL Most Viewed Products] | I cinque prodotti più visualizzati durante il periodo di tempo specificato. |
| [!UICONTROL New Customers] | Gli ultimi cinque clienti che si sono registrati per un account durante il periodo di tempo specificato. |
| [!UICONTROL Customers] | Gli ultimi cinque clienti con un ordine che ha completato l’elaborazione durante il periodo di tempo specificato. |

{style="table-layout:auto"}

## Pulsanti del dashboard

| Pulsante | Descrizione |
|--- |--- |
| [!UICONTROL Reload Data] | Aggiorna i dati del dashboard. |
| [!UICONTROL Go to Advanced Reporting] | Visualizza un dashboard personalizzato di grafici e rapporti dinamici in base ai dati di prodotto, ordine e cliente. Per un’analisi più approfondita, consulta [Reporting avanzato](business-intelligence.md#advanced-reporting). |

{style="table-layout:auto"}
