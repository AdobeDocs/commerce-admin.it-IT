---
title: Ordini rapidi
description: Scopri le funzionalità di ordine rapido e come abilitarle per i clienti.
exl-id: 7007e1b4-a64f-46fe-a235-3ca9f64e77e4
feature: B2B, Orders
source-git-commit: c94d4e8d13c32c1c1b1d37440fdb953c8527b76c
workflow-type: tm+mt
source-wordcount: '438'
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
