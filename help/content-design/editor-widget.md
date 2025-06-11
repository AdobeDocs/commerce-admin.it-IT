---
title: Inserire un widget nell’editor
description: Aggiungi vari elementi di contenuto a una pagina utilizzando lo strumento widget nell’editor di WYSIWYG.
exl-id: bbc5e059-06d8-4dda-89a7-6c9826b73fd3
badgePaas: label="Solo PaaS" type="Informative" url="https://experienceleague.adobe.com/it/docs/commerce/user-guides/product-solutions" tooltip="Applicabile solo ai progetti Adobe Commerce on Cloud (infrastruttura PaaS gestita da Adobe) e ai progetti on-premise."
source-git-commit: 57a913b21f4cbbb4f0800afe13012ff46d578f8e
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---

# Inserire un widget nell’editor

Lo strumento [widget](widget-create.md) può essere utilizzato per aggiungere vari elementi di contenuto alla pagina, inclusi collegamenti a qualsiasi pagina di contenuto Commerce o a qualsiasi nodo, prodotto o categoria. I collegamenti possono essere posizionati sulla pagina in formato blocco o incorporati direttamente nel contenuto. È possibile utilizzare lo strumento Widget per creare collegamenti ai seguenti tipi di contenuto:

- [Pagine contenuto](pages.md)
- [Categorie catalogo](../catalog/categories.md)
- [Catalogo prodotti](../catalog/product-create.md)

Per impostazione predefinita, i collegamenti ereditano il proprio stile dal foglio di stile del tema.

{{$include /help/_includes/directives-caution.md}}

1. Apri una pagina, un blocco o un blocco dinamico in modalità di modifica.

1. Andare alla sezione _[!UICONTROL Content]_&#x200B;e fare clic su qualsiasi elemento che supporta l&#39;editor.

1. Posizionare il cursore nel punto in cui si desidera visualizzare il widget e fare clic sull&#39;icona _Inserisci widget_.

   ![Barra degli strumenti dell&#39;editor - Inserisci widget](./assets/editor-toolbar-widget-button.png){width="700" zoomable="yes"}

   Se Page Builder non è abilitato e si preferisce utilizzare il codice, fare clic su **[!UICONTROL Show / Hide Editor]**. Posizionate il punto di inserimento nel testo nel punto in cui desiderate visualizzare il widget. Quindi fare clic su **[!UICONTROL Insert Widget]**.

1. Scegliere **[!UICONTROL Widget Type]**.

   Per ulteriori informazioni su queste opzioni, vedere [Tipi di widget](widgets.md#widget-types). Nei passaggi seguenti viene utilizzato un esempio per inserire un collegamento a un prodotto.

1. Per utilizzare il nome del prodotto, lasciare vuoto il campo **[!UICONTROL Anchor Custom Text]**.

1. Immetti **[!UICONTROL Anchor Custom Title]** come best practice per l&#39;ottimizzazione SEO (Search Engine Optimization).

   Questo titolo non è visibile sulla pagina.

1. Imposta **[!UICONTROL Template]** su uno dei seguenti:

   - Per incorporare il collegamento nel testo, selezionare `Product Link Inline Template`.

   - Per posizionare il collegamento su una riga separata, selezionare `Product Link Block Template`.

1. Fare clic su **[!UICONTROL Select Product]** ed effettuare le seguenti operazioni:

   - Nella struttura passare alla categoria desiderata.

   - Nell’elenco, scegli il prodotto collegato.

1. Fare clic su **[!UICONTROL Insert Widget]** per inserire il collegamento nella pagina.

   Se si utilizza il codice HTML, nella parte superiore della pagina verrà visualizzato un tag [markup](../systems/markup-tags.md) per il collegamento, racchiuso tra parentesi graffe. Se necessario, utilizzare _Taglia e incolla_ per posizionare il tag di markup nel codice nel punto in cui si desidera visualizzare il collegamento.

1. Al termine delle modifiche apportate al contenuto, fare clic su **[!UICONTROL Save]**.
