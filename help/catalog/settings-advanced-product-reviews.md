---
title: Impostazioni prodotto - [!UICONTROL Product Reviews]
description: Per un prodotto, le impostazioni [!UICONTROL Product Reviews] consentono di accedere alle revisioni inviate per il prodotto e di modificare lo stato delle revisioni in sospeso.
exl-id: 9328c9f5-dcd4-4837-8902-39dc48cb8151
feature: Catalog Management, Products
TQID: https://experienceleague.adobe.com/GdeAB8bT8WjR9vSGjuD-h5I3O6vYNxyaaUQYAjjy8ME
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c18ed297-2187-4aec-affb-9d9654eca6fcid: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: ccaac3a13a346ce192a724efb3384ef2d612c980
workflow-type: tm+mt
source-wordcount: 212
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

