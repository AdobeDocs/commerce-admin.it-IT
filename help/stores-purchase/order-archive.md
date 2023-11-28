---
title: Archivia ordini
description: Scopri come configurare l’archivio ordini per migliorare le prestazioni e semplificare Commerce per la tua organizzazione.
exl-id: 12025591-bfe2-4f44-9358-a38ea4493b5c
feature: Orders, Configuration
source-git-commit: 47f170f1a1dd1c236b99c2e7139bb119368abf47
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# Archivia ordini

{{ee-feature}}

L&#39;archiviazione degli ordini migliora regolarmente le prestazioni e consente di mantenere l&#39;area di lavoro libera da informazioni non necessarie, in modo da poter concentrarsi sulle attività aziendali correnti. Le fatture, le spedizioni e le note di accredito possono essere archiviate automaticamente o manualmente e possono essere visualizzate in qualsiasi momento.

>[!NOTE]
>
>Il _[!UICONTROL Archive]_viene visualizzata nella [[!UICONTROL Sales] menu](sales-menu.md) solo quando l&#39;archiviazione è [abilitato](../configuration-reference/sales/sales.md).

## Configurare l’archivio degli ordini

È possibile configurare lo store per archiviare ordini, fatture, spedizioni e note di credito dopo un determinato numero di giorni. È possibile spostare gli ordini e i documenti associati nell&#39;archivio o ripristinarli allo stato precedente. Gli ordini archiviati non vengono eliminati e rimangono disponibili dall’amministratore. I dati archiviati possono essere esportati in un file CSV e aperti in un foglio di calcolo. Quando è attivata, la _Archivia_ nella parte superiore dell&#39;area di lavoro.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegliere **[!UICONTROL Sales]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]** sezione.

   ![Impostazioni di configurazione per l&#39;archiviazione di ordini, fatture, spedizioni e note di credito](../configuration-reference/sales/assets/sales-orders-invoices-shipments-credit-memos-archiving.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable Archiving]** a `Yes`.

   >[!NOTE]
   >
   >Se successivamente si decide di disattivare l&#39;archiviazione, tutti gli ordini archiviati vengono ripristinati allo stato precedente.

1. Imposta **[!UICONTROL Archive Orders Purchased]** al numero di giorni di attesa prima dell&#39;archiviazione degli ordini completati.

   Per impostazione predefinita, gli ordini vengono archiviati 30 giorni dopo l’acquisto.

1. In **[!UICONTROL Order Statuses to be Archived]** selezionare lo stato di ciascun ordine da utilizzare per identificare gli ordini da archiviare.

   Per selezionare più elementi, tenere premuto il tasto Ctrl (Windows) o Comando (Mac) mentre si fa clic su ogni elemento.

1. Clic **[!UICONTROL Save Config]**.

1. Quando richiesto, aggiorna eventuali cache non valide.

## Visualizza documenti archiviati

1. In _[!UICONTROL Sales]_menu in_[!UICONTROL Archive]_, scegli una delle seguenti opzioni:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Per visualizzare i dettagli, fare clic su qualsiasi documento archiviato nell&#39;elenco.

## Applicare un&#39;azione a un documento archiviato

Selezionare ogni documento come destinazione dell&#39;azione e scegliere una delle opzioni seguenti **[!UICONTROL Actions]**:

- `Cancel`
- `Hold`
- `Unhold`
- `Print`
- `Move to Orders Management`

## Archiviare manualmente i documenti

1. Selezionare il tipo di documento da archiviare tra i seguenti:

   - **[!UICONTROL Orders]**
   - **[!UICONTROL Invoices]**
   - **[!UICONTROL Shipments]**
   - **[!UICONTROL Credit Memos]**

1. Selezionare la casella di controllo di ogni elemento da archiviare.

1. Nell&#39;angolo in alto a destra, imposta **[!UICONTROL Actions]** a `Move to Archive`.

1. Clic **[!UICONTROL Submit]** per archiviare i documenti selezionati.

## Ripristina documenti archiviati

1. Scegliere il tipo di documento da ripristinare.

1. Selezionare i documenti utilizzando una delle opzioni seguenti:

   - Per selezionare tutti i documenti visibili, nell&#39;angolo superiore sinistro fare clic su **[!UICONTROL Select Visible]**.

   - Selezionare manualmente la casella di controllo di ogni documento che si desidera ripristinare.

1. In alto a destra, imposta **[!UICONTROL Action]** a `Move to Orders Management`.

1. Clic **[!UICONTROL Submit]** per ripristinare i documenti.

## Esporta documenti archiviati

1. Scegliere il tipo di documento da esportare.

1. Nel menu in alto a destra, imposta **[!UICONTROL Export to:]** a uno dei seguenti valori:

   - `CSV`
   - `Excel`

1. Clic **[!UICONTROL Export]**.

È possibile configurare lo store per archiviare ordini, fatture, spedizioni e note di credito dopo un determinato numero di giorni. È possibile spostare gli ordini e i documenti associati nell&#39;archivio o ripristinarli allo stato precedente. Gli ordini archiviati non vengono eliminati e rimangono disponibili dall’amministratore. I dati archiviati possono essere esportati in un file CSV e aperti in un foglio di calcolo. Quando è attivata, la _[!UICONTROL Archive]_nella parte superiore dell&#39;area di lavoro.

## Archivia manualmente gli ordini

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Per selezionare l&#39;ordine nella griglia, selezionare la casella di controllo nella prima colonna.

1. Imposta il **[!UICONTROL Actions]** controllo a `Move to Archive` e cerca il messaggio che l’ordine è stato archiviato.

   ![Spostamento degli ordini selezionati nell&#39;archivio ](./assets/order-move-to-archive.png){width="700" zoomable="yes"}

>[!TIP]
>
>Per specificare un elenco degli stati degli ordini che è possibile archiviare, vedere [Configurare l’archivio degli ordini](#configure-the-order-archive).

## Visualizzare un ordine archiviato

1. Aprire la vista archivio utilizzando uno dei metodi seguenti:

   - Nella barra dei pulsanti sopra _[!UICONTROL Orders]_griglia, fare clic su **[!UICONTROL Go to Archive]**.

   - Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Archive]_>**[!UICONTROL Orders]**.

   >[!NOTE]
   >
   >Come per la pagina Ordini, il titolo della pagina Ordini archiviati è _[!UICONTROL Orders]_. L’unica differenza evidente è l’opzione nella barra dei pulsanti per_[!UICONTROL Return to Orders Management]_. L’URL della pagina indica anche che ti trovi nell’archivio dell’ordine.

1. In _Azione_ , fare clic su **[!UICONTROL View]**.

   ![Visualizzare un ordine archiviato](./assets/order-archived-view.png){width="600" zoomable="yes"}

## Ripristinare un ordine archiviato

>[!NOTE]
>
>Un ordine ripristinato da un ordine archiviato viene archiviato nuovamente in base al numero di giorni configurati in [!UICONTROL Archive Orders Purchased] (vedere [Configurare l’archivio degli ordini](#configure-the-order-archive)). Il numero di giorni viene calcolato rispetto al [!UICONTROL Updated At] data dell&#39;ordine, che viene modificata quando l&#39;ordine viene spostato dall&#39;archivio.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Nella barra dei pulsanti, fai clic su **[!UICONTROL Go to Archive]**.

1. Individuare il record da ripristinare e fare clic sulla casella di controllo per selezionarlo.

   ![Seleziona ordine da ripristinare](./assets/order-archived-select-to-restore.png){width="600" zoomable="yes"}

1. Imposta il **[!UICONTROL Actions]** valore di controllo a `Move to Order Management`.

Cercare il messaggio che indica che l&#39;ordine archiviato è stato rimosso dall&#39;archivio.

## Esporta ordine archiviato

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > _[!UICONTROL Operations]_>**[!UICONTROL Orders]**.

1. Nel menu Azioni, fai clic su **[!UICONTROL Export]** e selezionare il formato desiderato.
