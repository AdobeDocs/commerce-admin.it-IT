---
title: Crea un ordine
description: Scopri come creare un ordine per un cliente in Commerce Admin.
exl-id: 8a766a5b-55d6-4d78-859e-38937e0183d3
feature: Orders, Customer Service
TQID: https://experienceleague.adobe.com/0TUx-cDuonSkm4G0zWaU95ZKDuB-yhPb0aaEW57K-3g
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
source-wordcount: 376
ht-degree: 0%

---

# Crea un ordine

Per i clienti registrati che necessitano di assistenza, puoi creare un intero ordine direttamente dall’Amministratore. Il modulo _[!UICONTROL Create New Order]_&#x200B;include tutte le informazioni necessarie per il normale processo di pagamento, con i riepiloghi attività dal dashboard account del cliente.

![Crea un ordine per un cliente](./assets/create-new-order.png){width="700" zoomable="yes"}

## Passaggio 1: creare un ordine

1. Nella barra laterale _Admin_, fai clic su **[!UICONTROL Customers]**.

1. Individuare il cliente nella griglia.

1. Nella colonna _Azione_ fare clic su **[!UICONTROL Edit]**.

1. Nell&#39;intestazione dell&#39;area di lavoro fare clic su **[!UICONTROL Create Order]**.

   ![Intestazione Workspace](./assets/order-create-buttons.png){width="700" zoomable="yes"}

   Puoi anche creare un ordine nell&#39;[Area di lavoro ordini](orders.md#orders-workspace) facendo clic su **[!UICONTROL Create New Order]**.

## Passaggio 2: Aggiungere prodotti

Se il tuo Negozio ha più visualizzazioni, scegli la visualizzazione del Negozio in cui deve essere effettuato l’ordine.

### Aggiungi prodotti dalla barra laterale [!UICONTROL Customer's Activities]

Puoi trasferire gli articoli nel carrello dalla lista dei desideri di un cliente o da qualsiasi articolo visualizzato di recente, confrontato o ordinato.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) in una delle sezioni seguenti:

   - **[!UICONTROL Wish List]**
   - **[!UICONTROL Last Ordered Items]**
   - **[!UICONTROL Products in Comparison List]**
   - **[!UICONTROL Recently Compared Products]**
   - **[!UICONTROL Recently Viewed Products]**

1. Seleziona la casella di controllo di ciascun prodotto nel pannello a sinistra.

1. Scorrere verso il basso e fare clic su **[!UICONTROL Update Changes]**.

   L&#39;elemento viene visualizzato nel modulo d&#39;ordine.

   ![Aggiungi al carrello](./assets/create-order-add-wishlist.png){width="600" zoomable="yes"}

### Aggiungi prodotti dal catalogo

1. Fare clic su **[!UICONTROL Add Products]**.

   ![Aggiungi prodotti](./assets/account-add-wishlist-product.png){width="600" zoomable="yes"}

1. Nella griglia, selezionare la casella di controllo di ciascun prodotto da aggiungere al carrello e immettere **[!UICONTROL Qty]** da acquistare.

   ![Seleziona prodotti](./assets/create-order-from-catalog.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >La griglia di selezione dei prodotti mostra sempre i prezzi base regolari per i prodotti, senza sconti e senza le regole di prezzo applicate al carrello o al gruppo. Il prezzo finale del prodotto viene calcolato solo quando il prodotto viene aggiunto a un ordine/carrello.

1. Configurare le opzioni di prodotto disponibili:

   - Fare clic su **[!UICONTROL Configure]**.

   - Completa le opzioni in base alle esigenze.

   - Fare clic su **[!UICONTROL OK]**.

   - Fare clic su **[!UICONTROL Add Selected Product(s) to Order]** per aggiornare il carrello.

1. Se un prodotto è configurato per [opzioni regalo](../catalog/product-gift-options.md), impostare le opzioni in base alle esigenze.

1. Sostituisci il prezzo di un articolo, se necessario:

   - Selezionare la casella di controllo **[!UICONTROL Custom Price]** e immettere il nuovo prezzo nella casella seguente.

   - Per aggiornare i totali del carrello, fare clic su **[!UICONTROL Update Items and Quantities]**.

   ![Prezzo personalizzato](./assets/create-order-custom-price.png){width="600" zoomable="yes"}

1. Completare le sezioni seguenti in base alle esigenze dell&#39;ordine:

   - [!UICONTROL Order Currency]
   - [!UICONTROL Apply Coupon Codes / Gift Card Code]
   - [!UICONTROL Payment Method]
   - [!UICONTROL Shipping Method]
   - [!UICONTROL Order Comments]
   - [[!UICONTROL [Attributi ordine personalizzati]]](../stores-purchase/order-processing.md#custom-order-attributes)

>[!NOTE]
>
>Per ulteriori informazioni sui metodi di pagamento per supportare questa funzionalità quando l&#39;estensione Payment Services è installata e configurata, vedere la [Guida di Payment Services](https://experienceleague.adobe.com/en/docs/commerce/payment-services/guide-overview).

## Passaggio 3: sottomettere l&#39;ordine

Fare clic su **[!UICONTROL Submit Order]**.

Viene inviata una conferma al cliente che può visualizzare i dettagli dell&#39;ordine dal proprio account.
