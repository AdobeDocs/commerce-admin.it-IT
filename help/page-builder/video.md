---
title: Media - Video
description: Scopri il tipo di contenuto Video, utilizzato per aggiungere al video in hosting su YouTube o Vimeo [!DNL Page Builder] fase.
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 79dc16dcba239af12793813ae19636bbd7ec49c5
workflow-type: tm+mt
source-wordcount: '935'
ht-degree: 0%

---

# Media - Video

Utilizza il _Video_ tipo di contenuto per aggiungere un video in hosting su [YouTube][1] o [Vimeo][2] al [[!DNL Page Builder] fase](workspace.md#stage). È facile incorporare i video in una pagina o in un blocco oppure nelle descrizioni di prodotti e categorie.

![Video nella home page della vetrina](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Casella degli strumenti Video

![Casella degli strumenti Video](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| Strumento | Icona | Descrizione |
|--- |--- |--- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta il video in un&#39;altra posizione sullo stage. |
| (etichetta) | [!UICONTROL Video] | Identifica il contenitore di contenuto corrente sotto forma di video. Passa il cursore del mouse sul contenitore di immagini per visualizzare la casella degli strumenti. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre il _[!UICONTROL Edit Video]_, in cui è possibile modificare le proprietà del video e del contenitore. |
| Nascondi | ![Nascondi icona](./assets/pb-icon-hide.png){width="25"} | Nasconde il video corrente. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra il video nascosto. |
| Duplica | ![Icona Duplica](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia del video. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina il video dall&#39;area di visualizzazione. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Aggiungi un video

1. Prima di iniziare, passare alla [YouTube][1] o [Vimeo][2] video da incorporare e copia il collegamento.

   In alternativa, è possibile copiare un collegamento diretto in un file video valido. Consulta [Impostazioni video di base](#basic-video-settings) per collegamenti validi.

1. In [!DNL Commerce] Amministratore, torna a [!DNL Page Builder] in cui desideri aggiungere il video.

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Media]** e trascina un **[!UICONTROL Video]** segnaposto nell&#39;area di visualizzazione.

   ![Trascinamento di un segnaposto video nell’area di visualizzazione](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. Passa il puntatore del mouse sul contenitore video per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Per **[!UICONTROL Video URL]**, incolla l’URL del video copiato.

   L’URL del [!DNL Page Builder] il video utilizzato in questo esempio è: `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. Per limitare **[!UICONTROL Maximum Width]** del video, immetti la larghezza massima in pixel.

   Se vuoto, il video ha la larghezza consentita dal contenitore, consentendo margini e spaziatura.

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare al [!DNL Page Builder] Workspace.

## Modificare le impostazioni video

1. Passa il puntatore del mouse sul contenitore video per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Modificate le impostazioni in base alle sezioni riportate di seguito.

   - [Base](#basic-video-settings)
   - [Avanzate](#advanced)

1. Nell’angolo superiore destro, fai clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare al [!DNL Page Builder] Workspace.

### Impostazioni video di base

1. Per modificare il video corrente, aggiorna il **[!UICONTROL Video URL]**.

   Immetti un URL video valido. Gli URL video validi possono essere collegamenti a:

   - Video su YouTube: `https://youtu.be/CoDhMRUUjeI`
   - Video su Vimeo: `https://vimeo.com/190156113`
   - File video validi (`.mp4` consigliato): `https://myvideos.com/spiral.mp4`

1. Per modificare la larghezza consentita per il video nella vetrina, immetti il nuovo **[!UICONTROL Maximum Width]** in pixel.

   Se vuoto, il video estende l’intera larghezza del contenitore, meno margini e spaziatura interna.

1. Per avviare automaticamente il video dopo il caricamento della pagina, imposta **[!UICONTROL Autoplay]** a `Yes`.

   Se Riproduzione automatica è impostato su `Yes`, il video viene disattivato durante la riproduzione in base ai criteri. Tuttavia, anche con questa impostazione, i dispositivi mobili non possono riprodurre automaticamente i video. Per ulteriori informazioni su questi criteri, consulta le seguenti risorse per sviluppatori:

   - [Criterio Riproduzione automatica da Vimeo](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Criterio Autoplay da Google (Chrome/YouTube)](https://developer.chrome.com/blog/autoplay/)
   - [Criterio Autoplay per video locali](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   Se Riproduzione automatica è impostato su `No`, il video viene riprodotto solo su richiesta dell’utente.

### [!UICONTROL Advanced]

1. Per controllare il posizionamento orizzontale del video all’interno del contenitore, scegli un’ **[!UICONTROL Alignment]**:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
   | `Left` | Allinea il contenuto lungo il bordo sinistro del contenitore video, tenendo conto di eventuali spaziature specificate. |
   | `Center` | Allinea il contenuto al centro del contenitore video, tenendo conto di eventuali spaziature specificate. |
   | `Right` | Allinea il contenuto lungo il bordo destro del contenitore video, tenendo conto di eventuali spaziature specificate. |

   {style="table-layout:auto"}

- Imposta il **[!UICONTROL Border]** stile applicato a tutti e quattro i lati del contenitore video:

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

- (Facoltativo) Specifica i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente per applicarlo al contenitore video.

  Separare più nomi di classe con uno spazio.

- Immetti i valori, in pixel, per il **[!UICONTROL Margins and Padding]** per specificare i margini esterni e la spaziatura interna del contenitore video.

  Immetti ogni valore corrispondente nel diagramma contenitore video.

  | Area contenitore | Descrizione |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. |
  | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. |

  {style="table-layout:auto"}

## Spostare un video

1. Passa il puntatore del mouse sul contenitore video per visualizzare la casella degli strumenti e scegli _Sposta_ ( ![Icona Sposta](./assets/pb-icon-move.png){width="20"} ).

   ![Spostamento di un video](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. Seleziona e trascina il video nella nuova posizione, appena sotto la linea guida rossa.

   ![Utilizzo della linea guida rossa per inserire il video](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## Rimuovere un video dall&#39;area di visualizzazione

1. Passa il puntatore del mouse sul contenitore video per visualizzare la casella degli strumenti e scegli _Rimuovi_ (![Icona Rimuovi](./assets/pb-icon-remove.png)).

1. Quando viene richiesto di confermare, fai clic su **[!UICONTROL OK]**.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/
