---
title: E-mail di vendita
description: Scopri come configurare le e-mail di vendita per supportare le comunicazioni ai clienti sui loro ordini.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
source-git-commit: 8b5af316ab1d2e632ed5fc2066974326830ab3f7
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---

# E-mail di vendita

Diversi messaggi e-mail vengono attivati dagli eventi relativi a un ordine e la configurazione è simile. Accertati di identificare il contatto del negozio che viene visualizzato come mittente del messaggio, il modello di e-mail da utilizzare e chiunque debba ricevere una copia del messaggio. Le e-mail di vendita possono essere inviate quando attivate da un evento o da un intervallo predeterminato.

![Configurazione vendite - e-mail di vendita](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Passaggio 1: Aggiornare i modelli e-mail

Assicurati di aggiornare [intestazione e-mail](../systems/email-template-custom.md#header-template) in modo che rispecchi il tuo marchio e gli altri modelli e-mail in base alle esigenze. Per un elenco completo dei modelli, consulta [Modelli e-mail](../systems/email-templates.md).

## Passaggio 2: Scegli il tipo di trasmissione

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales Emails]**.

1. Se necessario, espandere ![Selettore di espansione](../assets/icon-display-expand.png) il  **[!UICONTROL General Settings]** sezione.

   ![Configurazione vendite - Impostazioni generali e-mail vendite](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Per impostazione predefinita, l’invio asincrono è impostato su `Disable`. Per modificare l&#39;impostazione di sistema, deselezionare **[!UICONTROL Use system value]** casella di controllo e impostazione **[!UICONTROL Asynchronous sending]** a uno dei seguenti elementi:

   - `Disable` - Invia e-mail di vendita quando attivato da un evento.
   - `Enable` - Invia e-mail di vendita a intervalli regolari prestabiliti.

   Il supporto Adobe Commerce consiglia di abilitare l’invio asincrono per migliorare le prestazioni di posizionamento dell’ordine. Consulta [Best practice di configurazione per l’elaborazione degli ordini](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html) nella Knowledge Base di supporto di Adobe Commerce.

## Passaggio 3: Completa i dettagli di ogni messaggio e-mail di vendita

1. Se necessario, espandere ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Order]** sezione.

   ![Configurazione vendite - ordine e-mail di vendita](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Verifica che **[!UICONTROL Enabled]** è impostato su `Yes` (impostazione predefinita).

1. Imposta **[!UICONTROL New Order Confirmation Email]** al contatto del punto vendita che viene visualizzato come mittente del messaggio.

1. Imposta **[!UICONTROL New Order Confirmation Template]** al modello utilizzato per l’e-mail inviata ai clienti registrati.

1. Imposta **[!UICONTROL New Order Confirmation Template for Guest]** al modello utilizzato per l’e-mail inviata agli ospiti che non hanno un account con il tuo negozio.

1. Per **[!UICONTROL Send Order Email Copy To]**, immettere l&#39;indirizzo e-mail di tutti coloro che devono ricevere una copia del nuovo indirizzo e-mail dell&#39;ordine.

   Se invii una copia a più destinatari, separa ogni indirizzo con una virgola.

1. Imposta **[!UICONTROL Send Order Email Copy Method]** a uno dei seguenti elementi:

   - `Bcc` - Invia una _copia per cortesia cieca_ includendo il destinatario nell’intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
   - `Separate Email` - Invia la copia come e-mail separata.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Order Comments]** e ripetere questi passaggi.

   ![Configurazione vendite - E-mail di vendita commenti ordine](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Completa la configurazione per i restanti tipi di e-mail di vendita:

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

   Quando richiesto, fare clic su [Gestione cache](../systems/cache-management.md) nel messaggio nella parte superiore dell’area di lavoro e cancella tutte le cache non valide.
