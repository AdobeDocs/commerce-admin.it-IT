---
title: Trasferisci magazzino all'origine
description: Scopri in che modo i commercianti multi-sorgente possono trasferire l’inventario dei prodotti da una posizione di origine a un’altra.
exl-id: 30438412-bc93-4e65-8b6a-5ddb50afa7ff
feature: Inventory, Configuration
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Trasferisci magazzino all&#39;origine

A seconda delle esigenze aziendali e dello stato dell’ubicazione, i commercianti multi-sorgente spesso trasferiscono l’inventario dei prodotti da un’ubicazione di origine a un’altra. Ad esempio, è possibile che si stia chiudendo un&#39;ubicazione di magazzino o che non si stia più effettuando la spedizione di prodotti specifici da un&#39;ubicazione, spostando tutte le operazioni relative a tali prodotti in una nuova ubicazione.

Questa opzione consente di selezionare uno o più prodotti, l&#39;origine di origine per il trasferimento del magazzino e l&#39;origine di destinazione per la ricezione delle quantità:

- Le quantità di magazzino, lo stato dell&#39;articolo Source (in magazzino/esaurito) e la quantità di notifica per l&#39;origine selezionata vengono spostati per prodotto.

- Se un prodotto non dispone di tale origine, viene saltato.

- Viene spostato tutto l’inventario dei prodotti per l’origine. Impossibile trasferire una quantità parziale.

>[!NOTE]
>
>Se le origini di origine e destinazione si trovano in scorte diverse, questo influisce sulla quantità di vendita e sulle prenotazioni aggregate per gli ordini in corso.

È inoltre possibile annullare l&#39;assegnazione dell&#39;origine durante il trasferimento delle quantità di magazzino.

{{$include /help/_includes/unassign-source.md}}

![Trasferisci scorte in un&#39;altra origine](assets/inventory-bulk-transfer-source.gif)

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Seleziona i prodotti per i quali desideri modificare le origini.

   Sfoglia o cerca i prodotti e seleziona le caselle di controllo per il trasferimento.

1. Fai clic sul menu **[!UICONTROL Actions]** nella parte superiore e scegli **[!UICONTROL Transfer Inventory to Source]**.

1. Fare clic su **[!UICONTROL OK]** nella finestra di conferma.

1. Per trasferire i prodotti in una nuova destinazione, selezionare l&#39;origine (_[!UICONTROL from]_).

1. per trasferire i prodotti in una nuova destinazione, selezionare l&#39;origine di destinazione (_[!UICONTROL to]_).

1. Per rimuovere l&#39;origine dai prodotti, selezionare la casella di controllo facoltativa **[!UICONTROL Unassign from origin source after transfer]**.

   ![Seleziona origine e destinazione per il trasferimento](assets/inventory-bulk-transfer-summary.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Transfer Inventory]**.

   Tutte le quantità di prodotto vengono detratte dall&#39;origine e aggiunte all&#39;origine di destinazione. La quantità e la quantità vendibile vengono aggiornate automaticamente.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
