---
title: Editor WYSIWYG
description: Scopri come utilizzare l’editor e lavorare con i contenuti in una visualizzazione _What You See Is What You Get_ (WYSIWYG).
exl-id: 209ca9d6-973c-4ad9-b7cd-4fba58dbfbb8
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 0%

---

# Editor WYSIWYG

L’editor consente di inserire e formattare mentre si lavora in un _Quello Che Vedi È Quello Che Ottieni_ (WYSIWYG). Se preferisci lavorare direttamente con il codice HTML sottostante, puoi facilmente cambiare modalità. L’editor può essere utilizzato per creare contenuti per [pagine](pages.md), [blocchi](blocks.md), e [descrizioni dei prodotti](../catalog/product-content.md). Quando lavori sui dettagli del prodotto, accedi all’editor facendo clic su **[!UICONTROL Show / Hide Editor]**.

>[!NOTE]
>
>TinyMCE 5 è l&#39;editor WYSIWYG predefinito. Un aggiornamento della libreria TinyMCE 5.10 in Adobe Commerce e Magento Open Source 2.4.5 risolve una vulnerabilità che consentiva l’esecuzione arbitraria di JavaScript durante l’aggiornamento di un’immagine o di un collegamento utilizzando alcuni tipi di URL. TinyMCE 3 è stato dichiarato obsoleto nella versione 2.4.0 e rimosso nella versione 2.4.3. TinyMCE 4 è stato rimosso nella versione 2.4.4.

![Barra degli strumenti dell’editor](./assets/editor-toolbar.png){width="700" zoomable="yes"}

Gli argomenti seguenti forniscono informazioni dettagliate sull’utilizzo dell’editor:

- [Inserimento di un collegamento](editor-insert-link.md)
- [Inserimento di un’immagine](editor-insert-image.md)
- [Inserimento di un widget](editor-widget.md)
- [Inserimento di una variabile](editor-insert-variable.md)

## Configurare l’editor

L’editor WYSIWYG è attivato per impostazione predefinita e può essere utilizzato per modificare il contenuto su pagine e blocchi CMS e in prodotti e categorie. Dalla configurazione, puoi attivare o disattivare l’editor e scegliere di utilizzare statico, anziché [dinamico](../catalog/catalog-urls.md#dynamic-url), URL per il contenuto multimediale nelle descrizioni di prodotti e categorie.

![Opzioni WYSIWYG](./assets/content-management-wysiwyg-options.png){width="600" zoomable="yes"}

Per una descrizione dettagliata di tutte le opzioni WYSIWYG, vedi [Gestione dei contenuti](../configuration-reference/general/content-management.md) nel _Riferimento configurazione_.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL WYSIWYG Options]**.

1. Imposta **[!UICONTROL Enable WYSIWYG Editor]** secondo le tue preferenze.

   L’editor è attivato per impostazione predefinita.

1. Imposta **[!UICONTROL Static URLs for Media Content in WYSIWYG]** alle tue preferenze per tutti [contenuti multimediali](../catalog/catalog-urls.md#static-url) immesso con l’editor WYSIWYG.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.
