---
title: Spedisci un ordine
description: Scopri come completare le informazioni di spedizione per un ordine di elaborazione e visualizzare le informazioni di spedizione e tracciamento.
exl-id: 60b0e66a-8ee6-4091-94ce-179cc2fdf57a
feature: Orders, Shipping/Delivery
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 0%

---

# Spedisci un ordine

Un ordine che è stato pagato, ma è in attesa di spedizione ha il `Processing` stato. Il record di spedizione contiene una cronologia dettagliata del processo di evasione associato all&#39;ordine. Le spedizioni parziali possono essere effettuate fino all&#39;evasione dell&#39;ordine.

1. Il giorno _Amministratore_ barra laterale, seleziona **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. In _[!UICONTROL Orders]_trovare l&#39;ordine da spedire e fare clic per aprirlo.

1. Nell’angolo in alto a destra, fai clic su **[!UICONTROL Ship]** pulsante.

1. Se desideri aggiornare l’indirizzo di fatturazione o di spedizione, fai clic su **[!UICONTROL Edit]** nell’angolo superiore destro della sezione.

   Apporta le modifiche necessarie e fai clic su **[!UICONTROL Save Order Address]**.

1. Per fare in modo che il vettore generi un&#39;etichetta di spedizione, selezionare **[!UICONTROL Create Shipping Label]** e impostare le opzioni:

   - Per aggiungere un numero di tracciamento, scorri verso il basso fino al _[!UICONTROL Shipping Information]_e fai clic su **[!UICONTROL Add Tracking Number]**.

   - Effettuare una delle seguenti operazioni:

      - Seleziona la **[!UICONTROL Carrier]** e inserisci il tracciamento **[!UICONTROL Number]**.

      - Imposta **[!UICONTROL Carrier]** a `Custom Value`, immetti un **[!UICONTROL Title]** per il vettore personalizzato e inserire il tracciamento **[!UICONTROL Number]**.

      - [Visualizza informazioni di tracciamento](#track-the-shipment).

1. Per effettuare una spedizione parziale, scorrere verso il basso fino alla sezione Articoli da spedire e inserire **[!UICONTROL Qty to Ship]** per ogni elemento.

1. Per notificare la spedizione ai clienti via e-mail, effettuare le seguenti operazioni:

   - Inserisci eventuali commenti da includere nel **[!UICONTROL Shipment Comments]** casella.

   - Per includere i commenti nell’e-mail di notifica inviata al cliente, seleziona la **[!UICONTROL Append Comments]** casella di controllo.

   - Per inviare una copia dell&#39;e-mail di spedizione, selezionare **[!UICONTROL Email Copy of Shipment]** casella di controllo.

     Lo stato di un&#39;e-mail di fattura viene visualizzato accanto al numero della fattura completata come inviata o non inviata.

1. Al termine, fai clic su **[!UICONTROL Submit Shipment]**.

   Lo stato dell’ordine cambia da `Processing` a `Complete`.

>[!NOTE]
>
>Se un ordine viene effettuato come &quot;consegna in-store&quot;, le opzioni di spedizione non sono disponibili. Clic **[!UICONTROL Notify Order is Ready for Pickup]** per attivare un’e-mail al cliente. Lo stato dell’ordine viene quindi modificato in `Complete`.

## Visualizza i dettagli della spedizione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Individuare la spedizione nell&#39;elenco e fare clic per aprire il record.

1. Se desideri aggiungere un commento all’ordine, scorri verso il basso fino a _[!UICONTROL Comments History]_e immettere il commento nella casella.

   - Per inviare il commento al cliente tramite e-mail, seleziona la **[!UICONTROL Notify Customer by Email]** casella di controllo.

   - Per pubblicare il commento nell’account del cliente, seleziona la **[!UICONTROL Visible on Frontend]** casella di controllo.

1. Clic **[!UICONTROL Submit Comment]**.

## Tracciare la spedizione

**Metodo 1:** Scheda Informazioni ordine - Da

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > **[!UICONTROL Orders]**.

1. Individuare l&#39;ordine di spedizione nella griglia e fare clic su **[!UICONTROL View]**.

1. Scorri verso il basso fino a _[!UICONTROL Shipping & Handling Information]_e fai clic su **[!UICONTROL Track Order]**.

   Tutte le informazioni di tracciamento disponibili vengono visualizzate in una finestra popup.

1. Quando è pronto, fai clic su **[!UICONTROL Close Window]**.

**Metodo 2:** Dalla scheda spedizione ordine

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Sales]** > **[!UICONTROL Shipments]**.

1. Individuare la spedizione nell&#39;elenco e fare clic per aprire il record.

1. Clic **[!UICONTROL Track this Shipment]**.

   Tutte le informazioni di tracciamento disponibili vengono visualizzate in una finestra popup.

1. Quando è pronto, fai clic su **[!UICONTROL Close Window]**.
