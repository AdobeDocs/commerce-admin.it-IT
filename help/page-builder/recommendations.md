---
title: Aggiungi contenuto - Consigli di prodotto
description: Scopri il tipo di contenuto Consigli di prodotto, utilizzato per aggiungere un elenco di consigli alla fase  [!DNL Page Builder] .
exl-id: ca90c10d-8d7a-42a2-bb13-2602aa9d6eef
feature: Page Builder, Page Content, Recommendations
source-git-commit: 5da244a548b15863fe31b5df8b509f8e63df27c2
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 0%

---

# Aggiungi contenuto - Consigli di prodotto

Utilizza il tipo di contenuto _Consigli di prodotto_ per aggiungere una [unità di consigli](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) attiva e esistente alla [[!DNL Page Builder] fase](workspace.md#stage) per una pagina, un blocco o un blocco dinamico di CMS.

>[!NOTE]
>
>Il tipo di contenuto [!DNL Page Builder] _Consigli di prodotto_ è supportato in Adobe Commerce 2.4.4 e versioni successive e disponibile nel [pacchetto metapacchetto di consigli di prodotto versioni 3.0.x o successive](https://commercemarketplace.adobe.com/magento-product-recommendations.html). Per aggiungere il supporto di [!DNL Page Builder] per Product Recommendations, [visualizzare le informazioni sull&#39;installazione](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/getting-started/install-configure). **Questo tipo di contenuto non è disponibile per Magento Open Source.**

{{$include /help/_includes/page-builder-save-timeout.md}}

## Casella degli strumenti Consigli di prodotto

| Strumento | Icona | Descrizione |
| --- | --| --- |
| Sposta | ![Icona Sposta](./assets/pb-icon-move.png){width="25"} | Sposta il contenitore di consigli del prodotto e il relativo contenuto in un’altra posizione sullo stage. |
| Impostazioni | ![Icona Impostazioni](./assets/pb-icon-settings.png){width="25"} | Apre la pagina Modifica consiglio prodotto, in cui è possibile scegliere l&#39;unità di consigli e modificare le proprietà del contenitore. |
| Nascondi | ![Icona Nascondi](./assets/pb-icon-hide.png){width="25"} | Nasconde il contenitore di consigli prodotto corrente e il relativo contenuto. |
| Spettacolo | ![Mostra icona](./assets/pb-icon-show.png){width="25"} | Mostra il contenitore per consigli di prodotti nascosto e il relativo contenuto. |
| Duplica | ![Icona duplicata](./assets/pb-icon-duplicate.png){width="25"} | Crea una copia duplicata del contenitore per consigli di prodotto e del relativo contenuto. |
| Rimuovi | ![Icona Rimuovi](./assets/pb-icon-remove.png){width="25"} | Elimina dall’area di visualizzazione il contenitore per consigli di prodotto e il relativo contenuto. |

{style="table-layout:auto"}

{{$include /help/_includes/page-builder-hidden-element-note.md}}

## Aggiungi un&#39;unità di consigli esistente

1. Assicurarsi di avere già [creato un&#39;unità di consigli](https://experienceleague.adobe.com/en/docs/commerce/product-recommendations/admin/create) per il tipo di pagina [!DNL Page Builder].

>[!NOTE]
>
>È possibile creare unità di consigli per il tipo di pagina [!DNL Page Builder] solo nella visualizzazione predefinita dello store.

1. Apri la pagina, il blocco o il blocco dinamico in modalità di modifica.

1. Espandere la sezione _[!UICONTROL Content]_e fare clic su **[!UICONTROL Edit with Page Builder]**o nell&#39;area di anteprima del contenuto per aprire l&#39;area di lavoro [!DNL Page Builder].

1. Nel pannello [!DNL Page Builder] sotto _[!UICONTROL Layout]_, trascina un segnaposto **[!UICONTROL Row]**nell&#39;area di visualizzazione.

1. Nel pannello [!DNL Page Builder] sotto _[!UICONTROL Add Content]_, trascina un segnaposto **[!UICONTROL Product Recommendation]**nella riga.

   ![Aggiunta del tipo di contenuto Consiglio di prodotto](./assets/pb-add-prex-drag.png){width="600" zoomable="yes"}

1. Effettuare una delle seguenti operazioni:

   - Fare clic su **[!UICONTROL Edit Product Recommendation]**.
   - Passa il puntatore del mouse sul contenitore vuoto per visualizzare la casella degli strumenti e fai clic sull&#39;icona _Impostazioni_ (![Icona Impostazioni](./assets/pb-icon-settings.png)).

   ![Modifica consiglio prodotto](./assets/pb-prex-toolbox.png){width="600" zoomable="yes"}

1. Nella sezione _[!UICONTROL Selection]_, fare clic su **[!UICONTROL Select]**.

1. Nell&#39;elenco dei consigli di prodotti attivi, trovare la riga con l&#39;unità di consigli che si desidera aggiungere e fare clic su **[!UICONTROL Select]** nell&#39;ultima colonna.

   ![Consiglio di prodotto selezionato](./assets/pb-prex-select.png){width="600" zoomable="yes"}

1. Nell&#39;angolo superiore destro fare clic su **[!UICONTROL Add Selected]**.

   Il nome del consiglio di prodotto selezionato viene visualizzato nella sezione _[!UICONTROL Selection]_della pagina_[!UICONTROL Edit Product Recommendation]_.

1. Apporta le modifiche necessarie alle [Impostazioni avanzate](#advanced-settings).

   ![Modifica consiglio prodotto](./assets/pb-prex-edit.png){width="600" zoomable="yes"}

1. Al termine, effettuare le seguenti operazioni:

   - Se utilizzi una finestra del browser completamente ingrandita, fai clic sull&#39;icona _Chiudi schermo intero_ (![Chiudi icona schermo intero](./assets/pb-icon-reduce.png)) nell&#39;angolo superiore destro dell&#39;area di lavoro.

   - Fare clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare all&#39;area di lavoro [!DNL Page Builder].

   Quando ritorni all’area di visualizzazione, nel contenitore vengono visualizzate le immagini segnaposto del prodotto.

## Modifica impostazioni unità di consigli

1. Passa il puntatore del mouse sul contenitore unità di consigli per visualizzare la casella degli strumenti e fai clic sull&#39;icona _Impostazioni_ (![Icona Impostazioni](./assets/pb-icon-settings.png)).

   ![Casella degli strumenti consigli](./assets/pb-placeholder-toolbox.png){width="600" zoomable="yes"}

1. Apporta le modifiche necessarie alle [Impostazioni avanzate](#advanced-settings).

1. Al termine, fare clic su **[!UICONTROL Save]** per applicare le impostazioni e tornare all&#39;area di lavoro [!DNL Page Builder].

## Duplicare un’unità di consigli

1. Passa il puntatore del mouse sul contenitore di unità di consigli per visualizzare la casella degli strumenti e fai clic sull&#39;icona _Duplica_ (![Icona Duplica](./assets/pb-icon-duplicate.png)) nella casella degli strumenti.

   Il duplicato viene visualizzato immediatamente sotto l&#39;originale.

1. Per spostare l&#39;unità di consigli duplicata in una nuova posizione, posizionare il puntatore del mouse sul contenitore e fare clic sull&#39;icona _Sposta_ (![Icona Sposta](./assets/pb-icon-move.png)) nella casella degli strumenti.

1. Seleziona e trascina l’unità di consigli fino a quando la linea guida rossa non viene visualizzata nella nuova posizione.

   Durante lo spostamento dell’unità di consigli, i bordi superiore e inferiore di ciascun contenitore vengono visualizzati come linee tratteggiate.

## Rimuovere un’unità di consigli dalla fase

1. Passa il puntatore del mouse sul contenitore di unità di consigli e fai clic sull&#39;icona _Rimuovi_ ( ![Icona Rimuovi](./assets/pb-icon-remove.png)) nella casella degli strumenti.

1. Quando viene richiesto di confermare, fare clic su **[!UICONTROL OK]**.

## Impostazioni avanzate

1. Per controllare il posizionamento dell&#39;unità Product Recommendations all&#39;interno del contenitore padre, scegliere **[!UICONTROL Alignment]**:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Applica l&#39;impostazione predefinita di allineamento specificata nel foglio di stile del tema corrente. |
   | `Left` | Allinea l&#39;unità lungo il bordo sinistro del contenitore padre, tenendo conto di eventuali spaziature specificate. |
   | `Center` | Allinea l&#39;unità al centro del contenitore padre, tenendo conto di qualsiasi spaziatura specificata. |
   | `Right` | Allinea l&#39;unità lungo il bordo destro del contenitore principale, tenendo conto di qualsiasi spaziatura specificata. |

   {style="table-layout:auto"}

1. Imposta lo stile **[!UICONTROL Border]** applicato a tutti e quattro i lati dell&#39;unità Consigli di prodotto:

   | Opzione | Descrizione |
   | ------ | ----------- |
   | `Default` | Applica lo stile di bordo predefinito specificato dal foglio di stile associato. |
   | `None` | Non fornisce alcuna indicazione visibile dei bordi delle unità. |
   | `Dotted` | Il bordo dell&#39;unità viene visualizzato come una linea tratteggiata. |
   | `Dashed` | Il bordo unità viene visualizzato come una linea tratteggiata. |
   | `Solid` | Il bordo dell&#39;unità viene visualizzato come linea continua. |
   | `Double` | Il bordo dell&#39;unità viene visualizzato come una doppia riga. |
   | `Groove` | Il bordo unità viene visualizzato come una linea scanalata. |
   | `Ridge` | Il bordo unità viene visualizzato come una linea scanalata. |
   | `Inset` | Il bordo dell&#39;unità viene visualizzato come una linea di inserimento. |
   | `Outset` | Il bordo dell&#39;unità viene visualizzato come una linea di contorno. |

   {style="table-layout:auto"}

1. Se si imposta uno stile di bordo diverso da `None`, completare le opzioni di visualizzazione del bordo:

   | Opzione | Descrizione |
   | ------ |------------ |
   | [!UICONTROL Border Color] | Specificate il colore scegliendo un campione, facendo clic sul selettore del colore oppure immettendo un nome di colore valido o un valore esadecimale equivalente. |
   | [!UICONTROL Border Width] | Immettere il numero di pixel per lo spessore della linea del bordo. |
   | [!UICONTROL Border Radius] | Immettere il numero di pixel per definire la dimensione del raggio utilizzato per arrotondare ogni angolo del bordo. |

   {style="table-layout:auto"}

1. (Facoltativo) Specificare i nomi di **[!UICONTROL CSS classes]** dal foglio di stile corrente da applicare all&#39;unità.

   Separare più nomi di classe con uno spazio.

1. Immettere i valori, in pixel, per **[!UICONTROL Margins and Padding]** per determinare i margini esterni e la spaziatura interna dell&#39;unità.

   Immettere i valori corrispondenti nel diagramma.

   | Area contenitore | Descrizione |
   | ------ | ----------- |
   | [!UICONTROL Margins] | Quantità di spazio vuoto applicata al bordo esterno di tutti i lati dell&#39;unità. Opzioni: `Top` / `Right` / `Bottom` / `Left` |
   | [!UICONTROL Padding] | Quantità di spazio vuoto applicata allo spigolo interno di tutti i lati dell&#39;unità. Opzioni: `Top` / `Right` / `Bottom` / `Left` |

   {style="table-layout:auto"}
