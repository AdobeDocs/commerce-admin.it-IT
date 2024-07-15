---
title: Editor WYSIWYG
description: Scopri come utilizzare l’editor e lavorare con i contenuti in una visualizzazione _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 0%

---

# Editor WYSIWYG

L&#39;editor consente di immettere e formattare il contenuto mentre si lavora in una visualizzazione _What You See Is What You Get_ (WYSIWYG) del contenuto. Se preferisci lavorare direttamente con il codice HTML sottostante, puoi facilmente cambiare modalità. L&#39;editor può essere utilizzato per creare contenuti per [pagine](pages.md), [blocchi](blocks.md) e [descrizioni prodotto](../catalog/product-content.md). Quando si lavora sui dettagli del prodotto, accedere all&#39;editor facendo clic su **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 è l&#39;editor WYSIWYG predefinito. Un aggiornamento della libreria TinyMCE 5.10 in Adobe Commerce e Magento Open Source 2.4.5 risolve una vulnerabilità che consentiva un’esecuzione arbitraria di JavaScript durante l’aggiornamento di un’immagine o di un collegamento utilizzando alcuni tipi di URL. TinyMCE 3 è stato dichiarato obsoleto nella versione 2.4.0 e rimosso nella versione 2.4.3. TinyMCE 4 è stato rimosso nella versione 2.4.4.

![Barra degli strumenti dell&#39;editor](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Gli argomenti seguenti forniscono informazioni dettagliate sull’utilizzo dell’editor:

- [Inserimento di un collegamento](editor-insert-link.md)
- [Inserimento di un’immagine](editor-insert-image.md)
- [Inserimento di un widget](editor-widget.md)
- [Inserimento di una variabile](editor-insert-variable.md)

## Configurare l’editor

L’editor WYSIWYG è attivato per impostazione predefinita e può essere utilizzato per modificare il contenuto su pagine e blocchi CMS e in prodotti e categorie. Dalla configurazione, puoi attivare o disattivare l&#39;editor e scegliere di utilizzare URL statici, anziché [dinamici](../catalog/catalog-urls.md#dynamic-url), per i contenuti multimediali nelle descrizioni di prodotti e categorie.

![Opzioni WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Per una descrizione dettagliata di tutte le opzioni WYSIWYG, vedere [Gestione contenuto](../configuration-reference/general/content-management.md) nella _Guida di riferimento configurazione_.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Imposta **[!UICONTROL Enable WYSIWYG Editor]** sulla tua preferenza.

   L’editor è attivato per impostazione predefinita.

1. Imposta **[!UICONTROL Static URLs for Media Content in WYSIWYG]** sulle preferenze per tutti i [contenuti multimediali](../catalog/catalog-urls.md#static-url) immessi con l&#39;editor WYSIWYG.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.
