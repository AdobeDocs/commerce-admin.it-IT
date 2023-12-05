---
title: Prodotto bundle
description: Scopri come creare un pacchetto di prodotti che consenta agli acquirenti di creare un prodotto personalizzato nel tuo negozio.
exl-id: dfa31eb8-2330-44eb-889b-5d10ce56ef13
feature: Catalog Management, Products
source-git-commit: eca41f653aa6499743982199f067d6df86079010
workflow-type: tm+mt
source-wordcount: '1547'
ht-degree: 0%

---

# Prodotto bundle

Un bundle è un _crea il tuo_, prodotto personalizzabile. Ogni elemento in un bundle può essere basato su uno dei seguenti tipi di prodotto:

- [Prodotto semplice](product-create-simple.md)
- [Prodotto virtuale](product-create-virtual.md)

![Prodotto bundle](./assets/product-bundle.png){width="700" zoomable="yes"}

Le opzioni vengono visualizzate quando il cliente fa clic su **[!UICONTROL Customize]** o **[!UICONTROL Add to Cart]**. Poiché i prodotti inclusi nel bundle variano, lo SKU, il prezzo e il peso possono essere impostati su un valore dinamico o fisso.

>[!NOTE]
>
>Il prezzo minimo annunciato (MAP) non è disponibile per i prodotti bundle che utilizzano prezzi dinamici.

>[!NOTE]
>
>Il pacchetto principale viene sempre visualizzato automaticamente come prodotto di up-sell per tutti i suoi prodotti secondari.

Se [Acquisto immediato](../stores-purchase/checkout-instant-purchase.md) è disponibile, il _Acquisto immediato_ sotto il _Aggiungi al carrello_ per ogni elemento nel bundle.

![Personalizza bundle](./assets/product-bundle-customize.png){width="600" zoomable="yes"}

Le seguenti istruzioni spiegano come creare un pacchetto di prodotti utilizzando un [modello di prodotto](attribute-sets.md), campi obbligatori e impostazioni di base. Ogni campo obbligatorio è contrassegnato da un asterisco rosso (`*`). Al termine delle nozioni di base, puoi completare le altre impostazioni del prodotto in base alle esigenze.

## Passaggio 1: scegliere il tipo di prodotto

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Nell&#39;angolo in alto a destra del _[!UICONTROL Add Product]_( ![Freccia del menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), scegliere **[!UICONTROL Bundle Product]**.

   ![Aggiungi prodotto bundle](./assets/product-add-bundle.png){width="700" zoomable="yes"}

## Passaggio 2: scegliere la serie di attributi

Per scegliere il [set di attributi](attribute-sets.md) utilizzato come modello per il prodotto, eseguire una delle operazioni seguenti:

- Per **[!UICONTROL Search]**, immettere il nome della serie di attributi,
- Nell&#39;elenco, scegliere il set di attributi che si desidera utilizzare.

Il modulo viene aggiornato per riflettere la modifica.

