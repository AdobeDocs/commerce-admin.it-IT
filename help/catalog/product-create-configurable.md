---
title: Prodotto configurabile
description: Scopri come creare un prodotto configurabile che fornisca agli acquirenti varianti per la selezione.
exl-id: 2066fd20-5227-41e9-b213-31825a58ebd9
feature: Catalog Management, Products
source-git-commit: 6fcbcd3b7cace10f0841a46b3cd27343862b3f3b
workflow-type: tm+mt
source-wordcount: '1981'
ht-degree: 0%

---

# Prodotto configurabile

Un prodotto configurabile viene visualizzato come un singolo prodotto con opzioni a discesa per le varianti (come colore o dimensione). Ogni variante è un prodotto semplice separato con la propria SKU, che consente il tracciamento delle singole scorte, a differenza dei prodotti semplici con opzioni personalizzate.

**Ideale per:** prodotti con più opzioni (colore, dimensioni, materiale, ecc.) in cui è necessario tenere traccia dell&#39;inventario per ogni variante. La configurazione iniziale richiede più tempo, ma offre una migliore scalabilità.

![Prodotto configurabile](./assets/product-configurable.png){width="700" zoomable="yes"}

## Prima di iniziare

### Elenco di controllo dei prerequisiti

Prima di creare un prodotto configurabile, assicurati di disporre di:

1. **Set di attributi** - Set di attributi che include attributi di varianti (ad esempio colore e dimensioni)
1. **Attributi variante creati** - Attributi configurati con le impostazioni seguenti
1. **Immagini del prodotto** - (Facoltativo ma consigliato) Immagini del prodotto principale e di ogni variante

### Requisiti degli attributi

Ogni attributo utilizzato per le varianti di prodotto deve avere le seguenti impostazioni:

| Proprietà | Impostazione necessaria |
|--- |--- |
| [!UICONTROL Scope] | `Global` |
| [!UICONTROL Catalog Input Type for Store Owner] | `Dropdown`, `Visual Swatch` o `Text Swatch` |
| [!UICONTROL Values Required] | `Yes` |

{style="table-layout:auto"}

Per istruzioni sulla creazione degli attributi, vedere [Attributi del prodotto](product-attributes.md).

## Fase 1: creare la base del prodotto

### Passaggio 1: scegliere il tipo di prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Scegliere _[!UICONTROL Add Product]_&#x200B;dal menu ![&#x200B; ( &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"}Freccia menu **[!UICONTROL Configurable Product]**) nell&#39;angolo superiore destro.

   ![Aggiungi prodotto configurabile](./assets/product-add-configurable.png){width="700" zoomable="yes"}

### Passaggio 2: scegliere la serie di attributi

Il [set di attributi](attribute-sets.md) determina quali campi vengono visualizzati nel modulo del prodotto e quali attributi sono disponibili per le varianti.

1. Fare clic sul campo set di attributi nella parte superiore della pagina ed effettuare una delle operazioni seguenti:

   - Per **[!UICONTROL Search]**, immettere il nome del set di attributi.
   - Nell&#39;elenco, scegliere il set di attributi che si desidera utilizzare.

   Il modulo viene aggiornato in base al set di attributi selezionato.

