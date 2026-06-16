---
title: Widget Ordini e restituzioni
description: Scopri come utilizzare il widget Ordini e restituzioni per consentire ai clienti di controllare lo stato dei loro ordini, stampare le fatture e tenere traccia delle spedizioni.
exl-id: 1c3948e6-a0de-4ee4-8abf-10ab845a94a7
feature: Page Content, Orders, Returns
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/jWpFWPBwvKr5EnMXdV5-3zAqagGuzPrvOL6-gMiEw-M
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: bd989d82-1e15-4534-88db-f1f51dd77ffa
  - id: c1256247-af4b-46d8-9dca-0c654ecfa157
  - id: d1e21356-0064-4f48-9089-16e3f0dbd2a6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b9626700040bdf9de5aa9a987dec28a08243a9e1
workflow-type: tm+mt
source-wordcount: 382
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

1. Nella sezione _[!UICONTROL Settings]_&#x200B;eseguire le operazioni seguenti:

   - Imposta **[!UICONTROL Type]** su `Orders and Returns`.

   - Scegliere **[!UICONTROL Design Theme]** utilizzato dall&#39;archivio.

1. Fare clic su **[!UICONTROL Continue]**.

1. Nella sezione _[!UICONTROL Storefront Properties]_&#x200B;eseguire le operazioni seguenti:

   - Per **[!UICONTROL Widget Title]**, immettere un titolo descrittivo per il widget.

     Questo titolo è visibile solo dall’amministratore.

   - Per **[!UICONTROL Assign to Store Views]**, selezionare le visualizzazioni dello store in cui è visibile il widget.

     È possibile selezionare una visualizzazione archivio specifica o `All Store Views`. Per selezionare più viste, tenere premuto il tasto Ctrl (PC) o Comando (Mac) e fare clic su ciascuna opzione.

   - (Facoltativo) Per **[!UICONTROL Sort Order]**, immettere un numero per determinare l&#39;ordine di visualizzazione di questo elemento con altri nella stessa parte della pagina. (`0` = primo, `1` = secondo, `3` = terzo e così via).

1. Nella sezione _[!UICONTROL Layout Updates]_, fare clic su **[!UICONTROL Add Layout Update]**&#x200B;ed eseguire le operazioni seguenti:

   - Impostare **[!UICONTROL Display On]** sul tipo di pagina in cui si desidera visualizzare il widget.

   - Per determinare la posizione di visualizzazione del widget sulla pagina, completare le altre informazioni di aggiornamento del layout.

1. Al termine, fare clic su **[!UICONTROL Save]**.

1. Quando viene richiesto di aggiornare la cache, fai clic sul collegamento nel messaggio nella parte superiore della pagina e segui le istruzioni.
