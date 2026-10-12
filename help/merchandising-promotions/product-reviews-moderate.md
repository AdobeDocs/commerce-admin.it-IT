---
title: Modera recensioni prodotto
description: Scopri come moderare le recensioni dei prodotti per garantire che quelle inviate siano appropriate per la visualizzazione pubblica del tuo store.
exl-id: 90c3e918-f435-4468-b41b-e8044ad14fb0
feature: Merchandising, Products
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: 'https://experienceleague.adobe.com/DGRJr-P9TUQ1TFh4Da1Z4VwrKfWe2rw5wmbwq9IlAFg'
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
    internal-label: Commerce
feature_v2:
  - id: 58c984c2-e237-5c50-9718-500e40d1e82c
    internal-label: Merchandising
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
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
    internal-label: Customer engagement
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
    internal-label: Administration
source-git-commit: acc7571574eb9c7e96911266897350a77913488e
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%
---
# Modera recensioni prodotto

Per le revisioni dei prodotti Commerce, prima di poter essere visualizzata, è necessario approvare una revisione del prodotto inviata. In questo modo le recensioni sono appropriate per visualizzare pubblicamente il tuo negozio. Lo stato di una revisione inviata è `Pending` finché non viene approvata o rifiutata.

## Visualizzare le recensioni dei prodotti in Admin

Per visualizzare tutte le recensioni per un prodotto specifico nell’Admin, effettua le seguenti operazioni:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Individuare il prodotto che si desidera visualizzare e fare clic su **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

1. Nella pagina del prodotto, scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Product Reviews]**.

   In questa griglia è inoltre possibile modificare la revisione specifica facendo clic sul collegamento **[!UICONTROL Edit]** nella colonna _[!UICONTROL Action]_.

## Aggiorna stato per le recensioni

1. Nella barra laterale _Admin_, vai a **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL Pending Reviews]**o **[!UICONTROL All Reviews]**.

1. Nell’elenco, fai clic su una revisione in sospeso per visualizzare i dettagli e modificarli, se necessario.

1. Modifica **[!UICONTROL Status]** in base alla tua valutazione:

   - Per approvare una revisione in sospeso, selezionare `Approved`.

   - Per rifiutare una revisione, selezionare `Not Approved`. Le revisioni non approvate scompaiono dall&#39;elenco della pagina _[!UICONTROL Pending Reviews]_.

   >[!NOTE]
   >
   >Le recensioni con gli stati `Pending` e `Not Approved` non vengono visualizzate nella vetrina.

1. Se applicabile, imposta **[!UICONTROL Visibility]** di una recensione di prodotto per visualizzarla in diverse visualizzazioni dello store.

1. Se necessario, modificare i valori per **[!UICONTROL Detailed Rating]**, **[!UICONTROL Nickname]** e **[!UICONTROL Summary of Review]**.

   Per modificare la visualizzazione archivio in cui è disponibile una revisione, scegliere la visualizzazione archivio necessaria nella colonna _[!UICONTROL Visibility]_.

   ![Modifica pagina di revisione](./assets/edit-review-page.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Review]**.

## Aggiornamento batch

Puoi aggiornare o eliminare più recensioni contemporaneamente:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**.

1. Seleziona le recensioni da aggiornare.

1. Utilizza il selettore _[!UICONTROL Action]_in alto a sinistra per applicare un&#39;azione.

1. Fai clic su **[!UICONTROL Submit]**

## Eliminare una recensione di prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Marketing]** > _[!UICONTROL User Content]_>**[!UICONTROL All Reviews]**.

1. Trova la recensione del prodotto da eliminare e aprila in modalità di modifica.

1. Nella barra dei menu fare clic sul pulsante **[!UICONTROL Delete Review]**.

1. Per confermare l&#39;azione, fare clic su **[!UICONTROL OK]**.

## Barra dei pulsanti

| Pulsante | Descrizione |
|----------|--------------|
| **[!UICONTROL Back]** | Torna alla pagina Recensioni senza salvare le modifiche |
| **[!UICONTROL Delete Review]** | Elimina la revisione |
| **[!UICONTROL Reset]** | Ripristina i valori precedenti delle modifiche non salvate nel modulo di revisione |
| **[!UICONTROL Previous]** | Apre la revisione precedente |
| **[!UICONTROL Next]** | Apre la revisione successiva |
| **[!UICONTROL Save and Previous]** | Salva le modifiche correnti e apre la revisione precedente. Questo pulsante viene visualizzato se sono presenti altre recensioni. |
| **[!UICONTROL Save and Next]** | Salva le modifiche correnti e apre la visualizzazione successiva. Questo pulsante viene visualizzato se sono presenti altre recensioni. |
| **[!UICONTROL Save Review]** | Salva le modifiche e chiude la pagina di modifica della revisione |
