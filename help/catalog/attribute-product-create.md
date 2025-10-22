---
title: Creare ed eliminare attributi di prodotto
description: Scopri come creare e rimuovere gli attributi del prodotto, utilizzati per descrivere caratteristiche specifiche dei prodotti nel catalogo.
exl-id: fd0e5d5b-a917-4e55-8ec2-7ebb040d3d06
feature: Catalog Management, Products
source-git-commit: ab91c19cda6a89219fc8946dad4a0a70d0991b38
workflow-type: tm+mt
source-wordcount: '1246'
ht-degree: 0%

---

# Creare ed eliminare attributi di prodotto

È possibile creare attributi mentre si lavora su un prodotto o dalla pagina _[!UICONTROL Product Attributes]_. Nei passaggi seguenti viene illustrato come creare attributi dal menu&#x200B;_[!UICONTROL Stores]_.

## Passaggio 1: descrivere le proprietà dell’attributo di base

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Fare clic su **[!UICONTROL Add New Attribute]**.

   ![Nuove proprietà attributo](./assets/attribute-properties.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Default Label]**, immettere un&#39;etichetta che identifichi l&#39;attributo.

1. Per determinare il tipo di controllo di input utilizzato per l&#39;immissione dei dati, impostare **[!UICONTROL Catalog Input Type for Store Owner]** su uno dei seguenti valori:

   | Proprietà | Descrizione |
   |--- |--- |
   | `Text Field` | Campo di input a riga singola per il testo. |
   | `Text Area` | Campo di input a più righe per l&#39;immissione di paragrafi di testo, ad esempio la descrizione di un prodotto. È possibile utilizzare WYSIWYG Editor per formattare il testo con i tag di HTML o immettere i tag direttamente nel testo. |
   | `Text Editor` | Un editor di testo perfettamente funzionante nella posizione dell’attributo. |
   | Data | Visualizza un valore di data nel [formato preferito](attributes-input-types.md#date-and-time-options) e nel [fuso orario](../getting-started/store-details.md#locale-options). I valori di data possono essere selezionati da un elenco o da un calendario ( ![icona Calendario](../assets/icon-calendar.png) ). <br/><br/>**_Nota:_** A seconda della configurazione del sistema, gli utenti _Amministratore_ possono immettere le date direttamente in un campo o selezionare una data dal calendario o dall&#39;elenco. Per informazioni su come specificare i valori di data e ora, vedere [Opzioni data e ora](attributes-input-types.md#date-and-time-options). |
   | `Yes/No` | Visualizza un elenco a discesa con opzioni predefinite di `Yes` e `No`. |
   | `Dropdown` | Visualizza un elenco a discesa di valori che accetta una sola selezione. Il tipo di input a discesa è un componente chiave di [prodotti configurabili](product-create-configurable.md). |
   | `Multiple Select` | Visualizza un elenco a discesa di valori che accetta selezioni multiple. |
   | `Price` | Questo tipo di input viene utilizzato per creare campi prezzo in aggiunta agli attributi predefiniti: Prezzo, Prezzo speciale, Prezzo livello e Costo. La valuta utilizzata è determinata dalla configurazione del sistema. |
   | `Media Image` | Associa un&#39;immagine aggiuntiva a un prodotto, ad esempio il logo di un prodotto, le istruzioni per la cura o gli ingredienti di un&#39;etichetta di cibo. Quando aggiungi un attributo di immagine multimediale al set di attributi di un prodotto, questo diventa un tipo di immagine aggiuntivo, insieme a Base, Piccola e Miniatura. L&#39;attributo immagine multimediale può essere escluso dal [browser multimediale storefront](catalog-images-video.md#storefront-media-browser). |
   | `Fixed Product Tax` | Consente di definire [tariffe FPT](../stores-purchase/fixed-product-tax.md) in base ai requisiti delle impostazioni internazionali. |
   | `Visual Swatch` | Visualizza un campione che rappresenta il colore, la trama o il motivo di un prodotto configurabile. Un [campione visivo](swatches.md) può essere riempito con un valore di colore esadecimale o visualizzare un&#39;immagine caricata che rappresenta il colore, il materiale, la trama o il modello dell&#39;opzione. |
   | `Text Swatch` | Rappresentazione testuale di un’opzione di prodotto configurabile utilizzata di frequente per le dimensioni. [I campioni di testo](swatches.md#text-based-swatches) possono includere anche valori di colore esadecimali. |
   | `Page Builder` | Un&#39;area di lavoro [Page Builder](../page-builder/introduction.md) perfettamente funzionante nella posizione dell&#39;attributo che consente di aggiungere facilmente contenuto coinvolgente alla pagina del prodotto. |

   {style="table-layout:auto"}

1. Se si desidera richiedere la selezione di un&#39;opzione prima che il cliente possa acquistare il prodotto, impostare **[!UICONTROL Values Required]** su `Yes`.

1. Per i tipi di input [!UICONTROL Dropdown] e [!UICONTROL Multiple Select], eseguire le operazioni seguenti:

   - In _[!UICONTROL Manage Options]_, fare clic su **[!UICONTROL Add Option]**.

   - Immettere il primo valore da visualizzare nell&#39;elenco.

     Puoi immettere un valore per l’amministratore e una traduzione del valore per ogni visualizzazione store. Se disponi di una sola visualizzazione store, puoi immettere solo il valore Admin e viene utilizzato anche per la vetrina.

   - Fare clic su **[!UICONTROL Add Option]** e ripetere il passaggio precedente per ogni opzione da includere nell&#39;elenco.

   - Selezionare **[!UICONTROL Is Default]** per utilizzare l&#39;opzione come valore predefinito.

   ![Attributo prodotto - Opzioni di gestione](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

## Passaggio 2: descrivi le proprietà avanzate (se necessario)

1. Immettere un **[!UICONTROL Attribute Code]** univoco in caratteri minuscoli e senza spazi.

   >[!NOTE]
   >
   >Non è consigliabile utilizzare il valore `type` nel campo [!UICONTROL Attribute Code]. Ciò può causare errori perché il valore `type` è riservato per l&#39;uso di sistema.

   ![Attributo prodotto - proprietà avanzate](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

   Le opzioni disponibili dipendono dall&#39;impostazione _[!UICONTROL Catalog Input Type for Store Owner]_.

1. Impostare **[!UICONTROL Scope]** per indicare la posizione nella gerarchia [store](../getting-started/websites-stores-views.md) in cui è possibile utilizzare l&#39;attributo.

1. Se si desidera impedire l&#39;immissione di valori duplicati, impostare **[!UICONTROL Unique Value]** su `Yes`.

1. Per i tipi di input che vengono immessi valori, eseguire un test di validità di tutti i dati immessi in un campo di testo impostando **[!UICONTROL Input Validation for Store Owner]** sul tipo di dati che il campo deve contenere.

   Questo campo non è disponibile per i tipi di input con valori selezionati. Il test può convalidare uno dei seguenti elementi:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Convalida input](./assets/product-attribute-input-validation.png){width="400"}

1. Per aggiungere questo attributo all&#39;elenco [Prodotti](products-list.md), impostare le opzioni seguenti su `Yes`.

   - **Aggiungi a opzioni colonna** - Include l&#39;attributo come colonna nell&#39;elenco _[!UICONTROL Products]_.
   - **Usa in opzioni filtro** - Aggiunge un controllo filtro all&#39;intestazione di colonna nell&#39;elenco _[!UICONTROL Products]_.

## Passaggio 3: immettere l&#39;etichetta del campo

1. Nel pannello di navigazione a sinistra, scegliere **[!UICONTROL Manage Labels]**.

1. Immettere **[!UICONTROL Title]** da utilizzare come etichetta per il campo.

   Se il tuo Negozio è disponibile in diverse lingue, puoi immettere un titolo tradotto per ogni visualizzazione.

   ![Attributo prodotto - Gestione titoli](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

   >[!NOTE]
   >
   > Se prevedi di utilizzare questo attributo come facet in Live Search, devi specificare un’etichetta specifica per lo store. In caso contrario, il nome dell&#39;attributo potrebbe non essere visualizzato correttamente nella pagina di configurazione del facet. Per aggiornare la configurazione, modifica manualmente l&#39;etichetta utilizzando l&#39;opzione [modifica nell&#39;elenco dei facet di Live Search](https://experienceleague.adobe.com/it/docs/commerce/live-search/live-search-admin/facets/facets-add#step-2-edit-facet-properties-optional) nella _Guida a Live Search_.

## Passaggio 4: descrivere le proprietà della vetrina

1. Nel pannello di navigazione a sinistra, scegliere **[!UICONTROL Storefront Properties]**.

   ![Attributi del prodotto - proprietà vetrina](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

   Le opzioni disponibili dipendono dall&#39;impostazione _[!UICONTROL Catalog Input Type for Store Owner]_.

1. Se l&#39;attributo deve essere disponibile per la ricerca, impostare **[!UICONTROL Use in Search]** su `Yes`.

   - Imposta il valore **[!UICONTROL Search Weight]** per controllare la posizione in cui viene visualizzato l&#39;elemento nei risultati di ricerca: da 1 (peso minimo) a 10 (peso massimo).

   - Imposta **[!UICONTROL Visible in Advanced Search]** come necessario. Ulteriori informazioni in [Ricerca avanzata](search.md#advanced-search).

1. Per includere l&#39;attributo in Confronto prodotti, impostare **[!UICONTROL Comparable on Storefront]** su `Yes`.

1. Per i campi a discesa, a selezione multipla e prezzo, eseguire le operazioni seguenti:

   - Per utilizzare l&#39;attributo come filtro nella navigazione a livelli, impostare **[!UICONTROL Use in Layered Navigation]** su `Yes`.

   - Per utilizzare l&#39;attributo nella navigazione a livelli nelle pagine dei risultati di ricerca, impostare **[!UICONTROL Use in Search Results Layered Navigation]** su `Yes`.

   - Per **[!UICONTROL Position]**, immettere un numero per indicare la posizione relativa dell&#39;attributo nel blocco di navigazione a livelli.

1. Per utilizzare l&#39;attributo nelle regole di prezzo, impostare **[!UICONTROL Use for Promo Rule Conditions]** su `Yes`.

1. Per consentire la formattazione del testo con HTML, impostare **[!UICONTROL Allow HTML Tags on Frontend]** su `Yes`.

   Questa impostazione rende disponibile l’editor di WYSIWYG per il campo.

1. Per includere l&#39;attributo nella pagina del prodotto, impostare **[!UICONTROL Visible on Catalog Pages on Storefront]** su `Yes`.

1. Se supportato dal tema, completa le seguenti impostazioni:

   - Per includere l&#39;attributo negli elenchi di prodotti, impostare **[!UICONTROL Used in Product Listing]** su `Yes`.

   - Per utilizzare l&#39;attributo come parametro di ordinamento per gli elenchi di prodotti, impostare **[!UICONTROL Used for Sorting in Product Listing]** su `Yes`.

1. Al termine, fare clic su **[!UICONTROL Save Attribute]**.

## Passaggio 5: assegnare l&#39;attributo creato alla serie di attributi

Affinché un attributo sia visibile nella pagina di creazione del prodotto, aggiungilo a un set di attributi specifico.

1. Dopo aver completato i passaggi precedenti, vai a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Attribute Set]**.

1. Selezionare il set di attributi desiderato nell&#39;elenco e aprirlo in modalità di modifica.

1. Trascinare l&#39;attributo creato dall&#39;elenco **[!UICONTROL Unassigned Attributes]** nella cartella appropriata nella colonna **Gruppi**.

1. Al termine, fare clic su **[!UICONTROL Save]**.

## Attributi per prodotti configurabili

Qualsiasi attributo utilizzato come elenco a discesa di opzioni per un [prodotto configurabile](product-create-configurable.md) deve avere le seguenti proprietà:

| Proprietà | Valore |
|----------|------ |
| Tipo di input del catalogo per il proprietario del negozio | A discesa |
| Ambito | Globale |

{style="table-layout:auto"}

## Eliminare un attributo

Quando un attributo viene eliminato, viene rimosso da tutti i prodotti e i set di attributi correlati. Gli attributi di sistema fanno parte delle funzionalità di base del tuo archivio e non possono essere eliminati.

Prima di eliminare un attributo, accertati che non sia attualmente utilizzato da alcun prodotto nel catalogo. Un modo semplice per determinare se un attributo è in uso consiste nell&#39;utilizzare lo strumento [Esporta](../systems/data-export.md) per controllare l&#39;elenco degli attributi di entità del prodotto. Se l’attributo non è incluso nell’elenco, non viene utilizzato da alcun prodotto nel catalogo.

**_Per eliminare un attributo:_**

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Attributes]_>**[!UICONTROL Product]**.

1. Trovare l&#39;attributo nell&#39;elenco e aprirlo in modalità di modifica.

1. Fare clic su **[!UICONTROL Delete Attribute]**.

   ![Elimina attributo](./assets/attribute-delete.png){width="600" zoomable="yes"}

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL OK]**.
