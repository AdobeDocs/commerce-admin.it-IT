---
title: URL Dynamic Media
description: Scopri come utilizzare un URL di elementi multimediali dinamici come riferimento relativo a un’immagine o a un’altra risorsa multimediale.
exl-id: 41aabde2-f6cc-4b83-8d56-9753a7aa93e9
feature: CMS, Media
source-git-commit: d3b9b4cd0d12f8d5feb2bad0bf601970f9ee1a36
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# URL Dynamic Media

Un URL di elementi multimediali dinamici è un riferimento relativo a un’immagine o a un’altra risorsa multimediale. Se questa opzione è abilitata, gli URL di elementi multimediali dinamici possono essere utilizzati per collegarsi direttamente alle risorse sul server o ai file archiviati in un [rete di distribuzione dei contenuti](media-storage-content-delivery-network.md). L’utilizzo degli URL di elementi multimediali dinamici può influire sulle prestazioni del catalogo e [editor](editor.md#configure-the-editor) può essere configurato per l’utilizzo di URL di elementi multimediali statici o dinamici.

Come per tutti [tag di markup](../systems/markup-tags.md), la direttiva è racchiusa tra parentesi graffe. Il formato di un URL di Dynamic Media è simile al seguente:

`\{\{media url="path/to/image.jpg"}}`

Le direttive URL dinamiche vengono elaborate dal contenuto HTML salvato quando la pagina viene sottoposta a rendering nella vetrina. Ogni volta che viene eseguito il rendering della pagina, il contenuto viene analizzato per `\{\{media url="..."}}` e ogni direttiva viene sostituita con l’URL del file multimediale corrispondente.

{{$include /help/_includes/directives-caution.md}}

## Configurare gli URL dei file multimediali statici

Per impostazione predefinita, le immagini inserite nel catalogo dall’editor WYSIWYG hanno URL relativi e dinamici. Se preferisci utilizzare un URL statico, puoi modificare l’impostazione di configurazione.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL WYSIWYG Options]** sezione.

   ![Opzioni WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Use Static URLs for Media Content in WYSIWYG]** a uno dei seguenti elementi:

   - `Yes` : utilizza URL statici per i contenuti multimediali inseriti con l’editor WYSIWYG. Gli URL statici sono assoluti e si interrompono se [URL di base](../stores-purchase/store-urls.md) dell&#39;archivio cambia.

   - `No` - (Impostazione predefinita) Utilizza URL dinamici per i contenuti multimediali inseriti con l’editor WYSIWYG, in base al `\{\{media url="..."}}` direttiva. Gli URL dinamici sono relativi e non si interrompono se l’URL di base dell’archivio cambia.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
