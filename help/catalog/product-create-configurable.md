---
title: Prodotto configurabile
description: Scopri come creare un prodotto configurabile che fornisca agli acquirenti varianti per la selezione.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: ee7928b50ddd07e757c71ce5bed84619f1437410
workflow-type: tm+mt
source-wordcount: '2506'
ht-degree: 0%

---

# Prodotto configurabile

Un prodotto configurabile è simile a un singolo prodotto con un elenco a discesa di ogni variante. Ogni voce di elenco è in realtà un prodotto semplice separato con una SKU univoca, che consente di tenere traccia dell’inventario per ogni variante di prodotto. Puoi ottenere un effetto simile utilizzando un prodotto semplice con opzioni personalizzate, ma senza la possibilità di tenere traccia dell’inventario per ogni variante.

Le istruzioni seguenti illustrano il processo di creazione di un prodotto configurabile utilizzando un [modello di prodotto](attribute-sets.md), campi obbligatori e impostazioni di base. Ogni campo obbligatorio è contrassegnato da un asterisco rosso (`*`). Al termine delle nozioni di base, puoi completare le altre impostazioni del prodotto in base alle esigenze.

![Prodotto configurabile](./assets/product-configurable.png){width="700" zoomable="yes"}

## Parte 1: Creazione di un prodotto configurabile

Sebbene un prodotto configurabile utilizzi più SKU e la configurazione iniziale possa richiedere un po’ di tempo, alla fine potrai risparmiare tempo. Se prevedi di espandere la tua attività, il tipo di prodotto configurabile è una buona scelta per i prodotti con più opzioni.

Prima di iniziare, preparare un [set di attributi](attribute-sets.md) che includa un attributo impostato su uno dei tipi di input consentiti per ogni variante di prodotto. Ad esempio, il set di attributi potrebbe includere attributi a discesa per colore e dimensione.

Le proprietà di ciascun attributo utilizzato per una variante di prodotto configurabile devono avere le seguenti impostazioni:

### Requisiti degli attributi di variazione del prodotto

| Proprietà | Impostazione |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | Il tipo di input di qualsiasi attributo utilizzato per una variante di prodotto deve essere uno dei seguenti: `Dropdown`, `Visual Swatch` o `Text Swatch`. |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

