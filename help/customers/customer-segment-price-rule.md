---
title: Segmenti di clienti nelle regole di prezzo
description: Scopri come associare i segmenti dei clienti a una regola di prezzo del carrello per definire promozioni mirate per il tuo negozio.
exl-id: eaa04e7a-c0f9-4f09-8e65-75965ccbdc69
feature: Customers, Configuration, Price Rules
TQID: https://experienceleague.adobe.com/MSMNikJwG2lQuLlQxnK82zjCOeF-u8JEjmabKFJgpZU
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 232
ht-degree: 0%

---

# Segmenti di clienti nelle regole di prezzo

{{ee-feature}}

Un segmento di clienti può essere utilizzato per promozioni mirate associandolo a una [regola prezzo carrello](../merchandising-promotions/price-rules-cart.md).

![Regola prezzo carrello - segmento cliente di destinazione](assets/price-rule-cart-condition-segments.png){width="700" zoomable="yes"}

_&#x200B;**Per associare un segmento a una regola prezzo carrello:**&#x200B;_

1. Nella barra laterale _Amministratore_, passa a **[!UICONTROL Marketing]** > _Promozioni_ > **[!UICONTROL Cart Price Rules]**.

1. Apri una regola nuova o esistente:

   * Per utilizzare una nuova regola, fare clic su **[!UICONTROL Add New Rule]** nell&#39;angolo superiore destro.
   * Per utilizzare una regola esistente, fai clic sulla regola nell’elenco per aprirla in modalità di modifica.

1. Scorri verso il basso ed espandi la sezione **[!UICONTROL Conditions]**.

1. Aggiungi la condizione.

   * Fai clic sull&#39;icona _Aggiungi_ (![icona Elenco](../assets/icon-add-green-circle.png)), che visualizza l&#39;elenco delle condizioni. Quindi, scegliere **[!UICONTROL Customer Segment]**.

   ![Regola prezzo carrello - aggiungi condizione segmento cliente](assets/condition-customer-segment.png){width="600" zoomable="yes"}

   Per impostazione predefinita, la condizione è impostata per trovare una condizione corrispondente. Se necessario, fare clic sul collegamento **[!UICONTROL matches]** e modificare l&#39;operatore in uno dei seguenti modi:

   * `does not match`
   * `is one of`
   * `is not one of`

   ![Operatore condizione](assets/price-rule-condition-customer-segment-operator.png){width="600" zoomable="yes"}

1. Per impostare come destinazione un segmento specifico, fare clic sul collegamento Altro **...** per visualizzare ulteriori opzioni. Quindi, fai clic sull&#39;icona _Selettore_ (![icona Elenco](../assets/icon-list-chooser.png)) per visualizzare l&#39;elenco dei segmenti dei clienti.

1. Nell’elenco, seleziona la casella di controllo di ciascun segmento di cui desideri eseguire il targeting con la condizione.

   ![Regola prezzo carrello - elenco selettori condizioni](assets/condition-segment-chooser-list.png){width="600" zoomable="yes"}

1. Fai clic su **[!UICONTROL Select]** per inserire i segmenti cliente selezionati nella condizione.

1. Completare il resto della regola prezzo in base alle esigenze.

1. Al termine, fare clic su **[!UICONTROL Save]**.
