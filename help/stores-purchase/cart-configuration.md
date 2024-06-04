---
title: Configurazione del carrello
description: Scopri le funzioni del carrello che puoi configurare per supportare l’esperienza di acquisto nel tuo negozio.
exl-id: b98ec7ce-9354-4f03-b67e-dd1587f0c866
feature: Shopping Cart, Configuration
source-git-commit: 61df9a4bcfaf09491ae2d353478ceb281082fa74
workflow-type: tm+mt
source-wordcount: '2449'
ht-degree: 0%

---

# Configurazione del carrello

La configurazione del carrello determina il modo in cui il carrello funziona per i clienti del negozio, compreso il momento in cui il cliente viene reindirizzato alla pagina del carrello e quali immagini vengono utilizzate per le miniature dei prodotti. È inoltre possibile richiedere un ordine per raggiungere un importo minimo prima dell&#39;inizio del processo di pagamento, specificare il numero di giorni in cui i prezzi quotati rimangono validi e specificare l&#39;ordine degli articoli nel _Totali ordine_ sezione.

[**Mini carrello**](#mini-cart) : configura questa opzione per determinare se l’icona o il collegamento al carrello mostra il numero di prodotti (o SKU) diversi nel carrello o la quantità totale di tutti gli articoli.

[**Collegamento al mini carrello**](#configure-the-cart-link) : configura questa opzione per determinare se il mini carrello viene visualizzato quando un cliente fa clic sul numero di elementi nell’icona del carrello nella parte superiore della pagina di un negozio.

[**Reindirizza al carrello**](#redirect-to-cart): configura questa opzione per determinare se la pagina del carrello viene visualizzata ogni volta che un articolo viene aggiunto al carrello o solo quando un cliente sceglie di passare alla pagina.

[**Durata offerta**](#quote-lifetime) : configura questa opzione per specificare la durata di validità di un prezzo.

[**Importo minimo ordine**](#minimum-order-amount) : configura queste opzioni per specificare un importo minimo, dopo l’applicazione degli sconti, che i subtotali dell’ordine devono soddisfare e i messaggi visualizzati nel carrello.

[**Quantità minima ordine**](#minimum-order-quantity) - Configura queste opzioni per specificare il numero minimo di elementi necessari per effettuare un ordine.

[**Miniature carrello**](#cart-thumbnails)  : configura le opzioni delle miniature del carrello per determinare le miniature visualizzate nel carrello per i prodotti raggruppati o configurabili.

[**Opzioni regalo**](#gift-options) : configura le opzioni regalo per determinare se i clienti possono aggiungere un messaggio regalo o un biglietto di auguri e se sono disponibili opzioni per la confezione regalo.

>[!NOTE]
>
>Per informazioni sulla configurazione del processo di pagamento, consulta [Opzioni di pagamento](checkout-process.md).

## Mini carrello

Il _mini carrello_ visualizza un riepilogo degli articoli nel carrello. È attivata per impostazione predefinita e viene visualizzata quando fai clic sul collegamento Carrello nella parte superiore della pagina.
Il collegamento può essere configurato in modo da visualizzare il numero di prodotti (o SKU) diversi nel carrello o la quantità totale di tutti gli articoli.

![L’acquirente visualizza la barra laterale del carrello da una pagina di prodotto](./assets/storefront-mini-cart-watch.png){width="700" zoomable="yes"}

>[!NOTE]
>
>Per un _registrato_ cliente, in alcuni casi il Mini Cart potrebbe non essere sincronizzato automaticamente tra più dispositivi e browser. Per sincronizzare il Mini Carrello in questi casi, il cliente può semplicemente aprire il [Carrello](cart.md) su tale dispositivo o browser.

### Configurare il mini carrello

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _[!UICONTROL Mini Cart]_sezione.

   ![Configurazione del mini carrello](../configuration-reference/sales/assets/checkout-mini-cart.png){width="600" zoomable="yes"}

1. Se l&#39;impostazione è per una visualizzazione archivio specifica, [scegli la visualizzazione store](../configuration-reference/scope-change.md#set-the-scope) dove si applica la configurazione.

   Quando richiesto, fai clic su **[!UICONTROL OK]** per continuare.

1. Imposta **[!UICONTROL Display Mini Cart]** a uno dei seguenti elementi:

   - `Yes` - Visualizza il mini carrello sulle pagine del negozio. L’aspetto della barra laterale dipende dal tema.
   - `No` - Disattiva la visualizzazione del mini carrello sulle pagine del negozio.

1. Se la visualizzazione è abilitata, aggiorna le altre opzioni per configurare la visualizzazione:

   - Per **[!UICONTROL Number of Items to Display Scrollbar]**, immettere il numero di elementi che possono essere visualizzati nella barra laterale prima che venga attivata la barra di scorrimento.
   - Per **[!UICONTROL Maximum Display Recently Added Item(s)]**, immetti il numero massimo di elementi aggiunti di recente che desideri visualizzare nel mini carrello.

1. Clic **[!UICONTROL Save Config]**.

### Configurare il collegamento al carrello

1. Il giorno _Amministratore_ barra laterale, arrivo a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL My Cart Link]** sezione.

1. Imposta **[!UICONTROL Display Cart Summary]** a una delle seguenti impostazioni:

   - `Display item quantities` - Questa impostazione visualizza il numero totale di prodotti nel carrello, aggiungendo le quantità per ciascun prodotto.
   - `Display number of items in cart` - Questa impostazione visualizza il numero di articoli prodotto nel carrello, indipendentemente dalla quantità.

   ![Opzioni di configurazione per Collegamento al carrello](../configuration-reference/sales/assets/checkout-my-cart-link.png){width="600" zoomable="yes"}

1. Clic **[!UICONTROL Save Config]**.

## Reindirizza al carrello

La pagina del carrello può essere configurata in modo da essere visualizzata ogni volta che un articolo viene aggiunto al carrello oppure solo quando i clienti scelgono di passare alla pagina. Le informazioni di base sugli articoli presenti nel carrello sono sempre disponibili nel [mini carrello](#mini-cart). La decisione è una questione di bilanciamento dei vantaggi di lasciare che i clienti continuano a fare acquisti, con i vantaggi di incoraggiare i clienti a procedere al pagamento. Potrebbe essere una semplice questione di preferenze personali. Tuttavia, se desideri eseguirne il backup con i numeri, puoi eseguire un test A/B per vedere quale approccio produce un tasso di conversione più elevato.

**_Per configurare quando viene visualizzato il carrello:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Shopping Cart]** sezione.

   ![Impostazioni di configurazione del carrello espanse nella pagina](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Se l&#39;impostazione è per una visualizzazione archivio specifica, [scegli la visualizzazione store](../configuration-reference/scope-change.md#set-the-scope) dove si applica la configurazione.

   Quando richiesto, fai clic su **[!UICONTROL OK]** per continuare.

1. Imposta **[!UICONTROL After Adding a Product Redirect to Shopping Cart]** a uno dei seguenti elementi:

   - `Yes` : mostra la pagina del carrello subito dopo l’aggiunta di un prodotto al carrello.
   - `No` : disabilita il reindirizzamento al carrello dopo l’aggiunta di un prodotto al carrello.

1. Clic **[!UICONTROL Save Config]**.

## Durata offerta

Con l’installazione e l’abilitazione di Adobe Commerce B2B, puoi aggiungere il supporto per _Virgolette_ funzionalità. Questa funzionalità consente agli acquirenti autorizzati di avviare il processo di negoziazione dei prezzi inviando una richiesta dal carrello. Il _Virgolette_ grid elenca ogni preventivo ricevuto e mantiene una cronologia della comunicazione tra l&#39;acquirente e il venditore. Per ulteriori informazioni sulle funzioni B2B, consulta [Offerte negoziate](../b2b/quotes.md) nel _Guida utente di Adobe Commerce B2B_.

Puoi determinare per quanto tempo un prezzo è valido impostando la durata dell’offerta del carrello nella configurazione. Ad esempio, se un acquirente lascia un carrello incustodito dopo diversi giorni, il prezzo di offerta per alcuni articoli potrebbe non essere più lo stesso. Per impostazione predefinita, la durata dell&#39;offerta è impostata su 30 giorni.

**_Per configurare la durata dell&#39;offerta:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Shopping Cart]** sezione.

   ![Impostazioni di configurazione del carrello espanse nella pagina](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Se l&#39;impostazione è per una visualizzazione archivio specifica, [scegli la visualizzazione store](../configuration-reference/scope-change.md#set-the-scope) dove si applica la configurazione.

   Quando richiesto, fai clic su **[!UICONTROL OK]** per continuare.

1. Per **[!UICONTROL Quote Lifetime (days)]**, immettere il numero di giorni di validità di un prezzo quotato.

1. Clic **[!UICONTROL Save Config]**.

## Importo minimo ordine

La configurazione consente di specificare un importo minimo, dopo l’applicazione degli sconti, che i subtotali dell’ordine devono soddisfare. Gli ordini spediti a più indirizzi possono essere richiesti per soddisfare l&#39;importo minimo dell&#39;ordine per indirizzo. Il pulsante Pagamento diventa disponibile solo una volta raggiunto l&#39;importo minimo dell&#39;ordine.

![Nel carrello viene visualizzato un messaggio di ordine minimo](./assets/storefront-cart-minimum-order-amount.png){width="700" zoomable="yes"}

**_Per configurare un importo minimo per l&#39;ordine:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Minimum Order Amount]** sezione.

   ![Opzioni di configurazione dell’ordine minimo espanse nella pagina](../configuration-reference/sales/assets/sales-minimum-order-amount.png){width="600" zoomable="yes"}

1. Per richiedere un importo minimo per l&#39;ordine, impostare **[!UICONTROL Enable]** a `Yes`.

1. Se l&#39;ordine minimo è abilitato, impostare le opzioni seguenti per configurare il requisito:

   - Inserisci il **[!UICONTROL Minimum Amount]** necessario per il subtotale, dopo l&#39;applicazione degli sconti.

   - Imposta **[!UICONTROL Include Discount Amount]** a uno dei seguenti elementi:

      - `Yes` - Richiede che il subtotale soddisfi l&#39;importo minimo con eventuali sconti inclusi. Utilizzando un esempio di un minimo di 50 $, se il carrello contiene un top di 60 $ con uno sconto del 25% applicato, il subtotale risultante è di 45 $ e il carrello non raggiungerebbe il minimo.
      - `No` - Richiede che il subtotale soddisfi l&#39;importo minimo senza sconti.

   - Imposta **[!UICONTROL Include Tax to Amount]** a uno dei seguenti elementi:

      - `Yes` - Richiede che il subtotale soddisfi l&#39;importo minimo con l&#39;imposta inclusa.
      - `No` - Richiede che il subtotale soddisfi l&#39;importo minimo al netto delle imposte.

1. È possibile personalizzare le impostazioni dei messaggi per l&#39;importo minimo dell&#39;ordine:

   - Per **[!UICONTROL Description Message]**, immetti il testo da utilizzare per personalizzare il messaggio visualizzato nella parte superiore del carrello quando il subtotale non raggiunge la quantità minima.

   - Per **[!UICONTROL Error to Show in Shopping Cart]**, immetti il testo da utilizzare per personalizzare il messaggio di errore del carrello.

   Lascia vuoti i campi di descrizione del messaggio per utilizzare i messaggi predefiniti.

1. Se necessario, configura l’impostazione dell’importo minimo dell’ordine per gli ordini con più indirizzi:

   - Per richiedere che ogni indirizzo in un ordine con più indirizzi soddisfi l&#39;importo minimo dell&#39;ordine, impostare **[!UICONTROL Validate Each Address Separately in Multi-address Checkout]** a `Yes`.

   - È possibile personalizzare le impostazioni dei messaggi per l&#39;importo minimo dell&#39;ordine:

      - **[!UICONTROL Multi-address Description Message]** - Immettere il testo che si desidera utilizzare per personalizzare il messaggio visualizzato nella parte superiore del carrello per gli ordini con più indirizzi che non soddisfano il requisito minimo.

      - **[!UICONTROL Multi-address Error to Show in Shopping Cart]** - Inserisci il testo da utilizzare per personalizzare il messaggio di errore del carrello per gli ordini con più indirizzi che non soddisfano il minimo, inserisci il testo nella casella.

     Lascia vuoti i campi di descrizione del messaggio per utilizzare i messaggi predefiniti.

1. Clic **[!UICONTROL Save Config]**.

## Quantità minima ordine

È possibile impostare la quantità minima consentita per un ordine. La quantità minima può anche essere configurata in base a ciascun gruppo di clienti.

1. Vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Inventory]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Product Stock Options]** sezione.

   ![Opzioni magazzino prodotto](../configuration-reference/catalog/assets/catalog-inventory-product-stock-options.png){width="600" zoomable="yes"}

1. Per **[!UICONTROL Minimum Qty Allowed in Shopping Cart]**, imposta la quantità minima del prodotto per un ordine.

   Se necessario, cancellare il **[!UICONTROL Use system value]** per modificare queste impostazioni.

   - Modificare il **[!UICONTROL Customer Group]** a un gruppo specifico e immettere il **[!UICONTROL Minimum Qty]** per quel gruppo. Per aggiungere un altro gruppo e un altro limite di quantità, fare clic su **[!UICONTROL Add Minimum Qty]**.

   - Per impostare lo stesso limite di quantità minima per tutti i clienti, mantenere `ALL GROUPS` e immettere il **[!UICONTROL Minimum Qty]**.

1. Clic **[!UICONTROL Save Config]**.

   ![Quantità minima richiesta nel carrello](./assets/minimum-qty-allowed-in-shopping-cart.png){width="700" zoomable="yes"}

## Miniature carrello

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

Le miniature visualizzate nel carrello offrono ai clienti una rapida panoramica degli articoli che stanno per acquistare. Tuttavia, per i prodotti con più opzioni, l’immagine potrebbe non corrispondere alla variante del prodotto presente nel carrello. Se il cliente acquista un articolo con un colore specifico, idealmente la miniatura nel carrello dovrebbe corrispondere.

L’immagine di anteprima sia per i prodotti raggruppati che per quelli configurabili può essere impostata in modo da visualizzare l’immagine dal prodotto &quot;principale&quot; o dalla variante di prodotto.

![Il carrello mostra le miniature di ciascun prodotto](./assets/storefront-cart.png){width="700" zoomable="yes"}

**_Per configurare le miniature del carrello:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Checkout]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Shopping Cart]** sezione.

   ![Impostazioni di configurazione del carrello espanse nella pagina](../configuration-reference/sales/assets/checkout-shopping-cart.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Grouped Product Image]** per determinare la miniatura utilizzata nel carrello per [prodotti raggruppati](../catalog/product-create-grouped.md):

   - `Product Thumbnail Itself` - Utilizza la miniatura assegnata alla variante di prodotto aggiunta al carrello.
   - `Parent Product Thumbnail` - Utilizza la miniatura assegnata al prodotto principale.

1. Imposta **[!UICONTROL Configurable Product Image]** per determinare la miniatura utilizzata nel carrello per [prodotti configurabili](../catalog/product-create-configurable.md):

   - `Product Thumbnail Itself` - Utilizza la miniatura assegnata alla variante di prodotto aggiunta al carrello.
   - `Parent Product Thumbnail` - Utilizza la miniatura assegnata al prodotto principale.

1. Clic **[!UICONTROL Save Config]**.

## Opzioni regalo

La selezione delle opzioni regalo disponibili viene visualizzata nel carrello prima dell&#39;inizio del processo di pagamento. La configurazione delle opzioni regalo determina se i clienti possono aggiungere un messaggio regalo o un biglietto di auguri e se sono disponibili opzioni per la confezione regalo. Ogni articolo nell&#39;ordine può avere un messaggio e una confezione regalo separati. Quando applicati all&#39;intero ordine, i clienti possono anche aggiungere una ricevuta regalo e una cartolina di saluto.

![Esempio di vetrina: opzioni regalo nel carrello](./assets/storefront-cart-gift-options-for-products-or-order.png){width="700" zoomable="yes"}

La configurazione Opzioni regalo si applica all’intero sito web, ma può essere ignorata a livello di prodotto.

### Abilita opzioni regalo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Sales]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Gift Options]** sulla pagina.

   ![Configurazione vendite - Impostazioni Opzioni regalo](../configuration-reference/sales/assets/sales-gift-options.png){width="600" zoomable="yes"}

1. Impostare le opzioni del messaggio regalo in base alle proprie preferenze:

   - Per **[!UICONTROL Allow Gift Messages on Order Level]**, seleziona `Yes` per attivare un singolo messaggio regalo per l&#39;intero ordine.
   - Per **[!UICONTROL Allow Gift Messages for Order Items]**, seleziona `Yes` per abilitare l&#39;aggiunta di messaggi regalo separati per i singoli articoli nel carrello acquisti.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) Imposta le opzioni per la confezione regalo in base alle tue preferenze:

   - Per **[!UICONTROL Allow Gift Wrapping on Order Level]**, seleziona `Yes` per abilitare una singola confezione regalo per l&#39;intero ordine.
   - Per **[!UICONTROL Allow Gift Wrapping for Order Items]**, seleziona `Yes` per abilitare l&#39;aggiunta della confezione regalo singolarmente a ogni articolo nel carrello acquisti del cliente.

   Puoi anche definire diversi [design per confezioni regalo](#gift-wrap) in modo che i clienti possano scegliere la confezione.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Per offrire ai clienti un&#39;opzione per includere una ricevuta regalo, impostare **[!UICONTROL Allow Gift Receipt]** a `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce) Per offrire ai clienti l&#39;opzione di includere una carta stampata, impostare **[!UICONTROL Allow Printed Card]** a `Yes`.

1. ![Adobe Commerce](../assets/adobe-logo.svg) (Solo per Adobe Commerce) Inserisci il **[!UICONTROL Default Price for Printed Card]**.

1. Clic **[!UICONTROL Save Config]**.

### Confezione regalo

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

La confezione regalo è disponibile per qualsiasi prodotto che può essere spedito e può essere offerto per singoli articoli o per l&#39;intero ordine. Puoi addebitare un prezzo separato per ogni design regalo e caricare un’immagine in miniatura per ogni design visualizzato come opzione per un prodotto nel carrello. Quando un cliente fa clic sulla miniatura del regalo, viene visualizzata un’immagine a dimensione intera. Durante la revisione del pagamento, l&#39;addebito del buono regalo viene visualizzato con l&#39;altro [totali di pagamento](checkout-totals-sort-order.md) nel _Riepilogo ordine_ sezione.

L&#39;immagine a capo regalo deve essere un campione che mostra il motivo ripetuto e può anche includere un campione della barra multifunzione da utilizzare. È possibile scansionare la carta o scattare una fotografia di una confezione. L’immagine caricata può essere un’immagine GIF, JPG o PNG e deve essere quadrata. Nell’esempio seguente, l’immagine a capo regalo caricata è 230 x 230 pixel.

![Opzioni regalo nel carrello](./assets/storefront-cart-gift-options-gift-wrap.png){width="700" zoomable="yes"}

#### Aggiungere un design a capo regalo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

   ![Griglia per confezione regalo](./assets/gift-wrapping.png){width="700" zoomable="yes"}

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Add Gift Wrapping]**.

1. Immetti il nome per **[!UICONTROL Gift Wrapping Design]** da visualizzare durante l&#39;estrazione.

   Se necessario, è possibile modificare **[!UICONTROL Scope]** e configura un nome diverso per ogni visualizzazione store.

1. Seleziona la **[!UICONTROL Websites]** dove è disponibile il design dell&#39;involucro regalo.

1. Imposta **[!UICONTROL Status]** a `Enabled`.

   Se si dispone di un&#39;opzione di disposizione stagionale, è possibile impostarla su `Disabled` quando non desideri che l’opzione sia disponibile.

1. Inserisci il **[!UICONTROL Price]** del design dell&#39;involucro regalo.

   Questa impostazione può essere sovrascritta dal prezzo per confezione regalo impostato a livello di prodotto.

   ![Nuova confezione regalo](./assets/gift-wrapping-new.png){width="600" zoomable="yes"}

1. Per caricare una miniatura **[!UICONTROL Image]** della confezione regalo, fai clic su **[!UICONTROL Choose File]** e seleziona il file da caricare dalla directory.

   Una miniatura dell&#39;immagine appare nella _[!UICONTROL Gift Wrapping Information]_dopo il salvataggio del record.

1. Clic **[!UICONTROL Save]**.

#### Modificare un design a capo regalo

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Other Settings]_>**[!UICONTROL Gift Wrapping]**.

1. Trovare il record a capo regalo nell&#39;elenco.

1. In _Azione_ , fare clic su **[!UICONTROL Edit]**.

   ![Modifica informazioni confezione regalo](./assets/gift-wrapping-edit.png){width="600" zoomable="yes"}

1. Apporta le modifiche necessarie.

1. Clic **[!UICONTROL Save]**.

#### Elimina schemi a capo regalo

Con il _Confezione Regalo_ griglia aperta, utilizzate uno di questi metodi per eliminare le progettazioni a capo.

**_Metodo 1: Eliminare un singolo schema di involucro regalo_**

1. Apri la progettazione della confezione regalo in modalità di modifica.

1. Nella parte superiore dell’area di lavoro, fai clic su **[!UICONTROL Delete]**.

1. Quando richiesto, fai clic su **[!UICONTROL OK]** per confermare.

**_Metodo 2: Eliminare più schemi di confezione regalo_**

1. In _Confezione Regalo_ griglia, selezionare la casella di spunta di ogni schema a capo personalizzato che si desidera eliminare.

1. Imposta il **[!UICONTROL Actions]** controllo a `Delete`.

1. Clic **[!UICONTROL Submit]**.

### Imposta opzioni regalo

![Adobe Commerce](../assets/adobe-logo.svg) (Solo Adobe Commerce)

I prezzi della confezione regalo e della gift card stampata possono essere configurati in modo da includere o escludere l&#39;imposta o da visualizzare entrambe le opzioni. È inoltre possibile specificare una classe fiscale per questi articoli, a livello globale o a livello di sito Web.

**_Per configurare le imposte sulle opzioni regalo:_**

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Sales]** e scegli **[!UICONTROL Tax]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Tax Classes]** sezione.

   ![Configurazione classe fiscale](../configuration-reference/sales/assets/tax-tax-classes.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Tax Class for Gift Options]** alla classe fiscale applicabile.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Orders, Invoices, Credit Memos Display Settings]** sezione.

   ![Impostazioni di visualizzazione di ordini, fatture e note di accredito](../configuration-reference/sales/assets/tax-orders-invoices-credit-memos-display-settings.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Display Gift Wrapping Prices]** a uno dei seguenti elementi:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Imposta **[!UICONTROL Display Printed Card Prices]** a uno dei seguenti elementi:

   - `Excluding Tax`
   - `Including Tax`
   - `Including and Excluding Tax`

1. Clic **[!UICONTROL Save Config]**.
