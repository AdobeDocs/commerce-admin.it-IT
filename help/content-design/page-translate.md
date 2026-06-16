---
title: Tradurre una pagina di contenuto
description: Scopri come creare una versione tradotta di ogni pagina disponibile dalla visualizzazione specifica dello store.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/9jox-v5fCEhPsaex70yQod--qH-Xnp9dkgmuxJGTZd0
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 368
ht-degree: 0%

---

# Tradurre una pagina di contenuto

Se nell&#39;archivio sono presenti più visualizzazioni in [lingue](../stores-purchase/store-localize.md) diverse e le impostazioni locali di ogni visualizzazione sono state impostate su una lingua diversa, il risultato sarà un sito tradotto parzialmente. Il passaggio successivo consiste nel creare una versione tradotta di ogni pagina disponibile dalla visualizzazione specifica dello store. La colonna [!UICONTROL Store View] dell&#39;elenco _[!UICONTROL Manage Pages]_mostra ogni visualizzazione con una versione tradotta della pagina.

Per tradurre una pagina di contenuto, devi creare un’altra pagina che abbia la stessa chiave URL dell’originale, ma che sia assegnata alla visualizzazione specifica dello store. Quindi, aggiorna la pagina per la visualizzazione specifica con il testo tradotto. Nell&#39;esempio seguente viene illustrato come creare una versione tradotta della pagina _Informazioni su di noi_ per la visualizzazione dello store spagnolo.

## Passaggio 1: copia la chiave URL per la pagina da tradurre

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Nella griglia, individua la pagina da tradurre e apri in modalità _modifica_.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Search Engine Optimization]** e copiare **[!UICONTROL URL Key]** negli Appunti.

1. Per tornare alla griglia _[!UICONTROL Pages]_, fare clic su **[!UICONTROL Back]**nella barra dei pulsanti superiore.

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
