---
title: Inserire un widget nell’editor
description: Aggiungi vari elementi di contenuto a una pagina utilizzando lo strumento widget nell’editor WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
source-git-commit: b659c7e1e8f2ae9883f1e24d8045d6dd1e90cfc0
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---

# Inserire un widget nell’editor

Il [widget](widget-create.md) Questo strumento può essere utilizzato per aggiungere vari elementi di contenuto alla pagina, inclusi i collegamenti a qualsiasi pagina di contenuto Commerce o nodo, prodotto o categoria. I collegamenti possono essere posizionati sulla pagina in formato blocco o incorporati direttamente nel contenuto. È possibile utilizzare lo strumento Widget per creare collegamenti ai seguenti tipi di contenuto:

- [Pagine contenuto](pages.md)
- [Categorie catalogo](../catalog/categories.md)
- [Catalogo prodotti](../catalog/product-create.md)

Per impostazione predefinita, i collegamenti ereditano il proprio stile dal foglio di stile del tema.

{{$include /help/_includes/directives-caution.md}}

1. Apri una pagina, un blocco o un blocco dinamico in modalità di modifica.

1. Vai a _[!UICONTROL Content]_e fai clic su qualsiasi elemento che supporta l’editor.

1. Posizionare il cursore nel punto in cui si desidera visualizzare il widget e fare clic sul pulsante _Inserisci widget_ icona.

   ![Barra degli strumenti dell’editor - Inserisci widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Se Page Builder non è abilitato e preferisci lavorare con il codice, fai clic su **[!UICONTROL Show / Hide Editor]**. Posizionate il punto di inserimento nel testo nel punto in cui desiderate visualizzare il widget. Quindi, fai clic su **[!UICONTROL Insert Widget]**.

1. Scegli la **[!UICONTROL Widget Type]**.

   Per ulteriori informazioni su queste opzioni, vedi [Tipi di widget](widgets.md#widget-types). Nei passaggi seguenti viene utilizzato un esempio per inserire un collegamento a un prodotto.

1. Per utilizzare il nome del prodotto, lascia **[!UICONTROL Anchor Custom Text]** campo vuoto.

1. Immetti un **[!UICONTROL Anchor Custom Title]** per la migliore pratica SEO (Search Engine Optimization).

   Questo titolo non è visibile sulla pagina.

1. Imposta **[!UICONTROL Template]** a uno dei seguenti elementi:

   - Per incorporare il collegamento nel testo, seleziona `Product Link Inline Template`.

   - Per posizionare il collegamento su una riga separata, selezionare `Product Link Block Template`.

1. Clic **[!UICONTROL Select Product]** ed effettuare le seguenti operazioni:

   - Nella struttura passare alla categoria desiderata.

   - Nell’elenco, scegli il prodotto collegato.

1. Clic **[!UICONTROL Insert Widget]** per inserire il collegamento nella pagina.

   Se utilizzi il codice HTML, un [tag markup](../systems/markup-tags.md) per il collegamento viene visualizzato nella parte superiore della pagina, racchiuso tra parentesi graffe. Se necessario, utilizza _Taglia e incolla_ per posizionare il tag di markup nel codice nel punto in cui si desidera visualizzare il collegamento.

1. Al termine delle modifiche apportate al contenuto, fai clic su **[!UICONTROL Save]**.
