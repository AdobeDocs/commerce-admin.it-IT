---
title: Ordini rapidi
description: Scopri le funzionalità di ordine rapido e come abilitarle per i clienti.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
TQID: https://experienceleague.adobe.com/iwH1JStasz7KM-ECeWAvP-x4niVm-QFg4-GMw8r3SoI
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: bd989d82-1e15-4534-88db-f1f51dd77ffaid: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
subfeature_v2: id: f56d26ed-050b-4fb7-b29b-8e6e994e80a2
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 438
ht-degree: 0%

---

# Ordini rapidi

La funzionalità _Ordine rapido_ riduce il processo di ordinazione a diversi clic per i clienti che conoscono il nome del prodotto o lo SKU dei prodotti che desiderano ordinare. Gli ordini con più SKU possono essere immessi manualmente o importati nel modulo Ordine rapido. L’ordine rapido può essere utilizzato dai clienti che hanno effettuato l’accesso ai loro account e dagli ospiti. Se attivato, il collegamento _Ordine rapido_ viene visualizzato nella parte superiore della pagina, accanto al nome del cliente.

![Collegamento per ordine rapido](./assets/quick-order-link.png){width="700" zoomable="yes"}

## Abilita ordini rapidi per il tuo negozio

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nella sezione _[!UICONTROL General]_del pannello a sinistra, scegli **[!UICONTROL B2B Features]**.

1. Imposta **[!UICONTROL Enable Quick Order]** su `Yes`.

   ![Attiva ordine rapido](./assets/quick-orders-config.png){width="600" zoomable="yes"}

1. Fare clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, fare clic su [Gestione cache](../systems/cache-management.md) e aggiornare le cache non valide.

## Flussi di lavoro a ordine rapido

I clienti possono specificare i prodotti per gli ordini rapidi utilizzando uno dei metodi seguenti.

### Metodo 1: inserire i singoli prodotti

1. Il cliente fa clic sul collegamento **[!UICONTROL Quick Order]**.

1. Seleziona il prodotto per SKU o nome prodotto:

   Per effettuare un **ordine rapido per SKU**, il cliente effettua le seguenti operazioni:

   - Immette **[!UICONTROL SKU]**.

   - Clic su **[!UICONTROL Add to List]**.

     Lo SKU viene visualizzato nella riga di input, con i dettagli del prodotto riportati di seguito.

     ![Dettagli ordine rapido](./assets/quick-order-product-detail.png){width="600" zoomable="yes"}

   Per ordinare **rapidamente in base al nome del prodotto**, il cliente effettua le seguenti operazioni:

   - Immette i primi caratteri di **[!UICONTROL Product Name]**.

     >[!NOTE]
     >
     >Non utilizzare il tasto _Invio_ per scegliere il nome del prodotto.

   - Quando viene visualizzato l’elenco delle possibili corrispondenze, il cliente fa clic sul prodotto che desidera ordinare.

     ![Fare clic per scegliere il nome del prodotto](./assets/quick-order-product-name.png){width="700" zoomable="yes"}

1. Immette **[!UICONTROL Qty]**.

1. Utilizzando la riga di input successiva, ripete questo processo il numero di volte necessario.

1. Clic su **[!UICONTROL Add to Cart]**.

### Metodo 2: immettere più prodotti

1. Nella casella **[!UICONTROL Enter Multiple SKUs]** il cliente effettua una delle seguenti operazioni:

   - Immette un SKU per riga

   - Immette tutti gli SKU sulla stessa riga, separati da virgole e senza spazi.

     ![Immettere più SKU](./assets/quick-order-skus.png){width="600" zoomable="yes"}

1. Per aggiungere i prodotti all&#39;elenco, fare clic su **[!UICONTROL Add to List]**.

1. Immette **[!UICONTROL Qty]** da ordinare per ogni elemento dell&#39;elenco.

   ![Elenco ordini rapidi](./assets/quick-order-skus-detail.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se il prodotto dispone delle opzioni richieste, al cliente viene richiesto di scegliere le opzioni. Possono aspettare fino a quando non raggiungono il carrello per aggiungere opzioni di prodotto.

   ![Scegli le opzioni](./assets/quick-order-skus-product-options.png){width="600" zoomable="yes"}

### Metodo 3: Caricare un elenco di prodotti

1. Nella sezione _[!UICONTROL Add from File]_, fare clic su **[!UICONTROL Download Sample]**per scaricare un modello di ordine.

   ![Aggiungi da file](./assets/quick-order-skus-add-from-file.png){width="600" zoomable="yes"}

1. Apre il file scaricato.

1. Utilizza il modello per aggiungere gli SKU del prodotto da caricare per l’elenco degli ordini rapidi.

1. Al termine, fa clic su **[!UICONTROL Save]**.

   ![SKU da caricare](./assets/quick-order-skus-add-from-file-sample.png){width="400" zoomable="yes"}

1. Per caricare il file, fare clic su **[!UICONTROL Choose]** e selezionare il file dal proprio sistema.

   Gli elementi vengono aggiunti all&#39;elenco Ordine rapido.

1. Quando è pronto, fa clic su **[!UICONTROL Add to Cart]**.

Dopo che il cliente ha creato l&#39;ordine rapido, può procedere come di consueto attraverso il pagamento.

![Ordine rapido](./assets/quick-order-add-to-cart.png){width="700" zoomable="yes"}
