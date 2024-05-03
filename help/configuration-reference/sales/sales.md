---
title: '[!UICONTROL Sales] &gt; [!UICONTROL Sales]'
description: Rivedi le impostazioni di configurazione su [!UICONTROL Sales] &gt; [!UICONTROL Sales] pagina dell’amministratore di Commerce.
exl-id: 29091aab-e608-4e68-a6fe-f2808c78581c
feature: Configuration, Orders
source-git-commit: 9827b08e5b0123f84c87cbac672ce9bbec86f511
workflow-type: tm+mt
source-wordcount: '1186'
ht-degree: 1%

---

# [!UICONTROL Sales] > [!UICONTROL Sales]

{{config}}

## [!UICONTROL General]

![Generale](./assets/sales-general.png)<!-- zoom -->

<!-- [General](https://docs.magento.com/user-guide/marketing/sales-documents-ref-id.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Hide Customer IP] | Visualizzazione store | Determina se l&#39;indirizzo IP del cliente viene visualizzato in ordini, fatture, spedizioni e note di accredito. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Checkout Totals Sort Order]

![Ordinamento dei totali di cassa](./assets/sales-checkout-totals-sort-order.png)<!-- zoom -->

<!-- [Checkout Totals Sort Order](https://docs.magento.com/user-guide/sales/checkout-totals-sort-order.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Subtotal] | Sito Web | Numero che determina quando viene calcolato il subtotale in relazione ad altri totali di pagamento. Valore predefinito: `10` |
| [!UICONTROL Discount] | Sito Web | Numero che determina quando viene calcolato lo sconto in relazione ad altri totali di pagamento. Valore predefinito: `20` |
| [!UICONTROL Shipping] | Sito Web | Numero che determina quando viene calcolata la spedizione in relazione ad altri totali di pagamento. Valore predefinito: `30` |
| [!UICONTROL Tax] | Sito Web | Numero che determina quando l&#39;imposta viene calcolata in relazione ad altri totali di pagamento. Valore predefinito: `40` |
| [!UICONTROL Fixed Product Tax] | Sito Web | Numero che determina quando viene calcolata l&#39;imposta sul prodotto fissa in relazione ad altri totali di pagamento. Valore predefinito: `50` |
| [!UICONTROL Grand Total] | Sito Web | Numero che determina quando viene calcolato il totale complessivo in relazione ad altri totali di pagamento. Valore predefinito: `100` |

{style="table-layout:auto"}

## [!UICONTROL Reorder]

![Riordina](./assets/sales-reorder.png)<!-- zoom -->

<!-- [Reorder](https://docs.magento.com/user-guide/sales/reorders-allow.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Allow Reorder] | Visualizzazione store | Determina se i clienti possono riordinare dai propri account. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Allow Zero Grand Total]

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Allow Zero Grand Total for Credit Memo] | Visualizzazione store | Determina la possibilità di creare una nota di credito con un totale complessivo pari a zero. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Invoice and Packing Slip Design]

![Progettazione fatture e documenti di trasporto](./assets/sales-invoice-packing-slip-design.png)<!-- zoom -->

<!-- [Invoice and Packing Slip Design](https://docs.magento.com/user-guide/marketing/sales-document-pdf-logo.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Logo for PDF Print-outs] | Visualizzazione store | Identifica il file del logo visualizzato nell&#39;intestazione delle fatture e dei documenti di trasporto PDF. Tipi di file consentiti: <br/>JPG/JPEG <br/>TIF/TIFF <br/>PNG |
| [!UICONTROL Logo for HTML Print View] | Visualizzazione store | Identifica il file del logo visualizzato nell&#39;intestazione della visualizzazione Stampa HTML delle fatture e dei documenti di trasporto. Tipi di file consentiti: <br/>JPG/JPEG <br/>GIF <br/>PNG |
| [!UICONTROL Address] | Visualizzazione store | L&#39;indirizzo del punto vendita che si desidera venga visualizzato nelle fatture e nei documenti di trasporto. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Order Amount]

![Importo minimo ordine](./assets/sales-minimum-order-amount.png)<!-- zoom -->

<!-- [Minimum Order Amount](https://docs.magento.com/user-guide/sales/cart-minimum-order-amount.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable] | Sito Web | Determina se viene impostato un importo minimo per l&#39;ordine del sito. Opzioni: `Yes` / `No` |
| [!UICONTROL Minimum Amount] | Sito Web | Specifica il subtotale minimo, da ordinare dopo l&#39;applicazione degli sconti. |
| [!UICONTROL Include Discount Amount] | Sito Web | Determina se l&#39;importo minimo dell&#39;ordine include gli sconti applicati. Opzioni: `Yes` / `No` |
| [!UICONTROL Include Tax to Amount] | Sito Web | Determina se l&#39;importo dell&#39;ordine minimo include l&#39;imposta. Opzioni: `Yes` / `No` |
| [!UICONTROL Description Message] | Visualizzazione store | Determina il messaggio visualizzato nella parte superiore del carrello quando il totale del carrello è inferiore all’importo minimo dell’ordine. Se non specificato, viene visualizzato il seguente messaggio predefinito: `Minimum order amount is $[minimum_amount]` |
| [!UICONTROL Error to Show in Shopping Cart] | Visualizzazione store | Determina il messaggio visualizzato dal mini carrello o dal collegamento di pagamento quando l&#39;importo dell&#39;ordine è inferiore all&#39;importo minimo richiesto. Se non specificato, viene visualizzato un messaggio predefinito. |
| [!UICONTROL Validate Each Address Separately in Multi-address Checkout] | Sito Web | Per gli ordini con più articoli, determina se gli articoli dell’ordine che verranno separati dagli indirizzi soddisfano di gran lunga l’importo minimo dell’ordine. Opzioni: `Yes` / `No` |
| [!UICONTROL Multi-address Description Message] | Visualizzazione store | Per gli ordini con più indirizzi, determina il messaggio visualizzato nel carrello se gli articoli inviati a un indirizzo sono inferiori all’importo minimo dell’ordine. |
| [!UICONTROL Multi-address Error to Show in Shopping Cart] | Visualizzazione store | Per gli ordini con più indirizzi, determina il messaggio visualizzato dal mini carrello o dal collegamento di pagamento quando l’importo dell’ordine è inferiore all’importo minimo richiesto. Se non specificato, viene visualizzato un messaggio predefinito. |

{style="table-layout:auto"}

## [!UICONTROL Dashboard]

![Dashboard](./assets/sales-dashboard.png)<!-- zoom -->

<!-- [Dashboard](https://docs.magento.com/user-guide/stores/admin-dashboard.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Use Aggregated Data] | Globale | Determina se i dati di vendita aggregati in tempo reale vengono utilizzati per produrre report snapshot del dashboard. Se la quantità di dati da elaborare è elevata, è possibile migliorare le prestazioni disattivando la visualizzazione dei dati in tempo reale. Opzioni: `Yes` / `No` |

{style="table-layout:auto"}

## [!UICONTROL Orders Cron Settings]

![Impostazioni Cron Ordini](./assets/sales-orders-cron-settings.png)<!-- zoom -->

<!-- [Orders Cron Settings](https://docs.magento.com/user-guide/system/cron.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Pending Payment Order Lifetime] | Sito Web | Determina la durata in minuti degli ordini in sospeso. Impostazione predefinita: `480` minuti (8 ore) |

{style="table-layout:auto"}

## [!UICONTROL Gift Options]

![Opzioni regalo](./assets/sales-gift-options.png)<!-- zoom -->

<!-- [Gift Options](https://docs.magento.com/user-guide/sales/gift-options.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Allow Gift Messages on Order Level] | Sito Web | Specificare se è possibile aggiungere un messaggio regalo per l&#39;intero ordine. |
| [!UICONTROL Allow Gift Messages on Order Items] | Sito Web | Specifica se è possibile aggiungere un messaggio regalo per un singolo articolo dell&#39;ordine. |
| [!UICONTROL Allow Gift Wrapping on Order Level] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo per Adobe Commerce) Specifica se è possibile aggiungere la confezione regalo per l&#39;intero ordine. |
| [!UICONTROL Allow Gift Wrapping for Order Items] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Specifica se è possibile aggiungere confezione regalo per il singolo articolo dell&#39;ordine. |
| [!UICONTROL Allow Gift Receipt] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo Adobe Commerce) Specifica se è possibile aggiungere una ricevuta regalo per l&#39;ordine. |
| [!UICONTROL Allow Printed Card] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo per Adobe Commerce) Specifica se è possibile aggiungere una scheda stampata per l’ordine. |
| [!UICONTROL Default Price for Printed Card] | Sito Web | ![Adobe Commerce](../../assets/adobe-logo.svg) (Solo per Adobe Commerce) Specifica il prezzo predefinito per la scheda stampata. |

{style="table-layout:auto"}

## [!UICONTROL Minimum Advertised Price]

![Prezzo minimo annunciato](./assets/sales-minimum-advertised-price.png)<!-- zoom -->

<!-- [Minimum Advertised Price](https://docs.magento.com/user-guide/catalog/product-price-minimum-advertised.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable MAP] | Sito Web | Attiva il prezzo minimo annunciato per il tuo negozio. Opzioni: `Yes` / `No` |
| [!UICONTROL Display Actual Price] | Sito Web | Determina dove il prezzo effettivo di un prodotto è visibile al cliente. Opzioni: <br/>**`In Cart`**- Visualizza il prezzo effettivo del prodotto nel carrello.<br/>**`Before Order Confirmation`** - Visualizza il prezzo effettivo del prodotto al termine del processo di pagamento, immediatamente prima della conferma dell&#39;ordine. <br/>**`On Gesture`**- Visualizza il prezzo effettivo del prodotto in un popup quando il cliente fa clic su &quot;Click for price&quot; o &quot;What&#39;s this?&quot; (Clic per il prezzo) collegamento. |
| [!UICONTROL Default Popup Text Message] | Visualizzazione store | Il messaggio di testo che viene visualizzato quando il cliente seleziona il collegamento &quot;Click for price&quot; (Fai clic per il prezzo) da un elenco di categorie o da una pagina di visualizzazione del prodotto. |
| [!UICONTROL Default "What's This" Text Message] | Visualizzazione store | Messaggio di testo visualizzato quando il cliente fa clic su &quot;Cos’è questo?&quot; dalla pagina di visualizzazione del prodotto. |
| [!UICONTROL Manufacturer's Suggested Retail Price] | Globale | Il prezzo al dettaglio suggerito dal produttore (MSRP). |

{style="table-layout:auto"}

## [!UICONTROL Multicoupon Settings]

{{ee-feature}}

![Impostazioni per più contatti](./assets/sales-multicoupon-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Maximum number of coupons per order] | Sito Web | Determina il numero massimo di coupon consentiti per ordine. Questa funzione è disponibile solo in Admin, GraphQL e REST API. Ed è **_non disponibile_** in Storefront. |

{style="table-layout:auto"}

## [!UICONTROL Order by SKU Settings]

{{ee-feature}}

![Impostazioni Ordina per SKU](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

<!-- [Order by SKU Settings](https://docs.magento.com/user-guide/customers/account-dashboard-order-by-sku.html) -->

![Impostazioni ordine per SKU per gruppo di clienti](./assets/sales-order-by-sku-settings.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Order by SKU on My Account in Storefront] | Sito Web | Determina se Ordina per SKU è disponibile nel dashboard dell&#39;account cliente. Opzioni: <br/>**`Yes, for Everyone`**- La scheda Ordina per SKU viene visualizzata nel dashboard account di tutti i clienti.<br/>**`Yes, for Specified Customer Groups`** - La scheda Ordina per SKU viene visualizzata nel dashboard account per i membri di gruppi specifici o di un catalogo condiviso. <br/>**`No`**- La scheda Ordina per SKU non è disponibile nel conto cliente. |
| [!UICONTROL Customer Groups] | Sito Web | Determina i gruppi di clienti. Opzioni: `General` / `Retailer` / `Wholesale` |

{style="table-layout:auto"}

## [!UICONTROL Instant Purchase]

![Acquisto immediato](./assets/sales-instant-purchase.png)<!-- zoom -->

<!-- [Instant Purchase](https://docs.magento.com/user-guide/sales/checkout-instant-purchase.html) -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enabled] | Visualizzazione store | Abilita l&#39;acquisto immediato per la visualizzazione del punto vendita se per il metodo di pagamento, ad esempio Braintree, è abilitato l&#39;archivio. Opzioni: `Yes` / `No` |
| [!UICONTROL Button Text] | Visualizzazione store | Specifica il testo visualizzato sul pulsante Acquisto immediato. Il testo predefinito è `Instant Purchase`. |

{style="table-layout:auto"}

## [!UICONTROL Rate Limiting]

![Limitazione di tariffa](assets/sales-rate-limiting.png)<!-- zoom -->

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--------------------------------------------------------|--- |------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Enable rate limiting for placing orders] | Visualizzazione store | Determina se viene utilizzata la limitazione della tariffa per l&#39;inserimento di ordini dalla vista Store (l&#39;impostazione predefinita è `No`). Opzioni: `Yes` / `No`. |
| [!UICONTROL Requests limit per authenticated customer] | Visualizzazione store | Il numero di richieste di acquisto che un cliente autenticato può effettuare durante il periodo. Il limite predefinito è `10`. |
| [!UICONTROL Requests limit per guest] | Visualizzazione store | Il numero di richieste di acquisto che un cliente non autenticato può effettuare durante il periodo specificato. Il valore predefinito è `50`. |
| [!UICONTROL Counter resets in a ...] | Visualizzazione store | Il periodo di tempo durante il quale un cliente autenticato/non autenticato può effettuare un certo numero di richieste di acquisto (l’impostazione predefinita è `Minute`). Opzioni: `Minute` / `Hour` /`Day` |

{style="table-layout:auto"}

## [!UICONTROL Orders, Invoices, Shipments, Credit Memos Archiving]

{{ee-feature}}

![Archiviazione di ordini, fatture, spedizioni e note di credito](./assets/sales-orders-invoices-shipments-credit-memos-archiving.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Configurare l’archivio degli ordini](../../stores-purchase/order-archive.md#configure-the-order-archive) nel _Guida ai negozi e all’esperienza di acquisto_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable Archiving] | Globale | Determina se l&#39;archiviazione è abilitata. Opzioni: `Yes` / `No` |
| [!UICONTROL Archive Orders Purchased] | Globale | Determina il numero di giorni trascorsi prima dell&#39;archiviazione di un ordine completato. Valore predefinito: `30` |
| [!UICONTROL Order  Statuses to be Archived] | Globale | Determina la [stato](../../stores-purchase/order-status.md) degli ordini da archiviare. Per impostazione predefinita, gli ordini con stato Completo o Chiuso vengono archiviati. Opzioni: `Pending` / `Processing` / `Suspected Fraud` / `Complete` / `Closed` / `Canceled` / `On Hold` |

{style="table-layout:auto"}

## [!UICONTROL RMA Settings]

{{ee-feature}}

![Impostazioni RMA](./assets/sales-rma-settings.png)<!-- zoom -->

Per ulteriori informazioni sulla modifica di queste impostazioni, vedere [Configurare i resi](../../stores-purchase/rma-configure.md) nel _Guida ai negozi e all’esperienza di acquisto_.

| Campo | [Ambito](../../getting-started/websites-stores-views.md#scope-settings) | Descrizione |
|--- |--- |--- |
| [!UICONTROL Enable RMA on Storefront] | Sito Web | Determina se i clienti possono creare e visualizzare richieste RMA dalla vetrina. RMA può essere applicato sia agli ordini nuovi che a quelli esistenti. Per impostazione predefinita, RMA non è abilitato per la vetrina. Opzioni: `Yes` / `No` |
| [!UICONTROL Enable RMA on Product Level] | Sito Web | Determina il valore predefinito per il campo Abilita RMA nelle informazioni sul prodotto. |
| [!UICONTROL Use Store Address] | Sito Web | Determina il nome e l&#39;indirizzo del contatto utilizzato per le spedizioni della merce restituita. Opzioni: <br/>**`Yes`**- Utilizza il [Punto di origine](../../stores-purchase/shipping-settings.md#point-of-origin) indirizzo da impostazioni di spedizione.<br/>**`No`** - Apre il modulo dell&#39;indirizzo in modo da poter immettere un indirizzo alternativo. |

{style="table-layout:auto"}
