---
title: Impostazioni prodotto - [!UICONTROL Sources]
description: Per un prodotto, il [!UICONTROL Sources] fornisce l'accesso a [!DNL Inventory Management] origini da cui il prodotto può essere distribuito.
exl-id: 986f6031-0edc-4105-aa02-1c22364b3e7c
feature: Catalog Management, Products, Inventory
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---

# Impostazioni prodotto - [!UICONTROL Sources]

Il _[!UICONTROL Sources]_nelle impostazioni del prodotto sono elencate le origini da cui è possibile distribuire il prodotto. Viene utilizzato per assegnare e annullare l’assegnazione delle origini e per gestire la quantità e la disponibilità del prodotto. Questa sezione viene visualizzata solo se per lo store sono definite più origini. Per ulteriori informazioni sulle origini, consulta [Gestire le origini](../inventory-management/sources-manage.md).

## Assegnare un&#39;origine per un prodotto

1. Clic **[!UICONTROL Assign Source]**.

1. Selezionare la casella di controllo per le origini richieste.

1. Clic **[!UICONTROL Done]**.

1. Seleziona **[!UICONTROL Source Item Status]** e immetti **[!UICONTROL Qty]** e **[!UICONTROL Notify Qty]** valori in base alle esigenze.

1. Clic **[!UICONTROL Save]** per salvare le modifiche.

![Visualizzazione origini](./assets/catalog-sources-list.png){width="600" zoomable="yes"}

## Riferimento campo

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL Name] | Nome univoco di un&#39;origine. |
| [!UICONTROL Source Status] | Determina se il prodotto è abilitato o disabilitato nel catalogo. |
| [!UICONTROL Source Item Status] | Determina la disponibilità corrente del prodotto. Opzioni:<br />**[!UICONTROL In Stock]**- Rende il prodotto disponibile per l&#39;acquisto.<br />**[!UICONTROL Out of Stock]** - Se non vengono attivati gli ordini inevasi, impedisce che il prodotto sia disponibile per l&#39;acquisto e rimuove l&#39;inserzione dal catalogo. |
| [!UICONTROL Qty] | Quantità di scorte disponibili per ciascuna origine. |
| [!UICONTROL Notify Qty] | Un importo per _Notifica per quantità_ per questa origine specifica se `Notify Quantity Use Default` non è selezionato. |
| [!UICONTROL Notify Qty Use Default] | Indica di utilizzare l’impostazione predefinita per _Notifica per quantità_ nell&#39;impostazione Inventario avanzato del prodotto o Globale nella configurazione del negozio. Per ulteriori informazioni sulle impostazioni di inventario avanzate per il prodotto, consulta [Configurare opzioni di prodotto avanzate](../inventory-management/product-options.md). |
| [!UICONTROL Actions] | Per un’origine assegnata, fai clic su **[!UICONTROL Unassign]** per rendere l’origine non disponibile per il prodotto. Per un’origine non assegnata, fai clic su **[!UICONTROL Assign Sources]** per rendere disponibile un&#39;origine per il prodotto. Per ulteriori informazioni su [!UICONTROL Assign Sources] opzioni, vedi [Assegnazione di origini per prodotto](../inventory-management/sources-assign-per-product.md). |

{style="table-layout:auto"}
