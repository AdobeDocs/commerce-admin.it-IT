---
title: Creare categorie
description: Puoi creare tutte le sottocategorie aggiuntive necessarie, in base alla profondità massima del menu impostata nella configurazione.
exl-id: 8ba5fc1a-3bf2-4a29-bbc3-709fc0ad7497
feature: Catalog Management, Categories
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 0%

---

# Creare categorie

La struttura delle categorie del catalogo è simile a una struttura capovolta, con la directory principale in alto. Ogni sezione della struttura può essere espansa e compressa. Qualsiasi categoria disabilitata o nascosta è disabilitata. Le categorie al primo livello (al di sotto del [radice](category-root.md)) vengono in genere visualizzate come opzioni nella [menu principale](navigation-top.md). Puoi creare tutte le sottocategorie aggiuntive necessarie, in base alla profondità massima del menu impostata nella configurazione. Le categorie possono essere trascinate e rilasciate in altre posizioni nella struttura. Il numero ID categoria viene visualizzato tra parentesi dopo il nome della categoria nella parte superiore della pagina.

Per un sito Web con più [store](../stores-purchase/stores.md#add-stores), puoi creare una categoria principale diversa per ogni archivio che definisce il set di categorie utilizzato per il [navigazione superiore](navigation-top.md).

![Albero categoria](./assets/category-selected.png){width="700" zoomable="yes"}

## Best practice

Utilizza queste best practice per pianificare e creare categorie.

### Struttura delle categorie

La struttura delle categorie nel menu principale può influire sulla customer experience e sulle prestazioni. Come best practice, è consigliabile identificare una categoria superiore generale ed evitare di avere altre categorie con lo stesso nome. Ad esempio, invece di avere più categorie per &quot;Bambini&quot; organizzate in dipartimenti diversi, come `Clothing/Kids`, `Shoes/Kids`, `Accessories/Kids`. Può essere più efficiente creare la categoria principale di livello superiore `Kids`, quindi crea le sottocategorie di seguito in base alle esigenze. Assicurati di essere coerente con la struttura delle categorie e utilizza lo stesso approccio per tutti i tipi di prodotto nel catalogo.

### Regole aziendali e automazione

Quando si utilizza la logica di business per visualizzare elementi simili in una pagina di catalogo o per impostare una promozione personalizzata, un processo automatizzato o criteri di ricerca, è necessario considerare la struttura delle categorie e i valori degli attributi disponibili. Ad esempio, se specifichi &quot;polo&quot; come categoria principale, i risultati potrebbero includere prodotti misti di genere e non appropriati per l’età. Tuttavia, se si abbina una specifica sottocategoria di polo camicie, i risultati sono più ristretti e più probabile che attragga un cliente specifico. I risultati possono essere ancora più specifici se combinati con altri valori di attributo destinati a un cliente specifico. Considera il numero di prodotti che devono essere filtrati e recuperati quando si fa riferimento a un percorso di categoria specifico. La differenza nei risultati può essere notevole. Considera i diversi risultati restituiti dai seguenti percorsi di categoria:

- `[Category:  All Products/Shirts/Father's Day/Polos/Sale]`
- `[Category Path: Men/Shirts/Polos]`
- `[Child Category: Polos]`

È importante definire chiaramente le relazioni categoriche, ad esempio:

- categoria principale
- sottocategoria
- percorso categoria

Definisci anche le parole chiave e gli attributi associati, ad esempio:

- disponibilità
- prezzo di vendita
- brand
- dimensione
- colore

## Passaggio 1: creare una categoria

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Categories]**.

1. Imposta **[!UICONTROL Store View]** per determinare dove sarà disponibile la nuova categoria.

1. Nell&#39;albero delle categorie selezionare la categoria padre della nuova categoria.

   Il livello padre è superiore alla nuova categoria.

   Se inizi dall’inizio senza dati, potrebbero essere presenti solo due categorie nell’elenco: _Categoria predefinita_, che è la radice, e un _Categoria di esempio_

1. Clic **[!UICONTROL Add Subcategory]**.

