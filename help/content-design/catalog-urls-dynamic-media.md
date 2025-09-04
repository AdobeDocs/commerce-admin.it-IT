---
title: URL Dynamic Media
description: Scopri come utilizzare un URL di elementi multimediali dinamici come riferimento relativo a un’immagine o a un’altra risorsa multimediale.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/en/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# URL Dynamic Media

Un URL di elementi multimediali dinamici è un riferimento relativo a un’immagine o a un’altra risorsa multimediale. Se abilitati, gli URL di elementi multimediali dinamici possono essere utilizzati per collegarsi direttamente alle risorse sul server o ai file archiviati in una [rete di distribuzione dei contenuti](media-storage-content-delivery-network.md). L&#39;utilizzo degli URL di elementi multimediali dinamici può influire sulle prestazioni del catalogo e [editor](editor.md#configure-the-editor) può essere configurato per l&#39;utilizzo di URL di elementi multimediali statici o dinamici.

Come per tutti i [tag di markup](../systems/markup-tags.md), la direttiva è racchiusa tra parentesi graffe. Il formato di un URL di Dynamic Media è simile al seguente:

`\{\{media url="path/to/image.jpg"}}`

Le direttive URL dinamiche vengono elaborate dal contenuto HTML salvato quando la pagina viene sottoposta a rendering nella vetrina. Ogni volta che viene eseguito il rendering della pagina, il contenuto viene analizzato per `\{\{media url="..."}}` e ogni direttiva viene sostituita con l&#39;URL del file multimediale corrispondente.

{{$include /help/_includes/directives-caution.md}}

## Configurare gli URL dei file multimediali statici

Per impostazione predefinita, le immagini inserite nel catalogo dall’editor di WYSIWYG hanno URL relativi e dinamici. Se preferisci utilizzare un URL statico, puoi modificare l’impostazione di configurazione.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione **[!UICONTROL WYSIWYG Options]**.

   ![Opzioni WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** su uno dei seguenti:

   - `Yes` - Utilizza URL statici per i contenuti multimediali inseriti con l&#39;editor WYSIWYG. Gli URL statici sono assoluti e si interrompono se l&#39;[URL di base](../stores-purchase/store-urls.md) dell&#39;archivio cambia.

   - `No` - (predefinito) Utilizza URL dinamici per contenuti multimediali inseriti con l&#39;editor di WYSIWYG, in base alla direttiva `\{\{media url="..."}}`. Gli URL dinamici sono relativi e non si interrompono se l’URL di base dell’archivio cambia.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

<!-- Last updated from includes: 2022-08-30 15:36:09 -->