### Passaggio 1: scegliere il tipo di prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Scegliere _[!UICONTROL Add Product]_&#x200B;dal menu ![&#x200B; ( &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"}Freccia menu **[!UICONTROL Configurable Product]**) nell&#39;angolo superiore destro.

   ![Aggiungi prodotto configurabile](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Passaggio 2: scegliere la serie di attributi

Il [set di attributi](attribute-sets.md) determina la selezione dei campi utilizzati nel prodotto. Il set di attributi utilizzato nell&#39;esempio seguente dispone di attributi per colore e dimensioni. Il nome del set di attributi è indicato nella parte superiore della pagina e inizialmente è impostato su `Default`.

1. Per scegliere il set di attributi per il prodotto, fai clic sul campo nella parte superiore della pagina ed effettua una delle seguenti operazioni:

   - Per **[!UICONTROL Search]**, immettere il nome del set di attributi.
   - Nell&#39;elenco, scegliere il set di attributi che si desidera utilizzare.

   Il modulo viene aggiornato per riflettere la modifica.

1. Se si desidera aggiungere un altro attributo al set di attributi, fare clic su **[!UICONTROL Add Attribute]** e seguire le istruzioni in [Aggiunta di un attributo](product-attributes-add.md).

   ![Scegli modello](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Passaggio 3: completare le impostazioni richieste

1. Immettere il prodotto **[!UICONTROL Product Name]**.

1. Accettare **[!UICONTROL SKU]** predefinito basato sul nome del prodotto o immetterne un altro.

1. Immettere il prodotto **[!UICONTROL Price]**.

1. Poiché il prodotto non è ancora pronto per la pubblicazione, impostare **[!UICONTROL Enable Product]** su `No`.

1. fare clic su **[!UICONTROL Save]** e continuare.

   Quando il prodotto viene salvato, il selettore [Visualizzazione store](introduction.md#product-scope) viene visualizzato nell&#39;angolo superiore sinistro.

1. Scegliere **[!UICONTROL Store View]** in cui il prodotto deve essere disponibile.

   ![Scegliere la visualizzazione dello store](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Passaggio 4: completare le impostazioni di base

1. Imposta **[!UICONTROL Tax Class]** su uno dei seguenti:

   - `None`
   - `Taxable Goods`

1. **[!UICONTROL Quantity]** è determinato dalle varianti di prodotto, quindi puoi lasciarlo vuoto.

1. Lascia **[!UICONTROL Stock Status]** impostato.

   Lo stato del magazzino di un prodotto configurabile è determinato da ciascuna configurazione associata. Poiché il prodotto è stato salvato senza immettere una quantità, **[!UICONTROL Stock Status]** è impostato su `Out of Stock`.

   >[!NOTE]
   >
   >Il **Stock Status** del prodotto configurabile è un&#39;impostazione controllata da **_semi-manualmente_**. È parzialmente controllata dallo stato delle scorte dei suoi prodotti secondari. Fa parte del calcolo dello stato delle scorte **_multi-criteri_**, descritto nella sezione [Configurare lo stato delle scorte](#configure-the-stock-status).

1. Immettere il prodotto **[!UICONTROL Weight]**.

>[!NOTE]
>
>Un prodotto configurabile deve avere sempre un peso. Se si seleziona **[!UICONTROL This item has no weight]** dall&#39;elenco a discesa, viene automaticamente modificato in **[!UICONTROL This item has weight]** dopo il salvataggio del prodotto.

1. Accettare l&#39;impostazione **[!UICONTROL Visibility]** predefinita di `Catalog, Search`.

1. Per inserire il prodotto nell&#39;elenco di [nuovi prodotti](../content-design/widget-new-products-list.md), selezionare la casella di controllo **[!UICONTROL Set Product as New]**.

1. Per assegnare le categorie al prodotto, fare clic sulla casella **[!UICONTROL Select…]** ed eseguire una delle operazioni seguenti:

   **Scegliere una categoria esistente**:

   - Inizia a digitare nella casella fino a trovare una corrispondenza.

   - Selezionare la casella di controllo della categoria da assegnare.

   ![Selezionare una o più categorie per il prodotto del bundle](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Crea una categoria**:

   - Fare clic su **[!UICONTROL New Category]**.

   - Immettere **[!UICONTROL Category Name]** e scegliere **[!UICONTROL Parent Category]**, che ne determina la posizione nella struttura del menu.

   s- Fare clic su **[!UICONTROL Create Category]**.

1. Scegliere **[!UICONTROL Country of Manufacture]**.

   Potrebbero essere presenti attributi aggiuntivi utilizzati per descrivere il prodotto. La selezione varia in base al set di attributi e può essere completata in un secondo momento.

### Passaggio 5: salvare e continuare

Ora è il momento giusto per salvare il tuo lavoro. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]**. Nella serie di passaggi successiva, imposterai le configurazioni per ogni variante del prodotto.

## Parte 2: aggiunta di configurazioni

L’esempio seguente mostra come aggiungere configurazioni per tre colori e tre dimensioni. In tutto, nove semplici prodotti sono creati con SKU univoci per coprire ogni possibile combinazione di varianti. Per impostazione predefinita, il nome del prodotto e lo SKU per ogni variante si basano sul valore dell’attributo e sul nome del prodotto principale o sullo SKU.

La barra di avanzamento nella parte superiore della pagina mostra la posizione in cui ti trovi durante il processo e ti guida attraverso ogni passaggio.

### Passaggio 1: scegliere gli attributi

1. Continuando dall&#39;alto, scorrere verso il basso fino alla sezione _[!UICONTROL Configurations]_&#x200B;e fare clic su **[!UICONTROL Create Configurations]**.

   ![Configurazioni](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Selezionare la casella di controllo di ogni attributo che si desidera includere come configurazione.

   Per questo esempio, sono selezionati `color` e `size`.

   ![Seleziona attributi](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   L’elenco include tutti gli attributi del set di attributi che possono essere utilizzati in un prodotto configurabile.

1. Se si desidera aggiungere un attributo, fare clic su **[!UICONTROL Create New Attribute]** ed eseguire le operazioni seguenti:

   - Completa le proprietà dell’attributo.

   - Fare clic su **[!UICONTROL Save Attribute]**.

   - Selezionare la casella di controllo per l&#39;attributo.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Next]**.

### Passaggio 2: immettere i valori degli attributi

1. Per ogni attributo, seleziona la casella di controllo dei valori applicabili al prodotto.

   ![Valori attributo](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Per ridisporre gli attributi, acquisire l&#39;icona _Riordina_ ( ![Icona Ordinamento](../assets/icon-sort-order.png) ) e spostare la sezione in una nuova posizione.

   L’ordine determina la posizione degli elenchi a discesa sulla pagina del prodotto.

1. Nella barra di avanzamento, fare clic su **[!UICONTROL Next]**.

### Passaggio 3: configurare immagini, prezzo e quantità

Questo passaggio determina le immagini, il prezzo e la quantità di ciascuna configurazione. Le opzioni disponibili sono le stesse per ciascuno di essi ed è possibile sceglierne solo una. Puoi applicare la stessa impostazione a tutte le SKU, applicare un’impostazione univoca a ciascuna SKU o saltare le impostazioni per il momento.

Scegliere le opzioni di configurazione applicabili.

Utilizzare uno dei metodi seguenti per configurare **[!UICONTROL images]**:

**Metodo 1:** Applica un singolo set di immagini a tutti gli SKU

1. Selezionare **[!UICONTROL Apply single set of images to all SKUs]**.

1. Individuare le immagini che si desidera includere nella raccolta prodotti o trascinarle nella casella.

![Usa le stesse immagini per tutti gli SKU](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Metodo 2:** Applica immagini univoche per ogni SKU

Poiché l’immagine del prodotto principale è già caricata, puoi utilizzare questa opzione per caricare un’immagine di ciascun colore. Puoi aggiungere un’immagine diversa che viene visualizzata nel carrello quando qualcuno acquista l’articolo con un colore specifico.

1. Selezionare **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Selezionare **[!UICONTROL Attribute]** illustrato dalle immagini, ad esempio `color`.

1. Per ogni valore di attributo, individua le immagini da utilizzare per la configurazione o trascinale nella casella.

   Se trascinate l&#39;immagine in una casella di valore, questa viene visualizzata anche nelle sezioni relative agli altri valori. Per eliminare un&#39;immagine, fare clic sull&#39;icona _Cestino_ (![icona Cestino](../assets/icon-delete-trashcan-solid.png)).

   ![Immagini univoche per SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

Utilizzare uno dei metodi seguenti per configurare **[!UICONTROL prices]**:

>[!NOTE]
>
>Un prodotto configurabile non ha un proprio prezzo nel catalogo. Il prezzo del prodotto configurabile deriva dai suoi [!UICONTROL In Stock] prodotti secondari.

**Metodo 1:** Applica lo stesso prezzo a tutti gli SKU

1. Se il prezzo è lo stesso per tutte le varianti, selezionare **[!UICONTROL Apply single price to all SKUs]**.

1. Immettere **[!UICONTROL Price]**.

   ![Stesso prezzo per SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Metodo 2:** Applicare un prezzo diverso per ogni SKU

1. Se il prezzo è diverso per ogni o per alcune varianti del prodotto, selezionare **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Selezionare **[!UICONTROL Attribute]** che rappresenta la base della differenza di prezzo.

1. Immettere **[!UICONTROL Price]** per ogni valore di attributo.

   In questo esempio, la dimensione XL costa di più.

   ![Prezzo univoco per SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

Utilizzare uno dei metodi seguenti per configurare **[!UICONTROL Quantity]**:

**Metodo 1:** Applicare la stessa quantità a tutti gli SKU

Se la quantità è la stessa per tutti gli SKU, selezionare **[!UICONTROL Apply single quantity to each SKU]** e specificare la quantità.

_Singoli commercianti di origine_ - Immettere **[!UICONTROL Quantity]**.

_Più commercianti Source che utilizzano [Inventory management](../inventory-management/introduction.md)_. Assegna origini e aggiungi quantità per tutte le varianti di prodotto generate:

1. Selezionare l&#39;opzione **[!UICONTROL Apply single quantity to each SKU]**.

1. Per aggiungere un&#39;origine, fare clic su **[!UICONTROL Assign Sources]**.

1. Individuare o cercare un&#39;origine da aggiungere. Seleziona la casella di controllo accanto alle origini che desideri aggiungere per il prodotto.

1. Inserire un importo scorte disponibili per origine.

   ![Quantità singola per tutti gli SKU, assegna origine](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Metodo 2:** Applicare una quantità diversa per attributo

_Singoli commercianti di origine_ - Immettere **[!UICONTROL Quantity]**.

_Più commercianti Source che utilizzano [Inventory management](../inventory-management/introduction.md)_. Assegna origini e aggiungi quantità per tutte le varianti di prodotto generate:

1. Se la quantità è diversa per ogni SKU, selezionare **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Immetti **[!UICONTROL Quantity]** per ciascuno di essi.

   ![Quantità diverse per attributo](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Al termine della configurazione di immagini, prezzo e quantità, fare clic su **[!UICONTROL Next]** nell&#39;angolo superiore destro.

### Passaggio 4: generare le configurazioni di prodotto

Attendi che l’elenco dei prodotti venga visualizzato ed effettua una delle seguenti operazioni:

- Se si è soddisfatti delle configurazioni, fare clic su **[!UICONTROL Generate Products]**.

- Per apportare correzioni, fare clic su **[!UICONTROL Back]**.

![Rivedi riepilogo prima di generare varianti di prodotto](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Le varianti di prodotto correnti vengono visualizzate nella parte inferiore della sezione _Configurazione_.

![Configurazioni correnti](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Passaggio 5: aggiungere immagini del prodotto

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Images and Videos]_.

1. Fai clic sul riquadro _Fotocamera_ e individua l&#39;immagine principale da utilizzare per il prodotto configurabile.

Per ulteriori informazioni, vedere [Immagini e video](product-images-and-video.md).

### Passaggio 6: Completare le informazioni sul prodotto

Scorri verso il basso e completa le informazioni nelle sezioni seguenti, in base alle esigenze:

- [Contenuto](product-content.md)

- [Prodotti correlati, up-selling e cross-selling](related-products-up-sells-cross-sells.md)

- [Ottimizzazione motore di ricerca](product-search-engine-optimization.md)

- [Opzioni personalizzabili](settings-advanced-custom-options.md)

- [Prodotti nei siti Web](settings-basic-websites.md)

- [Progettazione](settings-advanced-design.md)

- [Opzioni regalo](product-gift-options.md)

### Passaggio 7: pubblicare il prodotto

1. Se si è pronti a pubblicare il prodotto nel catalogo, impostare **[!UICONTROL Enable Product]** su `Yes` ed eseguire una delle operazioni seguenti:

   - **Metodo 1:** Salvataggio e anteprima

      - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]**.

      - Per visualizzare il prodotto nell&#39;archivio, scegli **[!UICONTROL Customer View]** nel menu _Amministratore_ ( ![Freccia menu](../assets/icon-menu-down-arrow-black.png) ).

     L’archivio si apre in una nuova scheda del browser.

     ![Visualizzazione clienti](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Metodo 2:** Salvare e chiudere

     Scegliere _[!UICONTROL Save]_&#x200B;dal menu ![&#x200B; ( &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"}Freccia menu **[!UICONTROL Save & Close]**).

### Passaggio 8: configurare le miniature del carrello

Se disponi di un’immagine diversa per ogni variante, puoi impostare la configurazione in modo da utilizzare l’immagine corretta per la miniatura del carrello acquisti.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]** sotto.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Shopping Cart]_.

1. Imposta **[!UICONTROL Configurable Product Image]** su `Product Thumbnail Itself`.

1. Al termine, fare clic su **[!UICONTROL Save Config]**.

   ![Carrello acquisti - immagine del prodotto configurabile](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Configurare lo stato del magazzino

Lo stato delle scorte del prodotto configurabile è diverso dallo stato delle scorte del prodotto semplice, dove rappresenta direttamente la disponibilità del prodotto. Per un prodotto configurabile, lo stato del magazzino fa parte di un calcolo dello stato del magazzino **_multi-criteria_**.

### Panoramica

I principi fondamentali delle relazioni di stato delle scorte sono i seguenti:

- Quando si modifica **[!UICONTROL Stock Status]** del prodotto configurabile come `Out of Stock` e si fa clic su **[!UICONTROL Save]**, il **_prodotto non è controllato_** dagli stati azionari dei suoi prodotti secondari. Viene sempre visualizzato come `Out of Stock` nell&#39;amministratore e nella vetrina.

- Quando si imposta **[!UICONTROL Stock Status]** del prodotto configurabile come `In Stock` e si fa clic su **[!UICONTROL Save]**, il **_prodotto è controllato solo parzialmente_** dagli stati azionari dei suoi prodotti secondari, che si riflettono in Admin e su Storefront.

### Descrizione dettagliata

Lo _stato Stock_ del prodotto configurabile è parzialmente controllato dallo stato Stock dei suoi prodotti secondari e in base ai seguenti **_multi-criteri_** calcoli dello stato Stock:

#### Solo con origine/magazzino di default:

- Se lo stato configurabile del materiale grezzo del prodotto è **_manualmente_** impostato su `Out of Stock` da un utente amministratore, da un&#39;importazione file o da una chiamata API, rimane `Out of Stock` sia per **_Admin_** che per **_Storefront_** finché non viene **_modificato manualmente_** in `In stock` da un utente amministratore, da un&#39;importazione file o da una chiamata API. Non può essere controllata dallo stato delle scorte dei suoi prodotti secondari.

- Se lo stato del magazzino del prodotto configurabile è **_manualmente_** impostato su `In Stock` da un utente amministratore, da un&#39;importazione di file o da una chiamata API, lo stato del magazzino è **_automaticamente_** controllato dallo stato del magazzino dei prodotti secondari sia su **_Admin_** che su **_Storefront_**.

>[!NOTE]
>
>Le scorte e le origini personalizzate fanno parte dell&#39;estensione [Inventory management](../inventory-management/sources-stocks.md) ed è consigliabile utilizzare questo strumento esclusivamente per la gestione delle scorte e delle origini. Le funzioni di origine e magazzino predefinite fanno parte del modulo `CatalogInventory`, che è ora obsoleto.

#### Con almeno una sorgente/scorta personalizzata:

- Se il valore Configurable Product Stock Status è **_manualmente_** impostato su `Out of Stock` da un utente Admin, da un&#39;importazione di file o da una chiamata API, rimarrà come `Out of Stock` sia per **_Admin_** che per **_Storefront_** finché non sarà **_manualmente_** modificato in `In Stock` da un utente Admin, da un&#39;importazione di file o da una chiamata API. **_non può_** essere controllato dallo stato azionario dei suoi prodotti secondari.

- Se il valore dello stato del magazzino del prodotto configurabile è **_manualmente_** impostato su `In Stock` da un utente amministratore, un&#39;importazione di file o una chiamata API, lo stato del magazzino è **_automaticamente_** controllato dallo stato del magazzino dei prodotti secondari solo su **_Storefront_**.

- Se il valore Configurable Product Stock Status è **_manualmente_** impostato su `In Stock` da un utente Admin, da un&#39;importazione di file o da una chiamata API, rimane `In Stock` in **_Admin_** finché non viene **_manualmente_** modificato in `Out of Stock` da un utente Admin, da un&#39;importazione di file o da una chiamata API. **_non può_** essere controllato dallo stato azionario dei suoi prodotti secondari.

## Aspetti da ricordare

- Un prodotto configurabile consente all’acquirente di scegliere le opzioni tra tipi di input a discesa, a selezione multipla, campione visivo e campione di testo. Ogni opzione è un prodotto separato e semplice.

- [Lo stato del magazzino](../inventory-management/sources-stocks.md) per un prodotto configurabile è un&#39;impostazione controllata semi-manualmente. È diverso dallo stato delle scorte del prodotto semplice, dove rappresenta direttamente la disponibilità del prodotto. Per un prodotto configurabile, lo stato delle scorte fa parte di un calcolo dello stato delle scorte basato su più criteri.

- I prodotti secondari configurabili possono essere prodotti semplici o virtuali **senza opzioni personalizzate**. Per rendere virtuali i prodotti secondari personalizzati, è necessario selezionare `Тhis item has no weight` per l&#39;impostazione **[!UICONTROL Weight]** per ciascuno di essi.

- Tutti i prodotti secondari vengono assegnati e non assegnati al prodotto configurabile **_globalmente_** per tutti i siti Web, gli store e le visualizzazioni dello store contemporaneamente.

- Un prodotto configurabile non ha un proprio prezzo nel catalogo. Il prezzo del prodotto configurabile deriva dai suoi [!UICONTROL In Stock] prodotti secondari.

- Gli attributi utilizzati per le varianti di prodotto devono avere un ambito globale e il cliente deve scegliere un valore. Gli attributi della variante di prodotto devono essere inclusi nella serie di attributi utilizzata come modello per il prodotto configurabile.

- Il set di attributi utilizzato come modello per un prodotto configurabile deve includere gli attributi che contengono i valori necessari per ogni variante di prodotto.

- L’immagine miniatura nel carrello può essere impostata in modo da visualizzare l’immagine dal record del prodotto configurabile o dalla variante di prodotto.

- È possibile configurare [attributi campione](swatches.md#create-swatches-for-products) in modo da non visualizzare le immagini di prodotto semplici corrispondenti quando il campione viene selezionato impostando il valore dell&#39;opzione **[!UICONTROL Update Product Preview Image]** su `No` nella pagina di modifica attributi in Amministrazione.

- Il tema controlla il comportamento della Galleria immagini quando un utente passa da una configurazione di prodotto all&#39;altra. Il comportamento predefinito per il tema _Vuoto_ consiste nell&#39;eseguire l&#39;override delle immagini del prodotto configurabili padre con la variante di prodotto selezionata. Per il tema Luma, il comportamento predefinito consiste nell’anteporre le immagini delle varianti di prodotto selezionate alle immagini del prodotto configurabili principale.
