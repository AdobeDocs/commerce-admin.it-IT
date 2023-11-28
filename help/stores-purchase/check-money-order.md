---
title: Assegni e vaglia postali
description: Scopri come impostare assegni e vaglia postale come metodo di pagamento offline sul tuo Negozio.
exl-id: e004f0c3-f659-4b08-a41a-88bfc05acaab
feature: Payments
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Assegni e vaglia postali

Adobe Commerce e Magento Open Source consentono di accettare pagamenti tramite assegno o vaglia postale. Il _Assegno/vaglia postale_ il metodo di pagamento è abilitato per il tuo archivio per impostazione predefinita. È possibile accettare assegni e ordini di pagamento solo da paesi specifici e perfezionare la configurazione con limiti totali minimi e massimi per gli ordini.

**_Per configurare il pagamento tramite assegno o vaglia postale:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Payment Methods]**.

1. Sotto _[!UICONTROL Other Payment Methods]_, espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Check / Money Order]**sezione.

   ![Assegno/vaglia postale](../configuration-reference/sales/assets/payment-methods-check-money-order.png){width="600" zoomable="yes"}

   Per una descrizione dettagliata di ciascuna di queste impostazioni di configurazione, vedi [Assegno/vaglia postale](../configuration-reference/sales/payment-methods.md#check--money-order) nel _Guida di riferimento alla configurazione_.

   >[!NOTE]
   >
   >Se necessario, cancellare prima **[!UICONTROL Use system value]** per modificare queste impostazioni.

1. Per accettare il pagamento tramite assegno o vaglia postale, impostare **[!UICONTROL Enabled]** a `Yes`.

1. Per **[!UICONTROL Title]**, immettere un titolo che identifichi il metodo di pagamento dell&#39;assegno o dell&#39;ordine di pagamento durante il pagamento.

1. Se gli ordini in genere attendono l’approvazione, accetta l’impostazione predefinita **[!UICONTROL New Order Status]** as `Pending"` fino all&#39;approvazione.

   Se preferisci, puoi utilizzare il `Processing` o `Suspected Fraud` stato dei nuovi ordini con questo metodo di pagamento.

1. Imposta **[!UICONTROL Payment from Applicable Countries]** a uno dei seguenti elementi:

   - `All Allowed Countries` - Clienti di tutti [paesi](../getting-started/store-details.md#country-options) specificato nella configurazione del negozio può utilizzare questo metodo di pagamento.
   - `Specific Countries` - Dopo aver scelto questa opzione, il _[!UICONTROL Payment from Specific Countries]_viene visualizzato. Per selezionare più paesi, tenere premuto il tasto Ctrl (PC) o il tasto Comando (Mac) e fare clic su ciascuna opzione.

1. Per **[!UICONTROL Make Check Payable To]**, inserire il nome della parte a cui deve essere dovuto l&#39;assegno.

1. Per **[!UICONTROL Send Check To]**, inserire l&#39;indirizzo postale o la casella postale in cui vengono inviati i controlli.

1. Imposta **[!UICONTROL Minimum Order Total]** e **[!UICONTROL Maximum Order Total]** agli importi degli ordini necessari per qualificarsi per questo metodo di pagamento.

   >[!NOTE]
   >
   >Un ordine è qualificato se il totale è compreso tra i valori totali minimi o massimi o corrisponde esattamente a tali valori.

1. Per **[!UICONTROL Sort Order]**, immettere un numero che determini la posizione di questo elemento nell&#39;elenco dei metodi di pagamento visualizzato durante l&#39;estrazione.

   Questo numero è relativo agli altri metodi di pagamento. (`0` = innanzitutto, `1` = secondo, `2` = terzo e così via.)

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