![Scegli modello](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Passaggio 3: completare le impostazioni richieste

1. Inserisci il prodotto **[!UICONTROL Product Name]**.

1. Accettare il valore predefinito **[!UICONTROL SKU]** in base al nome del prodotto o inserisci un valore diverso.

   Per determinare il tipo di SKU assegnato a ciascun elemento del bundle, effettuate le seguenti operazioni:

   - A **[!UICONTROL Dynamic SKU]** possono essere assegnate automaticamente a ciascun elemento del bundle aggiungendo un suffisso allo SKU predefinito. Per impostazione predefinita, è impostato su `Yes`.

   - Se preferisci assegnare uno SKU univoco per ciascun elemento del bundle, imposta **[!UICONTROL Dynamic SKU]** a `No`.

   ![SKU dinamica e prezzo](./assets/product-bundle-manual-sku.png){width="600" zoomable="yes"}

1. Per determinare il prezzo del bundle, effettuate una delle seguenti operazioni:

   - Per fare in modo che il prezzo rifletta le opzioni scelte dal cliente, impostare **[!UICONTROL Dynamic Price]** a `Yes` e lasciare **[!UICONTROL Price]** vuoto.

   - Per addebitare un prezzo fisso per il bundle, imposta **[!UICONTROL Dynamic Price]** a `No` e immetti **[!UICONTROL Price]** che desideri caricare per il bundle.

   >[!NOTE]
   >
   >[!UICONTROL Special Price] e [!UICONTROL Customer Group Price] (Prezzo livello) vengono sempre impostati come percentuale di sconto per tutti i tipi di prodotto del bundle.

1. Poiché il prodotto non è ancora pronto per la pubblicazione, imposta **[!UICONTROL Enable Product]** a `No`.

1. Clic **[!UICONTROL Save]** e continua.

   Quando il prodotto viene salvato, la [Visualizzazione store](introduction.md#product-scope) selettore viene visualizzato nell&#39;angolo superiore sinistro.

1. Scegli la **[!UICONTROL Store View]** dove il prodotto deve essere disponibile.

   ![Scegli la vista dello store](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Passaggio 4: completare le impostazioni di base

1. Se per il bundle è stata impostata la determinazione prezzi fissa, impostare **[!UICONTROL Tax Class]** a uno dei seguenti elementi:

   - `None`
   - `Taxable Goods`

   Se il bundle dispone di Dynamic Pricing, l&#39;imposta viene determinata per **_ogni_** elemento bundle. Se il bundle dispone di Determinazione prezzi, l&#39;imposta viene determinata per **_intero_** prodotto bundle.

1. Prendi nota di quanto segue:

   - Il **[!UICONTROL Quantity]** non è disponibile perché il valore viene determinato per ogni elemento del bundle.

   - Per impostazione predefinita, il **[!UICONTROL Stock Status]** è impostato su `In Stock`.

1. Per determinare lo spessore del fascio, effettuate una delle seguenti operazioni:

   - Per fare in modo che il peso rifletta le opzioni scelte dal cliente, impostare **[!UICONTROL Dynamic Weight]** set `Yes` e lasciare **[!UICONTROL Weight]** vuoto.

   - Per assegnare un peso fisso al fascio, impostare **[!UICONTROL Dynamic Weight]** a `No` e immetti **[!UICONTROL Weight]** del bundle.

   ![Spessore dinamico](./assets/product-bundle-dynamic-weight.png){width="600" zoomable="yes"}

1. Per inserire il prodotto nell’elenco di [nuovi prodotti](../content-design/widget-new-products-list.md), seleziona la **[!UICONTROL Set Product as New]** casella di controllo.

1. Accetta il valore predefinito **[!UICONTROL Visibility]** impostazione di `Catalog, Search`.

1. Da assegnare _[!UICONTROL Categories]_al prodotto, fai clic su **[!UICONTROL Select…]**ed effettuare una delle seguenti operazioni:

   **Scegli una categoria esistente:**

   - Inizia a digitare nella casella fino a trovare una corrispondenza.

   - Selezionare la casella di controllo di ciascuna categoria da assegnare.

   ![Seleziona una o più categorie per il prodotto bundle](./assets/product-create-categories.png){width="600" zoomable="yes"}

   **Creare una categoria:**

   - Clic **[!UICONTROL New Category]**.

   - Inserisci il **[!UICONTROL Category Name]** e scegli la **[!UICONTROL Parent Category]**, che ne determina la posizione nella struttura del menu.

   - Clic **[!UICONTROL Create Category]**.

1. Scegli la **[!UICONTROL Country of Manufacture]**.

   Potrebbero essere presenti attributi aggiuntivi che descrivono il prodotto. La selezione varia a seconda del set di attributi e può essere completata in un secondo momento.

## Passaggio 5: aggiungere gli elementi del bundle

Il _[!UICONTROL Bundle Items]_Questa sezione viene utilizzata per aggiungere elementi a un tipo di prodotto Bundle e per modificare la selezione corrente di elementi.

![Elementi del bundle definiti per un prodotto](./assets/product-bundle-items-ball.png){width="600" zoomable="yes"}

1. Scorri verso il basso fino a _Elementi bundle_ sezione e set **[!UICONTROL Ship Bundle Items]** a uno dei seguenti elementi:

   - `Separately`
   - `Together`

   Se si seleziona `Together`, tutti gli elementi del bundle devono essere assegnati allo stesso [sorgente](../inventory-management/sources-manage.md).

1. Clic **[!UICONTROL Add Option]** ed effettuare le seguenti operazioni:

   - Immetti un **[!UICONTROL Option Title]** da utilizzare come etichetta del campo.

   - Imposta **[!UICONTROL Input Type]** a uno dei seguenti elementi:

      - `Drop-down`
      - `Radio buttons`
      - `Checkbox`
      - `Multiple Select`

   - Per impostare il campo come obbligatorio, selezionare **[!UICONTROL Required]** casella di controllo.

   - Clic **[!UICONTROL Add Products to Option]** e seleziona la casella di controllo di ciascun prodotto che desideri includere in questa opzione.

     Se sono presenti molti prodotti, utilizza i filtri elenco e i controlli di impaginazione per trovare i prodotti necessari.

   - Clic **[!UICONTROL Add Selected Products]**.

     ![Aggiungi prodotti selezionati](./assets/product-bundle-add-products-to-option.png){width="600" zoomable="yes"}

   - Dopo che gli elementi vengono visualizzati nel _Opzioni_ sezione, scegli un elemento come **[!UICONTROL Default]** selezione.

   - In _Quantità predefinita_ inserire la quantità di ciascun articolo da aggiungere al bundle quando un cliente sceglie l&#39;articolo.

   - Per consentire ai clienti di modificare la quantità di un articolo del bundle, seleziona **[!UICONTROL User Defined]**.


     >[!NOTE]
     >
     >La quantità può essere un valore predefinito o definito dall&#39;utente. Tuttavia, non assegnare il _[!UICONTROL User Defined]_proprietà per la casella di controllo o per la selezione multipla dei tipi di input.

     Per impostazione predefinita, la quantità predefinita inclusa in un articolo del bundle non può essere modificata dal cliente. Tuttavia, il cliente può inserire la quantità dell&#39;articolo da includere nel bundle.

     Ad esempio, se la quantità predefinita della sfera di stato dello sprite è impostata su `2` e gli ordini dei clienti `4` di tale opzione di bundle, il numero totale di palle acquistate è `8`.

     ![Dettagli elemento](./assets/product-bundle-item-detail.png){width="600" zoomable="yes"}

1. Ripeti questi passaggi per ogni elemento da aggiungere al bundle.

1. Per modificare l’ordine degli elementi in una sezione bundle, fai clic su _Sposta_ ( ![Icona Sposta](../assets/icon-move.png) ) all&#39;inizio della riga e trascinare l&#39;elemento nella posizione desiderata.

   ![Modifica l&#39;ordine degli elementi del bundle](./assets/product-bundle-items-move.png){width="600" zoomable="yes"}

   L’ordine degli elementi può anche essere modificato nei dati di un prodotto bundle esportato e quindi reimportato nel catalogo. Per ulteriori informazioni, consulta [Importazione prodotti bundle](../systems/data-transfer-bundle-products.md).

   Per avere una migliore visualizzazione del workspace, comprimere prima ogni sezione e quindi trascinarle nella posizione desiderata.

1. Per rimuovere un elemento dal bundle, fai clic su **[!UICONTROL Delete]** ( ![Icona Elimina](../assets/icon-delete-trashcan.png) ).

1. Al termine, fai clic su **[!UICONTROL Save]**.

## Passaggio 6: Completare le informazioni sul prodotto

Scorri verso il basso e completa le informazioni nelle sezioni seguenti, in base alle esigenze:

- [Contenuto](product-content.md)
- [Immagini e video](product-images-and-video.md)
- [Ottimizzazione motore di ricerca](product-search-engine-optimization.md)
- [Prodotti correlati, up-selling e cross-selling](related-products-up-sells-cross-sells.md)
- [Opzioni personalizzabili](settings-advanced-custom-options.md)
- [Prodotti nei siti Web](settings-basic-websites.md)
- [Progettazione](settings-advanced-design.md)
- [Opzioni regalo](product-gift-options.md)

## Passaggio 7: pubblicare il prodotto

1. Se sei pronto per pubblicare il prodotto nel catalogo, imposta **[!UICONTROL Enable Product]** a `Yes` ( ![Attiva/disattiva sì](../assets/toggle-yes.png) ).

1. Effettuare una delle seguenti operazioni:

   **Metodo 1:** Salva e visualizza in anteprima

   - Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]**.

   - Per visualizzare il prodotto nel tuo negozio, scegli **[!UICONTROL Customer View]** il _Amministratore_ ( ![Freccia del menu](../assets/icon-menu-down-arrow-black.png) ).

     L’archivio si apre in una nuova scheda del browser.

   ![Visualizzazione cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   **Metodo 2:** Salva e chiudi

   Il giorno _[!UICONTROL Save]_( ![Freccia del menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), scegliere **[!UICONTROL Save & Close]**.

## Controlli di input

| Controllo | Descrizione | Esempio |
|--- |--- |--- |
| [!UICONTROL Drop-down] | Visualizza un elenco a discesa di opzioni con il nome e il prezzo del prodotto. È possibile selezionare un solo elemento. | ![Elenchi a discesa](./assets/product-bundle-input-type-drop-down.png){width="200"} |
| [!UICONTROL Radio Buttons] | Visualizza un pulsante di scelta per ogni opzione, seguito dal nome del prodotto e dal prezzo. È possibile selezionare un solo elemento. | ![Pulsanti di scelta](./assets/product-bundle-input-type-radio-buttons.png){width="200"} |
| [!UICONTROL Checkbox] | Visualizza una casella di controllo per ogni opzione, seguita dal nome del prodotto e dal prezzo. È possibile selezionare più elementi. | ![Casella di controllo](./assets/product-bundle-input-type-checkbox.png){width="200"} |
| [!UICONTROL Multiple Select] | Visualizza un elenco di opzioni con il nome e il prezzo del prodotto. Per selezionare più elementi, tenere premuto Ctrl (PC) o Comando (Mac) e fare clic su ogni elemento. | ![Selezione multipla](./assets/product-bundle-input-type-multiple-select.png){width="200"} |

{style="table-layout:auto"}

## Descrizioni dei campi

| Campo | Descrizione |
|--- |--- |
| [!UICONTROL SKU] | Determina se a ogni elemento viene assegnato uno SKU dinamico o variabile o se per il bundle viene utilizzato uno SKU fisso. Opzioni: `Fixed` / `Dynamic` |
| [!UICONTROL Weight] | Specifica se il peso viene calcolato in base agli elementi selezionati o se è fisso per l&#39;intero bundle. Opzioni: `Fixed` / `Dynamic` |
| [!UICONTROL Price View] | Determina se il prezzo del prodotto viene visualizzato come intervallo, dal meno costoso al più costoso (fascia di prezzo) o con il meno costoso indicato (come basso come). Opzioni: `Price Range` / `As Low As` |
| Articoli del bundle di spedizione | Specifica se i singoli articoli possono essere spediti separatamente. |

{style="table-layout:auto"}

## Stato scorte prodotto del bundle

Lo stato delle scorte dei prodotti del bundle è **_modificato automaticamente in esaurito_** quando si verifica uno di questi scenari:

- Tutte le opzioni sono facoltative e tutti i prodotti associati sono _Esaurito_.

- Alcune opzioni sono obbligatorie e i prodotti associati alle opzioni obbligatorie sono _Esaurito_.

Lo stato delle scorte dei prodotti del bundle è **_non modificato automaticamente in esaurito_** quando si verifica uno di questi scenari:

- Tutte le opzioni sono facoltative e almeno un prodotto associato è _In magazzino_.

- Sono necessarie alcune opzioni e almeno un prodotto associato in ciascuna opzione richiesta è _In magazzino_.

## Aspetti da ricordare

![Casella di controllo](../assets/checkbox.png) I clienti possono _costruisci il proprio_ prodotto bundle.

![Casella di controllo](../assets/checkbox.png) Gli elementi bundle possono essere prodotti semplici o virtuali senza opzioni personalizzate.

![Casella di controllo](../assets/checkbox.png) La visualizzazione del prezzo può essere impostata su `Price Range` o `As Low As`.

![Casella di controllo](../assets/checkbox.png) SKU e Peso possono essere `Fixed` o `Dynamic`.

![Casella di controllo](../assets/checkbox.png) La quantità può essere un valore predefinito o definito dall&#39;utente. Tuttavia, non assegnare il _[!UICONTROL User Defined]_proprietà per la casella di controllo o per la selezione multipla dei tipi di input.

![Casella di controllo](../assets/checkbox.png) Gli articoli in bundle possono essere spediti insieme o separatamente.

![Casella di controllo](../assets/checkbox.png) Il pacchetto principale viene sempre visualizzato automaticamente come prodotto di up-sell per tutti i suoi prodotti secondari.

![Casella di controllo](../assets/checkbox.png) [!UICONTROL Special Price] e [!UICONTROL Customer Group Price] (Prezzo livello) vengono sempre impostati come percentuale di sconto per tutti i tipi di prodotto del bundle.