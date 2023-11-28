---
title: Assegna quantità di magazzino per prodotto
description: Scopri come aggiornare le quantità di magazzino per il prodotto e tenere traccia delle scorte disponibili.
exl-id: 935385bb-6657-4d49-980e-96a3d0d3a187
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Assegna quantità per prodotto

Dopo l’aggiunta [sorgenti](sources-assign-per-product.md), aggiorna le quantità di magazzino per il prodotto. Questi valori tengono traccia degli importi delle scorte disponibili.

Per nascondere il magazzino di un&#39;origine dalle spedizioni senza rimuovere l&#39;origine, impostare _[!UICONTROL Source Item Status]_a `Out of Stock`. Le opzioni SSA e di spedizione accedono solo alle origini elencate come `In Stock` con quantità di magazzino disponibile.

Tutte le quantità e le origini aggiornate vengono visualizzate nella griglia di prodotto.

## Aggiorna quantità

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Individua e apri un prodotto in modalità di modifica.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Sources]** sezione.

1. Imposta **[!UICONTROL Source Item Status]** a `In Stock`.

1. per aggiornare la quantità per le scorte esistenti, inserire un importo per **[!UICONTROL Qty]**.

1. Per impostare una notifica per le quantità di magazzino, effettuare una delle seguenti operazioni:

   - Quantità notifica personalizzata: deseleziona la **[!UICONTROL Use Default]** e immettere un importo in **[!UICONTROL Notify Qty]**.
   - Quantità di notifica predefinita: seleziona la **[!UICONTROL Use Default]** casella di controllo. [!DNL Commerce] verifica e utilizza l’impostazione in _[!UICONTROL Advanced Inventory]_o configurazione dell’archivio globale.

   ![Aggiorna quantità prodotto per origine](assets/inventory-product-quantity-edit.png){width="350" zoomable="yes"}

1. Per salvare, effettuate una delle seguenti operazioni:

   - Clic **[!UICONTROL Save]**.

   - Il giorno **[!UICONTROL Save]** (![Freccia del menu](../assets/icon-menu-down-arrow-red.png)), scegliere **[!UICONTROL Save & Close]**.


La griglia prodotti viene aggiornata con un elenco di tutte le origini e delle quantità correlate. Per i prodotti con più di cinque sorgenti assegnate, passa il puntatore del mouse su _[!UICONTROL Quantity per Source]_per visualizzare l&#39;elenco completo.

![Quantità di prodotti per origine](assets/inventory-product-quantity.png){width="600" zoomable="yes"}
