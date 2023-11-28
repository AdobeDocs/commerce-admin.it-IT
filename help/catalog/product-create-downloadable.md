---
title: Prodotto scaricabile
description: Scopri come creare un prodotto scaricabile da distribuire come file digitale.
exl-id: c3dd4c5f-adc1-4a8f-a9da-7f0dedd1ee34
feature: Catalog Management, Products
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1619'
ht-degree: 0%

---

# Prodotto scaricabile

Un prodotto scaricabile può essere qualsiasi cosa sia possibile consegnare come file, ad esempio un eBook, musica, video, applicazione software o aggiornamento. È possibile offrire un album in vendita e vendere ogni singola canzone. Puoi anche utilizzare un prodotto scaricabile per distribuire una versione elettronica del catalogo dei prodotti.

Poiché il download è disponibile solo dopo l’acquisto, puoi fornire esempi, ad esempio un estratto da un libro, un clip da un file audio o un trailer da un video. Un esempio è qualcosa che il cliente può provare prima di acquistare il prodotto. I file che rendi disponibili per il download possono essere caricati sul tuo server o da un altro server.

![Prodotto scaricabile](./assets/storefront-product-downloadable.png){width="700" zoomable="yes"}

I prodotti scaricabili possono essere configurati in modo da richiedere che il cliente acceda a un account per ricevere il collegamento oppure possano essere inviati tramite e-mail e condivisi con altri utenti. Lo stato dell’ordine prima che il download diventi disponibile, i valori predefiniti e altre opzioni di consegna sono impostati nella configurazione. Quando pianifichi le aggiunte al catalogo scaricabili, tieni presente quanto segue:

- I prodotti scaricabili possono essere caricati sul server o collegati a da un altro server su Internet.

- Puoi determinare quante volte un cliente può scaricare un prodotto.

- Ai clienti che acquistano un prodotto scaricabile può essere richiesto di effettuare l’accesso prima di procedere al pagamento.

- La consegna di un prodotto scaricabile può essere effettuata quando l’ordine è in una `Pending` o `Invoiced` stato.

- Poiché i prodotti scaricabili non vengono spediti, il _Spedizione_ Il passaggio del pagamento viene ignorato quando il carrello contiene solo il prodotto scaricabile.


## Configurare le opzioni di download

Le impostazioni di configurazione scaricabili determinano i valori predefiniti e le opzioni di consegna per i prodotti scaricabili e specificano se gli ospiti possono acquistare i download.

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra, espandi **[!UICONTROL Catalog]** e scegli **[!UICONTROL Catalog]** sotto.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _[!UICONTROL Downloadable Product Options]_sezione.

   ![Opzioni di prodotto scaricabili](../configuration-reference/catalog/assets/catalog-downloadable-product-options.png){width="700" zoomable="yes"}

   Per un elenco dettagliato di queste opzioni di configurazione, vedi [_Opzioni di prodotto scaricabili_](../configuration-reference/catalog/catalog.md#downloadable-product-options) nel _Riferimento configurazione_.

1. Per determinare lo stato del processo dell&#39;ordine quando il download diventa disponibile, impostare **[!UICONTROL Order Item Status to Enable Downloads]** a uno dei seguenti elementi:

   - `Pending`
   - `Invoiced`

1. Per impostare un limite predefinito per il numero di download che un singolo cliente può effettuare, inserisci il numero per **[!UICONTROL Default Maximum Number of Downloads]**.

1. Imposta **[!UICONTROL Shareable]** a uno dei seguenti elementi:

   - `Yes` - Consente ai clienti di inviare ad altri il collegamento per il download tramite e-mail.
   - `No` - Impedisce ai clienti di condividere il collegamento di download con altri utenti richiedendo ai clienti di accedere al proprio account per accedere ai collegamenti di download.

1. Per **[!UICONTROL Default Sample Title]**, immettere l&#39;intestazione che si desidera visualizzare sopra la selezione dei campioni.

   ![Titolo esempio](./assets/product-downloadable-config-sample-title.png){width="400"}

1. Per **[!UICONTROL Default Link Title]**, immetti il testo predefinito che desideri utilizzare per i collegamenti di download.

1. Se vuoi che il collegamento di download si apra in una nuova finestra del browser, imposta **[!UICONTROL Opens Links in New Window]** a `Yes`.

   Questa impostazione viene utilizzata per mantenere aperta la finestra del browser per il tuo store.

1. Per determinare come viene distribuito il contenuto scaricabile, imposta **[!UICONTROL Use Content Disposition]** a uno dei seguenti elementi:

   - `Attachment` - Fornisce il collegamento per il download tramite e-mail come allegato.
   - `Inline` : fornisce il collegamento per il download come collegamento a una pagina web.

1. Se desideri che gli acquirenti si registrino per un account cliente e accedano prima di acquistare un download, imposta **[!UICONTROL Disable Guest Checkout if Cart Contains Downloadable Items]** a `Yes`.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

## Creare un prodotto scaricabile

Le istruzioni seguenti illustrano il processo di creazione di un prodotto scaricabile utilizzando un [modello di prodotto](attribute-sets.md), campi obbligatori e impostazioni di base. Ogni campo obbligatorio è contrassegnato da un asterisco rosso (`*`). Al termine delle nozioni di base, puoi completare le altre impostazioni del prodotto in base alle esigenze.

>[!NOTE]
>
>I nomi dei file scaricabili possono includere lettere e numeri. È possibile utilizzare un trattino o un carattere di sottolineatura per rappresentare uno spazio tra le parole. Eventuali caratteri non validi nel nome del file vengono sostituiti da un carattere di sottolineatura.

### Passaggio 1: scegliere il tipo di prodotto

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Catalog]** > **[!UICONTROL Products]**.

