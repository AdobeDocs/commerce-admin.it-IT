---
title: Operazioni ordine programmato
description: Scopri le operazioni dell’ordine programmato e le impostazioni cron dell’ordine che supportano questa funzionalità.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---

# Operazioni ordine programmato

Utilizzare [Cron](../systems/cron.md) OdL per programmare i seguenti task di elaborazione degli ordini:

![Griglia ordini](./assets/orders-grid.png){width="700" zoomable="yes"}

## Imposta durata ordine di pagamento in sospeso

La durata degli ordini con pagamenti in sospeso è determinata dalla _Impostazioni Cron Ordini_ configurazione. Il valore predefinito è impostato su 480 minuti, ovvero otto ore.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegliere **[!UICONTROL Sales]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Orders Cron Settings]** sezione.

   ![Impostazioni Cron Ordini](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, immettere il numero di minuti prima della scadenza di un pagamento in sospeso.

1. Clic **[!UICONTROL Save Config]**.

## Abilita aggiornamenti pianificati della griglia e reindicizzazione

La configurazione Impostazioni griglia pianifica gli aggiornamenti alle seguenti griglie di gestione degli ordini e reindicizza i dati come pianificato da [Cron](../systems/cron.md):

- [Ordini](orders.md#orders-workspace)
- [Fatture](invoices.md)
- [Spedizioni](shipments.md)
- [Note di credito](credit-memos.md)

Pianificando queste attività, puoi evitare i blocchi che si verificano quando i dati vengono salvati e ridurre il tempo di elaborazione. Quando questa opzione è attivata, gli aggiornamenti vengono eseguiti solo durante il processo cron pianificato. Per ottenere risultati ottimali, Cron deve essere configurato per essere eseguito una volta al minuto.

**_Per abilitare gli aggiornamenti e la reindicizzazione:_**

Quando [Modalità di produzione](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (la modalità predefinita utilizzata in Adobe Commerce sull’infrastruttura cloud) è abilitata, esegui il seguente comando:

``bin/magento config:set dev/grid/async_indexing 1``

Quando [Modalità predefinita](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode) è attivato, completa i passaggi seguenti:

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegliere **[!UICONTROL Developer]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Grid Settings]** sezione.

1. Imposta **[!UICONTROL Asynchronous Indexing]** a `Enable`.

   ![Impostazioni griglia](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.