## Passaggio 2: Completare le informazioni di base

1. Se si desidera che la categoria sia immediatamente disponibile nello store, impostare **[!UICONTROL Enable Category]** a `Yes`.

1. Per includere la categoria nel [navigazione superiore](navigation-top.md), impostato **[!UICONTROL Include in Menu]** a `Yes`.

1. Inserisci il **[!UICONTROL Category Name]**.

   ![Informazioni di base sulle categorie](./assets/catalog-categories-currently-active.png){width="500" zoomable="yes"}

1. click **[!UICONTROL Save]** e continua.

## Passaggio 3: completare il contenuto della categoria

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Content]** sezione.

   ![Contenuto categoria](./assets/category-content.png){width="600" zoomable="yes"}

1. Per visualizzare un **[!UICONTROL Category Image]** nella parte superiore della pagina, puoi caricare una tua immagine o utilizzare un’immagine esistente in [Storage multimediale](../content-design/media-storage.md).

   - Per caricare la tua immagine, fai clic su **[!UICONTROL Upload]** e scegliere l&#39;immagine che si desidera rappresentare per la categoria.

   - Per utilizzare le immagini da Media Storage, fare clic su **[!UICONTROL Select from Gallery]** e seleziona l’immagine che desideri rappresentare la categoria.

   >[!NOTE]
   >
   >All&#39;interno di Media Gallery, è inoltre possibile utilizzare [Integrazione di Adobe Stock](../content-design/adobe-stock.md) per trovare un&#39;immagine appropriata facendo clic su **[!UICONTROL Search Adobe Stock]**.

1. Per **[!UICONTROL Description]**, immetti il testo o altro contenuto che desideri visualizzare nella pagina di destinazione della categoria.

   Per ulteriori informazioni, consulta [Contenuto categoria](categories-content-settings.md).

1. Per includere un blocco di contenuto nella pagina di destinazione della categoria, scegli la **[!UICONTROL CMS Block]** che desideri visualizzare.

1. click **[!UICONTROL Save]** e continua.

## Passaggio 4: completare le impostazioni dello schermo

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Display Setting]** sezione.

   ![Impostazioni di visualizzazione](./assets/category-display-settings.png){width="600" zoomable="yes"}

   Per ulteriori informazioni su queste opzioni, vedere Per ulteriori informazioni su queste opzioni, vedere  [Impostazioni di visualizzazione](categories-display-settings.md).

1. Imposta **[!UICONTROL Display Mode]** a uno dei seguenti elementi:

   - `Products Only`
   - `Static Block Only`
   - `Static Block and Products`

1. Se si desidera che la pagina della categoria includa _`Filter by Attribute`_sezione della navigazione a livelli, set **[!UICONTROL Anchor]**a `Yes`.

1. Per **[!UICONTROL Available Product Listing Sort By]** selezionare uno o più valori disponibili per consentire ai clienti di ordinare l&#39;elenco. Questa impostazione non si applica al [!DNL Live Search] [Widget pagina elenco prodotti](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

   Per impostazione predefinita, sono inclusi tutti i valori disponibili. Deseleziona il **[!UICONTROL Use All]** per modificare le selezioni. Ad esempio, i valori possono includere:

   - `Position`
   - `Product Name`
   - `Price`

1. Per impostare l&#39;ordinamento predefinito per la categoria, scegliere **[!UICONTROL Default Product Listing Sort By]** valore. Questa impostazione non si applica al [!DNL Live Search] [Widget pagina elenco prodotti](https://experienceleague.adobe.com/en/docs/commerce-merchant-services/live-search/live-search-storefront/plp-styling).

1. Per modificare la navigazione a livelli predefinita [gradino di prezzo](navigation-layered.md#configure-price-navigation) effettuare le seguenti operazioni:

   - Deseleziona il **[!UICONTROL Use Config Settings]** casella di controllo.

   - Inserire il valore da utilizzare come livello di prezzo incrementale per la navigazione su più livelli.

1. Clic **[!UICONTROL Save]** e continua.

## Passaggio 5: completare le impostazioni di ottimizzazione del motore di ricerca

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Search Engine Optimization Settings]** sezione.

   ![Ottimizzazione dei motori di ricerca](./assets/categories-search-engine-optimization.png){width="600" zoomable="yes"}

   Per ulteriori informazioni su queste opzioni, vedi [Ottimizzazione dei motori di ricerca](categories-search-engine-optimization.md).

