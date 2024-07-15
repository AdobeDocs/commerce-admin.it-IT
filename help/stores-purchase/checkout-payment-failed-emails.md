---
title: Notifica di mancato pagamento
description: Scopri come configurare le comunicazioni e-mail per un metodo di pagamento che non riesce a completare una transazione.
exl-id: c64a4463-64d5-4dad-a8ad-13bfb141b65f
feature: Payments, Communications
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---

# Notifica di mancato pagamento

Se il metodo di pagamento selezionato durante l&#39;estrazione non riesce a completare la transazione, viene inviata una notifica al contatto del punto vendita o a un utente amministratore designato.

## Passaggio 1: aggiornare il modello e-mail

Assicurati di aver aggiornato il modello e-mail necessario per riflettere il brand. Per un elenco completo dei modelli, vedere [Elenco modelli di posta elettronica](../systems/email-templates.md#email-template-list).

## Passaggio 2: configurare le e-mail di pagamento non riuscito

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Payment Failed Emails]**.

   ![E-Mail Di Pagamento Non Riuscite](../configuration-reference/sales/assets/checkout-payment-failed-emails.png){width="600" zoomable="yes"}

1. Imposta le opzioni per le e-mail con pagamento non riuscito:

   - Impostare **[!UICONTROL Payment Failed Email Sender]** sul contatto dell&#39;archivio che viene visualizzato come mittente del messaggio.
   - Impostare **[!UICONTROL Payment Failed Email Receiver]** sul contatto dell&#39;archivio che deve ricevere la notifica delle trasmissioni e-mail non riuscite.
   - Imposta **[!UICONTROL Payment Failed Template]** sul modello utilizzato per l&#39;e-mail inviata quando il metodo di pagamento non riesce durante l&#39;estrazione.

1. Per **[!UICONTROL Send Payment Failed Email Copy To]**, immettere l&#39;indirizzo di posta elettronica di tutti coloro che devono ricevere una copia della notifica di pagamento non riuscito.

   Se invii una copia a più destinatari, separa ogni indirizzo con una virgola.

1. Imposta **[!UICONTROL Payment Failed Copy Method]** su uno dei seguenti:

   - `Bcc` - Invia una _copia di cortesia cieca_ includendo il destinatario nell&#39;intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
   - `Separate Email` - Invia la copia come messaggio e-mail separato.

1. Fare clic su **[!UICONTROL Save Config]**.
