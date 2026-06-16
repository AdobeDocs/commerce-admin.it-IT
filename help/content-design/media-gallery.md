---
title: ' [!DNL Media Gallery]'
description: Utilizzare la Raccolta file multimediali per organizzare e gestire i file multimediali sul server.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
TQID: https://experienceleague.adobe.com/PL80USg-GVh-vlWwoYCuWRzJdO-FzHDFmFSDjxhavo8
product_v2:
  - id: eadea719-cf89-469b-a6fd-a236a7138047
feature_v2:
  - id: dac87252-6066-4d6e-a9d2-f6d84c323de7
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
source-wordcount: 352
ht-degree: 0%

---

# [!DNL Media Gallery]

Con Adobe Commerce o Magento Open Source 2.4, i commercianti possono utilizzare il nuovo _avanzato_ [!DNL Media Gallery] per organizzare e gestire i file multimediali sul server. Questo nuovo [!DNL Media Gallery] contiene le stesse funzionalità dell&#39;archiviazione multimediale esistente, ma include un&#39;interfaccia utente migliorata e un&#39;integrazione più stretta con [Adobe Stock](https://stock.adobe.com).

![Immagini visualizzate nella griglia di Media Gallery](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Le immagini del prodotto aggiunte alla sezione [_[!UICONTROL Images and Videos]_](../catalog/product-image.md#upload-an-image) non sono gestite da [!DNL Media Gallery]. Solo le immagini utilizzate nei campi della sezione prodotto&#x200B;_[!UICONTROL Content]_ vengono visualizzate e filtrate nel nuovo [!DNL Media Gallery].

## Abilita il nuovo [!DNL Media Gallery]

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Configurazione avanzata - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable Old Media Gallery]** su `No`.

1. Fare clic su **[!UICONTROL Save Config]**.

1. Quando richiesto, fare clic sul collegamento **[!UICONTROL Cache Management]** nel messaggio di sistema e aggiornare la cache non valida.

   Il menu [[!UICONTROL Content]](/help/content-design/content-menu.md) visualizza ora la nuova opzione _[!UICONTROL Media Gallery]_.

>[!NOTE]
>
>La funzionalità completa per il nuovo [!DNL Media Gallery] richiede l&#39;avvio dei consumer della coda `media.gallery.synchronization` e `media.content.synchronization` per la sincronizzazione iniziale. Per ulteriori dettagli, vedere [Gestione delle code di messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html?lang=it) nella _Guida alla configurazione_.

## Accedi al nuovo [!DNL Media Gallery]

Il nuovo [!DNL Media Gallery] è accessibile dal menu Contenuto o quando [aggiungi o modifichi una pagina](/help/content-design/page-add.md). Puoi accedervi anche quando [crei o modifichi una categoria](/help/catalog/category-create.md) o quando [inserisci immagini utilizzando l&#39;Editor contenuto](/help/content-design/editor-insert-image.md).

Per accedere al nuovo [!UICONTROL Media Gallery] tramite il menu [!UICONTROL Content]:

- Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Per accedere alla nuova Raccolta multimediale durante l&#39;aggiunta o la modifica di una pagina:

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Fare clic su **[!UICONTROL Add a New Page]**.

   Per modificare una pagina esistente, è possibile utilizzare la colonna _[!UICONTROL Action]_&#x200B;per fare clic su **[!UICONTROL Select]**&#x200B;e scegliere **[!UICONTROL Edit]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL Content]** ed effettuare le seguenti operazioni:

   - Se [Page Builder è abilitato](../page-builder/setup.md), espandere il pannello **[!UICONTROL Media]** e trascinare un segnaposto **[!UICONTROL Image]** nel contenitore di destinazione. Quindi fare clic su **[!UICONTROL Select from Gallery]**.

     ![Trascina immagine nell&#39;area di visualizzazione](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Se l&#39;editor di WYSIWYG [è abilitato](/help/content-design/editor.md), fare clic su **[!UICONTROL Show/Hide Editor]** e quindi su **[!UICONTROL Insert Image]**.

## Demo di [!DNL Media Gallery]

Per ulteriori informazioni su [!DNL Media Gallery], guarda questo video:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12&learn=on)
