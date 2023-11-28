---
title: Tradurre una pagina di contenuto
description: Scopri come creare una versione tradotta di ogni pagina disponibile dalla visualizzazione specifica dello store.
exl-id: e8743ea5-0c8e-4970-987d-c9ac7c1e2a66
feature: Page Content
topic: Commerce, Localization
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---

# Tradurre una pagina di contenuto

Se il tuo negozio ha più visualizzazioni in diverse [lingue](../stores-purchase/store-localize.md)e se le impostazioni internazionali di ogni visualizzazione sono state impostate su una lingua diversa, il risultato sarà un sito tradotto parzialmente. Il passaggio successivo consiste nel creare una versione tradotta di ogni pagina disponibile dalla visualizzazione specifica dello store. Il [!UICONTROL Store View] colonna del _[!UICONTROL Manage Pages]_mostra ogni visualizzazione con una versione tradotta della pagina.

Per tradurre una pagina di contenuto, devi creare un’altra pagina che abbia la stessa chiave URL dell’originale, ma che sia assegnata alla visualizzazione specifica dello store. Quindi, aggiorna la pagina per la visualizzazione specifica con il testo tradotto. L’esempio seguente mostra come creare una versione tradotta del _Chi siamo_ pagina per la visualizzazione del punto vendita spagnolo.

## Passaggio 1: copia la chiave URL per la pagina da tradurre

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Nella griglia, individua la pagina da tradurre e apri in _modifica_ modalità.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization]** e copia il **[!UICONTROL URL Key]** negli Appunti.

1. Per tornare al _[!UICONTROL Pages]_griglia, fare clic su **[!UICONTROL Back]**nella barra dei pulsanti superiore.

## Passaggio 2: aggiungere una pagina per il contenuto tradotto

1. Clic **[!UICONTROL Add New Page]**.

1. Inserisci il **[!UICONTROL Page Title]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** e completa il testo tradotto per la pagina.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization]** ed effettuare le seguenti operazioni:

   - Incolla il **[!UICONTROL URL Key]** copiato dalla pagina originale.

   - Inserisci il testo tradotto per **[!UICONTROL Meta Title]**, **[!UICONTROL Meta Keywords]**, e **[!UICONTROL Meta Description]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Page in Websites]** sezione e set **[!UICONTROL Store View]** nella visualizzazione store in cui la pagina sarà disponibile.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Design]** e impostare la colonna **[!UICONTROL Layout]** della pagina.

1. Clic **[!UICONTROL Save]**.

1. Quando richiesto, aggiorna le opzioni non valide. [cache](../systems/cache-management.md).

## Passaggio 3: verificare la traduzione

Per verificare la traduzione, vai alla vetrina e utilizza il selettore di lingua per modificare la visualizzazione dello store.

Tieni presente che nella pagina sono ancora presenti alcuni elementi da tradurre, tra cui i collegamenti del piè di pagina della società [blocco](block-add.md), il [messaggio di benvenuto](../getting-started/storefront-branding.md#change-the-welcome-message), e [informazioni sul prodotto](../stores-purchase/store-localize.md#localize-products).
