---
title: Consegna in contanti (COD)
description: Scopri come impostare il contante alla consegna come metodo di pagamento offline sul tuo negozio.
exl-id: dcf94734-a66e-4d32-b389-b47c979ceaa9
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---

# Consegna in contanti (COD)

Adobe Commerce e il Magento Open Source ti consentono di accettare _pagamenti in contrassegno_ (COD) per gli acquisti. Puoi accettare il pagamento del codice di accesso solo da paesi specifici e perfezionare la configurazione con limiti totali minimi e massimi per gli ordini.

Il vettore di spedizione riceve il pagamento dal cliente al momento della consegna, che viene quindi trasferito al cliente. Puoi effettuare una rettifica per qualsiasi tariffa addebitata dal servizio di trasporto nelle spese di spedizione e imballaggio.

**_Per impostare i pagamenti con contanti:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. In _Altri metodi di pagamento_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) la sezione **[!UICONTROL Cash On Delivery Payment]**.

   ![Pagamento in contanti alla consegna](../configuration-reference/sales/assets/payment-methods-cash-on-delivery-payment.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Pagamento con consegna in contanti](../configuration-reference/sales/payment-methods.md#cash-on-delivery-payment) nella _Guida di riferimento alla configurazione_.

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare le impostazioni.

1. Per attivare il pagamento in contrassegno, impostare **[!UICONTROL Enabled]** su `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi il metodo di pagamento COD durante l&#39;estrazione.

1. Impostare **[!UICONTROL New Order Status]** su `Pending` fino alla conferma della ricezione del pagamento.

   Se si preferisce, è possibile utilizzare lo stato `Processing` o `Suspected Fraud` per i nuovi ordini con questo metodo di pagamento.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Immettere **[!UICONTROL Instructions]** per accettare la consegna di un ordine COD.

1. Impostare **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** sugli importi dell&#39;ordine necessari per il pagamento COD.

   >[!NOTE]
   >
   >Un ordine è qualificato se il totale è compreso tra il totale minimo o massimo dell&#39;ordine oppure se corrisponde a tale totale.

1. Per **[!UICONTROL Sort Order]**, immettere un numero che determini la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = primo, `1` = secondo, `2` = terzo e così via).

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
