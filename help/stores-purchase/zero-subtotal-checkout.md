---
title: Estrazione subtotale pari a zero
description: Scopri come impostare un subtotale pari a zero come metodo di pagamento offline nel tuo Negozio.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
TQID: https://experienceleague.adobe.com/WCWo0jvFkqHnwLX7QnAcJ1vDs66sdrtpba5hoxd-JKc
product_v2: id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2: id: c1256247-af4b-46d8-9dca-0c654ecfa157id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 347
ht-degree: 0%

---

# Estrazione subtotale pari a zero

_È possibile utilizzare un totale parziale pari a zero_ per gli ordini con un totale parziale pari a zero che vengono tassati dopo l&#39;applicazione di uno sconto. Ad esempio, il checkout del subtotale pari a zero può essere utilizzato nelle situazioni seguenti:

- Uno sconto copre l&#39;intero prezzo dell&#39;acquisto, senza alcun costo aggiuntivo per la spedizione.

- Il cliente aggiunge al carrello un prodotto [scaricabile](../catalog/product-create-downloadable.md) o [virtuale](../catalog/product-create-virtual.md) e il prezzo è uguale a zero.

- Il prezzo di un prodotto [simple](../catalog/product-create-simple.md) è zero ed è disponibile il metodo [spedizione gratuita](shipping-free.md).

- Un [codice coupon](../merchandising-promotions/price-rules-cart-coupon.md) copre l&#39;intero prezzo dei prodotti e della spedizione.

Per risparmiare tempo, è possibile impostare zero ordini di subtotale su fatturazione automatica.

**_Per configurare l&#39;estrazione del subtotale pari a zero:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. In _[!UICONTROL Other Payment Methods]_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) la sezione **[!UICONTROL Zero Subtotal Checkout]**.

   ![Estrazione Subtotale Zero](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare le impostazioni.

1. Per attivare l&#39;estrazione del subtotale zero, impostare **[!UICONTROL Enabled]** su `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi il metodo Subtotale zero durante l&#39;estrazione.

1. Se in genere gli ordini attendono l&#39;approvazione, accettare **[!UICONTROL New Order Status]** come `Pending"` predefinito fino all&#39;approvazione dell&#39;ordine.

   Se si preferisce, è possibile utilizzare lo stato `Processing` o `Suspected Fraud` per i nuovi ordini con questo metodo di pagamento.

1. Impostare **[!UICONTROL Automatically Invoice All Items]** su `Yes` se si desidera fatturare automaticamente tutti gli elementi con saldo pari a zero.

   Questa opzione è disponibile solo se l&#39;opzione **[!UICONTROL New Order Status]** è impostata su `Processing`.

   >[!NOTE]
   >
   >Se _[!UICONTROL New Order Status]_è impostato su `Processing` e_[!UICONTROL Automatically Invoice All Items]_ è impostato su `No`, è necessario assegnare anche **[!UICONTROL Order Status]** = `Processing` per il mapping **[!UICONTROL Order State]** = `Pending` e **[!UICONTROL Default Status]** = `No` nella pagina [Stato ordine](order-status.md#custom-order-status).

1. Imposta **[!UICONTROL Payment from Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Per **[!UICONTROL Sort Order]**, immettere un numero che determini la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = primo, `1` = secondo, `2` = terzo e così via).

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
