---
title: Prodotto semplice
description: Scopri come creare un prodotto semplice che può essere venduto singolarmente o come parte di un prodotto raggruppato, configurabile o in bundle.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Prodotto semplice

Uno dei fattori chiave per sfruttare la potenza dei tipi di prodotto è imparare a utilizzare un prodotto semplice e indipendente. Un prodotto semplice può essere venduto singolarmente o come parte di un prodotto raggruppato, configurabile o in bundle. Un prodotto semplice con opzioni personalizzate viene talvolta indicato come _prodotto composito_.

Le istruzioni seguenti illustrano il processo di creazione di un prodotto semplice utilizzando un [modello di prodotto](attribute-sets.md), campi obbligatori e impostazioni di base. Ogni campo obbligatorio è contrassegnato da un asterisco rosso (`*`). Al termine delle nozioni di base, puoi completare le altre impostazioni del prodotto in base alle esigenze.

![Prodotto semplice](./assets/product-simple.png){width="700" zoomable="yes"}

## Passaggio 1: scegliere il tipo di prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Scegliere _[!UICONTROL Add Product]_dal menu ![ ( ](../assets/icon-menu-down-arrow-red.png){width="25"}freccia menu **[!UICONTROL Simple Product]**) in alto a destra.

   ![Aggiungi prodotto semplice](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Passaggio 2: scegliere la serie di attributi

Per scegliere il [set di attributi](attribute-sets.md) utilizzato come modello per il prodotto:

- Fare clic nel campo **[!UICONTROL Attribute Set]** e immettere il nome completo o parziale del set di attributi.

- Nell&#39;elenco visualizzato scegliere il set di attributi che si desidera utilizzare.

Il modulo viene aggiornato per riflettere la modifica.

![Scegli set di attributi](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Passaggio 3: completare le impostazioni richieste

1. Immettere **[!UICONTROL Product Name]**.

1. Accettare **[!UICONTROL SKU]** predefinito basato sul nome del prodotto o immetterne un altro.

1. Immettere il prodotto **[!UICONTROL Price]**.

1. Poiché il prodotto non è ancora pronto per la pubblicazione, impostare l&#39;opzione **[!UICONTROL Enable Product]** su `No`.

1. fare clic su **[!UICONTROL Save]** e continuare.

   Quando il prodotto viene salvato, il selettore [Visualizzazione store](introduction.md#product-scope) viene visualizzato nell&#39;angolo superiore sinistro.

1. Scegliere **[!UICONTROL Store View]** in cui il prodotto deve essere disponibile.

   ![Scegliere la visualizzazione dello store](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Passaggio 4: completare le impostazioni di base

1. Imposta **[!UICONTROL Tax Class]** su uno dei seguenti:

   - `None`
   - `Taxable Goods`
   - `Refund Adjustments`
   - `Gift Options`
   - `Order Gift Wrapping`
   - `Item Gift Wrapping`
   - `Printed Gift Card`
   - `Reward Points`
   - `VAT Reduced`
   - `VAT Standard`

1. Immettere il **[!UICONTROL Quantity]** del prodotto in magazzino.

   Per impostazione predefinita, **[!UICONTROL Stock Status]** è impostato su `In Stock`.

   >[!NOTE]
   >
   >Se abiliti [Inventory management](../inventory-management/introduction.md), gli esercenti di Source singoli impostano la quantità in questa sezione. Gli esercenti Multi Source aggiungono origini e quantità nella sezione Origini. Consulta la seguente sezione _Assegnare origini e quantità (Inventory management)_.

1. Immettere **[!UICONTROL Weight]** del prodotto.

1. Accettare l&#39;impostazione **[!UICONTROL Visibility]** predefinita di `Catalog, Search`.

1. Per assegnare _[!UICONTROL Categories]_al prodotto, fare clic sulla casella **[!UICONTROL Select…]**ed eseguire una delle operazioni seguenti:

   **Scegliere una categoria esistente**:

   - Inizia a digitare nella casella fino a trovare una corrispondenza.

   - Selezionare la casella di controllo di ciascuna categoria da assegnare.

   **Crea una categoria**:

   - Fare clic su **[!UICONTROL New Category]**.

   - Immettere **[!UICONTROL Category Name]** e scegliere **[!UICONTROL Parent Category]**, che ne determina la posizione nella struttura del menu.

   - Fare clic su **[!UICONTROL Create Category]**.

1. Per inserire il prodotto nell&#39;elenco di [nuovi prodotti](../content-design/widget-new-products-list.md), selezionare la casella di controllo **[!UICONTROL Set Product as New]**.

1. Scegliere **[!UICONTROL Country of Manufacture]**.

Potrebbero essere presenti singoli attributi aggiuntivi che descrivono il prodotto. La selezione varia in base al set di attributi e può essere completata in un secondo momento.

### Assegna origini e quantità ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

## Passaggio 5: Completare le informazioni sul prodotto

Scorri verso il basso e completa le informazioni nelle sezioni seguenti, in base alle esigenze:

- [Contenuto](product-content.md)
- [Immagini e video](product-images-and-video.md)
- [Prodotti correlati, up-selling e cross-selling](related-products-up-sells-cross-sells.md)
- [Ottimizzazione motore di ricerca](product-search-engine-optimization.md)
- [Opzioni personalizzabili](settings-advanced-custom-options.md)
- [Prodotti nei siti Web](settings-basic-websites.md)
- [Progettazione](settings-advanced-design.md)
- [Opzioni regalo](product-gift-options.md)

## Passaggio 6: pubblicare il prodotto

1. Se si è pronti a pubblicare il prodotto nel catalogo, impostare l&#39;opzione **[!UICONTROL Enable Product]** su `Yes`.

1. Effettuare una delle seguenti operazioni:

   - **Metodo 1:** Salvataggio e anteprima

      - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]**.

      - Per visualizzare il prodotto nell&#39;archivio, scegli **[!UICONTROL Customer View]** nel menu _Amministratore_ (![Freccia menu](../assets/icon-menu-down-arrow-black.png)).

     L’archivio si apre in una nuova scheda del browser.

     ![Visualizzazione clienti](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Metodo 2:** Salva e chiudi

     Scegliere _[!UICONTROL Save]_dal menu ![ ( ](../assets/icon-menu-down-arrow-red.png){width="25"}Freccia menu **[!UICONTROL Save & Close]**).

## Aspetti da ricordare

- I prodotti semplici possono essere inclusi in tipi di prodotto configurabili, raggruppati e raggruppati.

- La semplice configurazione del prodotto sostituisce le configurazioni di prodotto configurabili per un prodotto specifico.

- Un prodotto semplice può avere opzioni personalizzate con vari tipi di input, il che rende possibile vendere molte varianti di prodotto da una singola SKU.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