1. Il giorno _[!UICONTROL Add Product]_( ![Freccia del menu](../assets/icon-menu-down-arrow-red.png){width="25"} ) nell&#39;angolo superiore destro, scegliere `Downloadable Product`.

   ![Aggiungi prodotto scaricabile](./assets/product-add-downloadable.png){width="700" zoomable="yes"}

### Passaggio 2: scegliere la serie di attributi

I dati di esempio includono [set di attributi](attribute-sets.md) ha chiamato _Download disponibile_ con campi speciali per i prodotti scaricabili. Puoi utilizzare un modello esistente o crearne un altro prima di salvare il prodotto.

Per scegliere la serie di attributi utilizzata come modello per il prodotto, effettuare una delle seguenti operazioni:

- Per **[!UICONTROL Search]**, immettere il nome della serie di attributi.

- Nell’elenco, scegli `Downloadable` set di attributi.

Il modulo viene aggiornato per riflettere la modifica.

![Scegli set di attributi](./assets/product-create-choose-attribute-set-downloadable.png){width="600" zoomable="yes"}

### Passaggio 3: completare le impostazioni richieste

1. Inserisci il **[!UICONTROL Product Name]**.

1. Accetta il valore predefinito **[!UICONTROL SKU]** in base al nome del prodotto o immettine un altro.

1. Inserisci il prodotto **[!UICONTROL Price]**.

1. Poiché il prodotto non è ancora pronto per la pubblicazione, imposta **[!UICONTROL Enable Product]** a `No`.

