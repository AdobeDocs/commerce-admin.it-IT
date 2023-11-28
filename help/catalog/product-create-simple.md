---
title: Prodotto semplice
description: Scopri come creare un prodotto semplice che può essere venduto singolarmente o come parte di un prodotto raggruppato, configurabile o in bundle.
exl-id: 3ac9b28d-3929-4fd6-97ca-145ea6d6897c
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '594'
ht-degree: 0%

---

# Prodotto semplice

Uno dei fattori chiave per sfruttare la potenza dei tipi di prodotto è imparare a utilizzare un prodotto semplice e indipendente. Un prodotto semplice può essere venduto singolarmente o come parte di un prodotto raggruppato, configurabile o in bundle. Un prodotto semplice con opzioni personalizzate è a volte indicato come _prodotto composito_.

Le istruzioni seguenti illustrano il processo di creazione di un prodotto semplice utilizzando un [modello di prodotto](attribute-sets.md), campi obbligatori e impostazioni di base. Ogni campo obbligatorio è contrassegnato da un asterisco rosso (`*`). Al termine delle nozioni di base, puoi completare le altre impostazioni del prodotto in base alle esigenze.

![Prodotto semplice](./assets/product-simple.png){width="700" zoomable="yes"}

## Passaggio 1: scegliere il tipo di prodotto

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Il giorno _[!UICONTROL Add Product]_( ![Freccia del menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) in alto a destra, scegli **[!UICONTROL Simple Product]**.

   ![Aggiungi prodotto semplice](./assets/product-add-simple.png){width="700" zoomable="yes"}

## Passaggio 2: scegliere la serie di attributi

Per scegliere il [set di attributi](attribute-sets.md) utilizzato come modello per il prodotto:

- Fai clic su nella **[!UICONTROL Attribute Set]** e immettere il nome completo o parziale della serie di attributi.

- Nell&#39;elenco visualizzato scegliere il set di attributi che si desidera utilizzare.

Il modulo viene aggiornato per riflettere la modifica.

![Scegli set di attributi](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Passaggio 3: completare le impostazioni richieste

1. Inserisci il **[!UICONTROL Product Name]**.

1. Accetta il valore predefinito **[!UICONTROL SKU]** in base al nome del prodotto o immettine un altro.

1. Inserisci il prodotto **[!UICONTROL Price]**.

1. Poiché il prodotto non è ancora pronto per la pubblicazione, imposta **[!UICONTROL Enable Product]** opzione per `No`.

1. click **[!UICONTROL Save]** e continua.

   Quando il prodotto viene salvato, la [Visualizzazione store](introduction.md#product-scope) selettore viene visualizzato nell&#39;angolo superiore sinistro.

1. Scegli la **[!UICONTROL Store View]** dove il prodotto deve essere disponibile.

   ![Scegliere la visualizzazione dello store](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Passaggio 4: completare le impostazioni di base

1. Imposta **[!UICONTROL Tax Class]** a uno dei seguenti elementi:

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

1. Inserisci il **[!UICONTROL Quantity]** del prodotto che è in magazzino.

   Per impostazione predefinita, **[!UICONTROL Stock Status]** è impostato su `In Stock`.

   >[!NOTE]
   >
   >Se si abilita [Inventory management](../inventory-management/introduction.md), i commercianti con origine singola impostano la quantità in questa sezione. I commercianti con più origini aggiungono origini e quantità nella sezione Origini. Vedi quanto segue _Assegna origini e quantità (Inventory management)_ sezione.

1. Inserisci il **[!UICONTROL Weight]** del prodotto.

1. Accetta il valore predefinito **[!UICONTROL Visibility]** impostazione di `Catalog, Search`.

1. Da assegnare _[!UICONTROL Categories]_al prodotto, fai clic su **[!UICONTROL Select…]**ed effettuare una delle seguenti operazioni:

   **Scegli una categoria esistente**:

   - Inizia a digitare nella casella fino a trovare una corrispondenza.

   - Selezionare la casella di controllo di ciascuna categoria da assegnare.

   **Creare una categoria**:

   - Clic **[!UICONTROL New Category]**.

   - Inserisci il **[!UICONTROL Category Name]** e scegli la **[!UICONTROL Parent Category]**, che ne determina la posizione nella struttura del menu.

   - Clic **[!UICONTROL Create Category]**.

1. Per inserire il prodotto nell’elenco di [nuovi prodotti](../content-design/widget-new-products-list.md), seleziona la **[!UICONTROL Set Product as New]** casella di controllo.

1. Scegli la **[!UICONTROL Country of Manufacture]**.

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

1. Se sei pronto a pubblicare il prodotto nel catalogo, imposta **[!UICONTROL Enable Product]** passa a `Yes`.

1. Effettuare una delle seguenti operazioni:

   - **Metodo 1:** Salva e visualizza anteprima

      - Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]**.

      - Per visualizzare il prodotto nel tuo negozio, scegli **[!UICONTROL Customer View]** il _Amministratore_ (![Freccia del menu](../assets/icon-menu-down-arrow-black.png)).

     L’archivio si apre in una nuova scheda del browser.

     ![Visualizzazione cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Metodo 2:** Salva e chiudi

     Il giorno _[!UICONTROL Save]_ ( ![Freccia del menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), scegliere **[!UICONTROL Save & Close]**.

## Aspetti da ricordare

- I prodotti semplici possono essere inclusi in tipi di prodotto configurabili, raggruppati e raggruppati.

- La semplice configurazione del prodotto sostituisce le configurazioni di prodotto configurabili per un prodotto specifico.

- Un prodotto semplice può avere opzioni personalizzate con vari tipi di input, il che rende possibile vendere molte varianti di prodotto da una singola SKU.
