---
title: Assegna origini magazzino per prodotto
description: Scopri come assegnare un’origine di inventario a un prodotto.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
source-git-commit: 4d89212585fa846eb94bf83a640d0358812afbc5
workflow-type: tm+mt
source-wordcount: '151'
ht-degree: 0%

---

# Assegna origini per prodotto

Prima di modificare quantità e impostazioni, è necessario assegnare [sorgenti](sources-manage.md) ai prodotti.

{{$include /help/_includes/unassign-source.md}}

## Assegnare origini a un prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Apri un prodotto in modalità _Modifica_.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Sources]**.

   Questa sezione consente di modificare l&#39;origine, aggiornare le quantità di magazzino e altro ancora.

   >[!NOTE]
   >
   >Attualmente, solo i prodotti semplici, configurabili, virtuali, scaricabili e raggruppati supportano più origini. I prodotti bundle possono essere creati e gestiti solo con il Source e Stock predefiniti.

   ![Sezione origini prodotto](assets/inventory-product-sources-before.png){width="600" zoomable="yes"}

1. Per aggiungere un&#39;origine, fare clic su **[!UICONTROL Assign Sources]**.

1. Nella pagina _[!UICONTROL Assign Sources]_selezionare la casella di controllo accanto a ogni origine che si desidera assegnare per il prodotto.

   ![Prodotto - Assegna origini](assets/inventory-product-assign-sources.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Done]** per aggiungere le origini.

1. Per salvare, effettuate una delle seguenti operazioni:

   - Fare clic su **[!UICONTROL Save]**.
   - Scegliere **[!UICONTROL Save & Close]** dal menu _[!UICONTROL Save]_(![freccia menu](../assets/icon-menu-down-arrow-red.png)).

Dopo aver assegnato le origini, aggiornare la [quantità di magazzino](quantities-assign-per-product.md) per ogni origine prodotto.
