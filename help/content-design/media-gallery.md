---
title: Il [!DNL Media Gallery]
description: Utilizzare la Raccolta file multimediali per organizzare e gestire i file multimediali sul server.
exl-id: bf730e46-70f3-405c-88cf-62d0a3e8634f
feature: Page Content, Media
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# Il [!DNL Media Gallery]

Con Adobe Commerce o Magento Open Source 2.4, i commercianti possono utilizzare il nuovo _migliorato_ [!DNL Media Gallery] per organizzare e gestire i file multimediali sul server. Questo nuovo [!DNL Media Gallery] contiene le stesse funzionalità dello storage multimediale esistente, ma include un&#39;interfaccia utente migliorata e una più stretta integrazione con [Adobe Stock][adobe-stock].

![Immagini visualizzate nella griglia di Media Gallery](./assets/media-gallery-grid.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Immagini dei prodotti aggiunte al [_[!UICONTROL Images and Videos]_sezione prodotto](../catalog/product-image.md#upload-an-image) non sono gestite da [!DNL Media Gallery]. Solo le immagini utilizzate nel_[!UICONTROL Content]_ i campi della sezione prodotto vengono visualizzati e filtrati nel nuovo [!DNL Media Gallery].

## Abilita il nuovo [!DNL Media Gallery]

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Advanced]** e scegli **[!UICONTROL System]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Media Gallery]**.

   ![Configurazione avanzata - [!DNL Media Gallery]](./assets/system-media-gallery.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Enable Old Media Gallery]** a `No`.

1. Clic **[!UICONTROL Save Config]**.

1. Quando richiesto, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema e aggiorna la cache non valida.

   Il [[!UICONTROL Content] menu](/help/content-design/content-menu.md) ora visualizza il nuovo _[!UICONTROL Media Gallery]_opzione.

>[!NOTE]
>
>Funzionalità complete per le nuove [!DNL Media Gallery] richiede `media.gallery.synchronization` e `media.content.synchronization` mettere in coda i consumer per la sincronizzazione iniziale. Consulta [Gestire le code dei messaggi](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) nel _Guida alla configurazione_ per ulteriori dettagli.

## Accedi al nuovo [!DNL Media Gallery]

Il nuovo [!DNL Media Gallery] è accessibile dal menu Contenuto o quando [aggiungere o modificare una pagina](/help/content-design/page-add.md). Puoi accedervi anche quando [creare o modificare una categoria](/help/catalog/category-create.md)o quando [inserire immagini tramite l’Editor di contenuto](/help/content-design/editor-insert-image.md).

Per accedere al nuovo [!UICONTROL Media Gallery] tramite [!UICONTROL Content] menu:

- Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

Per accedere alla nuova Raccolta multimediale durante l&#39;aggiunta o la modifica di una pagina:

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Elements]_>**[!UICONTROL Pages]**.

1. Clic **[!UICONTROL Add a New Page]**.

   Se desideri modificare una pagina esistente, puoi utilizzare _[!UICONTROL Action]_colonna su cui fare clic **[!UICONTROL Select]**e scegli **[!UICONTROL Edit]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** ed effettuare le seguenti operazioni:

   - Se è stato [Page Builder abilitato](../page-builder/setup.md), espandi **[!UICONTROL Media]** e trascina un **[!UICONTROL Image]** segnaposto al contenitore di destinazione. Quindi fai clic su **[!UICONTROL Select from Gallery]**.

     ![Trascina immagine nell&#39;area di visualizzazione](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

   - Se si dispone di [Editor WYSIWYG abilitato](/help/content-design/editor.md), fai clic su **[!UICONTROL Show/Hide Editor]** e quindi fare clic su **[!UICONTROL Insert Image]**.

## [!DNL Media Gallery] demo

Per ulteriori informazioni su [!DNL Media Gallery], guarda questo video:

>[!VIDEO](https://video.tv.adobe.com/v/343785?quality=12)

[adobe-stock]: https://stock.adobe.com

