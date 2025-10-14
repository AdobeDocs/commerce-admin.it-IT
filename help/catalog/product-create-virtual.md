---
title: Prodotto virtuale
description: Scopri come creare un prodotto virtuale che rappresenti un elemento non tangibile, ad esempio un’iscrizione, un servizio, una garanzia o un abbonamento.
exl-id: 8788ba04-e911-429e-9e48-ce589f0c9fa1
feature: Catalog Management, Products
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 0%

---

# Prodotto virtuale

I prodotti virtuali, o beni digitali, rappresentano elementi non tangibili come appartenenze, servizi, garanzie o abbonamenti e download digitali di libri, musica, video o altri prodotti. I prodotti virtuali possono essere venduti singolarmente o inclusi come parte dei tipi di prodotto [Prodotto raggruppato](product-create-grouped.md), [Prodotto configurabile](product-create-configurable.md) o [Prodotto aggregato](product-create-bundle.md).

A parte l&#39;assenza del campo _[!UICONTROL Weight]_, il processo di creazione di un prodotto virtuale e di un prodotto semplice è lo stesso. Le istruzioni seguenti illustrano il processo di creazione di un prodotto virtuale utilizzando un [modello di prodotto](attribute-sets.md), campi obbligatori e impostazioni di base. Al termine delle nozioni di base, puoi completare le altre impostazioni del prodotto in base alle esigenze.

>[!NOTE]
>
>PayPal ha dichiarato obsoleto il supporto per la vendita di beni digitali tramite PayPal Express Checkout. Si consiglia di utilizzare [PayPal Payments Standard](../stores-purchase/paypal-payments-standard.md) o qualsiasi altro gateway di pagamento PayPal per elaborare qualsiasi ordine che includa prodotti virtuali.

![Prodotto virtuale](./assets/product-virtual-membership.png){width="700" zoomable="yes"}

## Passaggio 1: scegliere il tipo di prodotto

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Scegliere _[!UICONTROL Add Product]_&#x200B;dal menu ![&#x200B; ( &#x200B;](../assets/icon-menu-down-arrow-red.png){width="25"}Freccia menu **[!UICONTROL Virtual Product]**) nell&#39;angolo superiore destro.

   ![Aggiungi prodotto virtuale](./assets/product-add-virtual.png){width="700" zoomable="yes"}

## Passaggio 2: scegliere la serie di attributi

Per scegliere il [set di attributi](attribute-sets.md) utilizzato come modello per il prodotto, eseguire una delle operazioni seguenti:

- Fare clic nel campo **[!UICONTROL Attribute Set]** e immettere il nome completo o parziale del set di attributi.

- Nell&#39;elenco visualizzato scegliere il set di attributi che si desidera utilizzare.

Il modulo viene aggiornato per riflettere la modifica.

![Scegli set di attributi](./assets/product-create-choose-attribute-set.png){width="600" zoomable="yes"}

## Passaggio 3: completare le impostazioni richieste

1. Immettere **[!UICONTROL Product Name]**.

1. Accettare **[!UICONTROL SKU]** predefinito basato sul nome del prodotto o immetterne un altro.

1. Immettere il prodotto **[!UICONTROL Price]**.

1. Poiché il prodotto non è ancora pronto per la pubblicazione, impostare **[!UICONTROL Enable Product]** su `No`.

1. Fare clic su **[!UICONTROL Save]** e continuare.

   Quando il prodotto viene salvato, il selettore [Visualizzazione store](introduction.md#product-scope) viene visualizzato nell&#39;angolo superiore sinistro.

1. Scegliere **[!UICONTROL Store View]** in cui il prodotto deve essere disponibile.

   ![Scegli visualizzazione store](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

## Passaggio 4: completare le impostazioni di base

1. Imposta **[!UICONTROL Tax Class]** su uno dei seguenti:

   - `None`
   - `Taxable Goods`

1. Immettere il **[!UICONTROL Quantity]** del prodotto in magazzino ed effettuare le seguenti operazioni:

   - Accettare l&#39;impostazione **[!UICONTROL Stock Status]** predefinita di `In Stock`.

     Poiché un prodotto virtuale non è stato spedito, il campo **[!UICONTROL Weight]** non viene utilizzato.

   - Accettare l&#39;impostazione **[!UICONTROL Visibility]** predefinita di `Catalog, Search`.

   >[!NOTE]
   >
   >Se abiliti [Inventory management](../inventory-management/introduction.md), i commercianti con una sola origine impostano la quantità in questa sezione. I commercianti con più origini aggiungono origini e quantità nella sezione Origini. Consulta la seguente sezione _Assegnare origini e quantità (Inventory management)_.

1. Per assegnare **[!UICONTROL Categories]** al prodotto, fare clic sulla casella **[!UICONTROL Select…]** ed eseguire una delle operazioni seguenti:

   **Scegliere una categoria esistente**:

   - Inizia a digitare nella casella fino a trovare una corrispondenza.

   - Selezionare la casella di controllo della categoria da assegnare.

   **Crea una categoria**:

   - Fare clic su **[!UICONTROL New Category]**.

   - Immettere **[!UICONTROL Category Name]** e scegliere **[!UICONTROL Parent Category]**, che ne determina la posizione nella struttura del menu.

   - Fare clic su **[!UICONTROL Create Category]**.

   Potrebbero essere presenti singoli attributi aggiuntivi che descrivono il prodotto. La selezione varia in base al set di attributi e può essere completata in un secondo momento.

### Assegna origini e quantità ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

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

>[!NOTE]
>
>L&#39;opzione _[!UICONTROL Is this downloadable product?]_&#x200B;è disabilitata per impostazione predefinita. L&#39;attivazione di questa funzionalità per un prodotto virtuale rende il prodotto [scaricabile](product-create-downloadable.md#downloadable-product).

## Passaggio 6: pubblicare il prodotto

1. Se si è pronti a pubblicare il prodotto nel catalogo, impostare **[!UICONTROL Enable Product]** su `Yes`.

1. Effettuare una delle seguenti operazioni:

   - **Metodo 1:** Salvataggio e anteprima

      - Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]**.

      - Per visualizzare il prodotto nell&#39;archivio, scegli **[!UICONTROL Customer View]** nel menu _Amministratore_ ( ![Freccia menu](../assets/icon-menu-down-arrow-black.png) ).

     L’archivio si apre in una nuova scheda del browser.

     ![Visualizzazione clienti](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

   - **Metodo 2:** Salvare e chiudere

     Scegliere _[!UICONTROL Save]_&#x200B;dal menu ![&#x200B; (](../assets/icon-menu-down-arrow-red.png){width="25"}Freccia menu **[!UICONTROL Save & Close]**).

## Aspetti da ricordare

- I prodotti virtuali sono utilizzati per prodotti non tangibili come servizi, abbonamenti e garanzie.

- I prodotti virtuali sono molto simili ai prodotti semplici, ma privi di peso.

- Le opzioni di spedizione non vengono visualizzate durante il pagamento a meno che non sia presente un prodotto tangibile nel carrello.

<!-- Last updated from includes: 2023-05-19 17:14:58 -->