1. Se devi aggiungere un altro attributo al set di attributi, fai clic su **[!UICONTROL Add Attribute]** e segui le istruzioni in [Aggiunta di un attributo](product-attributes-add.md).

   ![Scegli modello](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

### Passaggio 3: inserire le informazioni di base

1. Immettere il prodotto **[!UICONTROL Product Name]**.

1. Accettare il valore predefinito **[!UICONTROL SKU]** in base al nome del prodotto o immettere un valore diverso.

1. Immettere il prodotto **[!UICONTROL Price]**.

   >[!NOTE]
   >
   >Questo prezzo è sostituito dai prezzi dei prodotti secondari. Il prezzo effettivo visualizzato ai clienti proviene dai prodotti secondari [!UICONTROL In Stock].

1. Poiché il prodotto non è ancora pronto per la pubblicazione, impostare **[!UICONTROL Enable Product]** su `No`.

1. Fare clic su **[!UICONTROL Save]** e continuare.

   Quando il prodotto viene salvato, il selettore [Visualizzazione store](introduction.md#product-scope) viene visualizzato nell&#39;angolo superiore sinistro.

1. Scegliere **[!UICONTROL Store View]** in cui il prodotto deve essere disponibile.

   ![Scegliere la visualizzazione dello store](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Passaggio 4: completare le impostazioni di base

1. Imposta **[!UICONTROL Tax Class]** su uno dei seguenti:

   - `None`
   - `Taxable Goods`

1. Lascia **[!UICONTROL Quantity]** vuoto. La quantità è determinata dalle variazioni del prodotto.

1. Lascia **[!UICONTROL Stock Status]** impostato.

   Lo stato di magazzino di un prodotto configurabile è determinato dalle relative varianti associate. Poiché il prodotto è stato salvato senza una quantità, **[!UICONTROL Stock Status]** è impostato su `Out of Stock`.

   >[!NOTE]
   >
   >Il **Stock Status** di un prodotto configurabile è un&#39;impostazione controllata da **_semi-manualmente_**, in parte basata sullo stato azionario dei prodotti figlio. Fa parte del calcolo dello stato delle scorte **_multi-criteri_**. Per ulteriori informazioni, vedere [Configurare lo stato del magazzino](#configure-stock-status).

1. Immettere il prodotto **[!UICONTROL Weight]**.

   >[!NOTE]
   >
   >Un prodotto configurabile deve avere sempre un peso. Se si seleziona **[!UICONTROL This item has no weight]** dal menu a discesa, quando si salva il prodotto verrà automaticamente modificato in **[!UICONTROL This item has weight]**.

1. Accettare l&#39;impostazione **[!UICONTROL Visibility]** predefinita di `Catalog, Search`.

1. Per inserire il prodotto nell&#39;elenco di [nuovi prodotti](../content-design/widget-new-products-list.md), selezionare la casella di controllo **[!UICONTROL Set Product as New]**.

1. Per assegnare le categorie al prodotto, fare clic sulla casella **[!UICONTROL Select…]** ed eseguire una delle operazioni seguenti:

   **Scegli una categoria esistente:**

   - Inizia a digitare nella casella per trovare una corrispondenza.

   - Selezionare la casella di controllo di ciascuna categoria da assegnare.

   ![Selezionare una o più categorie per il prodotto del bundle](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Crea una nuova categoria:**

   - Fare clic su **[!UICONTROL New Category]**.

   - Immettere **[!UICONTROL Category Name]** e scegliere **[!UICONTROL Parent Category]** per determinarne la posizione nella struttura del menu.

   - Fare clic su **[!UICONTROL Create Category]**.

1. Scegliere **[!UICONTROL Country of Manufacture]**.

   Gli attributi aggiuntivi possono essere visualizzati a seconda della serie di attributi. Puoi completarli in un secondo momento.

### Passaggio 5: salvare e continuare

Questo è un buon momento per salvare il tuo lavoro. Fare clic su **[!UICONTROL Save]** nell&#39;angolo superiore destro. Nella fase successiva, imposterai le configurazioni per ogni variante.

## Fase 2: Aggiungere varianti di prodotto

I passaggi seguenti mostrano come aggiungere configurazioni per più varianti. La barra di avanzamento nella parte superiore della pagina mostra la posizione corrente nel processo.

**Esempio:** per una camicia con 3 colori e 3 taglie, creerai 9 prodotti semplici con SKU univoci (uno per ogni combinazione). Per impostazione predefinita, il nome del prodotto e lo SKU per ogni variante si basano sul valore dell’attributo e sul nome del prodotto principale o sullo SKU.

### Passaggio 6: scegliere gli attributi di variante

1. Scorri verso il basso fino alla sezione _[!UICONTROL Configurations]_&#x200B;e fai clic su **[!UICONTROL Create Configurations]**.

   ![Configurazioni](./assets/product-configurable-create-configurations.png){width="600" zoomable="yes"}

1. Seleziona la casella di controllo di ciascun attributo da includere come variante.

   Per questo esempio, sono selezionati `color` e `size`.

   ![Seleziona attributi](./assets/product-create-configurable-step1.png){width="600" zoomable="yes"}

   L’elenco include tutti gli attributi del set di attributi che possono essere utilizzati in un prodotto configurabile.

1. Se è necessario aggiungere un attributo, fare clic su **[!UICONTROL Create New Attribute]** ed eseguire le operazioni seguenti:

   - Completa le proprietà dell’attributo.

   - Fare clic su **[!UICONTROL Save Attribute]**.

   - Selezionare la casella di controllo per l&#39;attributo.

1. Fare clic su **[!UICONTROL Next]** nell&#39;angolo superiore destro.

### Passaggio 7: selezionare i valori degli attributi

1. Per ogni attributo, seleziona la casella di controllo dei valori applicabili al prodotto.

   ![Valori attributo](./assets/product-create-configurable-step2.png){width="600" zoomable="yes"}

1. Per ridisporre gli attributi, acquisire l&#39;icona _Riordina_ ( ![Icona Ordinamento](../assets/icon-sort-order.png) ) e spostare la sezione in una nuova posizione.

   L’ordine determina la posizione degli elenchi a discesa sulla pagina del prodotto.

1. Nella barra di avanzamento, fare clic su **[!UICONTROL Next]**.

### Passaggio 8: configurare immagini, prezzi e inventario

Questo passaggio determina le immagini, il prezzo e la quantità per ogni configurazione. Le opzioni disponibili sono le stesse per ciascuno di essi. Puoi applicare la stessa impostazione a tutte le SKU, applicare impostazioni univoche a ciascuna SKU o saltare le impostazioni per il momento.

#### Configurare le immagini

Scegli l’opzione di configurazione applicabile:

**Opzione 1: applicare un singolo set di immagini a tutti gli SKU**

1. Selezionare **[!UICONTROL Apply single set of images to all SKUs]**.

1. Individuare le immagini da includere nella raccolta prodotti o trascinarle nella casella.

![Usa le stesse immagini per tutti gli SKU](./assets/product-configurations-images-apply-single-set.png){width="600" zoomable="yes"}

**Opzione 2: applicare immagini univoche per ogni SKU**

Poiché l’immagine del prodotto principale è già caricata, utilizza questa opzione per caricare le immagini per ogni variante. Puoi aggiungere diverse immagini che appaiono nel carrello quando qualcuno acquista una variante specifica.

1. Selezionare **[!UICONTROL Apply unique images by attribute to each SKU]**.

1. Selezionare **[!UICONTROL Attribute]** illustrato dalle immagini, ad esempio `color`.

1. Per ogni valore di attributo, individua le immagini da utilizzare per la configurazione o trascinale nella casella.

   Se trascinate un&#39;immagine in una casella di valore, questa viene visualizzata anche nelle sezioni relative ad altri valori. Per eliminare un&#39;immagine, fare clic sull&#39;icona _Cestino_ (![Icona Cestino](../assets/icon-delete-trashcan-solid.png)).

   ![Immagini univoche per SKU](./assets/product-configurable-create-configurations-add-images-unique.png){width="600" zoomable="yes"}

#### Configurare i prezzi

>[!NOTE]
>
>Un prodotto configurabile non ha un proprio prezzo nel catalogo. Il prezzo del prodotto configurabile deriva dai suoi [!UICONTROL In Stock] prodotti secondari.

Scegli l’opzione di configurazione applicabile:

**Opzione 1: applicare lo stesso prezzo a tutti gli SKU**

1. Se il prezzo è lo stesso per tutte le varianti, selezionare **[!UICONTROL Apply single price to all SKUs]**.

1. Immettere **[!UICONTROL Price]**.

   ![Stesso prezzo per SKU](./assets/product-configurable-create-configurations-price-all-skus.png){width="600" zoomable="yes"}

**Opzione 2: applicare un prezzo diverso per ogni SKU**

1. Se il prezzo è diverso per ciascuna variante o per alcune varianti, selezionare **[!UICONTROL Apply unique prices by attribute to each SKU]**.

1. Selezionare **[!UICONTROL Attribute]** che rappresenta la base della differenza di prezzo.

1. Immettere **[!UICONTROL Price]** per ogni valore di attributo.

   In questo esempio, la dimensione XL costa di più.

   ![Prezzo univoco per SKU](./assets/product-configurable-create-configurations-price-unique.png){width="600" zoomable="yes"}

#### Configurare l’inventario

Scegli l’opzione di configurazione applicabile:

**Opzione 1: applicare la stessa quantità a tutti gli SKU**

Se la quantità è la stessa per tutti gli SKU, selezionare **[!UICONTROL Apply single quantity to each SKU]** e specificare la quantità.

_Singoli commercianti Source :_

Immettere **[!UICONTROL Quantity]**.

_Più commercianti Source che utilizzano [Inventory management &#x200B;](../inventory-management/introduction.md):_

Assegna origini e aggiungi quantità per tutte le varianti prodotto generate:

1. Selezionare l&#39;opzione **[!UICONTROL Apply single quantity to each SKU]**.

1. Per aggiungere un&#39;origine, fare clic su **[!UICONTROL Assign Sources]**.

1. Sfoglia o cerca un’origine da aggiungere. Seleziona la casella di controllo accanto alle origini del prodotto.

1. Inserire un importo scorte disponibili per origine.

   ![Quantità singola per tutti gli SKU, assegna origine](./assets/inventory-configure-product-quantity.png){width="600" zoomable="yes"}

**Opzione 2: applicare una quantità diversa per attributo**

_Singoli commercianti Source :_

Immettere **[!UICONTROL Quantity]** per ogni valore di attributo.

_Più commercianti Source che utilizzano [Inventory management &#x200B;](../inventory-management/introduction.md):_

Assegna origini e aggiungi quantità per tutte le varianti prodotto generate:

1. Selezionare **[!UICONTROL Apply unique quantity by attribute to each SKU]**.

1. Immetti **[!UICONTROL Quantity]** per ogni variante.

   ![Quantità diverse per attributo](./assets/product-configurations-quantity-different.png){width="600" zoomable="yes"}

Al termine della configurazione di immagini, prezzo e quantità, fare clic su **[!UICONTROL Next]** nell&#39;angolo superiore destro.

### Passaggio 9: generare le configurazioni di prodotto

Attendi che l’elenco dei prodotti venga visualizzato ed effettua una delle seguenti operazioni:

- Se si è soddisfatti delle configurazioni, fare clic su **[!UICONTROL Generate Products]**.

- Per apportare correzioni, fare clic su **[!UICONTROL Back]**.

![Rivedi riepilogo prima di generare varianti di prodotto](./assets/product-create-configurable-summary.png){width="600" zoomable="yes"}

Le varianti di prodotto correnti vengono visualizzate nella parte inferiore della sezione _Configurazione_.

![Configurazioni correnti](./assets/product-create-configurable-generated.png){width="600" zoomable="yes"}

### Passaggio 10: aggiungere immagini del prodotto

1. Scorri verso il basso ed espandi il ![selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Images and Videos]_.

1. Fai clic sul riquadro _Fotocamera_ e individua l&#39;immagine principale da utilizzare per il prodotto configurabile.

Per ulteriori informazioni, vedere [Immagini e video](product-images-and-video.md).

### Passaggio 11: Informazioni complete sul prodotto

Scorri verso il basso e completa le informazioni nelle sezioni seguenti, in base alle esigenze:

- [Contenuto](product-content.md)

- [Prodotti correlati, up-selling e cross-selling](related-products-up-sells-cross-sells.md)

- [Ottimizzazione motore di ricerca](product-search-engine-optimization.md)

- [Opzioni personalizzabili](settings-advanced-custom-options.md)

- [Prodotti nei siti Web](settings-basic-websites.md)

- [Progettazione](settings-advanced-design.md)

- [Opzioni regalo](product-gift-options.md)

## Fase 3: Pubblicare il prodotto

### Passaggio 12: pubblicare il prodotto

1. Se si è pronti a pubblicare il prodotto nel catalogo, impostare **[!UICONTROL Enable Product]** su `Yes`.

1. Effettuare una delle seguenti operazioni:

   **Metodo 1: salvataggio e anteprima**

   - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]**.

   - Per visualizzare il prodotto nell&#39;archivio, scegli **[!UICONTROL Customer View]** nel menu _Amministratore_ ( ![Freccia menu](../assets/icon-menu-down-arrow-black.png) ).

   L’archivio si apre in una nuova scheda del browser.

   ![Visualizzazione clienti](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Metodo 2: Salva e chiudi**

   Scegliere _[!UICONTROL Save]_&#x200B;dal menu ![&#x200B; ( &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"}Freccia menu **[!UICONTROL Save & Close]**).

## Configurare lo stato delle scorte

Lo stato delle scorte di prodotto configurabile è diverso dallo stato delle scorte di prodotto semplice. Per un prodotto configurabile, lo stato del magazzino fa parte di un calcolo di **_più criteri_**.

### Funzionamento dello stato delle scorte

Principi chiave del comportamento dello stato delle scorte:

| Hai Impostato Lo Stato Su | Risultato | Controllato Da Prodotti Bambini? |
|---|---|---|
| `Out of Stock` (manuale) | Visualizza sempre `Out of Stock` in Admin and Storefront | No - rimane finché non viene modificato manualmente in `In Stock` |
| `In Stock` (manuale) | Lo stato è dinamico in base ai prodotti secondari | Parziale - vedere i dettagli di seguito |

{style="table-layout:auto"}

### Se impostato su &quot;In magazzino&quot;

Quando imposti manualmente lo stato delle scorte di prodotto configurabili su `In Stock`, questo si comporta in modo diverso a seconda dell&#39;impostazione dell&#39;inventario:

**Solo con origine/titolo predefinito:**

- **Admin and Storefront:** lo stato del magazzino riflette automaticamente la disponibilità del prodotto figlio

**Con almeno un&#39;origine/magazzino personalizzata:**

- **Vetrina:** lo stato del magazzino riflette automaticamente la disponibilità del prodotto figlio
- **Amministratore:** rimane come `In Stock` fino a quando non viene modificato manualmente (non controllato dai prodotti secondari)

>[!NOTE]
>
>Le scorte e le origini personalizzate fanno parte dell&#39;estensione [Inventory management](../inventory-management/sources-stocks.md). Si consiglia vivamente di utilizzare questo strumento esclusivamente per la gestione delle scorte e dell’origine. Le funzioni di origine e magazzino predefinite fanno parte del modulo `CatalogInventory`, che è ora obsoleto.

### Modifiche manuali dello stato delle scorte

Se imposti manualmente lo stato delle scorte su `Out of Stock` (tramite l&#39;azione dell&#39;utente amministratore, l&#39;importazione del file o una chiamata API), rimarrà `Out of Stock` sia nell&#39;Admin che nello Storefront fino a quando non lo cambi manualmente in `In Stock`. Non è influenzato dallo stato delle scorte dei prodotti secondari.

## Configurazione del sistema (opzionale)

### Visualizzare le immagini delle varianti nelle miniature del carrello

Se disponi di immagini diverse per ogni variante, puoi configurare il sistema per visualizzare l’immagine corretta per la miniatura del carrello acquisti.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) nella sezione _[!UICONTROL Shopping Cart]_.

1. Imposta **[!UICONTROL Configurable Product Image]** su `Product Thumbnail Itself`.

1. Fare clic su **[!UICONTROL Save Config]**.

   ![Carrello acquisti - immagine del prodotto configurabile](./assets/config-checkout-configurable-product.png){width="600" zoomable="yes"}

## Considerazioni chiave

- **Tipi di variante:** gli acquirenti possono selezionare le opzioni dal menu a discesa, selezione multipla, campione visivo e campioni di testo. Ogni opzione è un prodotto separato e semplice.

- **Registrazione inventario:** A differenza dei prodotti semplici con opzioni personalizzate, i prodotti configurabili tengono traccia dell&#39;inventario per ogni variante in modo indipendente.

- **Tipi di prodotto secondari:** I prodotti secondari possono essere prodotti semplici o virtuali **senza opzioni personalizzate**. Per rendere virtuali i prodotti secondari, selezionare `Тhis item has no weight` per l&#39;impostazione **[!UICONTROL Weight]** per ogni elemento secondario.

- **Assegnazione globale:** i prodotti secondari vengono assegnati e non assegnati al prodotto configurabile **globalmente** in tutti i siti Web, gli archivi e le visualizzazioni dello store contemporaneamente.

- **Prezzi:** Un prodotto configurabile non ha un proprio prezzo nel catalogo. Il prezzo visualizzato proviene dai suoi [!UICONTROL In Stock] prodotti secondari.

- **Attributi:** gli attributi della variante devono avere un ambito globale e i clienti devono scegliere un valore. Gli attributi devono essere inclusi nel set di attributi utilizzato per il prodotto configurabile.

- **Miniature carrello:** La miniatura del carrello può visualizzare l&#39;immagine dal record di prodotto configurabile o dalla variante di prodotto. Vedi [Configurazione di sistema](#system-configuration-optional) qui sopra.

- **Comportamento campione:** [Gli attributi campione](swatches.md#create-swatches-for-products) possono essere configurati in modo da non visualizzare le immagini prodotto semplici corrispondenti quando il campione è selezionato impostando **[!UICONTROL Update Product Preview Image]** su `No` nella pagina di modifica degli attributi.

- **Comportamento galleria immagini:** il tema controlla il comportamento della Galleria immagini quando gli utenti passano da una configurazione di prodotto all&#39;altra. Il comportamento predefinito per il tema _Vuoto_ sostituisce le immagini del prodotto configurabili principali con la variante selezionata. Per il tema Luma, il comportamento predefinito consiste nell’anteporre le immagini della variante selezionata alle immagini del prodotto configurabili principali.
