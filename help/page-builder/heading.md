---
title: Elementi - Intestazione
description: Scopri il tipo di contenuto Titolo, utilizzato per aggiungere al [!DNL Page Builder] fase.
exl-id: dc51e7f6-a235-49dc-a978-1419a63fa33e
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '941'
ht-degree: 0%

---

# Elementi - Intestazione

I livelli di intestazione stabiliscono una gerarchia che organizza il contenuto e aiuta i motori di ricerca a indicizzare ogni pagina. Utilizza il _Intestazione_ tipo di contenuto in [[!DNL Page Builder] fase](workspace.md#stage) per aggiungere allo stage un contenitore di testo con un livello di intestazione da H1 a H6. Le intestazioni vengono formattate in base al foglio di stile associato al tema corrente.

Il [Intestazione contenuto](workspace.md) campo in _[!UICONTROL Content]_può essere utilizzato per aggiungere un’intestazione H1 nella parte superiore della pagina. Tuttavia, il campo è un legacy di precedente [!DNL Commerce] e viene fornito per supportare contenuti meno recenti. Questo campo non sfrutta [!DNL Page Builder]Funzioni avanzate di. È consigliabile lasciare vuoto il campo Intestazione contenuto e utilizzare il [!DNL Page Builder] Tipo di contenuto intestazione per aggiungere alla pagina titoli di qualsiasi livello.

L’esempio seguente mostra come vengono visualizzati l’intestazione di contenuto e il tipo di contenuto Intestazione quando vengono formattati dal tema Luma.

![Livelli di intestazione e intestazione del contenuto nella vetrina](./assets/pb-storefront-heading-levels.png){width="700" zoomable="yes"}

Puoi trascinare un’intestazione dal menu _Elementi_ sezione del [!DNL Page Builder] su una riga, colonna o scheda impostata sullo stage. Il livello dell’intestazione e l’allineamento possono essere controllati dalla barra degli strumenti dell’editor sullo stage oppure utilizzando _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

{{$include /help/_includes/page-builder-save-timeout.md}}

## Editor titoli

![Editor titoli con barra degli strumenti](./assets/pb-elements-heading-toolbar.png){width="500" zoomable="yes"}

## Casella degli strumenti Contenitore intestazione

Come per tutti i contenitori di contenuto, la casella degli strumenti viene visualizzata quando si passa il puntatore del mouse sul contenitore.

![Casella degli strumenti Contenitore intestazione](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

| Strumento | Icona | Descrizione |
| --------- | ----------------- | ---------------------- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta il contenitore del titolo in un&#39;altra posizione valida nella pagina. |
| (etichetta) | Intestazione | Identifica il contenitore corrente come intestazione. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre la pagina Modifica intestazione, in cui è possibile modificare le proprietà del contenitore. |
| Nascondi | ![Nascondi icona](./assets/pb-icon-hide.png){width="25"} | Nasconde il contenitore del titolo. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra il contenitore del titolo nascosto. |
| Duplica | ![Icona Duplica](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia del contenitore del titolo. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina dall’area di visualizzazione il contenitore dell’intestazione e il relativo contenuto. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Aggiungi un’intestazione

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Elements]** e trascina un **[!UICONTROL Heading]** segnaposto per una riga, colonna o gruppo di schede sullo stage.

   ![Trascinamento di un&#39;intestazione nell&#39;area di visualizzazione](./assets/pb-elements-heading-drag.png){width="600" zoomable="yes"}

1. Nell’editor, inserisci il testo dell’intestazione sopra `Edit Heading Text` segnaposto.

   Per impostazione predefinita, al testo dell’intestazione viene assegnato un tipo di intestazione di livello due (H2).

   ![Segnaposto nell’editor intestazione](./assets/pb-elements-header-editor-placeholder.png){width="500" zoomable="yes"}

1. Nella barra degli strumenti, scegli il tipo di intestazione appropriato tra H1 e H6.

1. Se necessario, modificate l&#39;allineamento.

## Modifica impostazioni intestazione

1. Passa il puntatore del mouse sul contenitore dell’intestazione per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

   ![Casella degli strumenti Intestazione](./assets/pb-elements-heading-toolbox.png){width="500" zoomable="yes"}

1. Aggiornare il contenuto dell’intestazione (**[!UICONTROL Heading Type]** e **[!UICONTROL Heading Text]**) se necessario.

   Puoi anche aggiornare questo contenuto nell’editor delle intestazioni.

1. Aggiornare il _[!UICONTROL Advanced]_in base alle esigenze.

   - Per controllare il posizionamento dell’intestazione all’interno del contenitore principale, scegli un **[!UICONTROL Alignment]**:

     | Opzione | Descrizione |
     | ------ | ----------- |
     | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
     | `Left` | Allinea l&#39;elenco lungo il bordo sinistro del contenitore principale, tenendo conto di eventuali spaziature specificate. |
     | `Center` | Allinea l&#39;elenco al centro del contenitore padre, tenendo conto di eventuali spaziature specificate. |
     | `Right` | Allinea il blocco lungo il bordo destro del contenitore principale, tenendo conto della spaziatura specificata. |

     {style="table-layout:auto"}

   - Imposta il **[!UICONTROL Border]** stile applicato a tutti e quattro i lati del contenitore del titolo:

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

     | Opzione | Descrizione |
     | ------ |------------ |
     | [!UICONTROL Border Color] | Specificate il colore scegliendo un campione, facendo clic sul selettore del colore oppure immettendo un nome di colore valido o un valore esadecimale equivalente. |
     | [!UICONTROL Border Width] | Immettere il numero di pixel per lo spessore della linea del bordo. |
     | [!UICONTROL Border Radius] | Immettere il numero di pixel per definire la dimensione del raggio utilizzato per arrotondare ogni angolo del bordo. |

     {style="table-layout:auto"}

   - (Facoltativo) Specifica i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente da applicare al contenitore.

     Separare più nomi di classe con uno spazio.

   - Immetti i valori, in pixel, per il **[!UICONTROL Margins and Padding]** per determinare i margini esterni e la spaziatura interna del contenitore del titolo.

     Immettere i valori corrispondenti nel diagramma.

     | Area contenitore | Descrizione |
     | -------------- | ----------- |
     | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. Opzioni: `Top` / `Right` / `Bottom` / `Left` |
     | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. Opzioni: `Top` / `Right` / `Bottom` / `Left` |

     {style="table-layout:auto"}

1. Al termine, fai clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare al [!DNL Page Builder] Workspace.

## Duplicare un’intestazione

Per un titolo formattato con impostazioni specifiche, è più efficiente duplicare l’intestazione, anziché ricominciare con un nuovo segnaposto.

1. Passa il puntatore del mouse sul contenitore dell’intestazione per visualizzare la casella degli strumenti e scegli _Duplica_ ( ![Icona Duplica](./assets/pb-icon-duplicate.png){width="20"} ).

   Il duplicato viene visualizzato immediatamente sotto l&#39;originale.

   ![Duplicazione di un contenitore di intestazione](./assets/pb-elements-heading-duplicate.png){width="500" zoomable="yes"}

1. Passa il puntatore del mouse sul nuovo contenitore di titoli per visualizzare la casella degli strumenti e scegli _Sposta_ ( ![Icona Sposta](./assets/pb-icon-move.png){width="20"} ).

   ![Spostamento di un titolo](./assets/pb-elements-heading-move.png){width="500" zoomable="yes"}

1. Seleziona e trascina l’intestazione fino a quando la linea guida rossa non contrassegna la nuova posizione.

   Durante lo spostamento dell&#39;intestazione, i bordi superiore e inferiore di ogni contenitore vengono visualizzati come linee tratteggiate.

   ![Spostamento dell&#39;intestazione duplicata in posizione](./assets/pb-elements-heading-move-guideline.png){width="500" zoomable="yes"}

1. Se si desidera modificare il livello di intestazione, fare clic sul testo dell&#39;intestazione e scegliere il nuovo livello nella barra degli strumenti dell&#39;editor.

   ![Scelta di un nuovo livello di intestazione](./assets/pb-elements-heading-change-heading-level.png){width="500" zoomable="yes"}
