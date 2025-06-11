---
title: Tradurre una pagina di contenuto
description: Scopri come creare una versione tradotta di ogni pagina disponibile dalla visualizzazione specifica dello store.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '358'
ht-degree: 0%

---

# Tradurre una pagina di contenuto

Se nell&#39;archivio sono presenti più visualizzazioni in [lingue](../stores-purchase/store-localize.md) diverse e le impostazioni locali di ogni visualizzazione sono state impostate su una lingua diversa, il risultato sarà un sito tradotto parzialmente. Il passaggio successivo consiste nel creare una versione tradotta di ogni pagina disponibile dalla visualizzazione specifica dello store. La colonna [!UICONTROL Store View] dell&#39;elenco _[!UICONTROL Manage Pages]_&#x200B;mostra ogni visualizzazione con una versione tradotta della pagina.

Per tradurre una pagina di contenuto, devi creare un’altra pagina che abbia la stessa chiave URL dell’originale, ma che sia assegnata alla visualizzazione specifica dello store. Quindi, aggiorna la pagina per la visualizzazione specifica con il testo tradotto. Nell&#39;esempio seguente viene illustrato come creare una versione tradotta della pagina _Informazioni su di noi_ per la visualizzazione dello store spagnolo.

## Passaggio 1: copia la chiave URL per la pagina da tradurre

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Nella griglia, individua la pagina da tradurre e apri in modalità _modifica_.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]** e copiare **[!UICONTROL URL Key]** negli Appunti.

1. Per tornare alla griglia _[!UICONTROL Pages]_, fare clic su **[!UICONTROL Back]**&#x200B;nella barra dei pulsanti superiore.

## Passaggio 2: aggiungere una pagina per il contenuto tradotto

1. Fare clic su **[!UICONTROL Add New Page]**.

1. Immetti **[!UICONTROL Page Title]** tradotto.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Content]** e completare il testo tradotto per la pagina.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]** ed effettuare le seguenti operazioni:

   - Incolla **[!UICONTROL URL Key]** copiato dalla pagina originale.

   - Immettere il testo tradotto per **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]** e **[!UICONTROL Meta Description]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Page in Websites]** e impostare **[!UICONTROL Store View]** nella visualizzazione archivio in cui la pagina sarà disponibile.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Design]** e impostare la colonna **[!UICONTROL Layout]** della pagina.

1. Fare clic su **[!UICONTROL Save]**.

1. Quando richiesto, aggiorna le [cache](../systems/cache-management.md) non valide.

## Passaggio 3: verificare la traduzione

Per verificare la traduzione, vai alla vetrina e utilizza il selettore di lingua per modificare la visualizzazione dello store.

Tieni presente che nella pagina sono ancora presenti alcuni elementi da tradurre, tra cui i collegamenti del piè di pagina della società [blocco](block-add.md), [messaggio di benvenuto](../getting-started/storefront-branding.md#change-the-welcome-message) e [informazioni sul prodotto](../stores-purchase/store-localize.md#localize-products).