1. Completa quanto segue [metadati](../merchandising-promotions/meta-data.md) per la categoria:

   - [!UICONTROL Meta Title]
   - [!UICONTROL Meta Keywords]
   - [!UICONTROL Meta Description]

1. Clic **[!UICONTROL Save]** e continua.

## Passaggio 6: scegliere i prodotti nella categoria

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Products in Category]** sezione.

   ![Prodotti nella categoria](./assets/category-products-in-category.png){width="600" zoomable="yes"}

   Per ulteriori informazioni su queste opzioni, vedi [Prodotti nella categoria](categories-product-assignments.md).

1. Se necessario, utilizza [filtri](../getting-started/admin-grid-controls.md) per trovare i prodotti.

   Per visualizzare tutti i record non ancora inclusi nella categoria, impostare il selettore di record nella prima colonna su `No` e fai clic su **[!UICONTROL Search]**.

1. Nella prima colonna selezionare la casella di controllo relativa a ciascun prodotto da includere nella categoria.

1. Clic **[!UICONTROL Save]** e continua.

## Passaggio 7: impostare le autorizzazioni per la categoria

{{ee-feature}}

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Category Permissions]** sezione.

1. Per un&#39;installazione multisito, scegliere **[!UICONTROL Website]** dove si applicano le autorizzazioni per la categoria.

1. Scegli la **[!UICONTROL Customer Group]** dove si applicano le autorizzazioni per la categoria.

   ![Adobe Commerce B2B](../assets/b2b.svg) ([Adobe Commerce B2B](../b2b/introduction.md) solo) Se necessario, è possibile scegliere un **[!UICONTROL Shared Catalog]** invece.

1. Imposta le seguenti autorizzazioni in base alle esigenze:

   - [!UICONTROL Browsing Category]
   - [!UICONTROL Display Product Prices]
   - [!UICONTROL Add to Cart]

1. Per aggiungere un’altra regola di autorizzazione, fai clic su **[!UICONTROL New Permission]** e ripetere il processo.

   ![Autorizzazioni categoria](./assets/category-create-permissions.png){width="600" zoomable="yes"}

## Passaggio 8: completare le impostazioni di progettazione

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Design]** sezione.

1. Impostare le impostazioni di progettazione in base alle esigenze:

   - ([Adobe Commerce B2B](../b2b/introduction.md) solo) Per applicare le impostazioni di progettazione della categoria padre a questa categoria, impostare **[!UICONTROL Use Parent Category Settings]** a `Yes`.

   - Per modificare la struttura delle pagine delle categorie, scegliere **[!UICONTROL Theme]** che desideri applicare.

   - Per modificare il layout delle colonne delle pagine delle categorie, scegliere **[!UICONTROL Layout]** che desideri applicare.

   - Per immettere un codice personalizzato, immettere un codice XML valido nel **[!UICONTROL Layout Update XML]** casella.

   - Per utilizzare lo stesso design per le pagine di prodotto, imposta **[!UICONTROL Apply Design to Products]** a `Yes`.

   ![Impostazioni di progettazione](./assets/category-design.png){width="600" zoomable="yes"}

1. ![Magento Open Source](../assets/open-source.svg) (Solo Magento Open Source) Per pianificare l&#39;aggiornamento della progettazione per un periodo di tempo specifico, effettuare le seguenti operazioni:

   - Espandi _[!UICONTROL Schedule Design Update]_sezione.

   - Utilizza il calendario (![Icona Calendario](../assets/icon-calendar.png)) per scegliere il programma di aggiornamento **[!UICONTROL from]** e **[!UICONTROL to]** date.

   ![Aggiornamento della progettazione pianificato](./assets/category-scheduled-design-update.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save]**.
