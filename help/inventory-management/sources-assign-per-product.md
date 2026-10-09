---
title: Assegna origini magazzino per prodotto
description: Assegnare una o più origini [!DNL Inventory Management] a un prodotto nell'amministratore prima di impostare le quantità e le soglie per origine.
exl-id: 7e47be25-633e-4f5d-bb61-0d9e79b6dbad
feature: Inventory, Products
last-update: 2023-10-26
TQID: 'https://experienceleague.adobe.com/Wjx3w6Z-oNALxNRHw65BZDeCzka3BQvtg-m4a9kp-Y8'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
    internal-label: Order Management System
  - id: 8dc0e58b-adf0-51bb-8db5-bb36e3e656fb
    internal-label: Inventory
  - id: 4067ab89-2e97-5de1-8d98-de8318461a8d
    internal-label: Products
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
    internal-label: Admin
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
    internal-label: Leader
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
    internal-label: Intermediate
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
    internal-label: Beginner
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: 15f1e2ee152fb047443da68dec2cc69551e6c7a0
workflow-type: tm+mt
source-wordcount: '160'
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

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
