---
title: Prodotto raggruppato
description: Scopri come creare un prodotto raggruppato costituito da semplici prodotti autonomi presentati come un gruppo.
exl-id: af42b7fc-27f2-4c5a-b504-a70a324fae76
feature: Catalog Management, Products
source-git-commit: 140930df515d1e0604b18a4ebf689254b9487b53
workflow-type: tm+mt
source-wordcount: '1055'
ht-degree: 0%

---

# Prodotto raggruppato

Un prodotto raggruppato è costituito da semplici prodotti autonomi presentati come un gruppo. Puoi offrire varianti di un singolo prodotto o raggrupparle per stagione o tema. Presentare un prodotto raggruppato può incentivare i clienti ad acquistare articoli aggiuntivi. Un prodotto raggruppato offre un modo semplice per offrire varianti di un prodotto e elencarle tutte sulla stessa pagina.

Ad esempio, è possibile vendere flatware open stock e elencare ogni tipo di utensile utilizzato in un luogo formale. Alcuni potrebbero ordinare più forchette per insalata, forchette di pesce, forchette per la cena, coltelli per la cena, coltelli per il pesce, coltelli per il burro, cucchiai da minestra e cucchiai da dessert. Altri clienti potrebbero ordinare una semplice forchetta, un coltello e un cucchiaio. I clienti possono ordinare qualsiasi numero di ogni elemento come desiderano.

Anche se vengono presentati come un gruppo, ogni prodotto del gruppo viene acquistato come un articolo separato. Nel carrello, ogni articolo e la quantità acquistata vengono visualizzati come una riga distinta.

Le istruzioni seguenti illustrano il processo di creazione di un prodotto raggruppato utilizzando un [modello di prodotto](attribute-sets.md), campi obbligatori e impostazioni di base. Ogni campo obbligatorio è contrassegnato da un asterisco rosso (`*`). Al termine delle nozioni di base, puoi completare le altre impostazioni del prodotto in base alle esigenze.

![Prodotto Raggruppato](./assets/product-grouped.png){width="700" zoomable="yes"}

## Passaggio 1: scegliere il tipo di prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Scegliere **[!UICONTROL Grouped Product]** dal menu _[!UICONTROL Add Product]_( ![Freccia menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) nell&#39;angolo superiore destro.

   ![Aggiungi prodotto raggruppato](./assets/product-add-grouped.png){width="700" zoomable="yes"}

## Passaggio 2: scegliere la serie di attributi

Per scegliere il [set di attributi](attribute-sets.md) utilizzato come modello per il prodotto, eseguire una delle operazioni seguenti:

- Per eseguire la ricerca, immettere il nome di **[!UICONTROL Attribute Set]**.
- Nell&#39;elenco, scegliere il set di attributi che si desidera utilizzare.

Il modulo viene aggiornato per riflettere la modifica.

![Scegli modello](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

Se gli attributi necessari non esistono, puoi aggiungere nuovi attributi durante la creazione di un prodotto:

- Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Attribute]**.
- Definisci un nuovo attributo (vedi [Aggiunta di un attributo a un prodotto](product-attributes-add.md)).

  ![Nuovo attributo](./assets/product-attribute-add-select.png){width="600" zoomable="yes"}

Per aggiungere un attributo esistente al prodotto, utilizzare i [controlli filtro](../getting-started/admin-grid-controls.md) per trovare l&#39;attributo nella griglia ed eseguire le operazioni seguenti:

- Selezionare la casella di controllo nella prima colonna di ogni attributo da aggiungere.
- Fare clic su **[!UICONTROL Add Selected]**.

## Passaggio 3: completare le impostazioni richieste

1. Immettere **[!UICONTROL Product Name]**.

1. Accettare **[!UICONTROL SKU]** predefinito basato sul nome del prodotto o immetterne un altro.

   Il campo **[!UICONTROL Quantity]** non è disponibile perché il valore è derivato dai singoli prodotti che compongono il gruppo.

   Un prodotto raggruppato non ha un proprio prezzo nel catalogo. Il prezzo del prodotto raggruppato è derivato dal prezzo dei singoli prodotti inclusi nel gruppo.

1. Poiché il prodotto non è ancora pronto per la pubblicazione, impostare **[!UICONTROL Enable Product]** su `No` ( ![Attiva/Disattiva n.](../assets/toggle-no.png) ).

