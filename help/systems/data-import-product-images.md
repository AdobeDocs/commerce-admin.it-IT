---
title: Importazione immagine prodotto
description: Scopri come importare le immagini dei prodotti utilizzando il percorso e il nome di file di ciascuna immagine.
exl-id: 991550e6-9ce2-4472-becb-3492bd4c9582
feature: Products, Data Import/Export, Media
source-git-commit: 64ccc2d5016e915a554c2253773bb50f4d33d6f4
workflow-type: tm+mt
source-wordcount: '835'
ht-degree: 0%

---

# Importazione immagine prodotto

È possibile importare più immagini di prodotto di ciascun tipo in Adobe Commerce e Magento Open Source e associarle a un prodotto specifico. Il percorso e il nome file di ciascuna immagine del prodotto vengono immessi nel file CSV e i file immagine da importare vengono caricati nel percorso corrispondente sul server Commerce o sul server esterno.

Commerce crea una propria struttura di directory per le immagini dei prodotti organizzate in ordine alfabetico. Quando esportate dati di prodotto con immagini esistenti in un file CSV, potete visualizzare il percorso alfabetico prima del nome di ogni immagine. Tuttavia, quando si importano nuove immagini, non è necessario specificare un percorso, perché Commerce gestisce automaticamente la struttura della directory. Tuttavia, assicurarsi di immettere il percorso relativo della directory di importazione prima del nome file di ciascuna immagine da importare.

Per caricare le immagini, è necessario disporre delle credenziali di accesso e delle autorizzazioni corrette per accedere alla cartella Commerce sul server. Con le credenziali corrette, puoi utilizzare qualsiasi utility SFTP per caricare i file dal computer desktop al server.

Prima di provare a importare molte immagini, rivedere i passaggi del metodo di importazione che si desidera utilizzare ed eseguire il processo con alcuni prodotti. Dopo aver compreso come funziona, si avrà la certezza di importare grandi quantità di immagini.

>[!IMPORTANT]
>
>Si consiglia di utilizzare un programma che supporti la codifica UTF-8 per modificare i file CSV, ad esempio Blocco note++. Microsoft® Excel inserisce caratteri aggiuntivi nell’intestazione di colonna del file CSV, impedendo in tal modo la reimportazione dei dati in Commerce.

## Metodo 1: importare immagini dal server locale

1. Sul server Commerce, carica i file immagine in `var/import/images` cartella o sottocartella, ad esempio `var/import/images/product_images`. Questa è la cartella principale predefinita per l’importazione delle immagini del prodotto.

   ```terminal
   <Magento root folder>/var/import/images
   ```

   >[!NOTE]
   >
   Iniziare con Adobe Commerce e Magento Open Source `2.3.2` versione, il percorso specificato nella **[!UICONTROL Images File Directory]** concatenati per l&#39;importazione nella directory base immagini - `<Magento-root-folder>/var/import/images`. Per le versioni precedenti di Adobe Commerce e Magento Open Source, puoi utilizzare una cartella diversa sul server Commerce, purché durante il processo di importazione sia specificato il percorso della cartella.

1. Nei dati CSV, inserisci il nome di ciascun file di immagine da importare nella riga corretta, `sku`, e nella colonna corretta in base al tipo di immagine (`base_image`, `small_image`, `thumbnail_image`, o `additional_images`).

   >[!NOTE]
   >
   Per le immagini nella cartella di importazione predefinita (`var/import/images`), non includere il percorso prima del nome file nei dati CSV.

   Il file CSV deve includere solo `sku` e le relative colonne di immagine.

   ![Esempio: importazione di dati immagine CSV](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Seguire le istruzioni per [importa](data-import.md) i dati.

1. Dopo aver selezionato il file da importare, immettete il percorso relativo indicato di seguito **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images
   ```

   ![Directory dei file delle immagini di importazione dati](./assets/data-import-file-to-import.png){width="600" zoomable="yes"}

   >[!TIP]
   >
   Esci _[!UICONTROL Images File Directory]_vuoto per utilizzare `<Magento-root-folder>/var/import/images` directory. A partire da Adobe Commerce e dalla versione 2.3.2 del Magento Open Source, questa è la directory base predefinita per le immagini di importazione.

   Se si importano più immagini per una singola `sku`, inserisci le immagini in una colonna denominata `additional_images` (se non è già stata aggiunta), separati da virgole. Esempio: `image02.jpg,image03.jpg`

## Metodo 2: importare immagini da un server esterno

1. Carica le immagini da importare nella cartella specificata sul server esterno.

1. Nei dati CSV, inserisci l’URL completo di ciascun file di immagine nella colonna corretta per tipo di immagine (`base_image`, `small_image`, `thumbnail_image`, o `additional_images`).

   ```terminal
   https://example.com/images/image.jpg
   ```

1. Seguire le istruzioni per [importa](data-import.md) i dati.

## Metodo 3: importare immagini con l&#39;archiviazione remota

1. Nel modulo di archiviazione remota, carica i file immagine in `var/import/images` cartella o sottocartella, ad esempio `var/import/images/product_images`. Questa è la cartella principale predefinita per l’importazione delle immagini del prodotto.

   ```terminal
   <remote-storage-root-folder>/var/import/images
   ```

   >[!NOTE]
   >
   Iniziare con Adobe Commerce e Magento Open Source `2.3.2` versione, il percorso specificato nella _[!UICONTROL Images File Directory]_concatena per l&#39;importazione nella directory base immagini: `<remote-storage-root-folder>/var/import/images`. Per le versioni precedenti di Adobe Commerce e Magento Open Source, puoi utilizzare una cartella diversa sul server Commerce, purché durante il processo di importazione sia specificato il percorso della cartella.

1. Nei dati CSV, inserisci il nome di ciascun file di immagine da importare nella riga corretta, `sku`, e nella colonna corretta in base al tipo di immagine (`base_image`, `small_image`, `thumbnail_image`, o `additional_images`).

   >[!NOTE]
   >
   Per le immagini nella cartella di importazione predefinita (`var/import/images`), non includere il percorso prima del nome file nei dati CSV.

   Il file CSV deve includere solo `sku` e le relative colonne di immagine.

   ![Esempio: importazione di dati immagine CSV](./assets/data-import-csv-image-files-default-local.png){width="600" zoomable="yes"}

1. Seguire le istruzioni per [importa](data-import.md) i dati.

1. Dopo aver selezionato il file da importare, immettete il percorso relativo indicato di seguito **[!UICONTROL Images File Directory]**.

   ```terminal
   var/import/images/product_images
   ```

   >[!TIP]
   >
   Lascia _[!UICONTROL Images File Directory]_vuoto per utilizzare `<Magento-root-folder>/var/import/images` directory. A partire da Adobe Commerce e dalla versione 2.3.2 del Magento Open Source, questa è la directory base predefinita per le immagini di importazione.

   Se si importano più immagini per una singola `sku`, inserisci le immagini in una colonna denominata `additional_images` (se non è già stata aggiunta), separati da virgole: `image02.jpg,image03.jpg`

Per ulteriori informazioni sull&#39;attivazione e la gestione del modulo di archiviazione remota, vedere [Configurare l’archiviazione remota](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage.html) nel _Guida alla configurazione_.

>[!NOTE]
>
L&#39;importazione di immagini di prodotto non avvia il ridimensionamento dell&#39;immagine. Le immagini dei prodotti vengono ridimensionate sul front-end da `pub/get.php`. Assicurati che il tuo `pub/get.php` funziona correttamente; in caso contrario, le immagini potrebbero non essere ridimensionate.
