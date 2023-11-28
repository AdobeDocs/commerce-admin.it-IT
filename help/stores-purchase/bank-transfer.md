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

**_Per configurare i pagamenti con bonifico bancario:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. Sotto _Altri metodi di pagamento_, espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Bank Transfer Payment]** sezione.

   ![Pagamento bonifico](../configuration-reference/sales/assets/payment-methods-bank-transfer-payment.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   >Se necessario, cancellare prima **[!UICONTROL Use system value]** per modificare queste impostazioni.

1. Per attivare i bonifici bancari, impostare **[!UICONTROL Enabled]** a `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi il metodo di pagamento del bonifico bancario durante il pagamento.

1. Imposta **[!UICONTROL New Order Status]** a `Pending` fino all&#39;autorizzazione del pagamento.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione del negozio può utilizzare questo metodo di pagamento.

   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Inserisci il **[!UICONTROL Instructions]** che i vostri clienti devono seguire per impostare un bonifico bancario.

   A seconda del paese in cui si trova la banca e dei requisiti della banca, è possibile includere le seguenti informazioni:

   - Nome conto bancario
   - Numero conto bancario
   - Codice di instradamento bancario
   - Nome banca
   - Indirizzo della banca

1. Imposta **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** agli importi necessari per poter utilizzare questo metodo di pagamento.

   >[!NOTE]
   >
   >Un ordine è qualificato se il totale è compreso tra i valori totali minimi o massimi o corrisponde esattamente a tali valori.

1. Per **[!UICONTROL Sort Order]**, immettere un numero che determini la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