1. Fare clic su **[!UICONTROL Save]** e continuare.

   Quando il prodotto viene salvato, il nome del prodotto viene visualizzato nella parte superiore della pagina e il selettore [Visualizzazione store](introduction.md#product-scope) viene visualizzato nell&#39;angolo superiore sinistro.

1. Scegliere **[!UICONTROL Store View]** in cui il prodotto deve essere disponibile.

   ![Scegli visualizzazione store](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Passaggio 4: completare le impostazioni di base

1. Accettare l&#39;impostazione **[!UICONTROL Stock Status]** di `In Stock`.

1. Per assegnare **[!UICONTROL Categories]** al prodotto, fare clic sulla casella **[!UICONTROL Select…]** ed eseguire una delle operazioni seguenti:

   **Scegli una categoria esistente:**

   - Inizia a digitare nella casella fino a trovare una corrispondenza.

   - Selezionare la casella di controllo della categoria da assegnare.

   **Crea una categoria:**

   - Fare clic su **[!UICONTROL New Category]**.

   - Immettere **[!UICONTROL Category Name]** e scegliere **[!UICONTROL Parent Category]**, che ne determina la posizione nella struttura del menu.

   - Fare clic su **[!UICONTROL Create Category]**.

1. Accettare le impostazioni **[!UICONTROL Visibility]** di `Catalog, Search`.

1. Per inserire il prodotto nell&#39;[elenco di nuovi prodotti](../content-design/widget-new-products-list.md), scegliere le date **[!UICONTROL Set Product as New]** **[!UICONTROL from]** e **[!UICONTROL to]** nel calendario.

1. Scegliere **[!UICONTROL Country of Manufacture]**.

   Potrebbero essere presenti singoli attributi aggiuntivi che descrivono il prodotto. La selezione varia a seconda del set di attributi e può essere completata in un secondo momento.

## Passaggio 5: aggiungere prodotti al gruppo

1. Scorri verso il basso fino alla sezione **[!UICONTROL Grouped Products]** e fai clic su **[!UICONTROL Add Products to Group]**.

   ![Prodotti Raggruppati](./assets/product-grouped-products.png){width="600" zoomable="yes"}

1. Se necessario, utilizzare i [filtri](../getting-started/admin-grid-controls.md) per trovare i prodotti da includere nel gruppo.

1. Nell&#39;elenco selezionare la casella di controllo di ogni elemento che si desidera includere nel gruppo.

   >[!NOTE]
   >
   >Solo i prodotti semplici, scaricabili e virtuali senza opzioni configurabili possono essere raggruppati come prodotti secondari. Altri tipi di prodotto non vengono visualizzati nell&#39;elenco di selezione.

   ![Aggiungi prodotti selezionati](./assets/product-grouped-add-products.png){width="600" zoomable="yes"}

1. Per aggiungerli al gruppo di prodotti, fare clic su **[!UICONTROL Add Selected Products]**.

   I prodotti selezionati vengono visualizzati nella sezione _[!UICONTROL Grouped Products]_.

   Per gli esercenti Multi Source con [Inventory management](../inventory-management/sources-stocks.md), la griglia include una colonna **[!UICONTROL Quantity per Source]** con ogni origine assegnata e l&#39;importo delle scorte di magazzino.

   ![Prodotti nel gruppo](./assets/product-grouped-grouped-products-section.png){width="600" zoomable="yes"}

1. Immettere **[!UICONTROL Default Quantity]** per uno qualsiasi degli elementi.

1. Per modificare l&#39;ordine dei prodotti, afferrare l&#39;icona _Cambia ordine_ ( ![Controller posizione](../assets/icon-sort-order.png) ) nella prima colonna e trascinare il prodotto nella nuova posizione nell&#39;elenco.

1. Per rimuovere un prodotto dal gruppo, scegliere **[!UICONTROL Remove]**.

## Passaggio 5: Completare le informazioni sul prodotto

Compila le informazioni nelle sezioni seguenti secondo necessità:

- [Contenuto](product-content.md)
- [Immagini e video](product-images-and-video.md)
- [Ottimizzazione motore di ricerca](product-search-engine-optimization.md)
- [Prodotti correlati, up-selling e cross-selling](related-products-up-sells-cross-sells.md)
- [Opzioni personalizzabili](settings-advanced-custom-options.md)
- [Prodotti nei siti Web](settings-basic-websites.md)
- [Progettazione](settings-advanced-design.md)
- [Opzioni regalo](product-gift-options.md)

## Passaggio 6: Publish del prodotto

1. Se si è pronti a pubblicare il prodotto nel catalogo, impostare **[!UICONTROL Enable Product]** su `Yes`.

1. Effettuare una delle seguenti operazioni:

   **Metodo 1:** Salvataggio e anteprima

   - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]**.

   - Per visualizzare il prodotto nell&#39;archivio, scegli **[!UICONTROL Customer View]** nel menu _Amministratore_ ( ![Freccia menu](../assets/icon-menu-down-arrow-black.png) ).

     L’archivio si apre in una nuova scheda del browser.

     ![Visualizzazione clienti](./assets/product-admin-customer-view.png){width="700" zoomable="yes"}

   **Metodo 2:** Salva e chiudi

   - Scegliere **[!UICONTROL Save & Close]** dal menu _[!UICONTROL Save]_( ![Freccia menu](../assets/icon-menu-down-arrow-red.png){width="25"} ).

## Passaggio 7: configurare le miniature del carrello (facoltativo)

Se hai un’immagine diversa per ciascun prodotto del gruppo, puoi impostare la configurazione in modo da utilizzare l’immagine corretta per la miniatura del carrello acquisti.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandere ![Il selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Shopping Cart]**.

   Per un elenco dettagliato di queste opzioni di configurazione, vedere [Carrello acquisti](../configuration-reference/sales/checkout.md#shopping-cart) nel _Riferimento configurazione_.

1. Imposta **[!UICONTROL Grouped Product Image]** su `Product Thumbnail Itself`.

   ![Carrello acquisti](./assets/config-sales-cart-grouped-product.png){width="600" zoomable="yes"}

   Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per impostare questa opzione.

1. Fare clic su **[!UICONTROL Save Config]**.

## Aspetti da ricordare

- Un prodotto raggruppato è essenzialmente una raccolta di semplici prodotti associati.

- I prodotti secondari raggruppati possono essere prodotti semplici, scaricabili o virtuali **[!UICONTROL without custom options]**.

- Ogni articolo acquistato viene visualizzato singolarmente nel carrello, anziché come parte del gruppo.

- Un prodotto raggruppato non ha un proprio prezzo nel catalogo. Il prezzo del prodotto raggruppato è derivato dal prezzo dei singoli prodotti inclusi nel gruppo.

- L’immagine miniatura nel carrello può essere impostata in modo da visualizzare l’immagine dal prodotto principale raggruppato o dal prodotto associato.
