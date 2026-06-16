---
title: E-mail di vendita
description: Scopri come configurare le e-mail di vendita per supportare le comunicazioni ai clienti sui loro ordini.
exl-id: b205dc61-08cc-4783-810c-686ccf2ba300
feature: Communications, Orders
TQID: https://experienceleague.adobe.com/M9-GhmO0XeRC9sgZmQXpv759NN-5cM92Bd8ZxxM96yg
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 436
ht-degree: 0%

---

# E-mail di vendita

Diversi messaggi e-mail vengono attivati dagli eventi relativi a un ordine e la configurazione è simile. Accertati di identificare il contatto del negozio che viene visualizzato come mittente del messaggio, il modello di e-mail da utilizzare e chiunque debba ricevere una copia del messaggio. Le e-mail di vendita possono essere inviate quando attivate da un evento o da un intervallo predeterminato.

![Configurazione vendite - e-mail vendite](./assets/config-sales-sales-email-full.png){width="600" zoomable="yes"}

## Passaggio 1: Aggiornare i modelli e-mail

Assicurati di aggiornare il modello [intestazione e-mail](../systems/email-template-custom.md#header-template) in modo che rifletta il tuo marchio e gli altri modelli e-mail in base alle esigenze. Per un elenco completo dei modelli, vedere [Modelli e-mail](../systems/email-templates.md).

## Passaggio 2: Scegli il tipo di trasmissione

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales Emails]**.

1. Se necessario, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL General Settings]**.

   ![Configurazione vendite - Impostazioni generali e-mail vendite](../configuration-reference/sales/assets/sales-emails-general-settings.png){width="600" zoomable="yes"}

   Per impostazione predefinita, l&#39;invio asincrono è impostato su `Disable`. Per modificare l&#39;impostazione di sistema, deselezionare la casella di controllo **[!UICONTROL Use system value]** e impostare **[!UICONTROL Asynchronous sending]** su una delle seguenti opzioni:

   - `Disable` - Invia e-mail di vendita quando attivato da un evento.
   - `Enable` - Invia e-mail di vendita a intervalli regolari predeterminati.

   Il supporto Adobe Commerce consiglia di abilitare l’invio asincrono per migliorare le prestazioni di posizionamento dell’ordine. Consulta [Best practice di configurazione per l&#39;elaborazione degli ordini](https://experienceleague.adobe.com/docs/commerce-operations/implementation-playbook/best-practices/maintenance/order-processing-configuration.html?lang=it) nella Knowledge Base di supporto di Adobe Commerce.

## Passaggio 3: Completa i dettagli di ogni messaggio e-mail di vendita

1. Se necessario, espandere ![Selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Order]**.

   ![Configurazione vendite - ordine e-mail vendite](../configuration-reference/sales/assets/sales-emails-order.png){width="600" zoomable="yes"}

1. Verificare che **[!UICONTROL Enabled]** sia impostato su `Yes` (impostazione predefinita).

1. Impostare **[!UICONTROL New Order Confirmation Email]** sul contatto dell&#39;archivio che viene visualizzato come mittente del messaggio.

1. Impostare **[!UICONTROL New Order Confirmation Template]** sul modello utilizzato per l&#39;e-mail inviata ai clienti registrati.

1. Imposta **[!UICONTROL New Order Confirmation Template for Guest]** sul modello utilizzato per l&#39;e-mail inviata agli ospiti che non hanno un account con il tuo store.

1. Per **[!UICONTROL Send Order Email Copy To]**, immettere l&#39;indirizzo di posta elettronica di tutti coloro che devono ricevere una copia del nuovo indirizzo di posta elettronica dell&#39;ordine.

   Se invii una copia a più destinatari, separa ogni indirizzo con una virgola.

1. Imposta **[!UICONTROL Send Order Email Copy Method]** su uno dei seguenti:

   - `Bcc` - Invia una _copia di cortesia cieca_ includendo il destinatario nell&#39;intestazione della stessa e-mail inviata al cliente. Il destinatario Ccn non è visibile al cliente.
   - `Separate Email` - Invia la copia come messaggio e-mail separato.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Order Comments]** e ripetere i passaggi seguenti.

   ![Configurazione vendite - Commenti ordine e-mail vendite](../configuration-reference/sales/assets/sales-emails-order-comments.png){width="600" zoomable="yes"}

1. Completa la configurazione per i restanti tipi di e-mail di vendita:

   - **[!UICONTROL Invoice]** / **[!UICONTROL Invoice Comments]**
   - **[!UICONTROL Shipment]** / **[!UICONTROL Shipment Comments]**
   - **[!UICONTROL Credit Memo]** / **[!UICONTROL Credit Memo Comments]**

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

   Quando richiesto, fare clic sul collegamento [Gestione cache](../systems/cache-management.md) nel messaggio nella parte superiore dell&#39;area di lavoro e cancellare tutte le cache non valide.
