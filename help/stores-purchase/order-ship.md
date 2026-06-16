---
title: Spedisci un ordine
description: Scopri come completare le informazioni di spedizione per un ordine di elaborazione e visualizzare le informazioni di spedizione e tracciamento.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
TQID: https://experienceleague.adobe.com/w1MPvqsRVfsRwEcRB5uClGM3vnwAda3sOtkZzuLBKAA
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
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
source-wordcount: 453
ht-degree: 0%

---

# Spedisci un ordine

Un ordine che è stato pagato, ma è in attesa di spedizione ha lo stato `Processing`. Il record di spedizione contiene una cronologia dettagliata del processo di evasione associato all&#39;ordine. Le spedizioni parziali possono essere effettuate fino all&#39;evasione dell&#39;ordine.

1. Nella barra laterale _Admin_, selezionare **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Nell&#39;elenco _[!UICONTROL Orders]_&#x200B;trovare l&#39;ordine da spedire e fare clic per aprirlo.

1. Nell&#39;angolo superiore destro fare clic sul pulsante **[!UICONTROL Ship]**.

1. Per aggiornare l&#39;indirizzo di fatturazione o di spedizione, fare clic sul collegamento **[!UICONTROL Edit]** nell&#39;angolo superiore destro della sezione.

   Apportare le modifiche necessarie e fare clic su **[!UICONTROL Save Order Address]**.

1. Per fare in modo che il vettore generi un&#39;etichetta di spedizione, selezionare la casella di controllo **[!UICONTROL Create Shipping Label]** e impostare le opzioni:

   - Per aggiungere un numero di tracciamento, scorrere verso il basso fino alla sezione _[!UICONTROL Shipping Information]_&#x200B;e fare clic su **[!UICONTROL Add Tracking Number]**.

   - Effettuare una delle seguenti operazioni:

      - Seleziona **[!UICONTROL Carrier]** e immetti il tracciamento **[!UICONTROL Number]**.

      - Imposta **[!UICONTROL Carrier]** su `Custom Value`, immetti **[!UICONTROL Title]** per il gestore personalizzato e immetti il tracciamento **[!UICONTROL Number]**.

      - [Visualizza informazioni di tracciamento](#track-the-shipment).

1. Per effettuare una spedizione parziale, scorrere verso il basso fino alla sezione Articoli da spedire e immettere **[!UICONTROL Qty to Ship]** per ciascun articolo.

1. Per notificare la spedizione ai clienti via e-mail, effettuare le seguenti operazioni:

   - Immettere i commenti da includere nella casella **[!UICONTROL Shipment Comments]**.

   - Per includere i commenti nell&#39;e-mail di notifica inviata al cliente, selezionare la casella di controllo **[!UICONTROL Append Comments]**.

   - Per inviare una copia dell&#39;e-mail di spedizione, selezionare la casella di controllo **[!UICONTROL Email Copy of Shipment]**.

     Lo stato di un&#39;e-mail di fattura viene visualizzato accanto al numero della fattura completata come inviata o non inviata.

1. Al termine, fare clic su **[!UICONTROL Submit Shipment]**.

   Lo stato dell&#39;ordine cambia da `Processing` a `Complete`.

>[!NOTE]
>
>Se un ordine viene effettuato come &quot;consegna in-store&quot;, le opzioni di spedizione non sono disponibili. Fare clic su **[!UICONTROL Notify Order is Ready for Pickup]** per attivare un&#39;e-mail al cliente. Lo stato dell&#39;ordine viene quindi modificato in `Complete`.

## Visualizza i dettagli della spedizione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Individuare la spedizione nell&#39;elenco e fare clic per aprire il record.

1. Se si desidera aggiungere un commento all&#39;ordine, scorrere verso il basso fino alla sezione _[!UICONTROL Comments History]_&#x200B;e immettere il commento nella casella.

   - Per inviare il commento al cliente tramite e-mail, selezionare la casella di controllo **[!UICONTROL Notify Customer by Email]**.

   - Per pubblicare il commento nell&#39;account del cliente, selezionare la casella di controllo **[!UICONTROL Visible on Frontend]**.

1. Fare clic su **[!UICONTROL Update]**.

## Tracciare la spedizione

**Metodo 1:** dalla scheda Informazioni ordine

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Trovare l&#39;ordine di spedizione nella griglia e fare clic su **[!UICONTROL View]**.

1. Scorri verso il basso fino alla sezione _[!UICONTROL Shipping & Handling Information]_&#x200B;e fai clic su **[!UICONTROL Track Order]**.

   Tutte le informazioni di tracciamento disponibili vengono visualizzate in una finestra popup.

1. Al termine, fare clic su **[!UICONTROL Close Window]**.

**Metodo 2:** dalla scheda spedizione ordine

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Individuare la spedizione nell&#39;elenco e fare clic per aprire il record.

1. Fare clic su **[!UICONTROL Track this Shipment]**.

   Tutte le informazioni di tracciamento disponibili vengono visualizzate in una finestra popup.

1. Al termine, fare clic su **[!UICONTROL Close Window]**.
