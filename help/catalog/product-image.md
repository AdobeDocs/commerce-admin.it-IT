---
title: Gestire immagini e video dei prodotti
description: Scopri come gestire le risorse immagine e video per gli elenchi dei prodotti.
exl-id: 3cb4ab8a-8966-400f-be94-a517634d1334
feature: Catalog Management, Products, Media
source-git-commit: 01148770946a236ece2122be5a88b963a0f07d1f
workflow-type: tm+mt
source-wordcount: '1013'
ht-degree: 0%

---

# Gestire immagini e video dei prodotti

Per ogni prodotto, puoi caricare più immagini e video, riorganizzarne l’ordine e controllarne l’utilizzo. Se devi gestire un numero elevato di immagini, puoi preferire importarle come batch, anziché caricarle singolarmente. Per ulteriori informazioni, consulta [Importare immagini prodotto](../systems/data-import-product-images.md).

Se prevedi di caricare immagini di grandi dimensioni da visualizzare sul _[!UICONTROL Product Details]_, è possibile impostare una dimensione massima in pixel (larghezza e altezza) e ridimensionare automaticamente i file al momento del caricamento. È disponibile un’opzione per abilitare il ridimensionamento automatico di file di immagine più grandi durante il caricamento. Per ulteriori informazioni, consulta [Ridimensionamento immagine prodotto](product-image-config.md#product-image-resizing).

## Aggiornare le immagini del prodotto

1. Apri il prodotto in modalità di modifica.

1. Per utilizzare una visualizzazione specifica dello store, impostare **[!UICONTROL Store View]** selettore nell’angolo in alto a sinistra della vista applicabile.

   >[!NOTE]
   >
   >Le nuove immagini dei prodotti sono **_sempre_** caricato e visibile in **_tutto_** archiviare le visualizzazioni, anche se `All Store Views` ambito non utilizzato per il caricamento. <br/><br/>Per nascondere un’immagine del prodotto da una visualizzazione specifica dello store, devi passare a tale visualizzazione, seleziona la **[!UICONTROL Hide from Product Page]** selezionare l&#39;immagine e fare clic su **[!UICONTROL Save]**.

1. Scorri verso il basso ed espandi _[!UICONTROL Images and Videos]_sezione.

### Carica un&#39;immagine

Per una migliore compatibilità, si consiglia di caricare tutte le immagini del prodotto con il `sRGB` profilo colore. Tutti gli altri profili colore vengono automaticamente convertiti in `sRGB` profilo colore durante il caricamento dell’immagine del prodotto, che potrebbe causare incoerenza colore nell’immagine caricata.

La lunghezza del nome del file di immagine, inclusa l&#39;estensione, non può superare i 90 caratteri.

Per caricare un&#39;immagine, effettuare una delle seguenti operazioni:

- Trascina un’immagine dal desktop e rilasciala sulla _Fotocamera_ ( ![Icona fotocamera](../assets/icon-camera.png) ) affiancare nella _[!UICONTROL Images And Videos]_casella.

- In _[!UICONTROL Images And Videos]_, fare clic sul pulsante_ Fotocamera _( ![Icona fotocamera](../assets/icon-camera.png) ), selezionare il file di immagine sul computer e fare clic su **[!UICONTROL Open]**.

  ![Carica o trascina](./assets/product-images-and-video-jewel-tee.png){width="600" zoomable="yes"}

### Ridisponi immagini

Per modificare l&#39;ordine delle immagini nella raccolta, fare clic sul pulsante _[!UICONTROL Sort]_( ![Icona Ordina](./assets/inventory-icon-sort.png) ) nella parte inferiore del riquadro immagine e trascinare l&#39;immagine in una posizione diversa nel riquadro_[!UICONTROL Images And Videos]_ casella.

![Cambia ordine](./assets/product-images-and-videos-drag.png){width="600" zoomable="yes"}

### Eliminare un’immagine

Per rimuovere un&#39;immagine dalla raccolta, fare clic su **[!UICONTROL Delete]** ( ![Icona Elimina](../assets/icon-delete-trashcan.png) ) nell’angolo superiore destro del riquadro immagine e fai clic su **[!UICONTROL Save]**.

### Imposta dettagli immagine

Fare clic sull&#39;immagine che si desidera aprire nella visualizzazione dei dettagli ed eseguire una delle operazioni seguenti:

![Vista dettagli immagine](./assets/product-image-detail-jewel-tee.png){width="600" zoomable="yes"}

Per chiudere la visualizzazione dei dettagli, fare clic sul pulsante _Chiudi_ ( ![Icona Chiudi](../assets/icon-close-x.png) ) in alto a destra.

Al termine, fai clic su **[!UICONTROL Save]**.

#### Inserisci testo alternativo

Per migliorare l’accessibilità web, gli assistenti vocali fanno riferimento al testo Image Alt e i motori di ricerca durante l’indicizzazione del sito fanno riferimento a tale testo. Alcuni browser visualizzano il testo Alt al passaggio del mouse. Il testo alternativo può contenere diverse parole e includere parole chiave selezionate con attenzione.

In _[!UICONTROL Alt Text]_immettere una breve descrizione dell&#39;immagine.

#### Assegna ruoli

Per impostazione predefinita, tutti i ruoli vengono assegnati alla prima immagine caricata sul prodotto. Per riassegnare un ruolo a un&#39;altra immagine, effettuare le seguenti operazioni:

In _[!UICONTROL Role]_selezionare il ruolo che si desidera assegnare all&#39;immagine.

Quando ritorni al _Immagini e video_ I ruoli attualmente assegnati vengono visualizzati sotto ogni immagine.

![Ruoli assegnati](./assets/product-images-video-swatch.png){width="600" zoomable="yes"}

#### Nascondi un&#39;immagine

Per escludere un&#39;immagine dalla raccolta miniature, selezionare **[!UICONTROL Hidden]** e fai clic su **[!UICONTROL Save]**.

![Immagini nascoste](./assets/product-images-and-videos-hidden.png){width="600" zoomable="yes"}

## Ruoli immagine

| Ruolo immagine | Descrizione |
|--- |--- |
| [!UICONTROL Thumbnail] | Le miniature vengono visualizzate nella raccolta miniature, nel carrello e in alcuni blocchi, ad esempio Elementi correlati. Esempio di dimensioni: 50 x 50 pixel |
| [!UICONTROL Small Image] | L’immagine piccola viene utilizzata per le immagini del prodotto negli elenchi nelle pagine delle categorie e dei risultati di ricerca e per visualizzare le immagini del prodotto necessarie per sezioni quali up-sell, cross-selling e elenco nuovi prodotti. Esempio di dimensioni: 470 x 470 pixel |
| [!UICONTROL Base Image] | L’immagine di base è l’immagine principale nella pagina dei dettagli del prodotto. Lo zoom dell’immagine viene attivato se carichi un’immagine di dimensioni superiori a quelle del contenitore dell’immagine. A seconda del livello di zoom da raggiungere, l’immagine di base deve essere due o tre volte la dimensione del contenitore. Esempi di dimensioni: 470 x 470 pixel (senza zoom), 1100 x 1100 pixel (con zoom) |
| [!UICONTROL Swatch] | A [campione](swatches.md) può essere utilizzato per illustrare il colore, il motivo o la texture. Esempio di dimensioni: 50 x 50 pixel |

{style="table-layout:auto"}

## Filigrane

Se si va a scapito di creare le proprie immagini di prodotto originali, non c&#39;è molto si può fare per evitare che concorrenti senza scrupoli di rubare loro con il clic di un mouse. Tuttavia, puoi renderli un target meno attraente inserendo una filigrana su ogni immagine per identificarli come proprietà. Un file di filigrana può essere un&#39;immagine JPG (JPEG), GIF o PNG. Entrambi i tipi di file GIF e PNG supportano livelli trasparenti, che possono essere utilizzati per conferire alla filigrana uno sfondo trasparente.

La filigrana utilizzata per _piccolo_ L&#39;immagine nell&#39;esempio seguente è un logo nero con uno sfondo trasparente e salvato come file PNG con le seguenti impostazioni:

- Dimensioni: 50x50
- Opacità: 5
- Posizione: sezione

![Filigrana affiancata](./assets/storefront-watermark-tiled.png){width="700" zoomable="yes"}

### Aggiungere filigrane alle immagini del prodotto

1. Il giorno _Amministratore_ barra laterale, vai a **[!UICONTROL Content]** > _[!UICONTROL Design]_>**[!UICONTROL Configuration]**.

   Per ulteriori informazioni sulle configurazioni di progettazione, consulta [Configurazione del progetto](../content-design/configuration.md).

1. Individuare la visualizzazione dello store che si desidera configurare e fare clic su **[!UICONTROL Edit]** nel _[!UICONTROL Action]_colonna.

1. Sotto _[!UICONTROL Other Settings]_, espandi ![Selettore di espansione](../assets/icon-display-expand.png) il **[!UICONTROL Product Image Watermarks]**sezione.

   ![Filigrane immagine prodotto - Base](./assets/config-design-product-image-watermarks-base.png){width="600" zoomable="yes"}

   Il **[!UICONTROL Base]**, **[!UICONTROL Thumbnail]**, **[!UICONTROL Small]**, e **[!UICONTROL Swatch Image]** le impostazioni dell&#39;immagine sono uguali.

1. Per aggiungere la risorsa immagine della filigrana, utilizza uno dei seguenti metodi:

   - Clic **[!UICONTROL Upload]** e scegliere il file di immagine sul sistema da caricare per utilizzarlo come filigrana.
   - Clic **[!UICONTROL Select from Gallery]** e seleziona una risorsa immagine da [Raccolta file multimediali](../content-design/media-gallery.md).

1. Completare le impostazioni per la visualizzazione della filigrana:

   - Inserisci il **[!UICONTROL Image Opacity]** come percentuale. Ad esempio: `40`

   - Inserisci il **[!UICONTROL Image Size]** in pixel. Ad esempio: `200 x 200`

   - Imposta **[!UICONTROL Image Position]** per determinare la posizione della filigrana.

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema e aggiorna la cache non valida.

   ![Aggiorna cache](./assets/msg-cache-management.png){width="600" zoomable="yes"}

>[!TIP]
>
>Puoi fare clic su **[!UICONTROL Use Default Value]** ![Ritorno a freccia](../assets/icon-arrow-return.png) per ripristinare il valore predefinito.

### Eliminare una filigrana

1. Nell’angolo inferiore sinistro dell’immagine, fai clic su **[!UICONTROL Delete]** ( ![Icona Elimina](../assets/icon-delete-trashcan-solid.png) ).

   ![Elimina filigrana](./assets/product-image-watermark-delete.png){width="300"}

1. Clic **[!UICONTROL Save Config]**.

1. Quando viene richiesto di aggiornare la cache, fare clic su **[!UICONTROL Cache Management]** nel messaggio di sistema e aggiorna la cache non valida.

   Se l’immagine della filigrana persiste nella vetrina, torna alla gestione della cache e fai clic su **[!UICONTROL Flush Magento Cache]**.
