---
title: Operazioni ordine programmato
description: Scopri le operazioni dell’ordine programmato e le impostazioni cron dell’ordine che supportano questa funzionalità.
exl-id: 330fe75a-d901-4696-946e-fa7af9ea3d40
feature: Orders, Configuration
source-git-commit: db859c40cd6f052a8f1153e245c23d9f1ea97d33
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Operazioni ordine programmato

Utilizza i processi [Cron](../systems/cron.md) per pianificare le seguenti attività di elaborazione degli ordini:

![Griglia ordini](./assets/orders-grid.png){width="700" zoomable="yes"}

## Imposta durata ordine di pagamento in sospeso

La durata degli ordini con pagamenti in sospeso è determinata dalla configurazione delle _impostazioni Cron ordini_. Il valore predefinito è impostato su 480 minuti, ovvero otto ore.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi la sezione **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Orders Cron Settings]**.

   ![Impostazioni Cron Ordini](../configuration-reference/sales/assets/sales-orders-cron-settings.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Pending Payment Order Lifetime (minutes)]**, immettere il numero di minuti prima della scadenza di un pagamento in sospeso.

1. Fare clic su **[!UICONTROL Save Config]**.

## Abilita aggiornamenti pianificati della griglia e reindicizzazione

La configurazione Impostazioni griglia pianifica gli aggiornamenti alle seguenti griglie di gestione degli ordini e reindicizza i dati come pianificato da [Cron](../systems/cron.md):

- [Ordini](orders.md#orders-workspace)
- [Fatture](invoices.md)
- [Spedizioni](shipments.md)
- [Note di credito](credit-memos.md)

Pianificando queste attività, puoi evitare i blocchi che si verificano quando i dati vengono salvati e ridurre il tempo di elaborazione. Quando questa opzione è attivata, gli aggiornamenti vengono eseguiti solo durante il processo cron pianificato. Per ottenere risultati ottimali, Cron deve essere configurato per essere eseguito una volta al minuto.

**_Per abilitare gli aggiornamenti e la reindicizzazione:_**

Quando è abilitata la [modalità di produzione](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#production-mode) (la modalità predefinita utilizzata in Adobe Commerce nell&#39;infrastruttura cloud), eseguire il comando seguente:

``bin/magento config:set dev/grid/async_indexing 1``

Quando è attivata la modalità predefinita [](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/setup/application-modes.html#default-mode), completare i passaggi seguenti:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi la sezione **[!UICONTROL Advanced]** e scegli **[!UICONTROL Developer]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Grid Settings]**.

1. Imposta **[!UICONTROL Asynchronous Indexing]** su `Enable`.

   ![Impostazioni griglia](../configuration-reference/advanced/assets/developer-grid-settings.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save Config]**.
