---
title: Promozioni omaggio
description: Scopri come configurare una promozione di regali gratuita con le regole di prezzo del carrello per offrire un regalo gratuito quando viene soddisfatta una serie di condizioni.
feature: Merchandising, Price Rules, Shopping Cart, Shipping/Delivery
TQID: https://experienceleague.adobe.com/FR-q4Qj-ZDDzmfEKSvSj-BlwsM7ro-BqAE1yCppTaXE
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: f8a45b24-4be7-4f1b-909b-60d06b483a20
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 3cddc90c619a27b1404e0be7bb4b2c9a3b77e443
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---


# Promozione omaggio

La promozione *Regalo gratuito* ti consente di impostare una [regola prezzo carrello](price-rules-cart.md) che aggiunge un articolo gratuito al carrello in condizioni specifiche.

>[!NOTE]
>
>Questa funzione non è supportata nelle vetrine Luma. È accessibile tramite [GraphQL](https://developer.adobe.com/commerce/webapi/graphql/schema/cart/mutations/select-free-gift/) ed è disponibile nelle vetrine di Edge Delivery Services (EDS).

## Crea una promozione gratuita

Questa sezione descrive come creare una promozione gratuita utilizzando il seguente formato:

**Acquista X prodotto, ottieni il prodotto Y gratuito**

1. [Crea una regola del prezzo del carrello](price-rules-cart.md#step-1-add-a-rule) con una promozione regalo gratuita.

1. [Descrivi le condizioni](price-rules-cart.md#step-2-describe-the-conditions) delle istruzioni del carrello per definire le condizioni per la regola prezzo. Questa è la prima di più condizioni che possono essere aggiunte alla regola e determina quando la regola viene attivata. Può essere basata su una combinazione dei seguenti elementi:

   - Attributi del prodotto
   - Prodotti
   - Attributi del carrello
   - Segmenti di clienti Adobe Commerce

   Se non specificato, la regola viene attivata per ogni carrello.

   ![Regola prezzo carrello - condizioni](./assets/conditions.png){width="600" zoomable="yes"}

1. Definisci le azioni per la regola prezzo carrello:

   1. Espandere  (../assets/icon-display-expand.png) la sezione **[!UICONTROL Actions]** e immettere le informazioni seguenti:

   - Imposta **[!UICONTROL Apply]** su `Free Gift`.
   - In **[!UICONTROL Gift SKU(s)]**, selezionare uno o più SKU che il cliente può scegliere come regalo gratuito.
   - Imposta **[!UICONTROL Free Gift Discount Type]** su **[!UICONTROL Price Based]** o **[!UICONTROL Discount Based]**.
   - In **[!UICONTROL Gift Qty]**, immettere la quantità di regalo gratuito ricevuto dal cliente. Ad esempio, immettere `2` se si desidera che il cliente riceva due articoli gratuiti.
   - Per impedire l&#39;applicazione di altri sconti, impostare **[!UICONTROL Discard subsequent rules]** su `Yes`.

   1. Fare clic su **[!UICONTROL Save and Continue Edit]** e completare il resto della regola in base alle esigenze.

1. [Completare l&#39;etichetta](price-rules-cart.md) delle istruzioni per la regola del prezzo del carrello per immettere l&#39;etichetta visualizzata durante l&#39;estrazione.

![Regola prezzo carrello - Etichetta omaggio](./assets/free-gift-promotion-label.png){width="600" zoomable="yes"}

{{new-price-rule}}

1. Al termine della regola, fare clic su **[!UICONTROL Save Rule]**.

## Varianti

Puoi personalizzare le regole del prezzo del carrello in molti modi diversi. La funzione Regalo gratuito può essere configurata con due diversi tipi di sconto:

- **Basato sul prezzo**: è stato aggiunto un articolo linea regalo al prezzo di `0`.
- **Basato su sconto**: viene applicato uno sconto completo alla voce regalo.
