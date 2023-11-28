---
title: Aggiungi contenuto - Blocco dinamico
description: Scopri il tipo di contenuto Blocco dinamico, utilizzato per aggiungere un blocco dinamico riutilizzabile al [!DNL Page Builder] fase.
exl-id: 04c90f47-9e32-4d34-ac0d-a2f2cec95ffc
feature: Page Builder, Page Content
source-git-commit: 167e9d906cebb645f76a5112fa629a73ba823ebc
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 0%

---

# Aggiungi contenuto - Blocco dinamico

Utilizza il tipo di contenuto Blocco dinamico per aggiungere un elemento esistente [blocco dinamico](../content-design/dynamic-blocks.md) al [[!DNL Page Builder] fase](workspace.md#stage).

![Blocco dinamico sulla vetrina](./assets/pb-tutorial2-dynamic-block-storefront.png){width="700" zoomable="yes"}

{{$include /help/_includes/page-builder-save-timeout.md}}

## Casella degli strumenti Blocco dinamico

| Strumento | Icona | Descrizione |
| --------- | ------------- | ----------------- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta il contenitore di blocchi e il relativo contenuto in un&#39;altra posizione sullo stage. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre il _Modifica blocco_ , in cui è possibile scegliere il blocco e modificare le proprietà del contenitore. |
| Nascondi | ![Nascondi icona](./assets/pb-icon-hide.png){width="25"} | Nasconde il contenitore di blocchi corrente e il relativo contenuto. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra il contenitore di blocchi nascosto e il relativo contenuto. |
| Duplica | ![Icona Duplica](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia del contenitore di blocchi e del relativo contenuto. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina dall’area di visualizzazione il contenitore di blocchi e il relativo contenuto. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Aggiungi un blocco dinamico esistente all&#39;area di visualizzazione

1. Accedi a [!DNL Page Builder] nella pagina, nel blocco, nel prodotto o nella categoria di destinazione.

1. In [!DNL Page Builder] pannello, espandere **[!UICONTROL Add Content]** e trascina un **[!UICONTROL Dynamic Block]** segnaposto nell&#39;area di visualizzazione.

   ![Trascinamento di un segnaposto di blocco dinamico nell&#39;area di visualizzazione](./assets/pb-dynamic-block-drag.png){width="600" zoomable="yes"}

1. Passa il cursore del mouse sul contenitore di blocchi dinamici vuoto per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

   ![Casella degli strumenti Blocco dinamico](./assets/pb-dynamic-block-settings.png){width="600" zoomable="yes"}

1. Il giorno _Modifica blocco dinamico_ pagina, fai clic su **[!UICONTROL Select Dynamic Block]** e utilizza l’elenco per selezionare il blocco.

   ![Selezione di un blocco dinamico](./assets/pb-dynamic-block-select.png){width="600" zoomable="yes"}

   Nell’elenco, individua il blocco dinamico da inserire e fai clic su **[!UICONTROL Select]**. Quindi, fai clic su **[!UICONTROL Add Selected]**.

   ![Selezione di un blocco dinamico nell’elenco](./assets/pb-add-content-dynamic-block-select-list.png){width="600" zoomable="yes"}

   Di seguito viene visualizzato un riepilogo delle informazioni sul blocco dinamico.

   ![Riepilogo blocco dinamico](./assets/pb-add-content-dynamic-block-summary.png){width="600" zoomable="yes"}

1. Imposta **[!UICONTROL Template]** a uno dei seguenti elementi:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Dynamic Block Block Template` | Aggiunge un blocco autonomo. |
   | `Dynamic Block Inline Template` | Inserisce il contenuto del blocco nel testo. |

   {style="table-layout:auto"}

   ![Modello blocco dinamico](./assets/pb-add-content-dynamic-block-template.png){width="200"}

1. Completare le impostazioni avanzate in base alle esigenze.

1. Al termine, fai clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare al [!DNL Page Builder] Workspace.

### Impostazioni avanzate

1. Per controllare il posizionamento del blocco dinamico all’interno del contenitore principale, scegli un **[!UICONTROL Alignment]**:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
   | `Left` | Allinea l&#39;elenco lungo il bordo sinistro del contenitore principale, tenendo conto di eventuali spaziature specificate. |
   | `Center` | Allinea l&#39;elenco al centro del contenitore padre, tenendo conto di eventuali spaziature specificate. |
   | `Right` | Allinea il blocco lungo il bordo destro del contenitore principale, tenendo conto della spaziatura specificata. |

   {style="table-layout:auto"}

1. Imposta il **[!UICONTROL Border]** stile applicato a tutti e quattro i lati del contenitore blocco dinamico:

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

1. (Facoltativo) Specifica i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente da applicare al contenitore.

   Separare più nomi di classe con uno spazio.

1. Immetti i valori, in pixel, per il **[!UICONTROL Margins and Padding]** per determinare i margini esterni e la spaziatura interna del contenitore di blocchi dinamici.

   Immettere i valori corrispondenti nel diagramma.

   | Area contenitore | Descrizione |
   | -------------- | ----------- |
   | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati del contenitore. Opzioni: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Quantità di spazio vuoto applicata al bordo interno di tutti i lati del contenitore. Opzioni: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}

## Modifica impostazioni contenitore blocco dinamico

1. Passa il puntatore del mouse sul contenitore di blocchi dinamici per visualizzare la casella degli strumenti e scegli _Impostazioni_ ( ![Icona Impostazioni](./assets/pb-icon-settings.png){width="20"} ).

   ![Casella degli strumenti Blocco dinamico](./assets/pb-add-content-dynamic-block-toolbox.png){width="500" zoomable="yes"}

1. Se necessario, modificare il blocco dinamico:

   - Clic **[!UICONTROL Select Dynamic Block]**.

     ![Selezione di un altro blocco dinamico](./assets/pb-add-content-dynamic-block-select.png){width="20"}

   - Nell’elenco dei blocchi dinamici attivi, fai clic su **[!UICONTROL Select]** per il blocco che desideri aggiungere.

1. Se necessario, aggiorna le impostazioni rimanenti.

1. Al termine, fai clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare al [!DNL Page Builder] Workspace.

## Duplicare un blocco dinamico

1. Passa il puntatore del mouse sul contenitore di blocchi dinamici per visualizzare la casella degli strumenti e scegli _Duplica_ ( ![Icona Duplica](./assets/pb-icon-duplicate.png){width="20"} ).

   Il duplicato viene visualizzato immediatamente sotto l&#39;originale.

   ![Duplicazione di un blocco dinamico](./assets/pb-add-content-dynamic-block-duplicate.png){width="500" zoomable="yes"}

1. Per spostare il nuovo blocco dinamico in una posizione diversa, posizionare il puntatore del mouse sul relativo contenitore, quindi scegliere _Sposta_ ( ![Icona Sposta](./assets/pb-icon-move.png){width="20"} ) nella casella degli strumenti.

1. Selezionate e trascinate il blocco dinamico fino a quando la linea guida rossa non viene visualizzata nella nuova posizione.

   Durante lo spostamento del blocco dinamico, i bordi superiore e inferiore di ciascun contenitore vengono visualizzati come linee tratteggiate.

## Rimuovere un blocco dinamico dall&#39;area di visualizzazione

1. Passa il puntatore del mouse sul contenitore di blocchi dinamici per visualizzare la casella degli strumenti e scegli _Rimuovi_ ( ![Icona Rimuovi](./assets/pb-icon-remove.png){width="20"} ).

1. Quando viene richiesto di confermare, fai clic su **[!UICONTROL OK]**.
