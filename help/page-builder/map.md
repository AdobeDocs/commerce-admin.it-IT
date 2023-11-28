---
title: Media - Mappa
description: Scopri il tipo di contenuto Mappa, utilizzato per aggiungere una mappa da [!DNL Google Maps] Piattaforma per [!DNL Page Builder] fase.
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '1583'
ht-degree: 0%

---

# Media - Mappa

Utilizza il _Mappa_ tipo di contenuto da cui aggiungere una mappa [[!DNL Google Maps] Piattaforma][1] al [[!DNL Page Builder] fase](workspace.md#stage). Ad esempio, puoi aggiungere una mappa a un blocco e quindi aggiungerlo al [Chi siamo](../content-design/pages.md#about-us) e [Contattaci](../getting-started/store-details.md#contact-us-form) pagine.

Per ottenere il massimo da [!DNL Google Maps] Platform, puoi personalizzare la mappa, evidenziare le posizioni dei tuoi negozi e utilizzare Google [Places][2] per aggiungere informazioni dettagliate sul tuo store a tutti [!DNL Google Maps].

## Vantaggi dell’incorporamento di una mappa Google

1. Fornisce agli acquirenti una gamma completa di informazioni sulla tua attività (numero di telefono, sito Web, recensioni, valutazioni a stelle e così via) direttamente sul tuo sito.

1. Una mappa Google solitamente evidenzia le attrazioni vicine, parchi, ristoranti e così via. Queste informazioni aiutano i clienti a determinare l&#39;ubicazione fisica e a pianificare il viaggio.

1. Consente ai clienti di trovare facilmente l’indirizzo del negozio fisico senza dover aprire una nuova finestra del browser e lasciare il sito.

1. Se disponi di una catena di negozi fisici, l’aggiunta di una Google Map sul sito ti aiuta a rafforzare la brand awareness e la credibilità sotto forma di elementi evidenziati.

![Esempio di vetrina: mappa con posizione](./assets/pb-media-maps-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Casella degli strumenti Mappa

La casella degli strumenti mappa viene visualizzata quando passi il cursore sul contenitore mappa.

| Strumento | Icona | Descrizione |
|--- |--- |--- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta la mappa in un&#39;altra posizione sull&#39;area di visualizzazione. |
| (etichetta) | [!UICONTROL Map] | Identifica il contenitore di contenuto corrente come mappa. Passa il cursore del mouse sul contenitore della mappa per visualizzare la casella degli strumenti. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre la pagina Modifica mappa, in cui è possibile modificare le proprietà della mappa e del contenitore. |
| Nascondi | ![Nascondi icona](./assets/pb-icon-hide.png){width="25"} | Nasconde la mappa corrente. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra la mappa nascosta. |
| Duplica | ![Icona Duplica](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia della mappa. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina la mappa dalla fase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Configura [!DNL Google Maps] per l’Amministratore

Prima di aggiungere una mappa, è necessario aprire una [account][3] per una prova gratuita di [!DNL Google Maps] Platform. La versione di prova gratuita dura 12 mesi e include un credito di 300 dollari. Se utilizzi il tuo credito, Google non fatturerà il tuo account senza la tua autorizzazione.

### Passaggio 1: ottenere [!DNL Google Maps] Chiave API

A seconda che tu disponga già di un [!DNL Google Maps] key, utilizza una delle procedure seguenti per ottenere la chiave API necessaria per la configurazione. Per impostare un [!DNL Google Maps] chiave, è necessario essere un amministratore del sito autorizzato per abilitare la fatturazione per il tuo account. Se non sei pronto a configurare un [!DNL Google Maps] Account Platform, puoi saltare questo passaggio e utilizzare per il momento la mappa dei segnaposto.

1. Vai a [Console della piattaforma Google Cloud](https://cloud.google.com/console/google/maps-apis/overview).

1. Fai clic sull’elenco a discesa del progetto e seleziona o crea il progetto per il quale desideri aggiungere una chiave API.

1. Per configurare le credenziali API, segui la sezione [istruzioni][4] nel [!DNL Google Maps] documentazioni.

1. Copia la chiave API negli Appunti.

### Passaggio 2: configurare [!DNL Google Maps] in [!DNL Commerce]

1. In _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Strumenti di contenuto avanzati](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Per ulteriori informazioni sulle opzioni di configurazione degli Strumenti avanzati di Content Management, vedere [Guida di riferimento alla configurazione](../configuration-reference/general/content-management.md).

1. Per **[!UICONTROL Google Maps API Key]**, incolla la chiave copiata nel passaggio 1.

1. Clic **[!UICONTROL Test Key]**.

   Se si è verificato un problema con la chiave, tornare al [!DNL Google Maps] Sito di Platform per risolvere il problema. Riprovare.

1. Dopo aver verificato la chiave, fai clic su **[!UICONTROL Save Config]**.

## Aggiungi una mappa all&#39;area di visualizzazione

1. Apri la pagina, il blocco o il blocco dinamico in [!DNL Page Builder] Workspace.

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Media]** e trascina un **[!UICONTROL Map]** segnaposto nell&#39;area di visualizzazione.

   ![Trascinamento di una mappa sull&#39;area di visualizzazione](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Se [!DNL Google Maps] Platform è configurato per il tuo archivio, viene visualizzata una mappa per la posizione del tuo archivio.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Se [!DNL Google Maps] Platform non è ancora configurato per lo store, verrà visualizzata una mappa segnaposto.

   ![[!DNL Google Maps] Segnaposto](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Aggiungi una posizione mappa personalizzata

1. Passa il puntatore del mouse sul contenitore della mappa per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Nell&#39;angolo superiore destro del _[!UICONTROL Edit Map]_pagina, fai clic su **[!UICONTROL Add Location]**.

1. Inserisci il **[!UICONTROL Location Name]** che desideri associare al pin sulla mappa.

1. Raccogli le coordinate di posizione che desideri utilizzare per la posizione personalizzata.

   In alternativa, in **[!UICONTROL Position]** nella casella, puoi trascinare il pin nella mappa visualizzata.

   Se necessario, vai a [[!DNL Google Maps]][5] in una nuova finestra del browser e utilizza uno dei seguenti metodi per ottenere le coordinate:

   ![Coordinate mappa](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Metodo 1:** Copia da URL

   - Nell&#39;angolo in alto a sinistra, immetti l&#39;indirizzo nel **[!UICONTROL Search]** e fare clic sul pulsante _Ricerca_ ( ![Icona Ricerca](../assets/icon-magnify-search.png){width="20"} ).

   - Copia le coordinate nell’URL e incollale in un blocco note.

   **Metodo 2:** Copia da &quot;Cosa c&#39;è qui?&quot;

   - Fare clic con il pulsante destro del mouse sulla puntina rossa che indica la posizione sulla mappa e scegliere **[!UICONTROL What's here?]** nel menu.

   - Nell&#39;etichetta visualizzata, copiare il testo, incluse le coordinate, e incollarlo in un blocco note.

1. Inserisci i numeri, senza la virgola, in ciascuno dei **[!UICONTROL Coordinates]** scatole.

   È inoltre possibile immettere tutte le informazioni rimanenti che si desidera siano disponibili sulla mappa.

1. Compilare le altre informazioni che si desidera associare alla posizione della mappa:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | [!UICONTROL Phone Number] | Il numero di telefono della posizione. |
   | [!UICONTROL Street Address] | Indirizzo della località. |
   | [!UICONTROL City] | La città del luogo. |
   | [!UICONTROL Region/State] | L’area geografica o lo stato dell’ubicazione. |
   | [!UICONTROL Zip/Postal Code] | Il codice postale o ZIP della posizione. |
   | [!UICONTROL Country] | Il paese del luogo. |
   | [!UICONTROL Comment] | Eventuali commenti che si desidera includere. |

   {style="table-layout:auto"}

1. Al termine, fai clic su **[!UICONTROL Save]**.

   La nuova posizione viene visualizzata nella mappa e nella griglia della posizione della mappa _[!UICONTROL Edit Map]_pagina.

   ![[!DNL Page Builder] - mappa la griglia di posizione](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Personalizzare lo stile della mappa {#styling}

Utilizza il [!DNL Google Maps] Platform Styling Wizard per applicare uno dei sei temi predefiniti o per creare un tema personalizzato. Puoi generare un file JSON con le proprietà di stile della mappa o un collegamento alla mappa formattata.

### Modificare lo stile della mappa

1. In _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Sotto **[!UICONTROL Google Maps Style]** casella di testo, fare clic su [Crea stile mappa][6].

   Questa azione apre il [[!DNL Google Maps] Creazione guidata stile piattaforma][6] in una scheda separata, in cui è possibile definire uno stile per [!DNL Google Maps] Progetto piattaforma.

1. Clic **[!UICONTROL Create a Style]** e seguire le istruzioni fornite.

   Al termine, fai clic su **[!UICONTROL Finish]**.

1. Esporta lo stile completato come codice JSON o come URL in modo da poterlo aggiungere al [!DNL Commerce] configurazione.

   - **JSON**: sotto la casella con il codice JSON generato, fai clic su **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: sotto la casella con l’URL generato, fai clic su **[!UICONTROL Copy URL]**.

1. Torna alla scheda del browser Amministratori e incolla il codice o l’URL generato nell’elenco **Stile mappe Google** casella.

   Se utilizzi un URL, sostituisci il `YOUR_API_KEY` segnaposto con il [!DNL Google Maps] Chiave API. Questo URL è collegato alla tua mappa Google formattata.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save Config]**.

### Modificare le impostazioni della mappa

1. Passa il puntatore del mouse sul contenitore della mappa per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Modifica le impostazioni di base in base alle esigenze:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | [!UICONTROL Height] | Specifica l&#39;altezza in pixel della mappa visualizzata. |
   | [!UICONTROL Show Controls] | Determina se vengono visualizzati i controlli standard di Google Map. |

   {style="table-layout:auto"}

1. Modifica il _[!UICONTROL Advanced]_impostazioni in base alle esigenze:

   - Per controllare il posizionamento orizzontale del contenuto della mappa aggiunto al contenitore, scegli un **[!UICONTROL Alignment]**:

     | Opzione | Descrizione |
     | ------ | ----------- |
     | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
     | `Left` | Allinea il contenuto lungo il bordo sinistro del contenitore di mappe, tenendo conto della spaziatura specificata. |
     | `Center` | Allinea il contenuto al centro del contenitore di mappe, tenendo conto di eventuali spaziature specificate. |
     | `Right` | Allinea il contenuto lungo il bordo destro del contenitore mappa, tenendo conto di eventuali spaziature specificate. |

     {style="table-layout:auto"}

   - Imposta il **[!UICONTROL Border]** stile applicato a tutti e quattro i lati del contenitore mappa:

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

   - (Facoltativo) Specifica i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente da applicare al contenitore mappa.

     Separare più nomi di classe con uno spazio.

   - Immetti i valori, in pixel, per il **[!UICONTROL Margins and Padding]** per specificare i margini esterni e la spaziatura interna del contenitore mappa.

     Immetti ogni valore corrispondente nel diagramma contenitore mappa.

     | Area contenitore | Descrizione |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. |
     | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >La spaziatura non è disponibile per il tipo di contenuto Mappa.

1. Al termine, fai clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare al [!DNL Page Builder] Workspace.

### Modificare le dimensioni della griglia

La dimensione della griglia determina la dimensione della mappa correlata a un [colonna](column.md) il [!DNL Page Builder] fase. Per impostazione predefinita, la mappa è larga 12 colonne, con un massimo di 16 colonne.

1. In _Amministratore_ barra laterale, vai a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra sotto _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandi ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Aggiornare le opzioni della griglia in base alle esigenze:

   >[!NOTE]
   >
   >Se necessario, cancellare il **[!UICONTROL Use system value]** per modificare queste impostazioni.

   - Per **[!UICONTROL Default Column Grid Size]**, immettere un nuovo valore per la dimensione predefinita della griglia.

   - Per **[!UICONTROL Maximum Column Grid Size]**, immetti un nuovo valore per la dimensione massima predefinita della griglia.

   ![Impostazioni delle dimensioni della griglia delle colonne](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Al termine, fai clic su **[!UICONTROL Save Config]**.

[1]: https://cloud.google.com/maps-platform/
[2]: https://cloud.google.com/maps-platform/places/
[3]: https://cloud.google.com/maps-platform/user-guide/
[4]: https://developers.google.com/maps/documentation/javascript/get-api-key
[5]: https://www.google.com/maps
[6]: https://mapstyle.withgoogle.com/
