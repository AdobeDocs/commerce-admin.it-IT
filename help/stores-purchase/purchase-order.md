---
title: Ordini di acquisto
description: Scopri come impostare gli ordini di acquisto come metodo di pagamento offline nel tuo store.
exl-id: 493c1b59-2155-449f-a08a-eb1aa2af9b3e
feature: Purchase Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Ordini di acquisto

Un _ordine di acquisto_ (OA) consente ai clienti commerciali di pagare per gli acquisti autorizzati facendo riferimento al numero dell&#39;ordine di acquisto. L’ordine di acquisto viene autorizzato ed emesso in anticipo dalla società che effettua l’acquisto. Durante il pagamento, il cliente sceglie Ordine di acquisto come metodo di pagamento. Al ricevimento della fattura, la società elabora il pagamento nel sistema di contabilità fornitori e paga l&#39;acquisto.

Prima di accettare il pagamento tramite ordine di acquisto, è necessario verificare sempre la solvibilità del cliente commerciale.

**_Per configurare il pagamento in base all&#39;ordine di acquisto:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. In _[!UICONTROL Other Payment Methods]_, espandere ![Selettore di espansione](../assets/icon-display-expand.png) la sezione **[!UICONTROL Purchase Order]**.

   ![Ordine di acquisto](../configuration-reference/sales/assets/payment-methods-purchase-order.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedere [Ordine di acquisto](../configuration-reference/sales/payment-methods.md#purchase-order) nella _Guida di riferimento alla configurazione_.

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare le impostazioni.

1. Per attivare questo metodo di pagamento, impostare **[!UICONTROL Enabled]** su `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi questo metodo di pagamento durante l&#39;estrazione.

1. Impostare **[!UICONTROL New Order Status]** su `Pending` finché il pagamento non viene autorizzato.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** su uno dei seguenti:

   - `All Allowed Countries` - I clienti di tutti i [paesi](../getting-started/store-details.md#country-options) specificati nella configurazione del tuo negozio possono utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, viene visualizzato l&#39;elenco _[!UICONTROL Payment from Specific Countries]_. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Impostare **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** sugli importi necessari per il metodo di pagamento.

   >[!NOTE]
   >
   >Un ordine è qualificato se il totale è compreso tra i valori totali minimi o massimi o corrisponde esattamente a tali valori.

1. Per **[!UICONTROL Sort Order]**, immettere un numero che determini la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = primo, `1` = secondo, `2` = terzo e così via).

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
