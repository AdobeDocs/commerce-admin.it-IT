---
title: Assegna quantità di magazzino per prodotto
description: Scopri come aggiornare le quantità di magazzino per il prodotto e tenere traccia delle scorte disponibili.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
TQID: https://experienceleague.adobe.com/0OBXyHUbsWVXmEnWEWd0CGcBNhci57w8HGtDCGCWuOk
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# Assegna quantità per prodotto

Dopo aver aggiunto [sorgenti](sources-assign-per-product.md), aggiorna le quantità di magazzino per il prodotto. Questi valori tengono traccia degli importi delle scorte disponibili.

Per nascondere le scorte di un&#39;origine dalle spedizioni senza rimuovere l&#39;origine, impostare _[!UICONTROL Source Item Status]_su `Out of Stock`. Le opzioni SSA e di spedizione accedono solo alle origini elencate come `In Stock` con quantità di magazzino disponibile.

Tutte le quantità e le origini aggiornate vengono visualizzate nella griglia di prodotto.

## Aggiorna quantità

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Individua e apri un prodotto in modalità di modifica.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Sources]**.

1. Imposta **[!UICONTROL Source Item Status]** su `In Stock`.

1. per aggiornare la quantità per le scorte esistenti, immettere un importo per **[!UICONTROL Qty]**.

1. Per impostare una notifica per le quantità di magazzino, effettuare una delle seguenti operazioni:

   - Quantità notifica personalizzata: deselezionare la casella di controllo **[!UICONTROL Use Default]** e immettere un importo in **[!UICONTROL Notify Qty]**.
   - Quantità di notifica predefinita: selezionare la casella di controllo **[!UICONTROL Use Default]**. [!DNL Commerce] verifica e utilizza l&#39;impostazione in _[!UICONTROL Advanced Inventory]_o nella configurazione dell&#39;archivio globale.

   ![Aggiorna quantità prodotto per Source](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Per salvare, effettuate una delle seguenti operazioni:

   - Fare clic su **[!UICONTROL Save]**.

   - Scegliere **[!UICONTROL Save & Close]** dal menu **[!UICONTROL Save]** (![freccia menu](../assets/icon-menu-down-arrow-red.png)).


La griglia prodotti viene aggiornata con un elenco di tutte le origini e delle quantità correlate. Per i prodotti con più di cinque origini assegnate, passa il cursore del mouse sulla colonna _[!UICONTROL Quantity per Source]_per visualizzare l&#39;elenco completo.

![Quantità di prodotti per origine](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
