---
title: Impostazioni prodotto - [!UICONTROL Product Reviews]
description: Per un prodotto, le impostazioni [!UICONTROL Product Reviews] consentono di accedere alle revisioni inviate per il prodotto e di modificare lo stato delle revisioni in sospeso.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Impostazioni prodotto - [!UICONTROL Product Reviews]

Nella sezione _[!UICONTROL Product Reviews]_sono elencate tutte le recensioni inviate dai clienti sul prodotto. Questa sezione viene visualizzata con le altre informazioni sul prodotto solo dopo il primo salvataggio di un nuovo prodotto. Per ulteriori informazioni, consulta [Recensioni prodotti](../merchandising-promotions/product-reviews.md).

![Recensioni prodotti](./assets/product-review.png){width="600" zoomable="yes"}

## Riferimento campo

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL ID] | ID numerico univoco generato per la voce di recensione prodotto |
| [!UICONTROL Created] | Data di pubblicazione del riesame |
| [!UICONTROL Status] | Stato revisione (`Pending`, `Approved` o `Not Approved`) |
| [!UICONTROL Title] | Rivedi titolo |
| [!UICONTROL Nickname] | Il nome alternativo dell’utente che ha lasciato la revisione |
| [!UICONTROL Review] | Analisi del prodotto corrente da parte del cliente |
| [!UICONTROL Visibility] | Visibilità nelle recensioni dei negozi |
| [!UICONTROL Type] | Tipo di utente che ha lasciato la revisione (`Guest` o `Customer`) |
| [!UICONTROL Product] | Nome prodotto revisionato |
| [!UICONTROL SKU] | Unità di stoccaggio univoca assegnata al prodotto |
| [!UICONTROL Action] | Apre il prodotto in modalità di modifica |

{style="table-layout:auto"}

## Recensioni moderate per un prodotto specifico

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Individua il prodotto e aprilo in modalità di modifica.

1. Scorri fino alla sezione _[!UICONTROL Product Reviews]_.

1. Fare clic su **[!UICONTROL Edit]** per una revisione del prodotto con stato `Pending` per visualizzare e modificare i dettagli.

1. Imposta lo stato per la revisione:

   - Per approvare una revisione in sospeso, selezionare `Approved`.
   - Per rifiutare una revisione, selezionare `Not Approved`.
   - È possibile ripristinare lo stato di revisione su `Pending` in qualsiasi momento.

1. Al termine, fare clic su **[!UICONTROL Save Review]**.

Le recensioni con gli stati `Pending` e `Not Approved` non vengono visualizzate nella vetrina.
