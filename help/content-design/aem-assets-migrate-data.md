---
title: Migrazione di file multimediali ad AEM
description: Migra i file multimediali da Adobe Commerce o da un’origine esterna a AEM Assets DAM.
feature: CMS, Media, Integration
source-git-commit: 094c585b335e5751a1387989d5ba33332c351c57
workflow-type: tm+mt
source-wordcount: '769'
ht-degree: 0%

---

# Migrare i file multimediali a AEM Assets DAM

Adobe Commerce e Adobe Experience Manager (AEM) forniscono funzioni integrate per semplificare la migrazione dei file multimediali da Commerce al sistema DAM (Digital Asset Management System) di AEM Assets. È inoltre possibile eseguire la migrazione di file multimediali da altre origini.

## Prerequisiti

| Categoria | Requisito |
|----------|-------------|
| **Requisiti di sistema** | <ul><li>Ambiente AEM as a Cloud Service fornito con AEM Assets</li><li>Capacità di stoccaggio sufficiente</li><li>Larghezza di banda di rete per trasferimenti di file di grandi dimensioni</li></ul> |
| **Accesso e autorizzazioni richiesti** | <ul><li>Accesso amministratore ad AEM Assets as a Cloud Service</li><li>Accesso al sistema di origine in cui sono archiviati i file multimediali (Adobe Commerce o sistema esterno)</li><li>Autorizzazioni appropriate per accedere ai servizi di archiviazione cloud</li></ul> |
| **Account archiviazione cloud** | <ul><li>Account di archiviazione AWS S3 o Azure Blob</li><li>Configurazione contenitore/bucket privato</li><li>Credenziali di autenticazione</li></ul> |
| **Contenuto Source** | <ul><li>File multimediali organizzati pronti per la migrazione</li><li>File immagine e video nei formati <a href="https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/file-format-support#image-formats"> supportati da AEM Assets</a>.</li><li>Risorse pulite e deduplicate</li></li> |
| **Preparazione metadati** | <ul><li><a href="https://experienceleague.adobe.com/en/docs/commerce-admin/content-design/aem-asset-management/getting-started/aem-assets-configure-aem">Profilo metadati AEM Assets configurato per le risorse Commerce</a></li><li>Valori metadati mappati per ogni risorsa</li><li>Editor file CSV (ad esempio, Microsoft Excel)</li></ul> |

## Best practice per la migrazione

1. Cura le risorse prima della migrazione rimuovendo il contenuto inutilizzato e duplicato.
1. Organizza le risorse in modo logico per dimensione, formato o caso d’uso.
1. È consigliabile suddividere le migrazioni di grandi dimensioni in batch più piccoli.
1. Pianificare le importazioni ad alta intensità di risorse durante le ore di minore utilizzo.
1. Convalida la mappatura dei metadati prima dell’importazione completa.

## Flusso di lavoro di migrazione

Segui il flusso di lavoro di migrazione per esportare i file multimediali da Adobe Commerce o da un altro sistema esterno e importarli in AEM Assets DAM.

### Passaggio 1: esportare il contenuto dall&#39;origine dati esistente

Per i rivenditori Adobe Commerce, il modulo di archiviazione remota offre un modo semplificato di esportare i file multimediali da Commerce e importarli in AEM Assets. Questo modulo consente di archiviare e gestire i file multimediali su servizi di archiviazione remota come AWS S3, rendendo il processo di migrazione più efficiente. Per configurare l&#39;archiviazione remota per l&#39;istanza di Commerce, vedere [Configurare l&#39;archiviazione remota](https://experienceleague.adobe.com/en/docs/commerce-operations/configuration-guide/storage/remote-storage/remote-storage-aws-s3) nella *Guida alla configurazione di Commerce*.

Se hai file multimediali archiviati all&#39;esterno di Adobe Commerce, caricali direttamente in una delle [origini dati](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/assets-view/bulk-import-assets-view#prerequisites) supportate da AEM as a Cloud Service.

### Passaggio 2: creare un file CSV per la mappatura dei metadati

Crea un file di mappatura metadati in formato CSV e caricalo nella cartella sorgente che contiene i tuoi file multimediali. Questo file mappa i metadati essenziali di ciascuna risorsa su:

- Organizzare e classificare le risorse in DAM per semplificarne l’individuazione
- Abilitare la corretta sincronizzazione tra Adobe Commerce e AEM Assets
- Gestisci relazioni tra risorse e prodotti dopo la migrazione

