---
title: Aggiungere attributi a un prodotto
description: Scopri come aggiungere attributi ai prodotti nel catalogo.
exl-id: 1f92807a-2362-48a2-8d3a-4aef90a5671f
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 0%

---

# Aggiungere attributi a un prodotto

Anche se gli attributi sono gestiti principalmente da [Negozi](../stores-purchase/stores-menu.md) , è inoltre possibile aggiungere nuovi attributi _al volo_ mentre si lavora su un prodotto. Puoi scegliere dall’elenco degli attributi esistenti o creare un attributo. Il nuovo attributo viene aggiunto al [set di attributi](../catalog/attribute-sets.md) su cui si basa il prodotto.

## Passaggio 1: aggiungere un attributo

1. Apri il prodotto in modalità di modifica.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Attribute]**.

   ![Nuovo prodotto con set di attributi predefinito](./assets/product-attribute-add.png){width="600" zoomable="yes"}

1. Per aggiungere un attributo esistente al prodotto, utilizza [controlli filtro](../getting-started/admin-grid-controls.md) per trovare l&#39;attributo nella griglia ed eseguire le operazioni seguenti:

   - Selezionare la casella di controllo nella prima colonna di ogni attributo da aggiungere.

   - Clic **[!UICONTROL Add Selected]**.

   ![Seleziona un attributo](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

1. Per definire un nuovo attributo, fare clic su **[!UICONTROL Create New Attribute]** e completare gli elementi nel passaggio 2.

## Passaggio 2: descrivere le proprietà dell’attributo di base

![Proprietà attributo](./assets/product-attribute-add-new.png){width="600" zoomable="yes"}

1. Sotto _[!UICONTROL Attribute Properties]_, immetti un **[!UICONTROL Attribute Label]**per identificare l&#39;attributo.

1. Imposta **[!UICONTROL Catalog Input Type for Store Owner]** al tipo di [controllo input](attributes-input-types.md) da utilizzare per l&#39;immissione dei dati.

   Se l’attributo è utilizzato per un [prodotto configurabile](product-create-configurable.md), scegli `Dropdown`. Quindi, imposta **[!UICONTROL Required]** a `Yes`.

1. Per `Dropdown` e `Multiple Select` tipi di input, effettuare le seguenti operazioni:

   - Sotto **[!UICONTROL Values]**, fai clic su **[!UICONTROL Add Value]**.

   - Immettere il primo valore da visualizzare nell&#39;elenco.

     Puoi immettere un valore per l’amministratore e una traduzione del valore per ogni visualizzazione store. Se disponi di una sola visualizzazione store, puoi immettere solo il valore Amministratore, che viene utilizzato anche per la vetrina.

   - Clic **[!UICONTROL Add Value]** e ripetere il passaggio precedente per ogni opzione da includere nell&#39;elenco.

   - Seleziona **[!UICONTROL Is Default]** per utilizzare l&#39;opzione come valore predefinito.

   ![Valori](./assets/product-attribute-add-values-colors.png){width="600" zoomable="yes"}

1. Se si desidera richiedere al cliente di scegliere un&#39;opzione prima che il prodotto possa essere acquistato, impostare **[!UICONTROL Required]** a `Yes`.

## Passaggio 3: descrivere le proprietà avanzate (facoltativo)

![Proprietà attributi avanzate](./assets/product-attribute-advanced-attribute-properties.png){width="600" zoomable="yes"}

1. Inserisci un valore univoco **[!UICONTROL Attribute Code]** in caratteri minuscoli e senza spazi.

1. Imposta **[!UICONTROL Scope]** per indicare la posizione nella gerarchia del punto vendita in cui può essere utilizzato l&#39;attributo.

   Se l’attributo è utilizzato per un [prodotto configurabile](product-create-configurable.md), scegli `Global`.

1. Se questo attributo si applica solo a questo prodotto, impostare **[!UICONTROL Unique Value]** a `Yes`.

1. Per eseguire un test di validità dei dati immessi in un campo di testo, impostare **[!UICONTROL Input Validation for Store Owner]** al tipo di dati che il campo deve contenere.

   Questo campo non è disponibile per i tipi di input con valori selezionati. La convalida di input può essere utilizzata per uno dei seguenti elementi:

   - `Decimal Number`
   - `Integer Number`
   - `Email`
   - `URL`
   - `Letters`
   - `Letters (a-z, A-Z) or Numbers (0-9)`

   ![Convalida input](./assets/product-attribute-input-validation.png){width="500"}

1. Se si desidera includere l&#39;attributo come colonna nella griglia Prodotti, impostare **[!UICONTROL Add to Column Options]** a `Yes`.

1. Se desideri filtrare il _[!UICONTROL Products]_griglia in base a questa colonna, impostata **[!UICONTROL Use in Filter Options]**a `Yes`.

## Passaggio 4: immettere l&#39;etichetta del campo

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Manage titles]** sezione.

