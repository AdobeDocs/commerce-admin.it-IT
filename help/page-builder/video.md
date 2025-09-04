---
title: Media - Video
description: Scopri il tipo di contenuto Video, utilizzato per aggiungere alla fase  [!DNL Page Builder]  un video in hosting su YouTube o Vimeo.
exl-id: 9cd075e7-c10d-4c34-8932-c1ccb32bf198
feature: Page Builder, Page Content
source-git-commit: 4a3aa2aa32b692341edabd41fdb608e3cff5d8e0
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 0%

---

# Media - Video

Utilizza il tipo di contenuto _Video_ per aggiungere un video in hosting su [YouTube][1] o [Vimeo][2] alla [[!DNL Page Builder] fase](workspace.md#stage). È facile incorporare i video in una pagina o in un blocco oppure nelle descrizioni di prodotti e categorie.

![Video nella home page della vetrina](./assets/pb-storefront-video.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Casella degli strumenti Video

![Casella degli strumenti video](./assets/pb-media-video-toolbox.png){width="600" zoomable="yes"}

| Strumento | Icona | Descrizione |
|--- |--- |--- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta il video in un&#39;altra posizione sullo stage. |
| (etichetta) | [!UICONTROL Video] | Identifica il contenitore di contenuto corrente sotto forma di video. Passa il cursore del mouse sul contenitore di immagini per visualizzare la casella degli strumenti. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre la pagina _[!UICONTROL Edit Video]_, in cui è possibile modificare le proprietà del video e del contenitore. |
| Nascondi | ![Icona Nascondi](./assets/pb-icon-hide.png){width="25"} | Nasconde il video corrente. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra il video nascosto. |
| Duplica | ![Icona duplicata](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia del video. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina il video dall&#39;area di visualizzazione. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Aggiungi un video

1. Prima di iniziare, passa al video [YouTube][1] o [Vimeo][2] che desideri incorporare e copia il collegamento.

   In alternativa, è possibile copiare un collegamento diretto in un file video valido. Per collegamenti validi, consulta [Impostazioni video di base](#basic-video-settings).

1. Nell&#39;amministratore [!DNL Commerce], tornare all&#39;area di lavoro [!DNL Page Builder] in cui si desidera aggiungere il video.

1. Nel pannello [!DNL Page Builder], espandere **[!UICONTROL Media]** e trascinare un segnaposto **[!UICONTROL Video]** nell&#39;area di visualizzazione.

   ![Trascinamento di un segnaposto video nell&#39;area di visualizzazione](./assets/pb-media-video-drag.png){width="600" zoomable="yes"}

1. Passa il puntatore del mouse sul contenitore video per visualizzare la casella degli strumenti e scegli l&#39;icona _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Per **[!UICONTROL Video URL]**, incolla l&#39;URL del video copiato.

   URL del video [!DNL Page Builder] utilizzato in questo esempio: `https://www.youtube.com/watch?v=Y0KNS7C5dZA`.

1. Per limitare il **[!UICONTROL Maximum Width]** del video, immetti la larghezza massima in pixel.

   Se vuoto, il video ha la larghezza consentita dal contenitore, consentendo margini e spaziatura.

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare all&#39;area di lavoro [!DNL Page Builder].

## Modificare le impostazioni video

1. Passa il puntatore del mouse sul contenitore video per visualizzare la casella degli strumenti e scegli l&#39;icona _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

1. Modificate le impostazioni in base alle sezioni riportate di seguito.

   - [Base](#basic-video-settings)
   - [Avanzate](#advanced)

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare all&#39;area di lavoro [!DNL Page Builder].

### Impostazioni video di base

1. Per modificare il video corrente, aggiornare **[!UICONTROL Video URL]**.

   Immetti un URL video valido. Gli URL video validi possono essere collegamenti a:

   - Video su YouTube: `https://youtu.be/CoDhMRUUjeI`
   - Video su Vimeo: `https://vimeo.com/190156113`
   - File video validi (`.mp4` è consigliato): `https://myvideos.com/spiral.mp4`

1. Per modificare la larghezza consentita per il video nella vetrina, immettere il nuovo **[!UICONTROL Maximum Width]** in pixel.

   Se vuoto, il video estende l’intera larghezza del contenitore, meno margini e spaziatura interna.

1. Per avviare automaticamente il video dopo il caricamento della pagina, impostare **[!UICONTROL Autoplay]** su `Yes`.

   Se Riproduzione automatica è impostato su `Yes`, il video viene disattivato durante la riproduzione in base ai criteri. Tuttavia, anche con questa impostazione, i dispositivi mobili non possono riprodurre automaticamente i video. Per ulteriori informazioni su questi criteri, consulta le seguenti risorse per sviluppatori:

   - [Riproduzione automatica da Vimeo](https://vimeo.zendesk.com/hc/en-us/articles/115004485728-Autoplaying-and-looping-embedded-videos)
   - [Criteri di riproduzione automatica da Google (Chrome/YouTube)](https://developer.chrome.com/blog/autoplay/)
   - [Criteri di riproduzione automatica per video locali](https://developer.mozilla.org/en-US/docs/Web/Media/Autoplay_guide)

   Se Riproduzione automatica è impostato su `No`, il video viene riprodotto solo su richiesta dell&#39;utente.

### [!UICONTROL Advanced]

1. Per controllare il posizionamento orizzontale del video all&#39;interno del contenitore, scegliere un **[!UICONTROL Alignment]**:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
   | `Left` | Allinea il contenuto lungo il bordo sinistro del contenitore video, tenendo conto di eventuali spaziature specificate. |
   | `Center` | Allinea il contenuto al centro del contenitore video, tenendo conto di eventuali spaziature specificate. |
   | `Right` | Allinea il contenuto lungo il bordo destro del contenitore video, tenendo conto di eventuali spaziature specificate. |

   {style="table-layout:auto"}

- Imposta lo stile **[!UICONTROL Border]** applicato a tutti e quattro i lati del contenitore video:

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

- (Facoltativo) Specificare i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente da applicare al contenitore video.

  Separare più nomi di classe con uno spazio.

- Immettere i valori, in pixel, per **[!UICONTROL Margins and Padding]** per specificare i margini esterni e la spaziatura interna del contenitore video.

  Immetti ogni valore corrispondente nel diagramma contenitore video.

  | Area contenitore | Descrizione |
  | -------------- | ----------- |
  | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. |
  | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. |

  {style="table-layout:auto"}

## Spostare un video

1. Passa il puntatore del mouse sul contenitore video per visualizzare la casella degli strumenti e scegli l&#39;icona _Sposta_ ( ![Icona Sposta](./assets/pb-icon-move.png){width="20"} ).

   ![Spostamento di un video](./assets/pb-media-video-toolbox-move-col1.png){width="500" zoomable="yes"}

1. Seleziona e trascina il video nella nuova posizione, appena sotto la linea guida rossa.

   ![Utilizzo della linea guida rossa per inserire il video](./assets/pb-media-video-toolbox-move-col2.png){width="500" zoomable="yes"}

## Rimuovere un video dall&#39;area di visualizzazione

1. Passa il puntatore del mouse sul contenitore video per visualizzare la casella degli strumenti e scegli l&#39;icona _Rimuovi_ (![Rimuovi icona](./assets/pb-icon-remove.png)).

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL OK]**.

[1]: https://www.youtube.com/
[2]: https://vimeo.com/

<!-- Last updated from includes: 2023-09-11 14:30:19 -->
