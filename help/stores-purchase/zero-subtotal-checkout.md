---
title: Estrazione subtotale pari a zero
description: Scopri come impostare un subtotale pari a zero come metodo di pagamento offline nel tuo Negozio.
exl-id: c14ce289-8292-41d9-a448-f493c784f35c
feature: Checkout, Configuration
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Estrazione subtotale pari a zero

_Estrazione subtotale pari a zero_ può essere utilizzato per gli ordini con un subtotale pari a zero che vengono tassati dopo l&#39;applicazione di uno sconto. Ad esempio, il checkout del subtotale pari a zero può essere utilizzato nelle situazioni seguenti:

- Uno sconto copre l&#39;intero prezzo dell&#39;acquisto, senza alcun costo aggiuntivo per la spedizione.

- Il cliente aggiunge una [scaricabile](../catalog/product-create-downloadable.md) o [virtuale](../catalog/product-create-virtual.md) al carrello e il prezzo è uguale a zero.

- Il prezzo di un [semplice](../catalog/product-create-simple.md) il prodotto è zero e il valore [spedizione gratuita](shipping-free.md) è disponibile.

- A [codice coupon](../merchandising-promotions/price-rules-cart-coupon.md) copre l&#39;intero prezzo dei prodotti e spedizione.

Per risparmiare tempo, è possibile impostare zero ordini di subtotale su fatturazione automatica.

**_Per configurare l&#39;estrazione del subtotale pari a zero:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. Sotto _[!UICONTROL Other Payment Methods]_, espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Zero Subtotal Checkout]**sezione.

   ![Estrazione subtotale pari a zero](../configuration-reference/sales/assets/payment-methods-zero-subtotal-checkout.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se necessario, cancellare prima **[!UICONTROL Use system value]** per modificare queste impostazioni.

1. Per attivare l&#39;estrazione del subtotale pari a zero, impostare **[!UICONTROL Enabled]** a `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi il metodo Subtotale zero durante l&#39;estrazione.

1. Se gli ordini in genere attendono l’approvazione, accetta l’impostazione predefinita **[!UICONTROL New Order Status]** as `Pending"` fino all’approvazione dell’ordine.

   Se preferisci, puoi utilizzare il `Processing` o `Suspected Fraud` stato dei nuovi ordini con questo metodo di pagamento.

1. Imposta **[!UICONTROL Automatically Invoice All Items]** a `Yes` se si desidera fatturare automaticamente tutti gli articoli con saldo zero.

   Questa opzione è disponibile solo se **[!UICONTROL New Order Status]** è impostata su `Processing`.

   >[!NOTE]
   >
   >Se _[!UICONTROL New Order Status]_è impostato su `Processing` e_[!UICONTROL Automatically Invoice All Items]_ è impostato su `No`, è inoltre necessario assegnare **[!UICONTROL Order Status]** = `Processing` per **[!UICONTROL Order State]** = `Pending` e **[!UICONTROL Default Status]** = `No` mappatura su [Stato ordine](order-status.md#custom-order-status) pagina.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione del negozio può utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Per **[!UICONTROL Sort Order]**, immettere un numero che determini la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