Per ogni file multimediale di cui si prevede la migrazione, fornire i valori per i campi di metadati inclusi nel profilo di metadati [AEM Assets per le risorse Commerce](aem-assets-configure-aem.md) come descritto nella tabella seguente.

| Metadati | Descrizione | Valore |
|-------|-------------|--------|
| assetPath | Percorso completo in cui la risorsa verrà memorizzata nell’archivio AEM Assets.<br><br>Utilizzare il percorso per creare sottocartelle per organizzare le risorse di Commerce, ad esempio `content/dam/commerce/<brand>/<type>`. | `/content/dam/commerce/<sub-folder>/..<filename>` |
| dc:title | Titolo visualizzato della risorsa in AEM Assets | Valore stringa (ad esempio, `Sample 1`) |
| dam:status | Stato di approvazione della risorsa in AEM Assets | `approved` |
| commerce:posizioni | Posizione/ordine della risorsa nelle gallerie di prodotti | Valore numerico (ad esempio, &quot;1&quot;) |
| commerce:isCommerce | Flag che indica se la risorsa è utilizzata in Commerce | `Yes` |
| commerce:skus | SKU di prodotto associati a questa risorsa | Valore stringa (ad esempio, `sample1`) |
| commerce:ruoli | I ruoli o i tipi di immagini per la risorsa (ad esempio, `thumbnail`, `main image`, `swatch`) | Più valori separati da punto e virgola (ad esempio, &quot;miniatura; immagine; swatch_image; small_image&quot;) |

+++Codice CSV

Utilizza questo codice CSV di esempio per creare il file in un editor di codice o in un’applicazione per fogli di calcolo come Microsoft Excel.

```csv
assetPath,dc:title{{String}},dam:status{{String}},commerce:positions{{String: multi}},commerce:isCommerce{{String}},commerce:skus{{String: multi}},commerce:roles{{String: multi}}
/content/dam/commerce/sample1.jpg,Sample 1,approved,1,Yes,sample1,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample2.jpg,Sample 2,approved,1,Yes,sample2,thumbnail; image; swatch_image; small_image
/content/dam/commerce/sample3.jpg,Sample 3,approved,1,Yes,sample3,thumbnail; image; swatch_image; small_image
```

+++

### Passaggio 3: importare in blocco Assets in AEM Assets

Dopo aver creato il file di mappatura dei metadati, utilizza lo strumento AEM Assets Bulk Import per importare le risorse.

Di seguito è riportata una panoramica generale sull&#39;utilizzo dello strumento.

1. [Accedi all&#39;ambiente di authoring AEM Assets as a Cloud Service](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/onboarding/journey/aem-users#login-aem).

1. Dalla vista Strumenti di Experience Manager, seleziona **[!UICONTROL Assets]** > **[!UICONTROL Bulk Import]**.

   ![Authoring di AEM Assets](./assets/aem-assets-bulk-import-selection.png){width="600" zoomable="yes"}

1. In Configurazioni di importazione in blocco, selezionare **[!UICONTROL Create]** per aprire il modulo di configurazione.

   ![Authoring di AEM Assets](./assets/aem-assets-bulk-import-configuration.png){width="600" zoomable="yes"}

1. Imposta e salva la configurazione.

   Sono necessari:

   - Credenziali di autenticazione per l’origine dati
   - Cartella di destinazione in AEM Assets in cui verranno archiviati i file importati
   - Informazioni sui tipi MIME, le dimensioni del file e altri parametri per personalizzare la configurazione di importazione (facoltativo)
   - Percorso del file CSV di mappatura metadati caricato nell’istanza di archiviazione Cloud.

   Per i passaggi dettagliati, consulta [Configurare lo strumento Importazione in blocco](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#configure-bulk-ingestor-tool) nella *Guida utente di AEM Assets as a Cloud Service*.

1. Dopo aver salvato la configurazione, utilizzare gli strumenti di importazione in blocco per testare ed eseguire l&#39;operazione di importazione.

>[!MORELIKETHIS]
>
>[Demo video strumento di importazione in blocco](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#asset-bulk-ingestor)
>[Suggerimenti, best practice e limitazioni](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/manage/add-assets#tips-limitations)
>[Carica o acquisisci risorse tramite API](https://experienceleague.adobe.com/en/docs/experience-manager-cloud-service/content/assets/admin/developer-reference-material-apis#asset-upload)

