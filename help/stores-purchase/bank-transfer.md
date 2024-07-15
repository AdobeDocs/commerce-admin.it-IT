---
title: Bonifici bancari
description: Scopri come impostare i bonifici bancari come metodo di pagamento offline nel tuo negozio.
exl-id: 34b2163c-2edd-4741-b002-3d8fb561fc78
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---

# Bonifici bancari

Adobe Commerce e Magento Open Source consentono di accettare pagamenti trasferiti da un conto bancario del cliente e versati sul conto bancario dell&#39;esercente.

**_Per configurare i pagamenti dei bonifici bancari:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. In _Altri metodi di pagamento_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) la sezione **[!UICONTROL Bank Transfer Payment]**.

   ![Bonifico bancario](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare le impostazioni.

1. Per attivare i trasferimenti bancari, impostare **[!UICONTROL Enabled]** su `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi il metodo di pagamento del bonifico bancario durante l&#39;estrazione.

1. Impostare **[!UICONTROL New Order Status]** su `Pending` finché il pagamento non viene autorizzato.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.

   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Immetti **[!UICONTROL Instructions]** che i clienti devono seguire per impostare un bonifico bancario.

   A seconda del paese in cui si trova la banca e dei requisiti della banca, è possibile includere le seguenti informazioni:

   - Nome conto bancario
   - Numero conto bancario
   - Codice di instradamento bancario
   - Nome banca
   - Indirizzo della banca

1. Impostare **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** sugli importi necessari per utilizzare questo metodo di pagamento.

   >[!NOTE]
   >
   >Un ordine è qualificato se il totale è compreso tra i valori totali minimi o massimi o corrisponde esattamente a tali valori.

1. Per **[!UICONTROL Sort Order]**, immettere un numero che determini la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = primo, `1` = secondo, `2` = terzo e così via).

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