1. Immetti un **[!UICONTROL Title]** da utilizzare come etichetta per il campo.

   Se il tuo Negozio è disponibile in diverse lingue, puoi immettere un titolo tradotto per ogni visualizzazione.

   ![Gestisci titoli](./assets/product-attribute-add-manage-titles.png){width="600" zoomable="yes"}

## Passaggio 5: descrivere le proprietà della vetrina

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Storefront Properties]** sezione.

   ![Proprietà vetrina](./assets/product-attribute-add-storefront-properties.png){width="600" zoomable="yes"}

1. Per rendere l&#39;attributo disponibile per la ricerca, impostare **[!UICONTROL Use in Search]** a `Yes`.

1. Per includere l’attributo in Product Compare, imposta **[!UICONTROL Comparable on Storefront]** a `Yes`.

1. Per includere gli attributi a discesa, selezione multipla o prezzo nella navigazione a livelli, impostare **[!UICONTROL Use in Search Results Layered Navigation]** a uno dei seguenti elementi:

   - `Filterable (with results)` - La navigazione a livelli include solo i filtri per i quali è possibile trovare prodotti corrispondenti. Qualsiasi valore di attributo che già si applica a tutti i prodotti visualizzati nell’elenco non viene visualizzato come filtro disponibile. Nell’elenco dei filtri disponibili vengono omessi anche i valori degli attributi con un conteggio di zero (0) corrispondenze prodotto.<br/><br/>L’elenco filtrato dei prodotti include solo i prodotti che corrispondono al filtro. L’elenco dei prodotti viene aggiornato solo se i filtri selezionati modificano ciò che viene visualizzato.

   - `Filterable (no results)` - La navigazione a livelli include filtri per tutti i valori di attributo disponibili e i relativi conteggi di prodotti, inclusi i prodotti con zero (0) corrispondenze di prodotto. Se il valore dell’attributo è un campione, viene visualizzato come filtro ma viene barrato.

1. Per utilizzare in una navigazione a più livelli nelle pagine dei risultati di ricerca, impostare **[!UICONTROL Use in Search Results Navigation]** a `Yes` e inserisci un numero in **[!UICONTROL Position]** campo.

   Il numero di posizione indica la posizione relativa dell&#39;attributo all&#39;interno del blocco di navigazione a livelli.

1. Per utilizzare l&#39;attributo nelle regole di prezzo, impostare **[!UICONTROL Use for Promo Rule Conditions]** a `Yes`.

1. Per consentire la formattazione del testo con HTML, impostare **[!UICONTROL Allow HTML Tags on Storefront]** a `Yes`.

   Questa impostazione rende disponibile l’editor WYSIWYG quando si modifica il campo.

1. Per includere l’attributo nella pagina del prodotto, imposta **[!UICONTROL Visible on Catalog Pages on Storefront]** a `Yes`.

1. Completa le seguenti impostazioni supportate dal tema:

   - Per includere l’attributo nell’elenco dei prodotti, imposta **[!UICONTROL Used in Product Listing]** a `Yes`.

   - Per utilizzare l’attributo come parametro di ordinamento per gli elenchi di prodotti, imposta **[!UICONTROL Used for Sorting in Product Listing]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Attribute]**.
