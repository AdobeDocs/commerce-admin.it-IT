---
title: Archiviazione di contenuti multimediali
description: Scopri in che modo l’archiviazione multimediale ti consente di organizzare e accedere ai file multimediali di Commerce memorizzati sul server.
exl-id: 5cf1bb20-d747-4a12-8558-e167c229efe8
feature: Page Content, Media
source-git-commit: 7dae6b6d387c796c5ff472293c6590fabaa83e85
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# Archiviazione di contenuti multimediali

L&#39;archiviazione multimediale consente di organizzare e accedere ai file multimediali memorizzati sul server. Il percorso della posizione dei file è determinato dal [URL di base](../stores-purchase/store-urls.md) configurazione. I file nell’archiviazione multimediale sono accessibili dall’editor mentre si lavora su pagine e blocchi statici. Di solito, lo storage dei supporti risiede nel file system sullo stesso server del [!DNL Commerce] file di programma.

In alternativa, i file multimediali possono essere gestiti in un [database](media-storage-database.md)o su un server separato o [rete di distribuzione dei contenuti](media-storage-content-delivery-network.md). Il vantaggio dell&#39;utilizzo di un sistema di storage alternativo è che riduce al minimo lo sforzo necessario per sincronizzare i supporti. Le prestazioni di sincronizzazione sono particolarmente influenzate quando più istanze del sistema vengono distribuite su server diversi che richiedono l&#39;accesso alle stesse immagini, file CSS e altri file multimediali.

L’editor può essere configurato per utilizzare sia statico che [URL di elementi multimediali dinamici](../catalog/catalog-urls.md#configure-catalog-media-url-format) per il contenuto del catalogo in descrizioni di categorie o prodotti.

![[!DNL Commerce] Storage multimediale](./assets/media-storage.png){width="650" zoomable="yes"}

## Aggiungere file all&#39;archivio multimediale

I primi due passaggi sono gli stessi dell&#39;inserimento di un&#39;immagine.

1. Il giorno [editor](editor.md) , fare clic sul pulsante _Inserisci immagine_ icona.

   ![Icona Inserisci immagine](./assets/editor-toolbar-image-button.png){width="700" zoomable="yes"}

   Questa azione apre il _[!UICONTROL Insert/edit image]_.

1. Dopo _[!UICONTROL Source]_, fare clic su_ Ricerca _icona (![Icona Ricerca](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

1. Nella struttura di directory a sinistra, effettuare una delle seguenti operazioni:

   - Passa alla cartella in cui desideri salvare l’immagine caricata.

   - Passa alla posizione in cui desideri creare una cartella e fai clic su **Crea cartella**.

     Per aggiungere una cartella, immetti il nome della cartella e fai clic su **[!UICONTROL OK]**.

1. Per aggiungere uno o più file a Media Storage, è possibile caricare i file dal sistema o utilizzare [Integrazione di Adobe Stock](adobe-stock.md):

   Per caricare i file dal sistema, fai clic su **[!UICONTROL Choose Files]** ed effettuare le seguenti operazioni:

   - Nella directory del computer locale passare alla posizione delle immagini.

   - Seleziona ogni immagine da caricare.

   - Clic **[!UICONTROL Open]**.

   Per utilizzare le risorse da Adobe Stock tramite [integrazione](adobe-stock.md):

   - Clic **[!UICONTROL Search Adobe Stock]**.

   - Aggiungi un’anteprima o un’immagine con licenza da Adobe Stock (consulta [Utilizzo delle immagini di Adobe Stock](adobe-stock-manage.md)).

Le immagini vengono caricate nella cartella Archiviazione file multimediali corrente sul server.

![[!DNL Commerce] Storage multimediale](./assets/media-storage.png){width="650" zoomable="yes"}

## Inserire un&#39;immagine dall&#39;archiviazione dei supporti

Apri la pagina o il blocco da modificare. Utilizzare quindi uno dei metodi seguenti per inserire un&#39;immagine dall&#39;archiviazione dei supporti:

### Metodo 1: modalità WYSIWYG

1. Il giorno [editor](editor.md) , fare clic sul pulsante _Inserisci immagine_ icona.

1. Dopo _[!UICONTROL Source]_, fare clic su_ Ricerca _icona (![Icona Ricerca](./assets/media-gallery-icon-browse.png){width="10" zoomable="no"}).

   ![Selezione dell’icona di ricerca](./assets/editor-dialog-insert-image.png){width="250" zoomable="yes"}

1. Nella struttura della directory a sinistra, individua la cartella in cui è memorizzata l&#39;immagine.

1. Seleziona il riquadro dell’immagine e fai clic su **[!UICONTROL Add Selected]**.

### Metodo 2: modalità HTML

1. Posizionare il cursore nel codice dove `<img>` deve essere inserito.

1. Clic **[!UICONTROL Insert Image]**.

   ![Inserisci immagine (modalità HTML)](./assets/editor-html-mode-insert-image.png){width="600" zoomable="yes"}
