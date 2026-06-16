---
title: Impostazioni prodotto - [!UICONTROL Sources]
description: Per un prodotto, le impostazioni [!UICONTROL Sources] consentono di accedere alle origini  [!DNL Inventory Management]  da cui è possibile distribuire il prodotto.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
TQID: https://experienceleague.adobe.com/7LFF4ufXyKtJwUp4DiNDdnRMhFRsM1tX8Z2TlPt1Kso
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: c18ed297-2187-4aec-affb-9d9654eca6fc
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 259
ht-degree: 0%

---

# Impostazioni prodotto - [!UICONTROL Sources]

Nella sezione _[!UICONTROL Sources]_&#x200B;delle impostazioni del prodotto sono elencate le origini da cui è possibile distribuire il prodotto. Viene utilizzato per assegnare e annullare l’assegnazione delle origini e per gestire la quantità e la disponibilità del prodotto. Questa sezione viene visualizzata solo se per lo store sono definite più origini. Per ulteriori informazioni sulle origini, vedere [Gestione origini](../inventory-management/sources-manage.md).

## Assegnare un&#39;origine per un prodotto

1. Fare clic su **[!UICONTROL Assign Source]**.

1. Selezionare la casella di controllo per le origini richieste.

1. Fare clic su **[!UICONTROL Done]**.

1. Selezionare **[!UICONTROL Source Item Status]** e immettere i valori **[!UICONTROL Qty]** e **[!UICONTROL Notify Qty]** in base alle esigenze.

1. Fare clic su **[!UICONTROL Save]** per salvare le modifiche.

![Visualizzazione origini](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Riferimento campo

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Name] | Nome univoco di un&#39;origine. |
| [!UICONTROL Source Status] | Determina se il prodotto è abilitato o disabilitato nel catalogo. |
| [!UICONTROL Source Item Status] | Determina la disponibilità corrente del prodotto. Opzioni:<br />**[!UICONTROL In Stock]**- Rende il prodotto disponibile per l&#39;acquisto.<br />**[!UICONTROL Out of Stock]** - Se non vengono attivati gli ordini inevasi, impedisce che il prodotto sia disponibile per l&#39;acquisto e rimuove l&#39;inserzione dal catalogo. |
| [!UICONTROL Qty] | Quantità di scorte disponibili per ciascuna origine. |
| [!UICONTROL Notify Qty] | Importo per _Notify per Quantità_ per questa origine specifica se `Notify Quantity Use Default` non è selezionato. |
| [!UICONTROL Notify Qty Use Default] | Indica di utilizzare l&#39;impostazione predefinita per _Notify for Quantity_ nell&#39;impostazione del prodotto Advanced Inventory o globale nella configurazione dell&#39;archivio. Per ulteriori informazioni sulle impostazioni di inventario avanzate per il prodotto, vedere [Configurare le opzioni di prodotto avanzate](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Per un&#39;origine assegnata, fare clic su **[!UICONTROL Unassign]** per rendere l&#39;origine non disponibile per il prodotto. Per un&#39;origine non assegnata, fare clic su **[!UICONTROL Assign Sources]** per rendere disponibile un&#39;origine per il prodotto. Per ulteriori informazioni sulle opzioni [!UICONTROL Assign Sources], vedere [Assegnazione di origini per prodotto](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
