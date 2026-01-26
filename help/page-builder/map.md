---
title: Media - Mappa
description: Scopri il tipo di contenuto Mappa, utilizzato per aggiungere una mappa da  [!DNL Google Maps] Platform alla fase  [!DNL Page Builder] .
exl-id: 91fea8f8-d48a-43f1-ba2a-212c7130cee9
feature: Page Builder, Page Content
source-git-commit: cace9d1de00955494d8bc607c017778ff7df4806
workflow-type: tm+mt
source-wordcount: '1572'
ht-degree: 0%

---

# Media - Mappa

Utilizza il tipo di contenuto _Map_ per aggiungere una mappa da [[!DNL Google Maps] Platform](https://cloud.google.com/maps-platform/) a [[!DNL Page Builder] stage](workspace.md#stage). Ad esempio, puoi aggiungere una mappa a un blocco, quindi aggiungerlo alle pagine [Informazioni su di noi](../content-design/pages.md#about-us) e [Contattaci](../getting-started/store-details.md#contact-us-form).

Per ottenere il massimo da [!DNL Google Maps] Platform, puoi personalizzare la mappa, evidenziare i tuoi luoghi di archiviazione e utilizzare Google [Places](https://cloud.google.com/maps-platform/places/) per aggiungere informazioni dettagliate sul tuo archivio a tutti [!DNL Google Maps].

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
| Nascondi | ![Icona Nascondi](./assets/pb-icon-hide.png){width="25"} | Nasconde la mappa corrente. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra la mappa nascosta. |
| Duplica | ![Icona duplicata](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia della mappa. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina la mappa dalla fase. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Configura [!DNL Google Maps] per l&#39;amministratore

Prima di aggiungere una mappa, è necessario aprire un account [account](https://cloud.google.com/maps-platform/user-guide/) per una versione di prova gratuita di [!DNL Google Maps] Platform. La versione di prova gratuita dura 12 mesi e include un credito di 300 dollari. Se utilizzi il tuo credito, Google non fatturerà il tuo account senza la tua autorizzazione.

### Passaggio 1: ottieni la chiave API [!DNL Google Maps]

A seconda che si disponga o meno di una chiave [!DNL Google Maps], utilizzare una delle procedure seguenti per ottenere la chiave API necessaria per la configurazione. Per impostare una chiave [!DNL Google Maps], è necessario essere un amministratore del sito autorizzato ad abilitare la fatturazione per il proprio account. Se non si è pronti a configurare un account Platform [!DNL Google Maps], è possibile saltare questo passaggio e utilizzare per il momento la mappa segnaposto.

1. Passa alla [console della piattaforma Google Cloud](https://cloud.google.com/console/google/maps-apis/overview).

1. Fai clic sull’elenco a discesa del progetto e seleziona o crea il progetto per il quale desideri aggiungere una chiave API.

1. Per configurare le credenziali API, segui le [istruzioni](https://developers.google.com/maps/documentation/javascript/get-api-key) nella documentazione di [!DNL Google Maps].

1. Copia la chiave API negli Appunti.

### Passaggio 2: configurare [!DNL Google Maps] in [!DNL Commerce]

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

   ![Strumenti di contenuto avanzati](../configuration-reference/general/assets/content-management-advanced-content-tools.png){width="600" zoomable="yes"}

   Per ulteriori informazioni sulle opzioni di configurazione degli strumenti avanzati di Content Management, vedere la [Guida di riferimento alla configurazione](../configuration-reference/general/content-management.md).

1. Per **[!UICONTROL Google Maps API Key]**, incolla la chiave copiata nel passaggio 1.

1. Fare clic su **[!UICONTROL Test Key]**.

   Se si è verificato un problema con la chiave, tornare al sito di [!DNL Google Maps] Platform per risolvere il problema. Riprovare.

1. Dopo aver verificato la chiave, fare clic su **[!UICONTROL Save Config]**.

## Aggiungi una mappa all&#39;area di visualizzazione

1. Aprire la pagina, il blocco o il blocco dinamico nell&#39;area di lavoro [!DNL Page Builder].

1. Nel pannello [!DNL Page Builder], espandere **[!UICONTROL Media]** e trascinare un segnaposto **[!UICONTROL Map]** nell&#39;area di visualizzazione.

   ![Trascinamento di una mappa nell&#39;area di visualizzazione](./assets/pb-media-map-drag.png){width="600" zoomable="yes"}

   Se [!DNL Google Maps] Platform è configurata per il tuo archivio, viene visualizzata una mappa per il percorso del tuo archivio.

   ![[!DNL Google Maps]](./assets/pb-tutorial2-google-map.png){width="600" zoomable="yes"}

   Se la piattaforma [!DNL Google Maps] non è ancora configurata per l&#39;archivio, verrà visualizzata una mappa segnaposto.

   Segnaposto ![[!DNL Google Maps]](./assets/pb-tutorial2-media-map-not-configured.png){width="600" zoomable="yes"}

## Aggiungi una posizione mappa personalizzata

1. Passa il puntatore del mouse sul contenitore della mappa per visualizzare la casella degli strumenti e scegli l&#39;icona _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Nell&#39;angolo superiore destro della pagina _[!UICONTROL Edit Map]_fare clic su **[!UICONTROL Add Location]**.

1. Immettere **[!UICONTROL Location Name]** che si desidera associare al pin sulla mappa.

1. Raccogli le coordinate di posizione che desideri utilizzare per la posizione personalizzata.

   In alternativa, nella casella **[!UICONTROL Position]** è possibile trascinare il pin nella mappa visualizzata.

   Se necessario, passare a [[!DNL Google Maps]](https://www.google.com/maps) in una nuova finestra del browser e utilizzare uno dei metodi seguenti per ottenere le coordinate:

   ![Coordinate mappa](./assets/pb-media-maps-settings-add-location-coordinates.png){width="600" zoomable="yes"}

   **Metodo 1:** Copia dall&#39;URL

   - Nell&#39;angolo superiore sinistro immettere l&#39;indirizzo nella casella **[!UICONTROL Search]** e fare clic sull&#39;icona _Cerca_ ( ![Icona Ricerca](../assets/icon-magnify-search.png){width="20"} ).

   - Copia le coordinate nell’URL e incollale in un blocco note.

   **Metodo 2:** Copia da &quot;What&#39;s here?&quot;

   - Fare clic con il pulsante destro del mouse sul pin rosso che indica la posizione sulla mappa e scegliere **[!UICONTROL What's here?]** nel menu.

   - Nell&#39;etichetta visualizzata, copiare il testo, incluse le coordinate, e incollarlo in un blocco note.

1. Immettere i numeri, senza la virgola, in ciascuna delle caselle **[!UICONTROL Coordinates]**.

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

1. Al termine, fare clic su **[!UICONTROL Save]**.

   La nuova posizione viene visualizzata nella mappa e nella griglia della posizione della mappa nella pagina _[!UICONTROL Edit Map]_.

   ![[!DNL Page Builder] - mappa la griglia di posizione](./assets/pb-media-maps-settings-add-location-grid.png){width="600" zoomable="yes"}

## Personalizzare lo stile della mappa {#styling}

Utilizzare la [!DNL Google Maps] Platform Styling Wizard per applicare uno dei sei temi predefiniti o per creare un tema personalizzato. Puoi generare un file JSON con le proprietà di stile della mappa o un collegamento alla mappa formattata.

### Modificare lo stile della mappa

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Nella casella di testo **[!UICONTROL Google Maps Style]** fare clic su [Crea stile mappa](https://mapstyle.withgoogle.com/).

   Questa azione apre la [[!DNL Google Maps] Creazione guidata Stile piattaforma](https://mapstyle.withgoogle.com/) in una scheda separata, in cui è possibile definire uno stile per il progetto [!DNL Google Maps] Platform.

1. Fare clic su **[!UICONTROL Create a Style]** e seguire le istruzioni fornite.

   Al termine, fare clic su **[!UICONTROL Finish]**.

1. Esporta lo stile completato come codice JSON o come URL in modo da poterlo aggiungere alla configurazione [!DNL Commerce].

   - **JSON**: sotto la casella con il codice JSON generato, fare clic su **[!UICONTROL Copy JSON]**.

   - **[!UICONTROL URL]**: sotto la casella con l&#39;URL generato, fare clic su **[!UICONTROL Copy URL]**.

1. Torna alla scheda del browser Amministratori e incolla il codice o l&#39;URL generato nella casella **Stile mappe Google**.

   Se utilizzi un URL, sostituisci il segnaposto `YOUR_API_KEY` con la tua chiave API [!DNL Google Maps]. Questo URL è collegato alla tua mappa Google formattata.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save Config]**.

### Modificare le impostazioni della mappa

1. Passa il puntatore del mouse sul contenitore della mappa per visualizzare la casella degli strumenti e scegli l&#39;icona _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Modifica le impostazioni di base in base alle esigenze:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | [!UICONTROL Height] | Specifica l&#39;altezza in pixel della mappa visualizzata. |
   | [!UICONTROL Show Controls] | Determina se vengono visualizzati i controlli standard di Google Map. |

   {style="table-layout:auto"}

1. Modificare le impostazioni di _[!UICONTROL Advanced]_in base alle esigenze:

   - Per controllare il posizionamento orizzontale del contenuto della mappa aggiunto al contenitore, scegliere un **[!UICONTROL Alignment]**:

     | Opzione | Descrizione |
     | ------ | ----------- |
     | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
     | `Left` | Allinea il contenuto lungo il bordo sinistro del contenitore di mappe, tenendo conto della spaziatura specificata. |
     | `Center` | Allinea il contenuto al centro del contenitore di mappe, tenendo conto di eventuali spaziature specificate. |
     | `Right` | Allinea il contenuto lungo il bordo destro del contenitore mappa, tenendo conto di eventuali spaziature specificate. |

     {style="table-layout:auto"}

   - Imposta lo stile **[!UICONTROL Border]** applicato a tutti e quattro i lati del contenitore mappa:

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

   - (Facoltativo) Specificare i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente da applicare al contenitore delle mappe.

     Separare più nomi di classe con uno spazio.

   - Immettere i valori, in pixel, per **[!UICONTROL Margins and Padding]** per specificare i margini esterni e la spaziatura interna del contenitore mappa.

     Immetti ogni valore corrispondente nel diagramma contenitore mappa.

     | Area contenitore | Descrizione |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. |
     | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. |

     {style="table-layout:auto"}

     >[!NOTE]
     >
     >La spaziatura non è disponibile per il tipo di contenuto Mappa.

1. Al termine, fare clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare all&#39;area di lavoro [!DNL Page Builder].

### Modificare le dimensioni della griglia

La dimensione della griglia determina la dimensione della mappa correlata a una [colonna](column.md) nella fase [!DNL Page Builder]. Per impostazione predefinita, la mappa è larga 12 colonne, con un massimo di 16 colonne.

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Stores]** > _[!UICONTROL Settings]_>**[!UICONTROL Configuration]**.

1. Nel pannello a sinistra in _[!UICONTROL General]_, scegli **[!UICONTROL Content Management]**.

1. Espandere ![Selettore di espansione](../assets/icon-display-expand.png) **[!UICONTROL Advanced Content Tools]**.

1. Aggiornare le opzioni della griglia in base alle esigenze:

   >[!NOTE]
   >
   >Se necessario, deselezionare la casella di controllo **[!UICONTROL Use system value]** per modificare queste impostazioni.

   - Per **[!UICONTROL Default Column Grid Size]**, immettere un nuovo valore per la dimensione predefinita della griglia.

   - Per **[!UICONTROL Maximum Column Grid Size]**, immettere un nuovo valore per la dimensione massima predefinita della griglia.

   ![Impostazioni dimensioni griglia colonne](./assets/pb-configure-advanced-content-tools-grid-size.png){width="600" zoomable="yes"}

1. Al termine, fare clic su **[!UICONTROL Save Config]**.


<!-- Last updated from includes: 2023-09-11 14:30:19 -->