1. click **[!UICONTROL Save]** e continua.

   Quando il prodotto viene salvato, la [Visualizzazione store](introduction.md#product-scope) selettore viene visualizzato nell&#39;angolo superiore sinistro.

1. Scegli la **[!UICONTROL Store View]** dove il prodotto deve essere disponibile.

   ![Scegli la vista dello store](./assets/product-create-store-view-choose.png){width="600" zoomable="yes"}

### Passaggio 4: completare le impostazioni di base

1. Imposta **[!UICONTROL Tax Class]** a uno dei seguenti elementi:

   - `None`
   - `Taxable Goods`

1. Inserisci il **[!UICONTROL Quantity]** del prodotto che è in magazzino.

   Prendi nota di quanto segue:

   - Per impostazione predefinita, **[!UICONTROL Stock Status]** è impostato su `Out of Stock`.

   - Poiché i prodotti scaricabili non vengono spediti, il **[!UICONTROL Weight]** non è utilizzato. Se abiliti questa funzione, diventa un [Prodotto semplice](product-create-simple.md) e _Questo prodotto è scaricabile?_ non può essere utilizzata.

   >[!NOTE]
   >
   >Se si abilita [Inventory management](../inventory-management/introduction.md), i commercianti con origine singola impostano la quantità in questa sezione. I commercianti con più origini aggiungono origini e quantità nella sezione Origini. Vedi quanto segue _Assegna origini e quantità (Inventory management)_ sezione.

1. Accetta il valore predefinito **[!UICONTROL Visibility]** impostazione di `Catalog, Search`.

1. Per inserire il prodotto in [elenco di nuovi prodotti](../content-design/widget-new-products-list.md), seleziona la **[!UICONTROL Set Product as New]** casella di controllo.

1. Da assegnare _[!UICONTROL Categories]_al prodotto, fai clic su **[!UICONTROL Select…]**ed effettuare una delle seguenti operazioni:

   **Scegli una categoria esistente**:

   - Inizia a digitare nella casella fino a trovare una corrispondenza.

   - Selezionare la casella di controllo di ciascuna categoria da assegnare.

   **Creare una categoria**:

   - Clic **[!UICONTROL New Category]**.

   - Inserisci il **[!UICONTROL Category Name]** e scegli la **[!UICONTROL Parent Category]**, che ne determina la posizione nel [struttura del menu](category-root.md).

   - Clic **[!UICONTROL Create Category]**.

1. Imposta **[!UICONTROL Format]** a uno dei seguenti elementi:

   - `Download`
   - `DVD`

   Se necessario, puoi modificare [attributo](attribute-product-create.md) per aggiungere altri valori.

   Potrebbero essere presenti attributi aggiuntivi che descrivono il prodotto. La selezione varia in base al set di attributi e può essere completata in un secondo momento.

#### Assegna origini e quantità ([!DNL Inventory Management])

{{$include /help/_includes/inventory-assign-sources.md}}

### Passaggio 5: completare le informazioni scaricabili

Scorri verso il basso, espandi ![Selettore di espansione](../assets/icon-display-expand.png) il _[!UICONTROL Downloadable Information]_e seleziona la sezione **[!UICONTROL Is this downloadable product?]**casella di controllo.

Quando è attivata, la _[!UICONTROL Downloadable Information]_La sezione è composta da due parti. La prima parte descrive ogni collegamento di download e la seconda descrive ogni file di esempio. Il valore predefinito per molte di queste opzioni può essere impostato nel [configurazione](#configure-the-download-options).

![Informazioni scaricabili](./assets/product-downloadable-information.png){width="600" zoomable="yes"}

#### Completa i collegamenti

1. In _[!UICONTROL Links]_, immetti il **[!UICONTROL Title]**che desideri utilizzare come intestazione per i collegamenti di download.

1. Se applicabile, selezionare **[!UICONTROL Links can be purchased separately]** casella di controllo.

1. Clic **[!UICONTROL Add Link]** ed effettuare le seguenti operazioni:

   - Inserisci il **[!UICONTROL Title]** e **[!UICONTROL Price]** del download.

   - Per entrambi **[!UICONTROL File]** e **[!UICONTROL Sample]** file, scegliere uno dei seguenti metodi di distribuzione per i download:

      - `Upload File` - Scegliere questo metodo per caricare il file di distribuzione sul server. Individua il file e selezionalo per il caricamento.
      - `URL` - Scegliere questo metodo per accedere al file di distribuzione da un URL. Immettere l&#39;URL completo del file di download.

   >[!NOTE]
   >
   >Non è possibile utilizzare collegamenti a risorse esterne come prodotti scaricabili. I domini di collegamento validi sono predefiniti a livello di programmazione nell&#39; `env.php` file (vedere [riferimento env.php](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/files/config-reference-envphp.html) nel _Guida alla configurazione_).

   - Imposta **[!UICONTROL Shareable]** a uno dei seguenti elementi:

      - `No` - Richiede ai clienti di accedere al proprio account per accedere al collegamento di download.

      - `Yes` : invia il collegamento tramite e-mail, che i clienti possono condividere con altri utenti.

      - `Use Config` : utilizza il metodo specificato in [Opzioni di prodotto scaricabili](../configuration-reference/catalog/catalog.md) configurazione.

   - Effettuare una delle seguenti operazioni:

      - Per limitare i download per cliente, inserisci il numero massimo di **[!UICONTROL Max. Downloads]**.
      - Per consentire download illimitati, seleziona la **[!UICONTROL Unlimited]** casella di controllo.

   ![Dettagli collegamento](./assets/product-downloadable-link-detail.png){width="600" zoomable="yes"}

1. Per aggiungere un altro collegamento, fai clic su **[!UICONTROL Add Link]** e ripeti questi passaggi.

#### Completa gli esempi

1. In _[!UICONTROL Samples]_, immetti il **[!UICONTROL Title]**che desideri utilizzare come intestazione per i campioni.

1. Per completare le informazioni per ciascun campione, fare clic su **[!UICONTROL Add Link]**.

   ![Esempi](./assets/product-downloadable-samples.png){width="600" zoomable="yes"}

1. Completa il collegamento come segue:

   - Inserisci il **[!UICONTROL Title]** del campione individuale.

   - Scegliere uno dei seguenti metodi di distribuzione:

      - `Upload File` - Scegliere questo metodo per caricare il file di distribuzione sul server. Individua il file e selezionalo per il caricamento.
      - `URL` - Scegliere questo metodo per accedere al file di distribuzione da un URL. Immettere l&#39;URL completo del file di download.

   - Per aggiungere un altro esempio, fai clic su **[!UICONTROL Add Link]** e ripeti questi passaggi.

   - Per modificare l&#39;ordine dei campioni, afferrare _Cambia ordine_ ( ![Controller posizione](../assets/icon-sort-order.png) ) e trascinare il campione in una nuova posizione.

### Passaggio 6: Completare le informazioni sul prodotto

Scorri verso il basso e completa le informazioni nelle sezioni seguenti, in base alle esigenze:

- [Contenuto](product-content.md)
- [Immagini e video](product-images-and-video.md)
- [Ottimizzazione motore di ricerca](product-search-engine-optimization.md)
- [Prodotti correlati, up-selling e cross-selling](related-products-up-sells-cross-sells.md)
- [Opzioni personalizzabili](settings-advanced-custom-options.md)
- [Prodotti nei siti Web](settings-basic-websites.md)
- [Progettazione](settings-advanced-design.md)
- [Opzioni regalo](product-gift-options.md)

### Passaggio 7: pubblicare il prodotto

Se sei pronto per pubblicare il prodotto nel catalogo, imposta **[!UICONTROL Enable Product]** a `Yes` ed effettuare una delle seguenti operazioni:

**Metodo 1:** Salva e visualizza anteprima

- Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]**.

- Per visualizzare il prodotto nel tuo negozio, scegli **[!UICONTROL Customer View]** il _Amministratore_ ( ![Freccia del menu](../assets/icon-menu-down-arrow-black.png) ).

  L’archivio si apre in una nuova scheda del browser.

  ![Visualizzazione cliente](./assets/product-admin-customer-view.png){width="600" zoomable="yes"}

**Metodo 2:** Salva e chiudi

Il giorno _[!UICONTROL Save]_( ![Freccia del menu](../assets/icon-menu-down-arrow-red.png){width="25"} ), scegliere **[!UICONTROL Save & Close]**.

## Esperienza vetrina

Nel dashboard dell’account del cliente, il _[!UICONTROL My Downloadable Products]_collegamenti alle pagine per ogni ordine di prodotti scaricabili. I download diventano disponibili dal conto del cliente quando l&#39;ordine è completato.

![Prodotti scaricabili](./assets/customer-account-my-downloadable-products.png){width="700" zoomable="yes"}

La tabella seguente descrive _Prodotti scaricabili_ valori:

| Colonna | Descrizione |
|--- |--- |
| [!UICONTROL Order#] | Il [ordine](../stores-purchase/orders.md) in cui è stato acquistato il prodotto scaricabile. Fornisce un collegamento ai dettagli dell’ordine. |
| [!UICONTROL Date] | Data di creazione ordine. |
| [!UICONTROL Title] | Il nome del prodotto scaricabile acquistato con l’ordine. Fornisce un collegamento al prodotto scaricabile. |
| [!UICONTROL Status] | Stato elaborazione ordine. |
| [!UICONTROL Remaining Downloads] | Numero di download disponibili del prodotto scaricato. |

_**Per scaricare un file di prodotto dal dashboard dell’account**_

1. Nel dashboard dell’account, il cliente sceglie **[!UICONTROL My Downloadable Products]**.

1. Trova l’ordine nell’elenco e fa clic sul collegamento dopo il titolo.

1. Nell’angolo inferiore destro della finestra di download, fai clic su _scaricare_ icona.

1. Individua il file nel percorso di download e lo salva nel percorso desiderato.
