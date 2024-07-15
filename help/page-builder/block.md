---
title: Aggiungi contenuto - Blocca
description: Scopri il tipo di contenuto Blocca, utilizzato per aggiungere un blocco riutilizzabile alla fase  [!DNL Page Builder] .
exl-id: fcedb125-e0c8-4b59-bd26-7f3912e0db2a
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '795'
ht-degree: 0%

---

# Aggiungi contenuto - Blocca

Utilizza il tipo di contenuto _Blocca_ per aggiungere un [blocco](../content-design/blocks.md) attivo esistente alla [[!DNL Page Builder] fase](workspace.md#stage). Nell’esempio seguente, la prima colonna contiene il blocco con un menu laterale per la pagina. La seconda colonna contiene un’immagine.

![Blocca con un menu laterale](./assets/pb-add-content-block-example.png){width="600" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Casella degli strumenti Blocca

| Strumento | Icona | Descrizione |
| --------- | -------- | ------------- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png) | Sposta il contenitore di blocchi e il relativo contenuto in un&#39;altra posizione sullo stage. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png) | Apre la pagina Modifica blocco, in cui è possibile scegliere il blocco e modificare le proprietà del contenitore. |
| Nascondi | ![Icona Nascondi](./assets/pb-icon-hide.png) | Nasconde il contenitore di blocchi corrente e il relativo contenuto. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png) | Mostra il contenitore di blocchi nascosto e il relativo contenuto. |
| Duplica | ![Icona duplicata](./assets/pb-icon-duplicate.png) | Crea una copia del contenitore di blocchi e del relativo contenuto. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png) | Elimina dall’area di visualizzazione il contenitore di blocchi e il relativo contenuto. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Aggiungi un blocco esistente

1. Passare all&#39;area di lavoro [!DNL Page Builder] nella pagina di destinazione, nel blocco, nel blocco dinamico, nel prodotto o nella categoria.

1. Nel pannello [!DNL Page Builder], espandere **[!UICONTROL Add Content]** e trascinare un segnaposto **[!UICONTROL Block]** nell&#39;area di visualizzazione.

   ![Trascinamento di un blocco nell&#39;area di visualizzazione](./assets/pb-add-content-block-drag.png){width="600" zoomable="yes"}

1. Passa il puntatore del mouse sul contenitore di blocchi vuoto per visualizzare la casella degli strumenti e scegli l&#39;icona _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} ).

1. Fare clic su **[!UICONTROL Select Block]**.

   ![Selezione di un blocco](./assets/pb-add-content-block-select.png){width="200"}

1. Nella riga del blocco che si desidera aggiungere fare clic su **[!UICONTROL Select]** nell&#39;ultima colonna.

   ![Blocco selezionato](./assets/pb-add-content-block-selected.png){width="600" zoomable="yes"}

   Il nome del blocco selezionato viene visualizzato nella pagina.

   ![Nome blocco](./assets/pb-add-content-block-name.png){width="200"}

1. Completa le altre impostazioni necessarie, utilizzando le descrizioni dei campi alla fine di questa pagina come riferimento.

1. Al termine, fare clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare all&#39;area di lavoro [!DNL Page Builder].

### Impostazioni avanzate

1. Per controllare il posizionamento del blocco all&#39;interno del contenitore padre, scegliere un **[!UICONTROL Alignment]**:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
   | `Left` | Allinea l&#39;elenco lungo il bordo sinistro del contenitore principale, tenendo conto di eventuali spaziature specificate. |
   | `Center` | Allinea l&#39;elenco al centro del contenitore padre, tenendo conto di eventuali spaziature specificate. |
   | `Right` | Allinea il blocco lungo il bordo destro del contenitore principale, tenendo conto della spaziatura specificata. |

   {style="table-layout:auto"}

1. Imposta uno stile **[!UICONTROL Border]** applicato a tutti e quattro i lati del contenitore di blocchi:

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

1. Se si imposta uno stile di bordo diverso da `None`, completare le opzioni di visualizzazione del bordo:

   | Opzione | Descrizione |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Specificate il colore scegliendo un campione, facendo clic sul selettore del colore oppure immettendo un nome di colore valido o un valore esadecimale equivalente. |
   | [!UICONTROL Border Width] | Immettere il numero di pixel per lo spessore della linea del bordo. |
   | [!UICONTROL Border Radius] | Immettere il numero di pixel per definire la dimensione del raggio utilizzato per arrotondare ogni angolo del bordo. |

   {style="table-layout:auto"}

1. (Facoltativo) Specificare i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente da applicare al contenitore.

   Separare più nomi di classe con uno spazio.

1. Immettere i valori, in pixel, per **[!UICONTROL Margins and Padding]** per determinare i margini esterni e la spaziatura interna del contenitore di blocchi.

   Immettere i valori corrispondenti nel diagramma.

   | Area contenitore | Descrizione |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. Opzioni: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. Opzioni: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Modifica impostazioni blocco

1. Passa il puntatore del mouse sul contenitore di blocchi e scegli l&#39;icona _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} ) nella casella degli strumenti.

   ![Blocca Casella Degli Strumenti](./assets/pb-add-content-block-toolbox.png){width="600" zoomable="yes"}

1. Per scegliere un blocco diverso, fare clic su **[!UICONTROL Select Block]**.

   - Nell&#39;elenco dei blocchi attivi fare clic su **[!UICONTROL Select]** il blocco che si desidera aggiungere.
   - Fare clic su **[!UICONTROL Add Selected]**.

1. Se necessario, aggiorna le altre impostazioni utilizzando le descrizioni dei campi alla fine di questa pagina come riferimento.

1. Al termine, fare clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare all&#39;area di lavoro [!DNL Page Builder].

## Duplicare un blocco

1. Passa il puntatore del mouse sul contenitore di blocchi per visualizzare la casella degli strumenti e scegli l&#39;icona _Duplica_ (![Icona Duplica](./assets/pb-icon-duplicate.png)).

   Il duplicato viene visualizzato immediatamente sotto l&#39;originale.

1. Per spostare il nuovo blocco in una nuova posizione, posizionare il puntatore del mouse sul contenitore, quindi fare clic su _Sposta_ (![Icona Sposta](./assets/pb-icon-move.png)) nella casella degli strumenti.

1. Seleziona e trascina il blocco fino a quando la linea guida rossa non viene visualizzata nella nuova posizione.

   Durante lo spostamento del blocco, i bordi superiore e inferiore di ciascun contenitore vengono visualizzati come linee tratteggiate.

## Rimuovere un blocco dall&#39;area di visualizzazione

1. Passa il puntatore del mouse sul contenitore di blocchi per visualizzare la casella degli strumenti e scegli l&#39;icona _Rimuovi_ (![Rimuovi icona](./assets/pb-icon-remove.png)).

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL OK]**.
