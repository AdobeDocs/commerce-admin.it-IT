---
title: Notifica di mancato pagamento
description: Scopri come configurare le comunicazioni e-mail per un metodo di pagamento che non riesce a completare una transazione.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# Notifica di mancato pagamento

Se il metodo di pagamento selezionato durante l&#39;estrazione non riesce a completare la transazione, viene inviata una notifica al contatto del punto vendita o a un utente amministratore designato.

## Passaggio 1: aggiornare il modello e-mail

Assicurati di aver aggiornato il modello e-mail necessario per riflettere il brand. Per un elenco completo dei modelli, consulta [Lista dei Modelli di Email](../systems/email-templates.md#email-template-list).

## Passaggio 2: configurare le e-mail di pagamento non riuscito

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Payment Failed Emails]** sezione.

   ![E-mail per pagamento non riuscito](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Imposta le opzioni per le e-mail con pagamento non riuscito:

   - Imposta **[!UICONTROL Payment Failed Email Sender]** al contatto del punto vendita che viene visualizzato come mittente del messaggio.
   - Imposta **[!UICONTROL Payment Failed Email Receiver]** al contatto dello store che deve ricevere la notifica delle trasmissioni e-mail non riuscite.
   - Imposta **[!UICONTROL Payment Failed Template]** al modello utilizzato per l’e-mail inviata quando il metodo di pagamento non riesce durante il pagamento.

1. Per **[!UICONTROL Send Payment Failed Email Copy To]**, immettere l&#39;indirizzo di posta elettronica di chiunque debba ricevere una copia della notifica di mancato pagamento.

   Se invii una copia a più destinatari, separa ogni indirizzo con una virgola.

1. Imposta **[!UICONTROL Payment Failed Copy Method]** a uno dei seguenti elementi:

   - `Bcc` - Invia una _copia per cortesia cieca_ includendo il destinatario nell’intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
   - `Separate Email` - Invia la copia come e-mail separata.

1. Clic **[!UICONTROL Save Config]**.
