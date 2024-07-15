---
title: Gestione risorse di Media Gallery
description: Scopri come gestire i file multimediali caricati e le risorse acquisite tramite un’integrazione Adobe Stock.
exl-id: 4fc489ae-b1e5-4aa4-832d-cd88c58d103a
feature: Page Content, Media
source-git-commit: a93e96353f4be0e771064cdcfbdf794772386a28
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 0%

---

# Gestione risorse di Media Gallery

La nuova [Raccolta file multimediali](media-gallery.md) fornisce gli strumenti per la gestione dei file multimediali caricati e delle risorse acquisite tramite un&#39;integrazione di [Adobe Stock](adobe-stock.md). Se hai salvato una [anteprima immagine](adobe-stock-save-preview.md) di Adobe Stock, puoi anche [concedere in licenza](adobe-stock-license-image.md) l&#39;immagine nella nuova Media Gallery.

## Caricare una risorsa

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Fare clic su **[!UICONTROL Upload Image]**.

1. Seleziona il file da caricare.

   La risorsa selezionata viene caricata automaticamente nella cartella selezionata (o nella directory principale di archiviazione, se non è selezionata alcuna cartella).

## Visualizza dettagli risorsa

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Fai clic sui tre punti sotto la risorsa (![icona Dettagli](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), quindi fai clic su **[!UICONTROL View Details]**.

   ![Azioni risorsa](./assets/media-gallery-asset-actions.png){width="600" zoomable="yes"}

   I dettagli della risorsa vengono visualizzati in un pannello diapositiva. Includono le informazioni in cui la risorsa viene utilizzata:

   - **[!UICONTROL Categories]**
   - **[!UICONTROL Products]**
   - **[!UICONTROL Pages]**
   - **[!UICONTROL Blocks]**

   ![Dettagli risorsa](./assets/media-gallery-asset-details.png){width="600" zoomable="yes"}

   Per visualizzare i dettagli, fare clic sui collegamenti **[!UICONTROL Used In]**. La griglia nell’esempio seguente mostra tutte le categorie in cui viene utilizzata una risorsa specifica.

   ![Griglia categorie](./assets/media-gallery-asset-categories.png){width="600" zoomable="yes"}

   È inoltre possibile eliminare la risorsa dalla sezione _Visualizza dettagli_.

## Modificare una risorsa

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Fai clic sui tre punti sotto la risorsa (![icona del menu della risorsa](./assets/media-gallery-asset-menu-icon.png){width="10" zoomable="no"}), quindi fai clic su **[!UICONTROL Edit]**.

   ![Modifica risorsa](./assets/media-gallery-edit-asset.png){width="600" zoomable="yes"}

1. Se necessario, modifica uno dei seguenti valori di metadati:

   - **[!UICONTROL Title]**
   - **[!UICONTROL Description]**
   - **[!UICONTROL Tags/Keywords]**

   Questi dati vengono salvati nel database e nei metadati del file stesso. Attualmente sono supportati i formati XMP e IPTC.

   Puoi scaricare l’immagine con i metadati aggiornati.

## Utilizzare una risorsa

Assets può essere utilizzato in modo estensivo in tutto l&#39;amministratore, ad esempio [aggiungere o modificare una pagina](page-add.md), [creare o modificare una categoria](../catalog/category-create.md) o [inserire immagini dall&#39;Editor contenuto](editor-insert-image.md).

1. Accedi alla nuova Media Gallery da un’area che ti consente di utilizzare le risorse multimediali.

1. Selezionare la risorsa e fare clic su **[!UICONTROL Add Selected]**.

{{$include /help/_includes/image-optimization-animated-gif-note.md}}

## Eliminare risorse

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Fare clic su **[!UICONTROL Delete Images...]** e selezionare la casella di controllo per ogni risorsa che si desidera eliminare.

1. Nella finestra di dialogo di conferma, fare clic su **[!UICONTROL Delete Image]**.

   ![Conferma eliminazione](./assets/media-gallery-bulk-delete-confirm.png){width="500" zoomable="yes"}

## Cercare le risorse

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Utilizza l&#39;input **[!UICONTROL Search by keywords]** per eseguire la ricerca di immagini per parole chiave/tag.

   La ricerca nell&#39;esempio seguente trova le risorse che contengono un tag specifico (`mountain`).

   ![Ricerca risorse](./assets/media-gallery-asset-search.png){width="600" zoomable="yes"}

>[!NOTE]
>
>Per informazioni su come aggiornare i tag immagine, consulta la sezione _[Modificare una risorsa](#edit-an-asset)_.

## Filtrare le risorse

>[!NOTE]
>
>La funzionalità _Utilizzata in_ richiede che [!UICONTROL Media Gallery Image Optimization] sia abilitato nelle [impostazioni di configurazione](media-gallery-image-optimization.md).

1. Nella barra laterale _Admin_, passa a **[!UICONTROL Content]** > _[!UICONTROL Media]_>**[!UICONTROL Media Gallery]**.

1. Fare clic sulla scheda **[!UICONTROL Filters]**.

   ![Filtri](./assets/media-gallery-filters.png){width="600" zoomable="yes"}

1. Imposta le opzioni di filtro.

   Puoi filtrare le risorse in base all’utilizzo da parte delle entità:

   - **[!UICONTROL Used in Categories]**
   - **[!UICONTROL Used in Products]**
   - **[!UICONTROL Used in Pages]**
   - **[!UICONTROL Used in Blocks]**

   È inoltre possibile filtrare le risorse in base a **[!UICONTROL Store View]**, **[!UICONTROL License Status]** e **[!UICONTROL Content Status]**. Imposta un intervallo di date per **[!UICONTROL Uploaded Date]** e/o **[!UICONTROL Modification Date]** per filtrare le risorse in base alle date dei file.

1. Fare clic su **[!UICONTROL Apply Filters]** per visualizzare i risultati.

   Il filtro nell&#39;esempio seguente trova le risorse utilizzate in una categoria specifica (`cars`) e abilitate.

   ![Filtro per Assets abilitato per categoria](./assets/media-gallery-filter-by-category.png){width="600" zoomable="yes"}

## Trova duplicati immagine

1. Fare clic sulla scheda **[!UICONTROL Filters]** e selezionare la casella di controllo **[!UICONTROL Show duplicates]**.

1. Per visualizzare i risultati, fare clic su **[!UICONTROL Apply Filters]**.
