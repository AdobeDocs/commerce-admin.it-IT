---
title: Widget Ordini e restituzioni
description: Scopri come utilizzare il widget Ordini e restituzioni per consentire ai clienti di controllare lo stato dei loro ordini, stampare le fatture e tenere traccia delle spedizioni.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 0%

---

# Widget Ordini e restituzioni

Il widget _Ordini e restituzioni_ consente agli ospiti di controllare lo stato degli ordini, stampare le fatture e tenere traccia delle spedizioni. Quando il widget viene aggiunto alla vetrina, è visibile solo per gli ospiti e per i clienti che non hanno effettuato l’accesso ai loro account. Per trovare gli ordini, fornisci l’ID ordine, il Cognome fatturazione e l’Indirizzo e-mail o il CAP.

![Widget Ordini e restituzioni nella barra laterale della vetrina](./assets/storefront-widget-orders-returns-sidebar.png){width="600" zoomable="yes"}

## Widget ordini e restituzioni nella vetrina

1. Il cliente può utilizzare l&#39;opzione **[!UICONTROL Find Order By]** per scegliere uno dei seguenti parametri da utilizzare per trovare l&#39;ordine:

   - Indirizzo e-mail
   - Codice postale

1. Il cliente immette **[!UICONTROL Order ID]** e **[!UICONTROL Billing Last Name]**.

1. Immette la fatturazione **[!UICONTROL Email Address]** o **[!UICONTROL ZIP Code]** associata all&#39;ordine.

1. Fai clic su **[!UICONTROL Search]** per recuperare l&#39;ordine.

   ![Informazioni sull&#39;ordine visualizzate nella vetrina](./assets/storefront-widget-orders-returns-view.png){width="700" zoomable="yes"}

## Impostare il widget Ordini e restituzioni

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Widgets]**.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Widget]**.

1. Nella sezione _[!UICONTROL Settings]_eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Type]** su `Orders and Returns`.

   - Scegliere **[!UICONTROL Design Theme]** utilizzato dall&#39;archivio.

1. Fare clic su **[!UICONTROL Continue]**.

1. Nella sezione _[!UICONTROL Storefront Properties]_eseguire le operazioni seguenti:

   - Per **[!UICONTROL Widget Title]**, immettere un titolo descrittivo per il widget.

     Questo titolo è visibile solo dall’amministratore.

   - Per **[!UICONTROL Assign to Store Views]**, selezionare le visualizzazioni dello store in cui è visibile il widget.

     È possibile selezionare una visualizzazione archivio specifica o `All Store Views`. Per selezionare più viste, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   - (Facoltativo) Per **[!UICONTROL Sort Order]**, immettere un numero per determinare l&#39;ordine di visualizzazione di questo elemento con altri nella stessa parte della pagina. (`0` = primo, `1` = secondo, `3` = terzo e così via).

1. Nella sezione _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**ed eseguire le operazioni seguenti:

   - Impostare **[!UICONTROL Display On]** sul tipo di pagina in cui si desidera visualizzare il widget.

   - Per determinare la posizione di visualizzazione del widget sulla pagina, completare le altre informazioni di aggiornamento del layout.

1. Al termine, fare clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache, fai clic sul collegamento nel messaggio nella parte superiore della pagina e segui le istruzioni.
