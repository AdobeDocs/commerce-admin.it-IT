---
title: Media - Immagine
description: Scopri il tipo di contenuto Immagine, utilizzato per aggiungere un’immagine JPG, GIF o PNG al [!DNL Page Builder] fase.
exl-id: 1b8d906e-7570-4c1f-87a0-992400faf55c
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1551'
ht-degree: 0%

---

# Media - Immagine

Utilizza il _Immagine_ tipo di contenuto per aggiungere un&#39;immagine JPG, GIF o PNG al [[!DNL Page Builder] fase](workspace.md#stage). Oltre all&#39;immagine desktop predefinita, è possibile specificare un&#39;immagine secondaria per i dispositivi mobili. Puoi anche aggiungere una didascalia che appare sotto l&#39;immagine e collegarla a qualsiasi URL, prodotto, categoria o pagina.

>[!TIP]
>
>È possibile utilizzare [Integrazione di Adobe Stock](../content-design/adobe-stock.md) per trovare e salvare una risorsa appropriata tra i milioni forniti da [Adobe Stock](https://stock.adobe.com). Consulta [Utilizzo delle immagini di Adobe Stock](../content-design/adobe-stock-manage.md) per informazioni dettagliate su come cercare, perfezionare e salvare le risorse Adobe Stock nella galleria.

{{$include /help/_includes/page-builder-save-timeout.md}}

## Casella degli strumenti Immagine

La casella degli strumenti Immagine viene visualizzata quando passi il cursore del mouse sul contenitore immagine.

![Casella degli strumenti Immagine](./assets/pb-media-image-giftcard-column-toolbox.png){width="500" zoomable="yes"}

| Strumento | Icona | Descrizione |
|--- |--- |--- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta l&#39;immagine in un&#39;altra posizione sullo stage. |
| (etichetta) | Immagine | Identifica il contenitore di contenuto corrente come immagine. Passa il cursore del mouse sul contenitore di immagini per visualizzare la casella degli strumenti. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre il _Modifica immagine_ , in cui è possibile modificare le proprietà dell’immagine e del contenitore. |
| Nascondi | ![Nascondi icona](./assets/pb-icon-hide.png){width="25"} | Nasconde l&#39;immagine corrente. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra l&#39;immagine nascosta. |
| Duplica | ![Icona Duplica](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia dell&#39;immagine. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina l&#39;immagine dalla fase. |
| Carica nuova immagine |  | Carica un&#39;immagine dal file system locale alla raccolta. |
| Seleziona dalla raccolta |  | Consente di scegliere un&#39;immagine esistente dalla raccolta. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Aggiungi un&#39;immagine

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Media]** e trascina un **[!UICONTROL Image]** segnaposto al contenitore di destinazione.

   È possibile aggiungere un&#39;immagine a una riga, colonna o scheda. Nell’esempio seguente, l’immagine viene trascinata in una colonna vuota.

   ![Trascinamento di un tipo di contenuto immagine nell’area di visualizzazione](./assets/pb-media-image-drag.png){width="600" zoomable="yes"}

1. Per aggiungere la risorsa immagine, utilizza uno dei seguenti metodi:

   ![Carica immagine o seleziona dagli strumenti della Galleria sull&#39;area di visualizzazione](./assets/pb-media-image-upload-select.png){width="500" zoomable="yes"}

   >[!NOTE]
   >
   >La dimensione massima del file è di 4 MB. I tipi di file supportati sono JPG, GIF e PNG.

   - _**Carica una nuova immagine**_: utilizza questo metodo per caricare un nuovo file di immagine dal sistema.

      - Clic **[!UICONTROL Upload Image]**.

      - Individua e scegli l’immagine da aggiungere alla galleria e al contenitore di destinazione.

     In alternativa, è possibile trascinare un file di immagine dal sistema e rilasciarlo sulla _Fotocamera_ ( ![Icona fotocamera](./assets/pb-icon-camera.png){width="20"} ).

   - _**Seleziona una risorsa esistente**_: utilizza questo metodo per selezionare una risorsa immagine esistente dall’archivio multimediale o dalla galleria.

      - Clic **[!UICONTROL Select from Gallery]**.

      - Utilizza la struttura ad albero per passare all’immagine.

      - Fai clic sulla miniatura e fai clic su **[!UICONTROL Add Selected]**.

        ![Aggiunta di un&#39;immagine selezionata](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - _**Cerca e seleziona un’immagine Adobe Stock**_: utilizza questo metodo per trovare un’immagine da Adobe Stock.

     >[!NOTE]
     >
     >Questo metodo richiede un [Integrazione con Adobe Stock](../content-design/adobe-stock.md) configurato per l’Amministratore.

      - Clic **[!UICONTROL Search Adobe Stock]** e cercare un&#39;immagine.

      - Salvare l&#39;anteprima o l&#39;immagine con licenza nella raccolta.

        Consulta [Utilizzo delle immagini di Adobe Stock](../content-design/adobe-stock-manage.md) per ulteriori informazioni sull’utilizzo delle risorse di Adobe Stock.

      - Seleziona la miniatura della risorsa nella galleria e fai clic su **[!UICONTROL Add Selected]**.

   L’immagine viene visualizzata nel contenitore di destinazione nella posizione del segnaposto. A differenza di un’immagine di sfondo, puoi spostare l’immagine in una posizione diversa all’interno del contenitore corrente o in un contenitore diverso.

   >[!NOTE]
   >
   >Il [Banner](banner.md) e [Cursore](slider.md) i tipi di contenuto includono _Carica immagine_ e _Seleziona dalla raccolta_ opzioni per l&#39;aggiunta di immagini.

   ![Immagine in una colonna](./assets/pb-media-image-column1-giftcard.png){width="500" zoomable="yes"}

## Modifica impostazioni immagine

1. Passa il cursore del mouse sul contenitore delle immagini per visualizzare la casella degli strumenti e scegli _Impostazioni_ (![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).
Il nome del file, le dimensioni e le dimensioni vengono visualizzati sotto l&#39;immagine corrente.

   ![Immagine corrente](./assets/pb-media-image-settings-image.png){width="600" zoomable="yes"}

1. Per modificare la **[!UICONTROL Image]**, eseguire una delle operazioni seguenti:

   - _**Carica una nuova immagine**_: utilizza questo metodo per caricare un nuovo file di immagine dal sistema.

      - Clic **[!UICONTROL Upload Image]**.

      - Individua e scegli l’immagine da aggiungere alla galleria e al contenitore di destinazione.

   - _**Seleziona una risorsa esistente**_: utilizza questo metodo per selezionare una risorsa immagine esistente dall’archivio multimediale o dalla galleria.

      - Clic **[!UICONTROL Select from Gallery]**.

      - Utilizza la struttura ad albero per passare all’immagine.

      - Fai clic sulla miniatura e fai clic su **[!UICONTROL Add Selected]**.

        ![Aggiunta di un&#39;immagine selezionata](./assets/pb-media-image-gallery-add-selected.png){width="600" zoomable="yes"}

   - **Cerca e seleziona un’immagine Adobe Stock**: utilizza questo metodo per trovare un’immagine da Adobe Stock.

     >[!NOTE]
     >
     >Questo metodo richiede un [Integrazione con Adobe Stock](../content-design/adobe-stock.md) configurato per l’Amministratore.

      - Clic **[!UICONTROL Search Adobe Stock]** e cercare un&#39;immagine.

      - Salvare l&#39;anteprima o l&#39;immagine con licenza nella raccolta.

        Consulta [Utilizzo delle immagini di Adobe Stock](../content-design/adobe-stock-manage.md) per ulteriori informazioni sull’utilizzo delle risorse di Adobe Stock.

      - Seleziona la miniatura della risorsa nella galleria e fai clic su **[!UICONTROL Add Selected]**.

1. Per aggiungere una **[!UICONTROL Mobile Image]**, utilizza gli stessi metodi descritti nel passaggio precedente per selezionare un’immagine da utilizzare per la visualizzazione su dispositivi mobili.

   ![Immagine mobile](./assets/pb-media-image-settings-mobile-image.png){width="600" zoomable="yes"}

1. Se necessario, specifica un **[!UICONTROL Link]** per l&#39;immagine.

   Il collegamento è la pagina di destinazione che viene visualizzata quando il cliente fa clic sull&#39;immagine. Puoi utilizzare uno dei tre tipi di collegamento seguenti:

   - **[!UICONTROL URL]** : collegamenti a un URL relativo o completo.

   - **[!UICONTROL Product]** : identifica la pagina di destinazione in base al nome del prodotto o allo SKU. Cerca il prodotto per nome in base a un nome parziale o completo. Scegli il prodotto dall’elenco dei risultati della ricerca.

     ![Scelta di un prodotto da collegare](./assets/pb-media-image-settings-image-link-product-results.png){width="600" zoomable="yes"}

   - **[!UICONTROL Category]** - Identifica la pagina di destinazione come una categoria o sottocategoria specifica nella struttura delle categorie. Cerca la categoria in base a un nome parziale o completo. Scegliete la categoria dalla sezione espansa della struttura visualizzata.

     ![Scelta di una categoria da collegare](./assets/pb-media-image-settings-image-link-category-tree.png){width="600" zoomable="yes"}

   - **[!UICONTROL Page]** : identifica la pagina di destinazione come pagina di contenuto specifica. Cerca la pagina in base a un nome parziale o completo. Scegliere la pagina dall&#39;elenco dei risultati di ricerca.

     ![Scelta della pagina da collegare](./assets/pb-media-image-settings-image-link-page-results.png){width="600" zoomable="yes"}

   Per evitare che il visitatore si allontani dal tuo negozio, seleziona la **[!UICONTROL Open in new tab]** casella di controllo. Quando la casella di controllo è deselezionata, la destinazione collegata si apre nella stessa scheda del browser, in modo da allontanare il visitatore dal tuo archivio.

1. Per aggiungere una **[!UICONTROL Image Caption]**, immetti il testo da visualizzare sotto l&#39;immagine.

   Il formato della didascalia è determinato dal foglio di stile associato al tema corrente.

   La didascalia viene in genere visualizzata sotto l’immagine e fornisce informazioni sull’immagine ai visitatori e ai motori di ricerca. Se il sito è disponibile in più lingue, è possibile utilizzare la stessa immagine, ma tradurre la didascalia. In HTML, il `<figcaption>` è un sottoinsieme del `<figure>` tag. `<figcaption>This is the image caption</figcaption>`

1. Aggiorna le altre impostazioni in base alle esigenze:

   - [Ottimizzazione motore di ricerca](#search-engine-optimization)
   - [Avanzate](#advanced)

1. Al termine, fai clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare al [!DNL Page Builder] Workspace.

## Spostare un’immagine

1. Passa il puntatore del mouse sul contenitore di immagini per visualizzare la casella degli strumenti e scegli _Sposta_ (![Icona Sposta](./assets/pb-icon-move.png){width="20"} ).

   ![Spostamento di un&#39;immagine](./assets/pb-media-image-column1-move-giftcard.png){width="500" zoomable="yes"}

1. Seleziona e trascina l’immagine nella nuova posizione, appena sotto la linea guida rossa.

   ![Utilizzo della linea guida rossa per posizionare l&#39;immagine](./assets/pb-media-image-column2-move-giftcard-red-guideline.png){width="500" zoomable="yes"}

## Rimuovere un&#39;immagine

1. Passa il puntatore del mouse sul contenitore di immagini per visualizzare la casella degli strumenti e scegli _Rimuovi_ ( ![Icona Rimuovi](./assets/pb-icon-remove.png){width="20"} ).

1. Quando viene richiesto di confermare, fai clic su **[!UICONTROL OK]**.

## Ottimizzazione motore di ricerca

Il testo di queste impostazioni è visibile ai motori di ricerca e migliora l’indicizzazione della pagina.

- Per **[!UICONTROL Alternative Text]**, immetti un _Alt_ descrizione testuale degli strumenti di accesso facilitato digitale da visualizzare.

  L’utilizzo di testo alternativo è una best practice in materia di accessibilità ed è richiesto per legge in alcune lingue. In HTML, il `alt` è un sottoinsieme del `image` tag: `<image title="tooltip" alt="description" src="image.jpg">`.

- Per **[!UICONTROL Title Attribute]**, immetti il testo da visualizzare come descrizione comando al passaggio del mouse.

  Come best practice, scegli un titolo descrittivo ricco di parole chiave per migliorare il modo in cui l’immagine viene indicizzata dai motori di ricerca. In HTML, il `title` è un sottoinsieme del `image` tag: `<image title="tooltip" alt="description" src="image.jpg">`.

## [!UICONTROL Advanced]

- Per controllare il posizionamento orizzontale delle immagini aggiunte al contenitore, scegliete un **[!UICONTROL Alignment]**.

  | Opzione | Descrizione |
  | ------ | ----------- |
  | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
  | `Left` | Allinea il contenuto dell’immagine lungo il bordo sinistro del contenitore di immagini, tenendo conto di eventuali spaziature specificate. |
  | `Center` | Allinea il contenuto dell’immagine al centro del contenitore immagini, tenendo conto di eventuali spaziature specificate. |
  | `Right` | Allinea il contenuto dell’immagine al bordo destro del contenitore immagini, tenendo conto di eventuali spaziature specificate. |

  {style="table-layout:auto"}

- Imposta il **[!UICONTROL Border]** stile applicato a tutti e quattro i lati del contenitore di immagini:

  | Opzione | Descrizione |
  | ------ | ----------- |
  | `Default` | Applica lo stile di bordo predefinito specificato dal foglio di stile associato. |
  | `None` | Non fornisce alcuna indicazione visibile dei bordi del contenitore. |
  | `Dotted` | Il bordo del contenitore viene visualizzato come una linea tratteggiata. |
  | `Dashed` | Il bordo del contenitore viene visualizzato come una linea tratteggiata. |
  | `Solid` | Il bordo del contenitore viene visualizzato come linea continua. |
  | `Double` | Il bordo del contenitore viene visualizzato come una doppia riga. |
  | `Groove` | Il bordo del contenitore viene visualizzato come una linea scanalata. |
  | `Ridge` | Il bordo del contenitore viene visualizzato come una linea scanalata. |
  | `Inset` | Il bordo del contenitore viene visualizzato come una linea interna. |
  | `Outset` | Il bordo del contenitore viene visualizzato come una linea di contorno. |

  {style="table-layout:auto"}

- Se si imposta uno stile di bordo diverso da `None`, completare le opzioni di visualizzazione del bordo:

  ![Colore bordo](./assets/pb-settings-border-color.png){width="600" zoomable="yes"}

  | Opzione | Descrizione |
  | ------ |------------ |
  | [!UICONTROL Border Color] | Specificate il colore scegliendo un campione, facendo clic sul selettore del colore oppure immettendo un nome di colore valido o un valore esadecimale equivalente. |
  | [!UICONTROL Border Width] | Immettere il numero di pixel per lo spessore della linea del bordo. |
  | [!UICONTROL Border Radius] | Immettere il numero di pixel per definire la dimensione del raggio utilizzato per arrotondare ogni angolo del bordo. |

  {style="table-layout:auto"}

- (Facoltativo) Specifica i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente per applicarlo al contenitore di immagini.

  Separare più nomi di classe con uno spazio.

- Immetti i valori, in pixel, per il **[!UICONTROL Margins and Padding]** per specificare i margini esterni e la spaziatura interna del contenitore di immagini.

  Immetti ogni valore corrispondente nel diagramma del contenitore di immagini.

  | Area contenitore | Descrizione |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. |
  | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. |

  {style="table-layout:auto"}
